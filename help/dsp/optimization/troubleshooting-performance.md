---
title: Solução de problemas de desempenho
description: Consulte problemas comuns de desempenho e veja como solucioná-los.
feature: DSP Optimization
exl-id: adb32257-dede-4623-9840-33221c218443
source-git-commit: d2ad7d47d9cf13411fc831526a6fa4ff698b0a15
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Solução de problemas de desempenho

| Problema | Causa Possível | Ações a serem tomadas |
| --- | --- | --- |
| Nenhum gasto com posicionamento | A disposição não inclui anúncios e/ou os anúncios não estão ativos. | Verifique se todos os anúncios esperados estão conectados à disposição e são aprovados e ativos.<br><br>Além disso, veja se a disposição inclui um agendamento de anúncio personalizado, o que pode limitar o período de voo de cada anúncio. Para visualizar o agendamento do anúncio para uma disposição na exibição Disposições, clique em  **[!UICONTROL ...]>[!UICONTROL Ad schedule]** ao lado do nome da disposição. |
|  | As datas afetadas não estão dentro das datas de envio configuradas. | Verifique se as datas de envio são válidas no nível da campanha, do pacote e da disposição &#x200B; s. |
|  | A meta de orçamento foi alcançada e/ou não é alta o suficiente. | Verifique as configurações de orçamento nos níveis de campanha, pacote e disposição. |
|  | A conta não tem financiamento suficiente. | Para ver se sua conta tem financiamento adequado, acesse **[!UICONTROL Settings]>[!UICONTROL Account]** e olhe para a quantidade de [!UICONTROL Usable Funds]. Se precisar adicionar mais fundos, entre em contato com seu [!DNL Adobe] gerente de conta. |
|  | Não há estoque disponível. | Verifique se as fontes de inventário especificadas ([!UICONTROL Public], [!UICONTROL Private]ou [!UICONTROL On Demand]) são:<ul><li>Configure corretamente.</li><li>Ativo e envio através de leilões.</li><li>Compatível com o tipo de anúncio e disposição aplicáveis.</li></ul><br>Se todas as fontes de inventário forem válidas e ativas, direcione fontes adicionais ou todas as fontes de inventário sempre que possível. |
|  | Nenhum usuário está disponível. | Verifique se os públicos-alvo especificados incluem suficientes usuários ativos. Caso contrário, expanda as metas adicionando mais públicos-alvo. |
| Baixo gasto com posicionamento | O [!UICONTROL Non Bids] A seção do relatório de diagnósticos de posicionamento mostra possíveis motivos para a colocação não ter sido feita uma oferta. | [Revise o [!UICONTROL Non Bids] relatório](/help/dsp/campaign-management/reports/placement-diagnostics.md) para entender por que a disposição não ofereceu.  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
|  | A disposição usa [filtros de pré-oferta](/help/dsp/campaign-management/placements/placement-settings.md) esse limite de licitação. | Reduza em 5% os limites de filtros pré-lances para avaliar o saldo de gastos e o desempenho. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>Lembre-se de que o uso de várias metas de disposição, como filtros pré-lances, geos, inventário e públicos-alvo, pode limitar cumulativamente os lances e os gastos. |
|  | O posicionamento tem uma baixa taxa de ganho. | Aumente o [!UICONTROL Max Bid] para melhorar a taxa de ganho.<br><br><b>OBSERVAÇÃO:</b> Os preços do estoque podem variar de acordo com o direcionamento da disposição.<br><br>Uma taxa de ganho de 10% é considerada saudável. |
|  | Um número reduzido de estoque está disponível. | Direcione fontes adicionais ou todas as fontes de inventário, se possível.<br><br>Lembre-se de que o uso de várias metas de disposição, como filtros pré-lances, geos, inventário e públicos-alvo, pode limitar cumulativamente os lances e os gastos. |
|  | Um número baixo de usuários está disponível. | Verifique se os públicos-alvo especificados incluem suficientes usuários ativos. Caso contrário, expanda as metas adicionando mais públicos-alvo.<br><br>Lembre-se de que o uso de várias metas de disposição, como filtros pré-lances, geos, inventário e públicos-alvo, pode limitar cumulativamente os lances e os gastos. |
|  | O pacote inclui um grande número de disposições ativas. | Reduza o número de disposições ativas no pacote ou aumente o orçamento geral do pacote.<br><br>Se o pacote tiver muitas disposições, mas não tiver orçamento suficiente, DSP poderá não ser capaz de alocar orçamento suficiente para cada disposição. Cada lugar deve ter a oportunidade de gastar pelo menos 2 USD/dia. Por exemplo, se o seu pacote tem um orçamento de 10 dólares por dia, é melhor incluir cinco ou menos disposições. &#x200B; |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configurações da campanha](/help/dsp/campaign-management/campaigns/campaign-settings.md)

