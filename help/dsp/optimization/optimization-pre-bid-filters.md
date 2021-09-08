---
title: Filtros de pré-lance em nível de posicionamento e como usá-los
description: Consulte os filtros pré-lances de nível de disposição disponíveis e veja como usá-los.
feature: Optimization
exl-id: c699e970-84ca-429b-8062-81804e6c9f21
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Filtros de pré-lance em nível de posicionamento e como usá-los

| Filtro pré-lance | Descrição | Quando usar este filtro |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Define um limite mínimo de previsão para a probabilidade de um leilão resultar em um clickthrough. Por exemplo, se você definir o limite como 0,1%, você não fará lances em um leilão, a menos que a probabilidade prevista de um clique seja maior ou igual a 0,1%.<br><br><b>Observação:</b> os filtros são aplicados antes das metas de otimização. Como resultado, filtros muito estritos podem evitar gastos. | Use quando tiver uma meta mínima de KPI para taxa de clickthrough (CTR) e não quiser gastar seu orçamento quando a CTR estiver abaixo do limite. Esse filtro pode ser bastante restritivo, então é importante definir objetivos realistas. Dependendo de outras restrições no posicionamento, uma meta de 0,03 a 0,07% geralmente é um bom ponto de partida. Você pode otimizar isso no nível do site, conforme necessário, para ajudar a melhorar as métricas.<br><br>Se o objetivo for alcançar um CTR mínimo e o melhor CPM possível, a configuração recomendada é combinar um  [!UICONTROL Click Through Rate] filtro com a meta de otimização &quot;[!UICONTROL Lowest CPM].&quot; Se sua meta for um CPM máximo sem nenhum benefício real para o excesso e um CTR mínimo, o emparelhamento de um filtro [!UICONTROL Click Through Rate] com a meta de otimização &quot;[!UICONTROL Always Max Bid + Highest CTR]&quot; pode ser mais apropriado. |
| [!UICONTROL 100% Completion Rate] | Define uma taxa mínima de conclusão necessária que deve ser cumprida antes de colocar uma impressão em lance. | Use esse filtro quando o objetivo principal da campanha for as taxas de conclusão. Fator em outros parâmetros de definição de metas, mas 65% é a porcentagem inicial recomendada. |
| [!UICONTROL Player Size - Adobe] | Define o tamanho mínimo do reprodutor necessário, usando dados do Advertising Cloud DSP. Você fará uma licitação em uma impressão quando o limite [!UICONTROL Player Size] for atingido. | Use para garantir que você esteja distribuindo o inventário do player em episódio completo usando dados do DSP. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Define o tamanho mínimo do reprodutor necessário, usando dados de [!DNL Moat] ou [!DNL Integral Ad Science] ([!DNL IAS]). Você fará uma licitação em uma impressão quando o limite [!UICONTROL Player Size] for atingido. | Use para garantir que você esteja distribuindo o inventário do player em episódio completo usando dados de [!DNL Moat] ou [!DNL IAS] toda a plataforma.<br><br><b>Observação:</b> use este filtro somente quando a campanha estiver configurada para usar  [!DNL Moat] ou  [!DNL IAS] dados. |
| [!UICONTROL Viewability IAS] | Define a porcentagem mínima de visibilidade necessária, usando dados históricos de [!DNL IAS]. Você fará uma licitação em uma impressão quando o limite especificado for atingido. | Esse filtro funciona melhor, pois mais dados são transferidos por meio de uma integração [!DNL IAS] no nível da campanha.<br><br>Quando a campanha é configurada para usar  [!DNL IAS] dados, a prática recomendada é usar esse filtro com a meta de otimização de pacote &quot;[!UICONTROL Lowest vCPM (IAS)].&quot; Se a integração não estiver habilitada, use esse filtro com a meta de otimização &quot;[!UICONTROL Lowest CPM]&quot;. |
| [!UICONTROL Viewability Moat] | Define a porcentagem mínima de visibilidade necessária, usando dados históricos de [!DNL Moat]. Você fará uma licitação em uma impressão quando o limite especificado for atingido. | Esse filtro funciona melhor, pois mais dados são transferidos por meio de uma integração [!DNL Moat] no nível da campanha.<br><br>Quando a campanha é configurada para usar  [!DNL Moat] dados, a prática recomendada é usar a meta de otimização de pacote &quot;[!UICONTROL Lowest vCPM (Moat)].&quot; Se a integração não estiver habilitada, use esse filtro com a meta de otimização &quot;[!UICONTROL Lowest CPM]&quot;. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Define a porcentagem mínima de visibilidade necessária, usando números e medidas de visibilidade do Advertising Cloud DSP. Você fará uma licitação em uma impressão quando o limite especificado for atingido.<br><br><b>Notas:</b><ul><li>Se a configuração [!UICONTROL Viewability Sensitivity] da campanha for &quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]&quot;, o padrão de avaliação da capacidade de visualização [!DNL Media Rating Council] (MRC) será usado para a campanha. Se a configuração [!UICONTROL Viewability Sensitivity] for &quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]&quot;, o [!DNL GroupM] padrão de avaliação da capacidade de visualização será usado para a campanha.</li><li>As definições de medição de Adobe diferem das definições de terceiros, portanto, pode haver pequenas discrepâncias com dados de terceiros.</li></ul> | A prática recomendada é corresponder a meta de otimização e qualquer configuração de filtro pré-lance com a configuração [!UICONTROL Viewability Sensitivity] da campanha. |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Como o DSP otimiza suas campanhas](optimization-how-dsp-optimizes-campaigns.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Configurações da campanha](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Metas de otimização e como usá-las](optimization-goals.md)

