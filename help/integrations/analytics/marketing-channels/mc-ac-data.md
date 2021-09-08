---
title: Uso de [!DNL Marketing Channels] com dados do Advertising Cloud
description: Saiba como usar os dados do Advertising Cloud em [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Uso de [!DNL Analytics Marketing Channels] com dados do Advertising Cloud

*Anunciantes somente com uma integração Advertising Cloud-Adobe Analytics*

Ao usar os relatórios do Advertising Cloud e [!DNL Marketing Channels], você pode obter informações valiosas sobre como sua mídia digital influencia a atividade do site.

<!-- from video: By using Marketing Channels with your Advertising Cloud data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

A ilustração a seguir mostra como o Advertising Cloud e [!DNL Marketing Channels] rastreiam as visitas individuais que compõem a jornada de um visitante. Os relatórios do Advertising Cloud em [!DNL Analytics] estão limitados a apenas a exibição paga e publicidade de pesquisa registrada pelo Advertising Cloud, usando a ID do AMO. No entanto, [!DNL Marketing Channels] rastreia todos os canais configurados nas [!DNL Marketing Channels] Regras de processamento.

![Como a Advertising Cloud e  [!DNL Marketing Channels] rastreiam as visitas individuais na jornada de um visitante](/help/integrations/assets/a4adc-mc-sample-journey2.png)

Na primeira visita, o usuário entrou no site por meio de uma campanha de email, executou dez visualizações de página e saiu. Na segunda visita, o usuário entrou no site por meio de um anúncio de exibição, executou dez exibições de página e saiu. Na terceira visita, o usuário entrou no site por meio de uma pesquisa natural, executou cinco exibições de página, executou uma conversão de US$ 250 e a esquerda. Observe a diferença no rastreamento entre [!DNL Marketing Channels] e Advertising Cloud. O único canal que o Advertising Cloud acompanha nesta jornada é [!UICONTROL Display]. O Advertising Cloud rastreia a visita do canal [!UICONTROL Display] e atribui os dados de envolvimento subsequentes (como exibições de página) e as conversões de volta à influência desse anúncio. [!DNL Marketing Channels], por outro lado, dá uma visão completa de todos os canais.

Como a ID do AMO persiste por meio da jornada do visitante, é possível usar os dados da ID do AMO para ver como a Advertising Cloud influencia outros canais de marketing. A ID do AMO [persiste por 60 dias por padrão](/help/integrations/analytics/overview.md), mas você pode configurar a persistência conforme necessário.

## Como combinar dados do Advertising Cloud e de canais de marketing para analisar o desempenho da mídia

Em [!DNL Analytics], você pode combinar os dados de publicidade paga persistentes do Advertising Cloud e os [!DNL Marketing Channels] dados de visita abrangentes para analisar melhor o desempenho da mídia, de modo que possa influenciar melhor a jornada do cliente.

A análise a seguir usa os dados do Advertising Cloud para mostrar diferentes versões de como um anúncio de exibição afeta a conversão do site. Todas as três colunas usam as mesmas métricas de conversão, mas cada coluna conta uma história diferente:

* A Coluna 1 observa os dados da ID do AMO que são persistentes na jornada do visitante. A coluna 1 indica que 641 Inicializações de aplicativos foram, em um ponto, vinculadas a um anúncio do Advertising Cloud por meio de um view-through ou de um evento de click-through. Essa exibição não considera nenhuma outra atribuição [!DNL Marketing Channels].

* No conjunto de dados [!DNL Marketing Channels], no entanto, os 641 Starts de aplicativos são atribuídos a outros canais de marketing. As duas últimas colunas pegam os 641 Aplicativos iniciados e limitam os dados aos canais [!UICONTROL Display Click-Through] e [!UICONTROL Display View-Through], mostrando as conversões que ocorrem em um modelo de atribuição de último toque.

![exemplo de como um anúncio de exibição afeta a conversão do site](/help/integrations/assets/a4adc-mc-display-impact.png)

Você pode levar essa análise um passo adiante. Você pode detalhar a linha do Advertising Cloud ainda mais por canal de marketing para ver onde as conversões do Advertising Cloud são atribuídas ao 641 Applications Starts. Você já sabe que cinco dessas conversões são atribuídas a um Click-through de exibição de último toque e 19 são atribuídas a um view-through de exibição de último toque. Isso ainda deixa 617 Aplicativos iniciados atribuídos a outros canais de marketing. Você pode arrastar e soltar a dimensão Canal de último contato na parte superior do item de linha do Advertising Cloud DSP para revelar a atribuição de canal para o resto dos Aplicativos iniciados e mostrar o impacto entre canais do canal de exibição.

![como adicionar a dimensão Canal de último contato](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Agora você pode ver como os Primeiros passos restantes são atribuídos. O email recebe crédito por 357 inicializações de aplicativos de último contato para as quais uma ID do AMO persistiu. Usando esse tipo de análise, você pode ver o impacto que os anúncios de exibição do Advertising Cloud tiveram em todos os canais. Com apenas um conjunto de dados e modelo de atribuição, esse tipo de insight não estaria disponível.

![exemplo do impacto entre canais dos canais de exibição](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

Você pode melhorar ainda mais a análise usando um Gráfico de pilha definido como &quot;100% empilhado&quot; para mostrar dados de tendência ao longo do tempo. Essa visualização facilita o monitoramento de quais canais de marketing de último toque são mais afetados por suas campanhas de marketing de exibição.

![exemplo do impacto de tendência entre canais de exibição](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Fundamentos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Uso de Advertising Cloud IDs para  [!DNL Marketing Channels] criar regras de processamento](mc-ids.md)
>* [Por que os dados de canal podem variar entre a Advertising Cloud e a [!DNL Marketing Channels]](mc-data-variances.md)
>* [Vídeo: Relatórios com o Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Visão geral da [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)

