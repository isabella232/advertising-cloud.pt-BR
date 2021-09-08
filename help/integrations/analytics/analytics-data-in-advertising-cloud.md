---
title: '[!DNL Analytics] Dados no Advertising Cloud'
description: '[!DNL Analytics] Dados no Advertising Cloud'
feature: Integration with Adobe Analytics
exl-id: 79fbc809-9965-41c1-971f-3652cc78fee3
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# [!DNL Analytics] Dados no Advertising Cloud

*Anunciantes somente com uma integração Advertising Cloud-Adobe Analytics*

## Segmentos do Analytics

Todos os segmentos criados em [!DNL Analytics] e publicados no Experience Cloud.

Novos segmentos levam de 24 a 48 horas para serem exibidos no Advertising Cloud. As atualizações para segmentos existentes são sincronizadas em cerca de oito horas.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Métricas de envolvimento do site

>[!NOTE]
>
>* [!DNL Analytics] O transmite eventos para o eVar EF ID no Advertising Cloud.  A integração padrão não é compatível com o envio de métricas calculadas ou outras dimensões (eVars) para o Advertising Cloud. No entanto, se a métrica calculada puder ser totalmente capturada em um evento personalizado, o Advertising Cloud poderá assimilar o evento personalizado.
>* [!DNL Analytics] O transmite dados para o Advertising Cloud por hora.


* [!UICONTROL Timespent_secs_1stvisit]: O número de segundos gastos no site durante a primeira visita do visitante.
* [!UICONTROL Timespent_secs_total]: O número total de segundos gastos no site em todas as visitas na janela de retrospectiva de clique.
* [!UICONTROL Pageviews_1stvisit]: O número de exibições de página no site durante a primeira visita do visitante.
* [!UICONTROL Pageviews_total]: O número total de exibições de página no site em todas as visitas na janela de retrospectiva de clique.
* [[!UICONTROL Bounces] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: O número de vezes que  [!DNL Analytics] coletou um  [!UICONTROL EF ID].

## Métricas de conversão

[!DNL Analytics] O transmite métricas de conversão para o Advertising Cloud diariamente.

### Métricas de conversão padrão

* [[!UICONTROL Revenue] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### Métricas de conversão personalizadas

Essas métricas são específicas para o conjunto de relatórios, portanto, as métricas disponíveis variam para cada cliente e conjunto de relatórios.

### Métricas de conversão reservadas

Essas métricas são específicas para o conjunto de relatórios, portanto, as métricas disponíveis variam para cada cliente e conjunto de relatórios.

>[!MORELIKETHIS]
>
>* [Visão geral da [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Métricas do Advertising Cloud no Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)

