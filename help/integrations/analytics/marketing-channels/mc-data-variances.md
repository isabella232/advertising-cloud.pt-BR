---
title: Por que os dados de canal podem variar entre a publicidade Adobe e [!DNL Marketing Channels]
description: Saiba por que os dados de canal rastreados pela ID do AMO podem variar em relação aos dados de canal rastreados por [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 4605dc7d-43d7-414f-a509-6096c6cf5fd2
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Por que os dados de canal podem variar entre a publicidade Adobe e [!DNL Marketing Channels]

*Anunciantes apenas com uma integração Adobe Advertising-Adobe Analytics*

Uma pergunta comum dos usuários que aprendem sobre a integração da publicidade Adobe e [!DNL Marketing Channels] Os conjuntos de dados do são &quot;O que causa a variação nos dados entre a ID do AMO e o [!DNL Marketing Channels]?&quot; Ou, às vezes, &quot;Por que os dados estão quebrados? Preciso que todas as métricas correspondam aos relatórios.&quot; Felizmente, as discrepâncias não indicam que os dados estão &quot;quebrados&quot;, e as discrepâncias são esperadas e até desejadas. Vamos ver por que a integração foi projetada dessa maneira.

Os dois conjuntos de dados têm casos de uso principal diferentes:

* [!DNL Marketing Channels]: O principal caso de uso para [!DNL Marketing Channels] O é comparar dados em vários canais com um modelo de atribuição comum. Os analistas podem usar a variável [!UICONTROL Marketing Channel] para obter insights aumentados sobre como os canais estão interagindo entre si. Esse insight pode ajudar a estimular decisões de nível macro sobre como investir em cada canal e pode levar a insights sobre como os visitantes de cada canal interagem com o site da Web.

   O [!DNL Analytics] [!UICONTROL Marketing Channel] , portanto, é configurada para capturar e rastrear todos os canais. [!DNL Marketing Channels] também pode ser configurado para capturar view-throughs e click-throughs do Advertising DSP e isso em relação aos outros canais de marketing.

* Adobe Advertising AMO ID: O principal caso de uso dos dados de ID de AMO de publicidade do Adobe é alimentar o [!DNL Adobe Sensei]algoritmos de lance alimentados por. Os algoritmos tomam automaticamente milhares de decisões de lances de nível micro feitas diariamente para maximizar os gastos com publicidade e alcançar os objetivos da [!DNL DSP] ou a [!DNL Search] carteira. Quanto mais dados de conversão os algoritmos conseguirem conectar campanhas, melhor será o algoritmo poder tomar essas decisões de licitação.

   Para coletar esses dados, a variável [!DNL Analytics for Advertising] A integração transmite IDs AMO brutas que podem ser traduzidas como códigos de rastreamento de click-through e view-through na dimensão ID do AMO do Adobe Analytics — que é armazenada como uma variável personalizada (eVar) ou reservada (rVar). Os click-throughs para outros canais não são definidos na dimensão da ID do AMO, portanto, a dimensão da ID do AMO não consegue rastrear a entrada desses outros canais. O resultado é que a ID do AMO persiste [!DNL Marketing Channels] pontos de entrada.

Para obter mais informações sobre possíveis variações de dados entre dados Adobe Advertising rastreados e [!DNL Analytics]-dados rastreados, consulte &quot;[Variações de dados esperadas entre [!DNL Analytics] e publicidade Adobe](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [Variações de dados esperadas entre [!DNL Analytics] e publicidade Adobe](/help/integrations/analytics/data-variances.md)
>* [Fundamentos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Usar IDs de publicidade do Adobe para criar [!DNL Marketing Channels] Regras de processamento](mc-ids.md)
>* [Usando [!DNL Analytics Marketing Channels] com dados de publicidade do Adobe](mc-ac-data.md)
>* [Vídeo: Usando [!DNL Marketing Channels] para relatórios de publicidade do Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

