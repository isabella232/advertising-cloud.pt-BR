---
title: Sobre as metas personalizadas
description: Saiba mais sobre as metas personalizadas para definir seus eventos de sucesso em pacotes otimizados para o CPA mais baixo ou o ROAS mais alto.
feature: DSP Optimization
exl-id: 623cb1ef-85ab-4535-aa3a-8e6ec8ae15ee
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Sobre as metas personalizadas

As metas personalizadas definem os eventos bem-sucedidos que um anunciante requer para atingir seus objetivos de negócios. Cada pacote que usa as metas de otimização &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; ou &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot; deve incluir uma meta personalizada que ajude a atingir a meta de otimização geral. Você pode criar metas personalizadas como *objetivos* no Advertising Cloud Search.

![metas personalizadas](/help/dsp/assets/objective-goals.png)

Cada meta personalizada consiste em uma ou mais métricas, ou *propriedades da transação* e os pesos relativos dessas propriedades de transação. As propriedades de transação disponíveis incluem todas as métricas rastreadas usando o pixel de conversão do Advertising Cloud e pelo Adobe Analytics.

>[!NOTE]
>
>* [!DNL Analytics] dimensões e segmentos não estão disponíveis para otimização do Advertising Cloud.
>* Para usar os eventos do Analytics no DSP, trabalhe com sua [!DNL Adobe] equipe de conta para configurar uma integração no nível do anunciante.
>* [!DNL Analytics] os eventos personalizados seguem essa convenção de nomenclatura: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exemplo: `custom_event_16_examplersid`


Por exemplo, suponha que três métricas (propriedades de transação) sejam relevantes para um pacote específico em uma de suas campanhas: &quot;PDF Download&quot; avaliado em 20 USD, &quot;Email Signup&quot; avaliado em 30 USD e &quot;Order Confirmation&quot; avaliado em 40 USD. Se você quiser dar peso de acordo com o valor monetário único da ação do cliente, os pesos relativos das propriedades serão 1, 2 e 1,5.

Consulte a [práticas recomendadas para a criação de metas personalizadas](custom-goal-best-practices.md) para obter dicas sobre como configurar suas metas personalizadas.

Uma vez [criar uma meta personalizada](custom-goal-create.md), você pode [atribuir a um pacote](/help/dsp/campaign-management/packages/package-settings.md) para relatórios e otimização de algoritmos usando o Adobe Sensei.

>[!MORELIKETHIS]
>
>* [Criar uma meta personalizada](custom-goal-create.md)
>* [Práticas recomendadas para criar uma meta personalizada](custom-goal-best-practices.md)
>* [Metas de otimização e como usá-las](optimization-goals.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
> * [Como o DSP otimiza suas campanhas](optimization-how-dsp-optimizes-campaigns.md)

