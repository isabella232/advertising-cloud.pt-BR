---
title: Sobre as metas personalizadas
description: Saiba mais sobre as metas personalizadas para definir seus eventos de sucesso em pacotes otimizados para o CPA mais baixo ou o ROAS mais alto.
feature: Optimization
exl-id: 623cb1ef-85ab-4535-aa3a-8e6ec8ae15ee
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Sobre as metas personalizadas

As metas personalizadas definem os eventos bem-sucedidos que um anunciante requer para atingir seus objetivos de negócios. Cada pacote que usa as metas de otimização &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; ou &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot; deve incluir uma meta personalizada que ajudará a atingir a meta de otimização geral. Você pode criar metas personalizadas como *objetives* no Advertising Cloud Search.

![metas personalizadas](/help/dsp/assets/objective-goals.png)

Cada meta personalizada consiste em uma ou mais métricas, ou *propriedades de transação*, e os pesos relativos dessas propriedades de transação. As propriedades de transação disponíveis incluem todas as métricas rastreadas usando o pixel de conversão do Advertising Cloud e pelo Adobe Analytics.

>[!NOTE]
>
>* [!DNL Analytics] dimensões e segmentos não estão disponíveis para otimização do Advertising Cloud.
>* Para usar os eventos do Analytics no DSP, trabalhe com o gerente de conta do Adobe para configurar uma integração no nível do anunciante.
>* [!DNL Analytics] os eventos personalizados seguem essa convenção de nomenclatura:  `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exemplo: `custom_event_16_examplersid`


Por exemplo, suponha que três métricas (propriedades de transação) sejam relevantes para um pacote específico em uma de suas campanhas: &quot;Download de PDF&quot; avaliado em 20 dólares, &quot;Assinatura de email&quot; avaliado em 30 dólares e &quot;Confirmação de pedido&quot; avaliado em 40 dólares. Se você quiser dar peso de acordo com o valor monetário único da ação do cliente, os pesos relativos das propriedades serão 1, 2 e 1,5.

Consulte as [práticas recomendadas para criar metas personalizadas](custom-goal-best-practices.md) para obter dicas sobre como configurar suas metas personalizadas.

Depois de [criar um objetivo personalizado](custom-goal-create.md), você pode [atribuí-lo a um pacote](/help/dsp/campaign-management/packages/package-settings.md) para relatórios e otimização algorítmica usando o Adobe Sensei.

>[!MORELIKETHIS]
>
>* [Criar uma meta personalizada](custom-goal-create.md)
>* [Práticas recomendadas para criar uma meta personalizada](custom-goal-best-practices.md)
>* [Metas de otimização e como usá-las](optimization-goals.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
> * [Como o DSP otimiza suas campanhas](optimization-how-dsp-optimizes-campaigns.md)

