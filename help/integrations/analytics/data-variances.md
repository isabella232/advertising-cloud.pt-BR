---
title: Variações de dados esperadas entre [!DNL Analytics] e publicidade Adobe
description: Variações de dados esperadas entre [!DNL Analytics] e publicidade Adobe
feature: Integration with Adobe Analytics
exl-id: 34685e04-d4f9-4e27-b83e-b56164244b2b
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '3278'
ht-degree: 0%

---

# Variações de dados esperadas entre [!DNL Analytics] e publicidade Adobe

*Anunciantes apenas com uma integração Adobe Advertising-Adobe Analytics*

Os anunciantes com o [!DNL Analytics for Advertising] <!-- (A4AdC) --> a integração rastreia a publicidade paga por meio da Adobe Advertising e do Adobe Analytics. Ao rastrear mídia, campanhas e canais por vários sistemas, os mesmos conjuntos de dados de diferentes sistemas raramente correspondem completamente. Este documento explica como você deve esperar que os dados de mídia que são transmitidos por meio de Adobe Advertising se comparem aos dados dos diferentes sistemas em que a mídia é rastreada [!DNL Analytics].

>[!NOTE]
>
>Este documento está focado em Adobe Advertising e Analytics, mas muitos dos pontos principais também são transferíveis para outras soluções de rastreamento.

## Diferenças de atribuição em relatórios semelhantes

### Janelas de pesquisa e modelos de atribuição potencialmente diferentes

O [!DNL Analytics for Advertising] a integração usa duas variáveis (eVars ou rVars \[eVars reservadas]\) para capturar a variável [EF ID e AMO ID](ids.md). Essas variáveis são configuradas com uma única janela de lookback (o tempo em que os click-throughs e view-throughs são atribuídos) e um modelo de atribuição. Salvo especificação em contrário, as variáveis são configuradas para corresponderem à janela de pesquisa de cliques padrão no nível do anunciante e ao modelo de atribuição no Adobe Advertising.

No entanto, as janelas de pesquisa e os modelos de atribuição são configuráveis no Analytics (por meio das eVars) e no Adobe Advertising. Além disso, no Adobe Advertising, o modelo de atribuição é configurável não apenas no nível do anunciante (para otimização de lance), mas também em visualizações de dados e relatórios individuais (somente para fins de relatório). Por exemplo, uma organização pode preferir usar o modelo de atribuição de distribuição par para otimização, mas usar a atribuição de último toque para relatórios em DSP de publicidade ou [!DNL Advertising Search]. Alterar modelos de atribuição altera o número de conversões atribuídas.

Se uma janela de lookback de relatório ou um modelo de atribuição for modificado em um produto e não no outro, os mesmos relatórios de cada sistema mostrarão dados distintos:

