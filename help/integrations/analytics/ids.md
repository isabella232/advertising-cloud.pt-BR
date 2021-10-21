---
title: Advertising Cloud IDs usadas por [!DNL Analytics]
description: Advertising Cloud IDs usadas por [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: bfbfc293ad04b294c813ce7c8a11200e70fc812f
workflow-type: tm+mt
source-wordcount: '1156'
ht-degree: 0%

---

# Advertising Cloud IDs usadas por [!DNL Analytics]

*Anunciantes somente com uma integração Advertising Cloud-Adobe Analytics*

*Aplicável ao Advertising Cloud DSP e Advertising Cloud Search*

O Advertising Cloud usa duas IDs para o rastreamento de desempenho no site: a EF ID e a AMO ID.

Quando ocorre uma impressão de anúncio, o Advertising Cloud cria os valores de ID AMO e ID EF e os armazena. Quando um visitante que viu um anúncio entra no site sem clicar em um anúncio, [!DNL Analytics] chama esses valores do Advertising Cloud por meio da variável [!DNL Analytics for Advertising Cloud] Código JavaScript. Para tráfego view-through, [!DNL Analytics] gera uma ID complementar (`SDID`), que é usado para unir a ID EF e a ID AMO em [!DNL Analytics]. Para o tráfego de click-through, essas IDs são incluídas no URL da página de aterrissagem usando o `s_kwcid` e `ef_id` parâmetros da string de consulta.

A Advertising Cloud faz a distinção entre uma entrada de click-through ou view-through no site usando os seguintes critérios:

* Uma entrada view-through é capturada quando um usuário visita o site após visualizar um anúncio, mas não clicar nele. [!DNL Analytics] registra um view-through se duas condições forem atendidas:
   * O visitante não tem click-throughs para um [!DNL DSP] ou [!DNL Search] durante a [janela de retrospectiva de clique](#lookback-a4adc).
   * O visitante viu pelo menos um [!DNL DSP] durante a [janela de retrospectiva de impressão](#lookback-a4adc). A última impressão é passada como view-through.
* Uma entrada de click-through é capturada quando um visitante do site clica em um anúncio antes de entrar do site. [!DNL Analytics] captura um click-through quando uma das seguintes condições ocorre:
   * O URL inclui uma EF ID e uma AMO ID, como adicionadas ao URL da página inicial pelo Advertising Cloud.
   * O URL não contém códigos de rastreamento, mas o código JavaScript do Advertising Cloud detecta um clique nos últimos dois minutos.

![Baseado em visualização do Advertising Cloud [!DNL Analytics] integração](/help/integrations/assets/a4adc-view-through-process.png)

*Figura 1: Baseado em visualização do Advertising Cloud [!DNL Analytics] integração*

![Advertising Cloud clique em baseado em URL [!DNL Analytics] integração](/help/integrations/assets/a4adc-click-through-process.png)

*Figura 2: Advertising Cloud clique em baseado em URL [!DNL Analytics] integração*

## Advertising Cloud EF IDs

A EF ID é um token exclusivo que a Advertising Cloud usa para associar a atividade a um clique ou exposição a anúncios online. A ID EF é armazenada num [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou a dimensão rVar (eVar reservado) (Advertising Cloud EF ID) e rastreia cada clique ou exposição de anúncio no nível de navegador ou dispositivo individual. As EF IDs atuam principalmente como chaves para envio [!DNL Analytics] dados para a Advertising Cloud para relatórios e otimização de lances no Advertising Cloud.

### Formato EF ID

```<Advertising Cloud visitor ID>:<timestamp>:<channel type>```

<!-- <*Advertising Cloud visitor ID*>:<*timestamp*>:<*channel type*> -->

em que:

* &lt;*ID de visitante da Advertising Cloud*> é uma ID exclusiva por visitante (como UhKVaAABCkJ0mDt). Também chamado de *surfer ID*.

* &lt;*timestamp*> é a hora no formato YYYYMMDDHHMMSS (como 20190821192533 para o ano de 2019, Mês 08, Dia 21, Tempo 19:25:33).

* &lt;*tipo de canal*> é o tipo de canal responsável pelo clique ou exposição:

   * `d` para um clique em um anúncio de exibição de DSP (click-through de exibição)
   * `i` para obter uma impressão de um anúncio de exibição DSP (view-through de exibição)
   * `s` para um clique em uma publicidade de pesquisa (click-through de pesquisa).

Exemplo `EF `ID: WcmibgAAHJK1RyY:1551968087687:d

>[!NOTE]
>
>EF IDs fazem distinção entre maiúsculas e minúsculas. Se uma [!DNL Analytics] A implementação força o rastreamento de URL para letras minúsculas, então o Advertising Cloud não reconhece a EF ID. Isso afetará os lances e os relatórios do Advertising Cloud, mas não terá impacto nos relatórios do Advertising Cloud no [!DNL Analytics].

### Dimension EF ID [!DNL Analytics]

Em [!DNL Analytics] você pode encontrar dados EF ID pesquisando [!UICONTROL EF ID] e usando a [!UICONTROL EF ID Instance] métrica.

`EF IDs` estão sujeitas ao limite de identificador exclusivo de 500k no Analysis Workspace. Quando o valor de 500k for atingido, todos os novos códigos de rastreamento serão reportados sob o título de item de uma linha &quot;[!UICONTROL Low Traffic].&quot; Devido à possibilidade de falta de fidelidade ao relatório, a variável `EF IDs` não são classificadas, e você não deve usá-las em segmentos ou relatórios no [!DNL Analytics].

## Advertising Cloud AMO IDs

A ID do AMO rastreia cada combinação de anúncios exclusiva em um nível menos granular e é usada para [!DNL Analytics] classificação de dados e assimilação de métricas de publicidade (como impressões, cliques e custo) do Advertising Cloud. A ID do AMO é armazenada em um [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou dimensão rVar (ID do AMO) e é usada exclusivamente para relatórios em [!DNL Analytics].

A ID do AMO também é chamada de `s_kwcid`, que por vezes é chamada de &quot;lula&quot;.

### Formato de ID do AMO para [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

em que:

* &lt;*ID do canal*> pode ser:

   * `AC` = Advertising Cloud DSP
   * `AL` para Advertising Cloud Search

* &lt;*ID do anúncio*> é usado um identificador exclusivo gerado pela Advertising Cloud para um anúncio. Ele serve como uma chave para traduzir metadados de entidade do Advertising Cloud em legíveis [!DNL Analytics] dimensões.

* &lt;*ID de posicionamento*> é um identificador exclusivo gerado pela Advertising Cloud para uma disposição. Ele serve como uma chave para traduzir metadados de entidade do Advertising Cloud em legíveis [!DNL Analytics] dimensões.

<!-- <*Channel ID*>!<*Ad ID*>!<*Placement ID*>

where:

* <*Channel ID*> may be:

    * `AC` = Advertising Cloud DSP
    * `AL` for Advertising Cloud Search

* <*Ad ID*> is used an Advertising Cloud-generated unique identifier for an ad. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.

* <*Placement ID*> is an Advertising Cloud-generated unique identifier for an placement. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.
 -->

Exemplo de ID do AMO: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### Formato de ID do AMO para [!DNL Search]

IDs do AMO para [!DNL Search] siga um formato distinto para cada mecanismo de pesquisa. O formato de todos os mecanismos de pesquisa começa com o seguinte:

```AL!{ef_userid}!{ef_sid}```

em que:

* `AL` é a ID do canal para o canal de pesquisa.
* `{ef_userid}` é a ID de usuário numérica exclusiva que a Advertising Cloud atribui ao anunciante.
* `{ef_sid}` é a ID numérica que o Advertising Cloud usa para o mecanismo de pesquisa especificado, como `3` para [!DNL Google Ads] ou `10` para [!DNL Microsoft Advertising].

Veja a seguir os formatos completos da ID do AMO para alguns mecanismos de pesquisa. Para formatos de ID do AMO para outros mecanismos de pesquisa, entre em contato com o [!DNL Adobe] gerente de conta.

Formato de ID do AMO para [!DNL Google Ads]:

```AL!{ef_userid}!{ef_sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

em que:

* `{creative}` é [!DNL Google Ads] ID numérica exclusiva para o anúncio.
* `{matchtype}` é o tipo de correspondência da palavra-chave que acionou a publicidade: `e` para as informações exatas, `p` para frase, ou `b` para uma dimensão ampla.
* `{placement}` é o nome de domínio do site no qual o anúncio foi clicado. Um valor está disponível para anúncios em campanhas direcionadas por disposições e para anúncios em campanhas direcionadas por palavras-chave que são exibidos em sites de conteúdo.
* `{network}` indica a rede da qual o clique ocorreu:  `g` para [!DNL Google] pesquisar (somente para anúncios direcionados por palavras-chave), `s` para um parceiro de pesquisa (somente para anúncios direcionados por palavras-chave) ou `d` para a Rede de exibição (para anúncios direcionados por palavras-chave ou direcionados por disposições).
* `{keyword}` é a palavra-chave específica que acionou sua publicidade (em sites de pesquisa) ou a palavra-chave melhor correspondente (em sites de conteúdo).

Formato de ID do AMO para [!DNL Microsoft Advertising]:

```AL!{ef_userid}!{ef_sid}!{AdId}!{OrderItemId}```

em que:

* `{AdId}` é [!DNL Microsoft Advertising] ID numérica exclusiva para o anúncio.
* `{OrderItemId}` é [!DNL Microsoft Advertising] ID numérica da palavra-chave.

### Dimension de ID do AMO [!DNL Analytics]

Nos relatórios do Analytics, é possível encontrar dados da ID do AMO pesquisando pela variável [!UICONTROL AMO ID] e usando a [!UICONTROL AMO ID Instance] métrica. O [!UICONTROL AMO ID] A dimensão hospeda todos os valores de ID do AMO capturados, enquanto a variável [!UICONTROL AMO ID Instance] indica com que frequência um valor de ID do AMO foi capturado pelo site. Por exemplo, se a mesma publicidade de pesquisa foi clicada quatro vezes, mas o Analytics rastreou sete entradas do site, então [!UICONTROL AMO ID Instance] seriam sete (7) e [!UICONTROL Clicks] seriam quatro (4).

Para qualquer relatório ou auditoria dentro de [!DNL Analytics], a prática recomendada é usar a ID do AMO juntamente com a instância correspondente. Para obter mais informações, consulte &quot;[Validação de dados para [!DNL Analytics for Advertising Cloud]](data-variances.md#data-validation)&quot; em &quot;Variações de dados esperadas entre [!DNL Analytics] e Advertising Cloud.&quot;

## Sobre as classificações do Analytics

Em [!DNL Analytics], a [classificação](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) é uma parte dos metadados para um determinado código de rastreamento, como Conta, Campanha ou Anúncio. O Advertising Cloud categoriza os dados brutos do Advertising Cloud usando classificações para que você possa exibir os dados de maneiras diferentes (por Tipo de anúncio ou Campanha) ao gerar relatórios. As classificações formam a base dos relatórios do Advertising Cloud em [!DNL Analytics] e podem ser usadas com as métricas do AMO, como [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions]e [!UICONTROL AMO Clicks], bem como com eventos personalizados e padrão no site como [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders]e [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Visão geral da [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Variações de dados esperadas entre [!DNL Analytics] e Advertising Cloud](data-variances.md)

