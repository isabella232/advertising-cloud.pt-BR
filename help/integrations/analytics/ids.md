---
title: Advertising Cloud IDs usadas por [!DNL Analytics]
description: Advertising Cloud IDs usadas por [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Advertising Cloud IDs usadas por [!DNL Analytics]

*Anunciantes somente com uma integração Advertising Cloud-Adobe Analytics*

*Aplicável ao Advertising Cloud DSP e Advertising Cloud Search*

O Advertising Cloud usa duas IDs para o rastreamento de desempenho no site:  a EF ID e a AMO ID.

Quando ocorre uma impressão de anúncio, o Advertising Cloud cria os valores de ID AMO e ID EF e os armazena. Quando um visitante que viu um anúncio entrar no site sem clicar em um anúncio, [!DNL Analytics] chama esses valores do Advertising Cloud por meio do [!DNL Analytics for Advertising Cloud] código JavaScript. Para o tráfego de view-through, [!DNL Analytics] gera uma ID adicional (`SDID`), que é usada para unir a ID EF e a ID do AMO em [!DNL Analytics]. Para o tráfego de click-through, essas IDs são incluídas no URL da página de aterrissagem usando os parâmetros `s_kwcid` e `ef_id` da sequência de consulta.

A Advertising Cloud faz a distinção entre uma entrada de click-through ou view-through no site usando os seguintes critérios:

* Uma entrada view-through é capturada quando um usuário visita o site após visualizar um anúncio, mas não clicar nele. [!DNL Analytics] registra um view-through se duas condições forem atendidas:
   * O visitante não tem click-throughs para um anúncio [!DNL DSP] ou [!DNL Search] durante a [janela de lookback de clique](#lookback-a4adc).
   * O visitante viu pelo menos um anúncio [!DNL DSP] durante a [janela de retrospectiva de impressão](#lookback-a4adc). A última impressão é passada como view-through.
* Uma entrada de click-through é capturada quando um visitante do site clica em um anúncio antes de entrar do site. [!DNL Analytics] captura um click-through quando uma das seguintes condições ocorre:
   * O URL inclui uma EF ID e uma AMO ID, como adicionadas ao URL da página inicial pelo Advertising Cloud.
   * O URL não contém códigos de rastreamento, mas o código JavaScript do Advertising Cloud detecta um clique nos últimos dois minutos.

![Integração baseada em visualização do Advertising Cloud  [!DNL Analytics] ](/help/integrations/assets/a4adc-view-through-process.png)

*Figura 1: Integração baseada em visualização do Advertising Cloud  [!DNL Analytics]*

![Advertising Cloud clique em  [!DNL Analytics] integração baseada em URL](/help/integrations/assets/a4adc-click-through-process.png)

*Figura 2: Advertising Cloud clique em  [!DNL Analytics] integração baseada em URL*

## Advertising Cloud EF IDs

A EF ID é um token exclusivo que a Advertising Cloud usa para associar a atividade a um clique ou exposição a anúncios online. A ID EF é armazenada em uma dimensão [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou rVar (eVar reservado) (Advertising Cloud EF ID) e rastreia cada clique ou exposição de anúncio no nível de navegador ou dispositivo individual. As EF IDs atuam principalmente como chaves para enviar dados [!DNL Analytics] ao Advertising Cloud para relatórios e otimização de lances no Advertising Cloud.

### Formato EF ID

```<Advertising Cloud visitor ID>:<timestamp>:<channel type>```

<!-- <*Advertising Cloud visitor ID*>:<*timestamp*>:<*channel type*> -->

em que:

* &lt;>ID de visitante da Advertising Cloud *> é uma ID exclusiva por visitante (como UhKVaAABCkJ0mDt).* Também chamado de *surfer ID*.

* &lt;>timestamp *> é a hora no formato YYYMMDDHHMMSS (como 20190821192533 para o ano 2019, Mês 08, Dia 21, Tempo 19:25:33).*

* &lt;>tipo de canal *> é o tipo de canal responsável pelo clique ou exposição:*

   * `d` para um clique em um anúncio de exibição de DSP (click-through de exibição)
   * `i` para obter uma impressão de um anúncio de exibição DSP (view-through de exibição)
   * `s` para um clique em uma publicidade de pesquisa (click-through de pesquisa).

Exemplo `EF `ID: WcmibgAAHJK1RyY:1551968087687:d

>[!NOTE]
>
>EF IDs fazem distinção entre maiúsculas e minúsculas. Se uma implementação [!DNL Analytics] forçar o rastreamento de URL para letras minúsculas, o Advertising Cloud não reconhecerá a ID EF. Isso afetará os lances e os relatórios do Advertising Cloud, mas não terá impacto nos relatórios do Advertising Cloud em [!DNL Analytics].

### O Dimension de ID EF em [!DNL Analytics]

Nos relatórios [!DNL Analytics], é possível encontrar dados de ID de EF pesquisando a dimensão [!UICONTROL EF ID] e usando a métrica [!UICONTROL EF ID Instance].

`EF IDs` estão sujeitas ao limite de identificador exclusivo de 500k no Analysis Workspace. Quando o valor de 500k é atingido, todos os novos códigos de rastreamento são relatados no título de item de uma linha &quot;[!UICONTROL Low Traffic]&quot;. Devido à possibilidade de falta de fidelidade do relatório, `EF IDs` não são classificadas e você não deve usá-las em segmentos ou relatórios em [!DNL Analytics].

## Advertising Cloud AMO IDs

A ID do AMO rastreia cada combinação de anúncios exclusiva em um nível menos granular e é usada para [!DNL Analytics] a classificação de dados e a assimilação de métricas de publicidade (como impressões, cliques e custo) da Advertising Cloud. A ID do AMO é armazenada em uma dimensão [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou rVar (ID do AMO) e é usada exclusivamente para relatórios em [!DNL Analytics].

A ID do AMO também é chamada de `s_kwcid`, que às vezes é chamada de &quot;a lula&quot;.

### Formato de ID do AMO para [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

em que:

* &lt;>ID *do canal > pode ser:*

   * `AC` = Advertising Cloud DSP
   * `AL` para Advertising Cloud Search

* &lt;>ID do anúncio *> é usado um identificador exclusivo gerado pela Advertising Cloud para um anúncio.* Ele serve como uma chave para traduzir metadados de entidade do Advertising Cloud em dimensões [!DNL Analytics] legíveis.

* &lt;>ID de disposição *> é um identificador exclusivo gerado pela Advertising Cloud para uma disposição.* Ele serve como uma chave para traduzir metadados de entidade do Advertising Cloud em dimensões [!DNL Analytics] legíveis.

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

As IDs do AMO para [!DNL Search] seguem um formato distinto para cada mecanismo de pesquisa. O formato de todos os mecanismos de pesquisa começa com o seguinte:

```AL!{ef_userid}!{ef_sid}```

em que:

* `AL` é a ID do canal para o canal de pesquisa.
* `{ef_userid}` é a ID de usuário numérica exclusiva que a Advertising Cloud atribui ao anunciante.
* `{ef_sid}` é a ID numérica que o Advertising Cloud usa para o mecanismo de pesquisa especificado, como  `3` para  [!DNL Google Ads] ou  `10` para  [!DNL Microsoft Advertising].

Veja a seguir os formatos completos da ID do AMO para alguns mecanismos de pesquisa. Para formatos de ID do AMO para outros mecanismos de pesquisa, entre em contato com o gerente de conta do Adobe.

Formato de ID do AMO para [!DNL Google Ads]:

```AL!{ef_userid}!{ef_sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

em que:

* `{creative}` é a ID numérica  [!DNL Google Ads] exclusiva para o anúncio.
* `{matchtype}` é o tipo de correspondência da palavra-chave que acionou a publicidade:  `e` para exato,  `p` para frase ou  `b` para amplo.
* `{placement}` é o nome de domínio do site no qual o anúncio foi clicado. Um valor está disponível para anúncios em campanhas direcionadas por disposições e para anúncios em campanhas direcionadas por palavras-chave que são exibidos em sites de conteúdo.
* `{network}` indica a rede da qual o clique ocorreu:   `g` para  [!DNL Google] pesquisa (somente para anúncios direcionados por palavras-chave),  `s` para um parceiro de pesquisa (somente para anúncios direcionados por palavras-chave) ou  `d` para a Rede de exibição (para anúncios direcionados por palavras-chave ou direcionados por disposições).
* `{keyword}` é a palavra-chave específica que acionou sua publicidade (em sites de pesquisa) ou a palavra-chave melhor correspondente (em sites de conteúdo).

Formato de ID do AMO para [!DNL Microsoft Advertising]:

```AL!{ef_userid}!{ef_sid}!{AdId}!{OrderItemId}```

em que:

* `{AdId}` é a ID numérica  [!DNL Microsoft Advertising] exclusiva para o anúncio.
* `{OrderItemId}` é a ID  [!DNL Microsoft Advertising] numérica da palavra-chave.

### Dimension de ID do AMO em [!DNL Analytics]

Nos relatórios do Analytics, é possível encontrar dados da ID do AMO pesquisando a dimensão [!UICONTROL AMO ID] e usando a métrica [!UICONTROL AMO ID Instance]. A dimensão [!UICONTROL AMO ID] abriga todos os valores de ID do AMO capturados, enquanto a métrica [!UICONTROL AMO ID Instance] indica a frequência com que um valor de ID do AMO foi capturado pelo site. Por exemplo, se a mesma publicidade de pesquisa foi clicada quatro vezes, mas o Analytics rastreou sete entradas do site, [!UICONTROL AMO ID Instance] seria sete (7) e [!UICONTROL Clicks] seria quatro (4).

Para qualquer relatório ou auditoria dentro de [!DNL Analytics], a prática recomendada é usar a ID do AMO juntamente com sua instância correspondente. Para obter mais informações, consulte &quot;[Validação de dados para [!DNL Analytics for Advertising Cloud]](data-variances.md#data-validation)&quot; em &quot;Variações de dados esperadas entre [!DNL Analytics] e Advertising Cloud.&quot;

## Sobre as classificações do Analytics

Em [!DNL Analytics], um [classification](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) é uma parte dos metadados para um determinado código de rastreamento, como Conta, Campanha ou Anúncio. O Advertising Cloud categoriza os dados brutos do Advertising Cloud usando classificações para que você possa exibir os dados de maneiras diferentes (por Tipo de anúncio ou Campanha) ao gerar relatórios. As classificações formam a base dos relatórios do Advertising Cloud em [!DNL Analytics] e podem ser usadas com as métricas do AMO, como [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions] e [!UICONTROL AMO Clicks], bem como com eventos personalizados e padrão no local, como [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] e [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Visão geral da [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Variações de dados esperadas  [!DNL Analytics] entre o e o Advertising Cloud](data-variances.md)

