---
title: Métricas do Advertising Cloud no Analysis Workspace
description: Métricas do Advertising Cloud no Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: d740bd19-c643-4917-9cfd-f9cf0affd07e
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Métricas do Advertising Cloud no Analysis Workspace

*Anunciantes somente com uma integração Advertising Cloud-Adobe Analytics*

>[!NOTE]
>
>* O Advertising Cloud transmite métricas e dimensões de tráfego para [!DNL Analytics] diariamente.
>* [!DNL Analytics] O captura click-throughs e view-throughs do Advertising Cloud em tempo real.


## Métricas de tráfego do Advertising Cloud

>[!NOTE]
>
>Todas as métricas de tráfego do Advertising Cloud em [!DNL Analytics] começam com &quot;AMO&quot;.

| Métrica de tráfego | Descrição |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | O número de impressões do Advertising Cloud. |
| [!UICONTROL AMO Clicks] | O número total de cliques do Advertising Cloud. |
| [!UICONTROL AMO Cost] | O gasto da Advertising Cloud na moeda do conjunto de relatórios. |
| [!UICONTROL AMO ID Instance] | O número de vezes em que a Advertising Cloud ID foi definida. |
| [!UICONTROL AMO Minutes Viewed] | O número de minutos em que um vídeo do Advertising Cloud foi exibido. |
| [!UICONTROL AMO Views] | O número de visualizações em um anúncio. Uma exibição é contabilizada quando o visualizador inicia o vídeo do Advertising Cloud. |
| [!UICONTROL AMO Views 25% Complete] | O número de visualizações nas quais pelo menos 25% de um vídeo do Advertising Cloud foi assistido. |
| [!UICONTROL AMO Views 50% Complete] | O número de visualizações nas quais pelo menos 50% de um vídeo do Advertising Cloud foi assistido. |
| [!UICONTROL AMO Views 75% Complete] | A quantidade de visualizações nas quais pelo menos 75% de um vídeo do Advertising Cloud foi assistido. |
| [!UICONTROL AMO Views 100% Complete] | O número de exibições para as quais 100% de um vídeo do Advertising Cloud foi assistido. |
| [!UICONTROL AMO Viewable Impressions] | O número de impressões que foram medidas para serem visualizadas de acordo com a configuração da disposição. |
| [!UICONTROL AMO Not Viewable Impressions] | O número de impressões que foram determinadas como não visualizáveis. Esse valor é calculado como ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable ]). |
| [!UICONTROL AMO Measurable Impressions] | O número de impressões servidas para as quais a instrumentação de visualização foi inicializada com êxito. Esse valor é calculado como (impressões instrumentadas - o número de impressões não mensuráveis). |

## Métricas calculadas personalizadas úteis para o Advertising Cloud

Considere a criação das seguintes métricas para os dados do Advertising Cloud.

* Cliques para Instância de Página Inicial ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]): Essa é a % de pessoas que clicaram no anúncio e o fizeram na página de aterrissagem.
* Taxa mensurável ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Taxa de impressão visualizável ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Custo por exibição ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Custo por clique ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Advertising Cloud Dimension

>[!NOTE]
>
>Todas as dimensões do Advertising Cloud em [!DNL Analytics] são seguidas por &quot;(ID do AMO)&quot;.

| Dimension | Dados Advertising Cloud aplicáveis | Descrição |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] e  [!DNL Search] dados | Advertising Cloud DSP ou o nome do mecanismo de pesquisa |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] e  [!DNL Search] dados | O nome da conta. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] e  [!DNL Search] dados | RTB ([!DNL DSP]) ou o nome da rede de anúncios ([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] e  [!DNL Search] dados | O nome da campanha. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] e  [!DNL Search] dados | O nome do pacote ([!DNL DSP]) ou do portfólio ([!DNL Search]). |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] dados | O nome da disposição. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] dados | O nome do grupo de anúncios. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] dados | A palavra-chave. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] dados | O tipo de correspondência da pesquisa. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] dados | A palavra-chave e o tipo de correspondência. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] e  [!DNL Search] dados | O tipo de anúncio, como `text`, `video`, `display` ou `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] e  [!DNL Search] dados | O tipo de anúncio ([!DNL DSP]) ou título de anúncio ([!DNL Search]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] e  [!DNL Search] dados | A descrição da publicidade ([!DNL DSP]) ou o corpo da publicidade ([!DNL Search]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] dados | O URL exibido na publicidade. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] dados | O URL de destino do anúncio. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] e  [!DNL Search] dados | Se a entrada da página de aterrissagem foi um view-through ou um click-through. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] dados | O direcionamento do produto para um anúncio de lista de produtos. |

>[!MORELIKETHIS]
>
>* [Visão geral da [!DNL Analytics for Advertising Cloud]](overview.md)
>* [[!DNL Analytics] Dados no Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

