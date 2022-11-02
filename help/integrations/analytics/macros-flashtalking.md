---
title: Anexar [!DNL Analytics for Advertising Cloud] Macros para [!DNL Flashtalking] Tags de anúncio
description: Saiba por que e como adicionar [!DNL Analytics for Advertising Cloud] macros para seu [!DNL Flashtalking] tags de publicidade
feature: Integration with Adobe Analytics
exl-id: 4b060668-723c-4cd2-b70e-409501ec67de
source-git-commit: ae516c1947d2b163ebd97dd05fb4e2870a1450d2
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Anexar [!DNL Analytics for Advertising Cloud] Macros para [!DNL Flashtalking] Tags de anúncio

*Anunciantes somente com uma integração Advertising Cloud-Adobe Analytics*

*Aplicável somente ao Advertising Cloud DSP*

Se você usar tags de publicidade do [!DNL Flashtalking] para seus anúncios do Advertising Cloud DSP, anexe os parâmetros do Analytics for Advertising Cloud aos URLs da página inicial. O registro de parâmetros `s_kwcid` e `ef_id` parâmetros da string de consulta no URL da página inicial, permitindo que o Advertising Cloud envie dados de clique para os anúncios para o Adobe Analytics.

Usar macros para [!DNL Flashtalking] anúncios de exibição e vídeo para os seguintes tipos de [!DNL Analytics for Advertising Cloud] implementações:

* **Os anunciantes com o [!DNL Adobe] [!DNL Analytics for Advertising Cloud] Código JavaScript implementado em seus sites**: O código JavaScript já registra a variável `s_kwcid` e `ef_id` parâmetros da string de consulta. No entanto, usar macros estende o rastreamento para incluir conversões baseadas em cliques quando cookies de terceiros não são compatíveis. A prática recomendada é adicionar as macros nas seções a seguir às tags de publicidade para capturar dados de click-through adicionais que não são capturados pelo código JavaScript.

>[!NOTE]
>
>O código JavaScript é uma solução para rastreamento de cliques somente enquanto os cookies ainda estão disponíveis. Quando os cookies forem descontinuados, será necessário implementar as seguintes macros.

* **Os anunciantes cujos sites não usam a variável [!DNL Analytics for Advertising Cloud] O código JavaScript e, em vez disso, depende do [!DNL Analytics] encaminhamento pelo lado do servidor somente para dados de click-through** (sem dados de view-through): As macros a seguir são necessárias para relatar a atividade de cliques no site orientada de anúncios que você comprar pelo Advertising Cloud.

## Exibir Tags de Anúncio

No [!DNL Flashtalking] configurações de tag de publicidade, anexe a seguinte macro ao final do URL de click-through na `Clicktag` campo :

```html
?[ftqs:[AdobeAMO]]
```

Exemplo:  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

![Exemplo de [!DNL Flashtalking] configurações de tag de publicidade](/help/integrations/assets/macro-flashtalking-display-ad.png)

## Tags de anúncio de vídeo

No [!DNL Flashtalking] configurações de tag de publicidade, anexe a seguinte macro ao final do URL de click-through na `Clicktag` campo :

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Exemplo:  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

![Exemplo de [!DNL Flashtalking] configurações de tag de publicidade](/help/integrations/assets/macro-flashtalking-video-ad.png)

>[!MORELIKETHIS]
>
>* [Visão geral da [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud IDs usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Anexar [!DNL Analytics for Advertising Cloud] Macros para [!DNL Google Campaign Manager 360] Tags de anúncio](/help/integrations/analytics/macros-google-campaign-manager.md)

