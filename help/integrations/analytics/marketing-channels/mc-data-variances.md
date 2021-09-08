---
title: Por que os dados de canal podem variar entre o Advertising Cloud e [!DNL Marketing Channels]
description: Saiba por que os dados de canal rastreados pela ID do AMO podem variar dos dados de canal rastreados por [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Por que os dados de canal podem variar entre o Advertising Cloud e [!DNL Marketing Channels]

*Anunciantes somente com uma integração Advertising Cloud-Adobe Analytics*

Uma pergunta comum dos usuários que aprendem sobre a integração do Advertising Cloud e dos conjuntos de dados [!DNL Marketing Channels] é &quot;O que causa a variação nos dados entre a ID do AMO e [!DNL Marketing Channels]?&quot; Ou, às vezes, &quot;Por que os dados estão quebrados? Preciso que todas as métricas correspondam aos relatórios.&quot; Felizmente, as discrepâncias não indicam que os dados estão &quot;quebrados&quot;, e as discrepâncias são esperadas e até desejadas. Vamos ver por que a integração foi projetada dessa maneira.

Os dois conjuntos de dados têm casos de uso principal diferentes:

* [!DNL Marketing Channels]: O principal caso de uso do  [!DNL Marketing Channels] é comparar dados em vários canais com um modelo de atribuição comum. Os analistas podem usar a dimensão [!UICONTROL Marketing Channel] para obter insights aumentados sobre como os canais estão interagindo entre si. Esse insight pode ajudar a estimular decisões de nível macro sobre como investir em cada canal e pode levar a insights sobre como os visitantes de cada canal interagem com o site da Web.

   A dimensão [!DNL Analytics] [!UICONTROL Marketing Channel], portanto, é configurada para capturar e rastrear todos os canais. [!DNL Marketing Channels] também pode ser configurado para capturar view-throughs e click-throughs do Advertising Cloud DSP, e isso ocorre em relação aos outros canais de marketing.

* Advertising Cloud AMO ID: O principal caso de uso dos dados da Advertising Cloud AMO ID é alimentar os algoritmos de lance avançados da Advertising Cloud [!DNL Adobe Sensei]. Os algoritmos tomam automaticamente milhares de decisões de lances de nível micro feitas diariamente para maximizar o gasto de publicidade e atingir os objetivos da campanha [!DNL DSP] ou do portfólio [!DNL Search]. Quanto mais dados de conversão os algoritmos conseguirem conectar campanhas, melhor será o algoritmo poder tomar essas decisões de licitação.

   Para coletar esses dados, a integração [!DNL Analytics for Advertising Cloud] passa IDs AMOs brutas que podem ser traduzidas como códigos de rastreamento de click-through e view-through na dimensão ID do AMO do Adobe Analytics — que é armazenada como uma variável personalizada (eVar) ou uma variável reservada (rVar). Os click-throughs para outros canais não são definidos na dimensão da ID do AMO, portanto, a dimensão da ID do AMO não consegue rastrear a entrada desses outros canais. O resultado é que a ID do AMO persiste por meio de pontos de entrada [!DNL Marketing Channes]l.

Para obter mais informações sobre possíveis variações de dados entre dados rastreados pelo Advertising Cloud e [!DNL Analytics] dados rastreados, consulte &quot;[Variações de dados esperadas entre [!DNL Analytics] e Advertising Cloud](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [Variações de dados esperadas  [!DNL Analytics] entre o e o Advertising Cloud](/help/integrations/analytics/data-variances.md)
>* [Fundamentos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Uso de Advertising Cloud IDs para  [!DNL Marketing Channels] criar regras de processamento](mc-ids.md)
>* [ [!DNL Analytics Marketing Channels] Usar com dados do Advertising Cloud](mc-ac-data.md)
>* [Vídeo: Relatórios com o Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

