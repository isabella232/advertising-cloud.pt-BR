---
title: Como o DSP otimiza suas campanhas
description: Saiba como o DSP otimiza os pacotes em suas campanhas.
feature: DSP Optimization
exl-id: 054582ef-b677-4725-b25c-b82bf3e5b43e
source-git-commit: d2ad7d47d9cf13411fc831526a6fa4ff698b0a15
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Como o DSP otimiza suas campanhas

Esta página descreve como o mecanismo de otimização do Advertising Cloud DSP, que é alimentado por [!DNL Adobe Sensei]O otimiza os pacotes em suas campanhas. Para dicas e truques sobre como otimizar manualmente suas campanhas, entre em contato com seu [!DNL Adobe] gerente de conta. <!-- add link to trading playbook if we add it to help -->

As metas de otimização de pacotes operam em dois níveis:

* Para cada pacote: DSP aloca o orçamento para cada disposição dentro do pacote com base no desempenho da disposição em relação ao KPI selecionado.

* Para cada colocação/leilão no pacote: DSP calcula o valor de KPI econômico em tempo real para cada leilão por disposição e usa esse valor para determinar a oferta.

   >[!NOTE]
   >
   >O valor econômico pode ser pesadamente ponderado com base no quão bem um posicionamento está a gastar. Se uma disposição estiver por trás da meta de gastos, então ela poderá comprar leilões de qualidade mais baixa. Se uma disposição for facilmente atingindo sua meta de gastos, ela se concentrará em leilões de maior qualidade.

## Otimização de pacotes

DSP pode otimizar sua entrega de duas maneiras fundamentais, com 20 variações disponíveis para alinhar-se à sua meta de desempenho específica. Você pode optar por:

* Priorize a taxa de desempenho

* Priorize o equilíbrio entre a eficiência de custos e a taxa de desempenho

Consulte [Metas de otimização e como usá-las](optimization-goals.md) para determinar qual meta de otimização o ajudará a atingir seus KPIs.

### Pacotes que priorizam a taxa de desempenho

Para metas de otimização que priorizam a taxa de desempenho, o DSP prevê o desempenho de cada leilão e sempre lances no Lance máximo. Exemplos de metas de otimização aplicáveis incluem [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate]e assim por diante.

Esse modo de otimização funciona bem se:

* Você já sabe o nível de CPM efetivo/aceitável (por exemplo, um referencial histórico).

* Você está disposto a ajustar manualmente a variável [!UICONTROL Max Bid] para cada disposição se você enfrentar desafios com o dimensionamento.

* Você está priorizando a escala em relação à eficiência.

#### Lógica de embalagem {#pacing-logic-performance}

* Se os gastos estiverem no ritmo, os lances se tornarão mais seletivos, de modo que você só fará lances em leilões previstos para ter altas taxas de desempenho.

* Se os gastos estiverem atrasados, os lances se tornarão menos seletivos, de modo que você fará lances em leilões que se prevê que tenham taxas de desempenho mais baixas para alcançar o objetivo de ritmo.

#### Limpando Preço/Sombreamento de Oferta {#clearing-price-performance}

Depois de executar a lógica de ritmo, DSP executa a licitação proposta por meio de um modelo de previsão de preço de compensação. Se a previsão indicar que a oferta pode ser reduzida com uma diminuição mínima na taxa de ganho, então a oferta é reduzida de acordo com a previsão.

### Pacotes Que Priorizam A Eficiência Do Equilíbrio De Custos Com A Taxa De Desempenho

Para algumas metas de otimização, o DSP prevê o desempenho de cada leilão e ajusta os preços de licitação automaticamente, nunca excedendo o valor de uma colocação [!UICONTROL Max Bid]. Exemplos de metas de otimização aplicáveis incluem [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click]e assim por diante.

#### Lógica de Pacote {#pacing-logic-balanced}

* Se a despesa estiver no ritmo, então DSP torna-se mais sensível aos preços, colocando os montantes mais baixos na licitação da taxa de ganho com o plano de ritmo.

* Se uma métrica de desempenho também estiver sendo equilibrada (todas as metas exceto [!UICONTROL Lowest CPM]), o KPI previsto é mesclado na quantia que é licitada. Portanto, você faz licitações mais altas para leilões que se prevê sejam mais eficientes com base no &quot;custo por&quot;.

* Se a despesa estiver atrasada, então DSP se torna menos sensível aos preços e propõe montantes mais elevados, até [!UICONTROL Max Bid], para compensar a taxa de ganho com o plano de ritmo.

#### Limpando Preço/Sombreamento de Oferta {#clearing-price-balanced}

Depois de executar a lógica de ritmo, DSP executa a licitação proposta por meio de um modelo de previsão de preço de compensação. Se a previsão indicar que a oferta pode ser reduzida com uma diminuição mínima na taxa de ganho, então a oferta é reduzida de acordo com a previsão.

## Otimização de posicionamento

Os filtros pré-lances de disposição são a maneira mais rígida de garantir um desempenho forte. O DSP usa filtros pré-lances estrategicamente em diferentes tipos de anúncios para atingir metas de desempenho em disposições dentro de cada pacote. Você pode usar filtros pré-lances simultaneamente com otimização em nível de pacote ou independentemente.

>[!NOTE]
>
>Os filtros de pré-lances disponíveis variam por tipo de anúncio. Por exemplo, para um posicionamento de exibição padrão, você pode filtrar por taxa de click-through e visibilidade, mas não por taxa de conclusão.

Consulte [Filtros de pré-lance em nível de posicionamento e como usá-los](optimization-pre-bid-filters.md) para determinar qual filtro pré-lance ajudará você a atingir seus KPIs.

>[!MORELIKETHIS]
>
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Metas de otimização e como usá-las](optimization-goals.md)
>* [Filtros de pré-lance em nível de posicionamento e como usá-los](optimization-pre-bid-filters.md)
>* [Solução de problemas de desempenho](/help/dsp/optimization/troubleshooting-performance.md)

