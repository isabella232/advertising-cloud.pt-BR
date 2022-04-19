---
title: Anexar [!DNL Analytics for Advertising Cloud] Macros para [!DNL Flashtalking] Tags de anúncio
description: Saiba por que e como adicionar [!DNL Analytics for Advertising Cloud] macros para seu [!DNL Flashtalking] tags de publicidade
feature: Integration with Adobe Analytics
source-git-commit: 915eea83b2dd246f0f512981efca7ac481cf0c6c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Anexar [!DNL Analytics for Advertising Cloud] Macros para [!DNL Flashtalking] Tags de anúncio

*Anunciantes somente com uma integração Advertising Cloud-Adobe Analytics*

*Aplicável somente ao Advertising Cloud DSP*

Se você usar tags de publicidade do [!DNL Flashtalking] para seus anúncios do Advertising Cloud DSP, anexe os parâmetros do Analytics for Advertising Cloud aos URLs da página inicial. Os parâmetros permitem que o Advertising Cloud envie dados de clique para os anúncios para o Adobe Analytics.

Usar macros para [!DNL Flashtalking] anúncios de exibição e vídeo para os seguintes tipos de [!DNL Analytics for Advertising Cloud] implementações:

* **Os anunciantes com o [!DNL Adobe] [!DNL Analytics for Advertising Cloud] Código JavaScript implementado em seus sites**: Você deve ver alguns dados de click-through no Adobe Analytics de anúncios que você compra pelo Advertising Cloud, sem macros extras. Para capturar dados de click-through em navegadores que não aceitam cookies de terceiros e, portanto, não são capturados por meio do código JavaScript, no entanto, adicione as macros nas seções a seguir ao [!DNL Flashtalking] tags de anúncio.

>[!NOTE]
>
>O código JavaScript é uma solução para rastreamento de cliques somente enquanto os cookies ainda estão disponíveis. Quando o Advertising Cloud descontinuar os cookies, a implementação das seguintes macros será necessária.

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


<!-- >* [Append [!DNL Analytics for Advertising Cloud] Macros to [!DNL Google Campaign Manager 360] Ad Tags](macros-google-campaign-manager.md) -->
