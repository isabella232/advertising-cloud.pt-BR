---
title: Casos de uso
description: Saiba mais sobre os casos de uso para compartilhar dados de mídia de DSP de publicidade com o Audience Manager
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Casos de uso para capturar dados de exposição de mídia no Adobe Audience Manager

*Somente anunciantes com DSP publicitária*

*Anunciantes apenas com uma integração Adobe Advertising-Adobe Audience Manager*

Veja a seguir algumas maneiras de se beneficiar da captura dos dados de exposição de mídia DSP publicidade <!-- ad impression data? --> em Audience Manager.

## Gerenciamento de recenticidade e frequência

Capturar dados de impressão no Audience Manager permite aprimorar o gerenciamento de frequência criando segmentos de usuários que foram expostos a um anúncio ou campanha específica. Você pode usar esses segmentos para o direcionamento de anúncios se quiser aumentar a frequência ou para a supressão de anúncios se desejar limitar a frequência.

Além disso, com Audience Manager [!DNL Segment Builder], você pode aplicar [controles de recenticidade e frequência](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) a qualquer [características com base em regras](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) que contêm sinais acionáveis. Isso permite, por exemplo, limitar o número de vezes que um usuário é exibido em um anúncio específico em uma campanha de mídia. Ler &quot;[Supressão instantânea entre dispositivos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)&quot; para aprender a fazer isso.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Mensagens sequenciais

Ao capturar dados de impressão, é possível criar um segmento de usuários que foram expostos a uma campanha ou anúncio e usar esse segmento para mensagens sequenciais ou supressão. Por exemplo, você pode redirecionar usuários que viram criativos `123` mas não clicou converteu ao mostrar a eles criativos `456`.

Para executar esse exemplo no Audience Manager, siga estas etapas:<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Crie uma característica para capturar os usuários que viram a criação.

   Por exemplo, para nomear a característica `Creative Trait 123`, use a seguinte regra de característica:

   `d_creative == 123 AND d_event == imp`

1. Crie uma característica para capturar usuários que clicam ou convertem.

   Por exemplo, para nomear essa característica `Click and Converter`, use a seguinte regra de característica:

   `d_event == click OR d_event=conv`

1. Crie um segmento chamado `Retarget Users` para preencher com usuários que viram criativos `123` mas não clicaram ou converteram. Use a seguinte regra de característica:

   `Creative Trait 123 AND NOT Click and Converter`

1. Mapear o segmento `Retarget Users` para um destino e direcione usuários no destino com criativos `456`.

## [!DNL Adobe Audience Analytics] Dados de exposição e campanha

Quando a impressão da campanha e os dados de cliques estiverem disponíveis no Audience Manager, você poderá criar características e segmentos de usuários que foram expostos ou interagiram com uma campanha ou tática específica. Com um [[!DNL Audience Analytics] integração](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html), seus segmentos do Audience Manager podem ser sincronizados com [!DNL Analytics] para uma análise mais aprofundada. Os casos de uso potenciais incluem:

* **Análise de interação entre DSP e [!DNL Adobe Advertising Search] anúncios:** O padrão [[!DNL Analytics for Advertising] integração](/help/integrations/analytics/overview.md) não fornece insights da interação entre o DSP e o [!DNL [!DNL Search]] porque ambos os canais usam IDs AMO que seguem regras de atribuição da ID do AMO, para as quais um clique de pesquisa substitui uma view-through de exibição. Ao criar um segmento de exposição de DSP no Audience Manager, você pode usar [!DNL Audience Analytics] para analisar a interação entre DSP e [!DNL [!DNL Search]] publicidades em [!DNL Analytics].

* **Análise de frequência:** Você pode criar segmentos no Audience Manager com base em quantas vezes um usuário foi exposto a um determinado anúncio ou campanha. Em seguida, você pode analisar os diferentes segmentos de exposição no Analytics para ver como o comportamento do usuário muda dependendo do número de exposições DSP.

## [!DNL Audience Optimization Reports]

Você pode aproveitar [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) para identificar oportunidades potenciais de desempenho para segmentos em suas campanhas. Esses relatórios combinam dados de impressão de campanha, clique e conversão com métricas de segmento para informar otimizações centradas em segmentos e uma combinação de canais eficaz.

### Tipos de relatórios relevantes do Audience Optimization

| Relatório | Descrição |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Relatório](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | Compara segmentos mapeados e não mapeados por impressões e taxas de conversão. |
| [[!UICONTROL Trend Analysis and Volume Analysis] Relatórios]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Retorne dados sobre impressões, taxas de click-through e conversões para uma grande variedade de dimensões de anúncio. |
| [[!UICONTROL Optimal Frequency] Relatório](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | Ajuda você a descobrir o equilíbrio ideal entre o número de impressões e conversões enviadas. Permite ajustar o número de impressões a serem exibidas antes de começar a ver retornos decrescentes. |
| [[!UICONTROL Unique User Reach] Relatório](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | Um gráfico de bolhas, em que cada bolha é dimensionada em proporção direta ao número de usuários únicos para a dimensão selecionada. |

### Considerações

* If [!DNL Audience Optimization Reports] os usuários têm controles de acesso com base em funções (RBAC) e [!DNL Adobe Customer Care] deve configurar um mapeamento entre a ID do anunciante e o código de integração da fonte de dados do Audience Manager da organização. Os usuários administradores podem então fornecer direitos RBAC para diferentes usuários.

* Relatório de conversão em [!DNL Audience Optimization Reports] exige configuração pelo usuário final. Os usuários devem preencher arquivos de metadados.

* [!DNL Audience Optimization Reports] não suporta alterações nos metadados da campanha (como nome da campanha ou nome da disposição).

* Cliques em anúncios de pesquisa são incluídos em [!DNL Audience Optimization Reports] somente quando estiverem correlacionadas com impressões. Em outras palavras, os cliques de pesquisa são tratados como conversões após impressões. Como resultado, muitos cliques de pesquisa podem não ser incluídos no [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [Visão geral do envio DSP dados de exposição de mídia para o Adobe Audience Manager](overview.md)
>* [Coletar dados de cliques e impressões de campanhas de publicidade DSP](collect.md)

