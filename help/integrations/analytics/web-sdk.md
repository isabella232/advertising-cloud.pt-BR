---
title: Usar o [!DNL Last Event Service] Biblioteca JavaScript com [!DNL Web SDK]
description: Saiba mais sobre as etapas para não usar o [!DNL Analytics] [!DNL visitorAPI] library to the [!DNL Experience Platform] [!DNL Web SDK] library for your [!DNL Analytics for Advertising Cloud] implementação.
feature: Integration with Adobe Analytics
source-git-commit: 1ae45d0ceee2efc4fc52b86fd6737d4c7467a6ca
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# Usar o [!DNL Last Event Service] Biblioteca JavaScript com Adobe Experience Platform [!DNL Web SDK]

*Anunciantes somente com uma integração Advertising Cloud-Adobe Analytics*

Se sua organização usar a Adobe Analytics herdada `visitorAPI.js` para coleta de dados, você pode alternar para usar a variável [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) biblioteca (`alloy.js`), que permite interagir com os vários serviços do Experience Cloud por meio da [!DNL Edge Network].

O [!DNL Analytics for Advertising Cloud] [!DNL Last Event Service] A biblioteca JavaScript, no seu estado atual, registra eventos de view-through e de click-through e os une às conversões associadas usando uma ID complementar (`SDID`). O [!DNL Web SDK] , no entanto, não fornece uma [!DNL stitch ID]. Para usar o [!DNL Web SDK] para [!DNL Analytics for Advertising Cloud], será necessário modificar 1) o [!DNL Last Event Service] nas suas páginas da Web e 2) nas suas [!DNL Web SDK] `sendEvent` Comandos adequadamente.

## Etapa 1: Edite seu [!DNL Last Event Service] Tag para gerar uma `[!DNL StitchID]`

No [!DNL Analytics for Advertising Cloud] [!DNL Last Event Service] adicionar código para gerar a tag usada em suas páginas da Web `[!DNL StitchID]` usando o gerador de ID aleatório que está empacotado na biblioteca.

**Tag herdada:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

**Nova tag:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

## Etapa 2: Use [!DNL Web SDK] para enviar o [!DNL StitchID] como Dados XDM para [!DNL Analytics]

Insira a seguinte propriedade no [!DNL Web SDK] `sendEvent` para enviar o [!DNL StitchID] para [!DNL Experience Edge] as [!DNL Experience Data Model] (XDM) para [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] usará o valor como um `SDID`.

**Propriedade a ser adicionada:**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**Exemplo:**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [Visão geral da [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Código JavaScript para [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/javascript.md)

