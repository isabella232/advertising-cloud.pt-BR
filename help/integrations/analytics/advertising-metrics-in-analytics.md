---
title: Métricas de publicidade do Adobe no Analysis Workspace
description: Métricas de publicidade do Adobe no Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: d740bd19-c643-4917-9cfd-f9cf0affd07e
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Métricas de publicidade do Adobe no Analysis Workspace

*Anunciantes apenas com uma integração Adobe Advertising-Adobe Analytics*

>[!NOTE]
>
>* O Adobe Advertising transmite métricas de tráfego e dimensões para [!DNL Analytics] diariamente.
>* [!DNL Analytics] captura Adobe Advertising click-throughs e view-throughs em tempo real.


## Métricas de tráfego da publicidade Adobe

>[!NOTE]
>
>Todas as métricas de tráfego do Adobe Advertising em [!DNL Analytics] comece com &quot;AMO&quot;.

| Métrica de tráfego | Descrição |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | O número de impressões de Adobe Advertising. |
| [!UICONTROL AMO Clicks] | O número total de cliques no Adobe Advertising. |
| [!UICONTROL AMO Cost] | O Adobe Advertising gasto na moeda do conjunto de relatórios. |
| [!UICONTROL AMO ID Instance] | O número de vezes em que a ID de publicidade do Adobe é definida. |
| [!UICONTROL AMO Minutes Viewed] | O número de minutos em que um vídeo Adobe Advertising foi visualizado. |
| [!UICONTROL AMO Views] | O número de visualizações em um anúncio. Uma exibição é contabilizada quando o visualizador inicia o vídeo Adobe Advertising. |
| [!UICONTROL AMO Views 25% Complete] | O número de visualizações nas quais pelo menos 25% de um vídeo de Adobe Advertising foi assistido. |
| [!UICONTROL AMO Views 50% Complete] | A quantidade de visualizações para as quais pelo menos 50% de um vídeo de Adobe Advertising foi assistido. |
| [!UICONTROL AMO Views 75% Complete] | O número de visualizações nas quais pelo menos 75% de um vídeo de Adobe Advertising foi assistido. |
| [!UICONTROL AMO Views 100% Complete] | A quantidade de visualizações para as quais 100% de um vídeo de anúncio de Adobe foi assistido. |
| [!UICONTROL AMO Viewable Impressions] | O número de impressões que foram medidas para serem visualizadas de acordo com a configuração da disposição. |
| [!UICONTROL AMO Not Viewable Impressions] | O número de impressões que foram determinadas como não visualizáveis. Esse valor é calculado como ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable ]). |
| [!UICONTROL AMO Measurable Impressions] | O número de impressões servidas para as quais a instrumentação de visualização foi inicializada com êxito. Esse valor é calculado como (impressões instrumentadas - o número de impressões não mensuráveis). |

## Métricas calculadas personalizadas úteis para publicidade no Adobe

Considere a criação das seguintes métricas para os dados de publicidade do Adobe.

* Cliques para a instância da página de aterrissagem ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]): Essa é a % de pessoas que clicaram no anúncio e o fizeram na página de aterrissagem.
* Taxa mensurável ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Taxa de impressão visualizável ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Custo por exibição ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Custo por clique ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Adobe Advertising Dimension

>[!NOTE]
>
>Todas as dimensões de publicidade Adobe em [!DNL Analytics] são seguidas por &quot;(ID do AMO)&quot;.

| Dimension | Dados de publicidade Adobe aplicáveis | Descrição |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] e [!DNL Search] dados | DSP de publicidade ou o nome do mecanismo de pesquisa |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] e [!DNL Search] dados | O nome da conta. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] e [!DNL Search] dados | RTB ([!DNL DSP]) ou o nome da rede de anúncios ([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] e [!DNL Search] dados | O nome da campanha. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] e [!DNL Search] dados | O pacote ([!DNL DSP]) ou portfólio ([!DNL Search]). |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] dados | O nome da disposição. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] dados | O nome do grupo de anúncios. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] dados | A palavra-chave. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] dados | O tipo de correspondência da pesquisa. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] dados | A palavra-chave e o tipo de correspondência. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] e [!DNL Search] dados | O tipo de anúncio, como `text`, `video`, `display`ou `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] e [!DNL Search] dados | O tipo de anúncio ([!DNL DSP]) ou título da publicidade ([!DNL Search]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] e [!DNL Search] dados | A descrição do anúncio ([!DNL DSP]) ou corpo do anúncio ([!DNL Search]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] dados | O URL exibido na publicidade. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] dados | O URL de destino do anúncio. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] e [!DNL Search] dados | Se a entrada da página de aterrissagem foi um view-through ou um click-through. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] dados | O direcionamento do produto para um anúncio de lista de produtos. |

>[!MORELIKETHIS]
>
>* [Visão geral da [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Dados na publicidade do Adobe](/help/integrations/analytics/analytics-data-in-advertising.md)