* **Exemplo de discrepâncias causadas por diferentes janelas de pesquisa:**

   Suponha que a Adobe Advertising tenha uma janela de retrospectiva de cliques de 60 dias e [!DNL Analytics] tem uma janela de lookback de 30 dias. E suponha que um usuário acesse o site por meio de um anúncio rastreado pelo Adobe Advertising, saia e retorne no dia 45 e converta. A Adobe Advertising atribuirá a conversão à visita inicial porque a conversão ocorreu dentro da janela de lookback de 60 dias. [!DNL Analytics], no entanto, não é possível atribuir a conversão para a visita inicial porque a conversão ocorreu depois que a janela de lookback de 30 dias expirou. Neste exemplo, a Adobe Advertising relataria um número maior de conversões do que [!DNL Analytics] seria.

   ![Exemplo de conversão atribuída na Adobe Advertising, mas não [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Exemplo de discrepâncias causadas por diferentes modelos de atribuição:**

   Suponha que um usuário interaja com três anúncios publicitários Adobe diferentes antes da conversão, com a receita como o tipo de conversão. Se um relatório Adobe Advertising usar um modelo de distribuição par para atribuição, ele atribuirá a receita uniformemente em todos os anúncios. If [!DNL Analytics] no entanto, o usa o modelo de atribuição de último toque e, em seguida, atribui a receita ao último anúncio. No exemplo a seguir, a Adobe Advertising atribui um valor igual a 10 dólares dos 30 dólares de receita capturada para cada um dos três anúncios, enquanto que [!DNL Analytics] atribui o total de 30 dólares de receita ao último anúncio visualizado pelo usuário. Ao comparar relatórios de publicidade Adobe e [!DNL Analytics], é possível observar o impacto da diferença na atribuição.

   ![Receitas diferentes atribuídas à Adobe Advertising e [!DNL Analytics] com base em diferentes modelos de atribuição](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>A prática recomendada é usar as mesmas janelas de retrospectiva e modelo de atribuição em Adobe Advertising e [!DNL Analytics]. Trabalhe com seu [!DNL Adobe] a equipe de conta conforme necessário para identificar as configurações atuais e manter as configurações sincronizadas.

Esses mesmos conceitos se aplicam a qualquer outro canal semelhante que usa janelas de retrospectiva ou modelos de atribuição diferentes.

#### Janelas de pesquisa diferentes para rastreamento de view-through {#impression-lookback}

Na Adobe Advertising, a atribuição é baseada em cliques e impressões, e você pode configurar diferentes janelas de pesquisa para cliques e impressões. Em [!DNL Analytics], no entanto, a atribuição é baseada em click-throughs e view-throughs, e você não tem a opção de definir diferentes janelas de atribuição para click-throughs e view-throughs; rastreamento para cada início na visita inicial ao site. Uma impressão pode ocorrer no mesmo dia ou vários dias antes de ocorrer um view-through, e isso pode afetar o local em que a janela de atribuição começa em cada sistema.

Normalmente, a maioria das conversões de view-through ocorre rapidamente o suficiente para que ambos os sistemas atribuam crédito. No entanto, algumas conversões podem ocorrer fora da janela de retrospectiva de impressão de Adobe Advertising, mas dentro do [!DNL Analytics] janela de retrospectiva; essas conversões são atribuídas ao view-through no [!DNL Analytics] mas não à impressão na Adobe Advertising.

No exemplo a seguir, suponha que um visitante recebeu um anúncio no Dia 1, realizou uma visita de view-through (ou seja, visitou a landing page do anúncio sem clicar anteriormente no anúncio) no Dia 2 e foi convertido no Dia 45. Nesse caso, a Adobe Advertising rastrearia o usuário dos Dias 1 a 14 (usando uma retrospectiva de 14 dias), [!DNL Analytics] rastrearia o usuário dos Dias 2 a 61 (usando uma retrospectiva de 60 dias), e a conversão no Dia 45 seria atribuída ao anúncio dentro de [!DNL Analytics] mas não dentro da Adobe Advertising.

![Exemplo de conversão view-through atribuída em [!DNL Analytics] mas não publicidade Adobe](/help/integrations/assets/a4adc-viewthrough-example.png)

Outra causa das discrepâncias é que, no Adobe Advertising, você pode atribuir conversões de view-through a um *peso de view-through* que é relativo ao peso atribuído a uma conversão baseada em clique. O peso de view-through padrão é de 40%, o que significa que uma conversão de view-through é contada como 40% do valor de uma conversão baseada em clique. [!DNL Analytics] O não fornece essa ponderação de conversões de view-through. Assim, por exemplo, uma ordem de 100 dólares de receita captada em [!DNL Analytics] será descontado para 40 dólares em Adobe Advertising se você estiver usando o peso de view-through padrão — uma diferença de 60 dólares.

Considere essas diferenças ao comparar conversões view-through entre a publicidade Adobe e a [!DNL Analytics] relatórios.

#### Modelos de atribuição disponíveis

| Atribuição de publicidade Adobe | [!DNL Analytics] Atribuição | Alocação de eVar/rVar |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | n/d | n/d |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>Não usar* |
| [!UICONTROL Weight Last Event More] | n/d | n/d |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | n/d |
| n/d | [!UICONTROL J-Shaped] | n/d |
| n/d | [!UICONTROL Inverse-J] | n/d |
| n/d | [!UICONTROL Custom] | n/d |
| n/d | [!UICONTROL Participation] | n/d |
| n/d | [!UICONTROL Algorithmic] | n/d |

>[!NOTE]
>
>Para alocação linear, [!DNL Analytics] atribui eventos bem-sucedidos igualmente entre todos os valores de eVar em uma única visita; portanto, use alocação linear com uma expiração de eVar de &quot;Visita&quot;. No entanto, para a publicidade, o uso da atribuição linear leva a uma alocação que não é realmente linear e a relatórios menos que ideais. Por exemplo, se um visitante interage com três anúncios antes de converter em três visitas separadas, somente o anúncio visualizado na última visita é atribuído à conversão, não aos três anúncios.
>
>Além disso, a alternância da alocação de conversão de ou para &quot;Linear&quot; impede que os dados históricos sejam exibidos, o que pode resultar em dados incorretos nos relatórios. Por exemplo, a alocação linear pode dividir a receita entre vários valores de eVar diferentes. Se você alterar a alocação para &quot;Mais recente&quot;, 100% dessa receita será associada ao valor único mais recente. Essa associação pode levar você a conclusões incorretas.
>
>Para evitar confusões, [!DNL Analytics] torna os dados históricos indisponíveis na interface de relatórios do . Você pode exibir os dados históricos se alterar o eVar de volta para a configuração de alocação inicial, embora não deva alterar as configurações de alocação de eVar simplesmente para acessar dados históricos. O Adobe recomenda usar um novo eVar quando você deseja aplicar uma nova configuração de alocação para dados que já estão sendo registrados, em vez de alterar as configurações de alocação para um eVar que já tem uma quantidade significativa de dados históricos.

Veja uma lista de [!DNL Analytics] modelos de atribuição e suas definições em [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

Se você estiver conectado [!DNL Search], você pode encontrar uma lista de modelos de atribuição em
[https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm).

#### Atribuição de data do evento na publicidade Adobe

Em Adobe Advertising, você pode relatar os dados de conversão pela data/data do clique associado (a data do evento clique ou impressão) ou pela data da transação (data de conversão). O conceito de relatório de clique/data do evento não existe em [!DNL Analytics]; todas as conversões acompanhadas [!DNL Analytics] são reportadas por data de transação. Como resultado, a mesma conversão pode ser relatada com datas diferentes em Adobe Advertising e [!DNL Analytics]. Por exemplo, considere um usuário que clicou em um anúncio em 1 de janeiro e converte em 5 de janeiro. Se você estiver visualizando os dados de conversão por data do evento em Adobe Advertising, a conversão será reportada em 1º de janeiro, quando o clique ocorrer. Em [!DNL Analytics], a mesma conversão seria relatada em 5 de janeiro.

![Exemplo de conversão atribuída a datas diferentes](/help/integrations/assets/a4adc-conversions-based-on.png)

## Atribuição em [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] relatórios](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) permite configurar regras para identificar diferentes canais de marketing com base em aspectos distintos das informações de ocorrência. Você pode rastrear canais Adobe Advertising acompanhados ([!UICONTROL Display Click Through], [!UICONTROL Display View Through]e [!UICONTROL Paid Search]) como [!DNL Marketing Channels] usando o `ef_id` parâmetro da string de consulta para identificar o canal. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> No entanto, mesmo que a variável [!DNL Marketing Channels] Os relatórios podem rastrear canais de Adobe Advertising, os dados podem não corresponder aos relatórios de Adobe Advertising por vários motivos. Consulte as seções a seguir para obter mais informações.

>[!NOTE]
>
> Os seguintes conceitos principais também se aplicam a qualquer rastreamento de vários canais que envolve campanhas não rastreadas na Adobe Advertising, como a [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) (também conhecida como Dimension de &quot;Código de rastreamento&quot; ou &quot;eVar 0&quot;) e rastreamento de eVar personalizado.

### Modelos de atribuição potencialmente diferentes no [!DNL Marketing Channels]

Mais [!DNL Marketing Channels] são configurados com [!UICONTROL Last Touch] atribuição, para a qual o último canal de marketing detectado é atribuído 100% do valor de conversão. Usar diferentes modelos de atribuição para a variável [!DNL Marketing Channels] relatórios e relatórios de Adobe Advertising levarão a discrepâncias em conversões atribuídas.

### Uma janela de lookback potencialmente diferente em [!DNL Marketing Channels]

A janela de pesquisa para [!DNL Marketing Channels] pode ser personalizada. No Adobe Advertising, a janela de pesquisa de cliques é configurável, embora uma janela fixa de 60 dias seja comum. Se os dois produtos usarem janelas de retrospectiva diferentes, você poderá esperar discrepâncias de dados.

### Atribuição de canal diferente no [!DNL Marketing Channels]

Os relatórios de publicidade Adobe capturam somente mídia paga registrada através da Adobe Advertising (pesquisa paga por [!DNL Advertising Search] anúncios e exibição para anúncios publicitários DSP), enquanto [!DNL Marketing Channels] Os relatórios do podem rastrear todos os canais digitais. Isso pode levar a uma discrepância no canal para o qual uma conversão é atribuída.

Por exemplo, os canais de pesquisa paga e natural geralmente têm uma relação simbiótica, em que cada canal auxilia o outro. O [!DNL Marketing Channels] O relatório atribuirá algumas conversões à pesquisa natural que a Adobe Advertising não irá porque não rastreia a pesquisa natural.

Considere também um cliente que exibe um anúncio de exibição, clica em um anúncio de pesquisa pago, clica em uma mensagem de email e coloca um pedido de 30 dólares. Mesmo se a publicidade Adobe e [!DNL Marketing Channels] ambos usam o modelo de atribuição de último toque, a conversão ainda seria atribuída de forma diferente a cada um. A Adobe Advertising não tem acesso ao [!UICONTROL Email] , portanto, creditaria a pesquisa paga pela conversão. [!DNL Marketing Channels], no entanto, tem acesso aos três canais, pelo que lhe seria concedido crédito [!UICONTROL Email] para a conversão.

![Exemplo de atribuição de conversão diferente em publicidade Adobe versus [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Para obter mais explicações sobre por que as métricas podem variar, consulte &quot;[Por que os dados de canal podem variar entre a publicidade Adobe e [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).&quot;

## Diferenças de dados no Adobe Analytics [!DNL Paid Search Detection]

O [legado [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) em [!DNL Analytics] permite que as empresas [definir regras para rastrear o tráfego de pesquisa paga e orgânica](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) para mecanismos de pesquisa especificados. O [!DNL Paid Search Detection] As regras usam uma sequência de consulta e o domínio de referência para identificar o tráfego de pesquisa paga e natural. O [!DNL Paid Search Detection] os relatórios do fazem parte do grupo maior de [Métodos de descoberta](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) relatórios, que expiram quando um evento especificado (como um Check-out do carrinho) ocorre ou a visita termina.

Esta é a interface para criar uma [!DNL Paid Search Detection] conjunto de regras:

![Exemplo de uma regra de Detecção de pesquisa paga definida em [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

O resultado [!DNL Paid Search Detection] os relatórios incluem [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine]e [!UICONTROL Natural Search Keywords] relatórios.

Observe as duas limitações a seguir com dados em [!DNL Paid Search Detection] relatórios:

* O [!UICONTROL Paid Search Keywords] e [!UICONTROL Natural Search Keywords] Os relatórios mostram as consultas de pesquisa, conforme identificadas pelos URLs de referência, não as palavras-chave nas quais os usuários fazem licitação. Publicidade Adobe e [!DNL Analytics] os relatórios mostram as palavras-chave reais, portanto, não espere que elas se alinhem com a variável [!DNL Paid Search Detection] relatórios de palavra-chave.

* Quando a variável [!DNL Paid Search Detection] foi criado originalmente, a consulta de pesquisa de origem (a sequência de caracteres inserida pelo usuário na barra de pesquisa no mecanismo de pesquisa) estava mais prontamente disponível para os anunciantes por meio da URL de referência. Atualmente, os mecanismos de pesquisa ofuscam bastante o query de pesquisa e o [!DNL Paid Search Detection] os relatórios de palavra-chave têm valor limitado, pois a maioria dos dados de consulta se enquadra em &quot;não especificado&quot;.

   Com [!DNL Analytics for Advertising], os anunciantes ainda podem rastrear palavras-chave pagas em [!DNL Analytics]. O domínio referenciador informa o mecanismo que o mecanismo de pesquisa direcionou o tráfego. Como as informações específicas da conta do anunciante não estão vinculadas ao domínio de referência, todo o tráfego é listado no mecanismo de pesquisa. Os anunciantes com várias contas no mesmo mecanismo de pesquisa devem se referir a Adobe Advertising ou [!DNL Analytics] relatórios para relatórios específicos da conta.

### Por que configurar [!DNL Paid Search Detection]?

O [!DNL Paid Search Detection] permitem identificar o tráfego de pesquisa natural na variável [[!DNL Analytics Marketing Channels] relatórios](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). Separar o tráfego de pesquisa paga do tráfego de pesquisa natural é uma ótima maneira de entender o valor que a pesquisa natural traz para o ecossistema de marketing completo.

## Validação de dados de click-through para [!DNL Analytics for Advertising] {#data-validation}

Para sua integração, você deve validar seus dados de click-through para garantir que todas as páginas do site estejam rastreando os click-throughs corretamente.

Em [!DNL Analytics], uma das maneiras mais fáceis de validar [!DNL Analytics for Advertising] O rastreamento é para comparar cliques com instâncias usando a métrica calculada &quot;Cliques para instâncias da ID do AMO&quot;, que é calculada da seguinte maneira:

```Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)```

[!UICONTROL AMO ID Instances] representa o número de vezes que as IDs do AMO (`s_kwcid` parâmetros) são rastreados no site. Cada vez que um anúncio é clicado, uma `s_kwcid` é adicionado ao URL da página inicial. O número de [!UICONTROL AMO ID Instances], portanto, é análogo ao número de cliques e pode ser validado em relação aos cliques de anúncios reais. Normalmente vemos uma taxa de correspondência de 80% para [!DNL Search] e uma taxa de correspondência de 30% para [!DNL DSP] tráfego (quando filtrado para incluir apenas click-through) [!UICONTROL AMO ID Instances]). A diferença nas expectativas entre pesquisa e exibição pode ser explicada pelo comportamento de tráfego esperado. A pesquisa captura a intenção e, como tal, os usuários geralmente pretendem clicar nos resultados da pesquisa de sua consulta. Os usuários que visualizam um vídeo ou anúncio online, no entanto, têm maior probabilidade de clicar no anúncio inintencionalmente e depois retornar do site ou abandonar a nova janela que é carregada antes que a atividade da página seja rastreada.

Nos relatórios de Adobe Advertising, você pode comparar cliques a instâncias usando o &quot;[!UICONTROL ef_id_instances]&quot; em vez de [!UICONTROL AMO ID Instances]:

```Clicks to [!UICONTROL EF ID Instances] = (ef_id_instances / Clicks)```

Embora você deva esperar uma alta taxa de correspondência entre a ID do AMO e a ID do EF, não espere 100% de paridade porque a ID do AMO e a ID do EF rastreiam dados diferentes fundamentalmente, e essa diferença pode levar a pequenas diferenças no total [!UICONTROL AMO ID Instances] e [!UICONTROL EF ID Instances]. Se o total [!UICONTROL AMO ID Instances] em [!DNL Analytics] diferem de [!UICONTROL EF ID Instances] no Adobe Advertising em mais de 1%, no entanto, entre em contato com seu [!DNL Adobe] equipe de conta para obter assistência.

Para obter mais informações sobre a ID do AMO e a ID do EF, consulte [IDs de publicidade do Adobe usadas pelo Analytics](ids.md).

A seguir, um exemplo de um espaço de trabalho para rastrear cliques em instâncias.

![Exemplo de um espaço de trabalho para rastrear cliques em instâncias](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## Comparação de conjuntos de dados em [!DNL Analytics for Advertising] Verso na publicidade Adobe

O [ID do AMO](ids.md) (parâmetro da string de consulta s_kwcid) é usado para relatórios em [!DNL Analytics]e o [EF ID](ids.md) é usada para relatórios em Adobe Advertising. Como são valores distintos, é possível que um valor seja corrompido ou não adicionado à página inicial.

Por exemplo, suponha que tenhamos a seguinte página de aterrissagem:

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id`

em que EF ID é &quot;`test_ef_id`&quot; e a ID do AMO é &quot;`test_amo_id`.&quot;

Se um redirecionamento do lado do site ocorrer, o URL poderá terminar assim:

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag`

em que EF ID é &quot;`test_ef_id`&quot; e a ID do AMO é &quot;`test_amo_id#redirectAnchorTag`.&quot;

Neste exemplo, a adição da tag de âncora adiciona caracteres inesperados à ID do AMO, resultando em um valor que o Analytics não reconhece. Essa ID do AMO não seria classificada, e as conversões associadas a ela se encaixariam em &quot;[!UICONTROL unspecified]&quot; ou &quot;[!UICONTROL none]&quot; in [!DNL Analytics] relatórios.

Felizmente, embora problemas como esse sejam comuns, eles normalmente não resultam em uma alta porcentagem de discrepância. No entanto, se você observar uma grande discrepância entre as IDs do AMO em [!DNL Analytics] e EF IDs na Adobe Advertising, entre em contato com seu [!DNL Adobe] equipe de conta para obter assistência.

## Outras considerações de métrica

### A diferença entre cliques e visitas {#clicks-vs-visits}

Eles parecem análogos, mas os cliques e visitas representam dados diferentes:

* **Clique em:** [!DNL DSP] ou o mecanismo de pesquisa registra um clique quando um visitante clica em uma publicidade no site de um editor.

* **Visita:** [!DNL Analytics] define um [visita](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) como uma série de exibições de página por um usuário, terminando de acordo com um de vários critérios, como 30 minutos de inatividade.

Por definição, um clique pode levar a várias visitas.

Considere o exemplo a seguir: Os usuários 1 e 2 acessam um site clicando em um anúncio Adobe Advertising. O usuário 1 visualiza quatro páginas e depois sai para o dia, então o clique inicial resulta em uma visita. O usuário 2 visualiza duas páginas, sai para um almoço de 45 minutos, retorna, visualiza mais duas páginas e depois sai; nesse caso, o clique inicial resulta em duas visitas.

![Exemplo da diferença entre cliques e visitas](/help/integrations/assets/a4adc-visits-example.png)

### A diferença entre cliques e click-throughs

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Cliques e click-throughs são duas métricas diferentes:

* **Clique em:** [!DNL DSP] ou o mecanismo de pesquisa registra um clique quando um visitante clica em uma publicidade no site de um editor.

* **Click-throughs:** [!DNL Analytics] registra um click-through quando o visitante acessa o site de destino, a página de aterrissagem é carregada e a variável [!DNL Analytics] na parte inferior da página, envia os dados para o [!DNL Analytics].

Cliques e click-throughs podem ser muito diferentes devido a cliques acidentais de anúncios. Observamos que a maioria dos cliques em anúncios de exibição são cliques acidentais e esses visitantes acidentais acessam o botão Voltar antes que a página de aterrissagem seja carregada, portanto [!DNL Analytics] não é possível gravar um click-through. Isso é especialmente verdadeiro para anúncios nos quais um clique acidental é mais provável, como anúncios móveis, anúncios de vídeo e anúncios que preenchem a tela e devem ser fechados antes que o usuário possa exibir a página.

Os sites carregados em dispositivos móveis também têm menos probabilidade de resultar em click-throughs devido a larguras de banda mais baixas ou poder de processamento disponível, fazendo com que as landing pages demorem mais tempo para carregar. Não é incomum que 50-70% dos cliques não resultem em click-throughs. Em ambientes móveis, a diferença pode chegar a 90% devido à combinação de um navegador mais lento e à maior probabilidade do usuário clicar no anúncio acidentalmente ao rolar pela página ou tentar fechar o anúncio.

Os dados de clique também podem ser registrados em ambientes que não podem registrar click-throughs com os mecanismos de rastreamento atuais (como cliques que entram ou saem de um aplicativo móvel) ou para os quais o anunciante implantou apenas uma abordagem de rastreamento (por exemplo, com a abordagem de view-through JavaScript, navegadores que bloqueiam cookies de terceiros rastrearão cliques, mas não click-throughs). Um motivo principal para o Adobe recomendar a implantação das abordagens de rastreamento de URL de clique e de view-through do JavaScript é maximizar a cobertura de click-throughs rastreáveis.

### Uso de métricas de tráfego de publicidade do Adobe para Dimension não-Adobe

A Adobe Advertising fornece ao Analytics com [métricas de tráfego específicas de publicidade e as dimensões relacionadas do DSP e do [!DNL [!DNL Search]]](advertising-metrics-in-analytics.md). As métricas fornecidas por Adobe Advertising são aplicáveis somente às dimensões especificadas de Adobe Advertising e os dados não estão disponíveis para outras dimensões em [!DNL Analytics].

Por exemplo, se você exibir a variável [!UICONTROL AMO Clicks] e [!UICONTROL AMO Cost] métricas por conta, que é uma dimensão Adobe Advertising, você verá o total [!UICONTROL AMO Clicks] e [!UICONTROL AMO Cost] por conta.

![Exemplo de métricas de Adobe Advertising em um relatório usando uma dimensão de Adobe Advertising](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

No entanto, se você exibir a variável [!UICONTROL AMO Clicks] e [!UICONTROL AMO Cost] métricas por uma dimensão na página (como Página), para a qual a Adobe Advertising não fornece dados, então a variável [!UICONTROL AMO Clicks] e [!UICONTROL AMO Cost] para cada página será zero (0).

![Exemplo de métricas de Adobe Advertising em um relatório usando uma dimensão não suportada](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Usando [!UICONTROL AMO ID Instances] como substituto de cliques com Dimension de publicidade não Adobe

Como você não pode usar [!UICONTROL AMO Clicks] com dimensões no site, talvez você queira encontrar um equivalente a cliques. Você pode ser tentado a usar Visitas como substituto, mas elas não são a melhor opção porque cada visitante pode ter várias visitas. (Consulte &quot;[A diferença entre cliques e visitas](#clicks-vs-visits).&quot; Em vez disso, recomendamos usar [!UICONTROL AMO ID Instances], que é o número de vezes em que a ID do AMO é capturada. Ao [!UICONTROL AMO ID Instances] não corresponde [!UICONTROL AMO Clicks] exatamente, elas são a melhor opção para medir o tráfego de cliques no site. Para obter mais informações, consulte &quot;[Validação de dados para [!DNL Analytics for Advertising]](#data-validation).&quot;

![Exemplo de [!UICONTROL AMO ID Instances] em vez de [!UICONTROL AMO Clicks] para uma dimensão não suportada](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Visão geral da [!DNL Analytics for Advertising]](overview.md)
>* [IDs de publicidade do Adobe usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Métricas de publicidade do Adobe no Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Dados na publicidade do Adobe](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Por que os dados podem variar entre a publicidade Adobe e [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

