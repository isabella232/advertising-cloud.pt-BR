---
title: Sobre a ativação de segmentos autenticados de fontes de público-alvo
description: Saiba mais sobre como assimilar segmentos primários de uma plataforma de dados do cliente.
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Sobre a ativação de segmentos autenticados de fontes de público-alvo

<!-- Doesn't specifically explain what you can do in our UI -->
*Recurso beta*

DSP pode assimilar segmentos primários compostos de sinais autenticados criados em uma CDP (Customer Data Platform, plataforma de dados do cliente). Você pode usar os segmentos assimilados como alvos para suas disposições.

## [!DNL Adobe Real-Time Customer Data Profile]

DSP é integrado ao [o [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), que faz parte da Adobe Experience Platform.

Em [!DNL Real-time CDP], *destinos* são conexões com plataformas de dados externas que permitem a ativação contínua de dados. Por exemplo, você pode usar destinos para ativar seus relacionamentos de clientes conhecidos (como endereços de email com hash) para anúncios direcionados em formatos digitais suportados por DSP.

Para obter mais informações sobre destinos, consulte o Experience Platform [Guia de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), incluindo uma visão geral do produto, instruções para [criação de espaços de trabalho de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) e [criação de conexões de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html)e [ativação de dados para destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

### Fluxo de trabalho para usar a integração de DSP com o [!DNL Real-time CDP] {#workflow-sources}

<!-- Make sure that titles make the distinctions clear -- everything can't be "Activate XXX." -->

1. [Permitir que DSP traduza segmentos de dados do cliente em [!DNL LiveRamp RampIDs]](source-durable-id.md) que são reconhecíveis em um ambiente de oferta.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your DSP account team will perform this configuration. -->

1. [Criar uma fonte de público-alvo](source-create.md) para importar públicos para sua conta DSP ou para uma conta do anunciante.

1. [Configure um [!DNL Real-Time CDP] conexão de destino no Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).

Para obter suporte adicional, entre em contato com seu [!DNL Adobe] equipe de conta ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Ativar segmentos autenticados de parceiros de ID duráveis](source-durable-id.md)
>* [Criar uma fonte de público-alvo para ativar públicos-alvo primários](source-create.md)
>* [Configurações de origem do público-alvo](source-settings.md)
>* [Conexão Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Visão geral do catálogo de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)

