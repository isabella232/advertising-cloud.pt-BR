---
title: Integrações do Advertising Cloud com o Adobe Audience Manager
description: Saiba mais sobre as diferentes maneiras pelas quais o Advertising Cloud pode trocar dados com o Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
source-git-commit: c761c96b32171bcfba12ed4a39235e6e8b6f6d34
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Integrações do Advertising Cloud com o Adobe Audience Manager

Você pode integrar o Advertising Cloud com o Audience Manager das seguintes maneiras.

## Sincronizar o Audience Manager e outros [!DNL Adobe] Segmentos para segmentação de anúncios

A Advertising Cloud Search e a Advertising Cloud DSP podem obter metadados, dados de hierarquia e dados exclusivos de público-alvo para o Audience Manager de um anunciante ou agência e outros [!DNL Adobe] públicos-alvo. Essa conexão única está disponível somente para profissionais de marketing que usam o Advertising Cloud. Consulte &quot;[Importar segmentos do Adobe Audience Manager para o direcionamento de anúncios](/help/integrations/audience-manager/import-audiences.md).&quot;

### Usar Audience Manager e outros [!DNL Adobe] Segmentos a serem criados [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Anunciantes aceitos com [!DNL Advertising Cloud Search] only*

Within [!DNL Search], você pode criar [!DNL Google Ads] O cliente do Google corresponde públicos-alvo de IDs de usuário usando seus segmentos de Audience Manager existentes que têm [!UICONTROL Adobe Media Optimizer (HTTP)] e [!UICONTROL Adobe Media Optimizer Batch Destination] como destinos. ([!DNL Media Optimizer] é um nome antigo para Advertising Cloud Search.) Isso inclui segmentos do Adobe Analytics publicados na Adobe Experience Cloud e segmentos que são criados na Adobe Experience Cloud usando a variável [!DNL People core service]. Para obter mais informações, consulte a ajuda do produto em [!DNL Search].

[Correspondência de clientes de IDs de usuário](https://support.google.com/google-ads/answer/9199250) funcionam como públicos-alvo baseados em tags de site, mas uma ID que não seja de PII é atribuída a membros exclusivos do público-alvo para benefícios distintos em relação à correspondência de clientes padrão e públicos baseados em tags de site.

Para criar as IDs de usuário necessárias, você deve usar uma tag JavaScript do Advertising Cloud <!-- with a user ID parameter -->em seus sites. Entre em contato com a equipe de conta da Advertising Cloud Search para obter mais informações.

![processo de criação de segmentos](/help/integrations/assets/ad_search_user_id_pic.png)

Depois de criar os públicos-alvo, você pode usá-los em [!DNL Google Ads] campanhas como [metas ou exclusões a nível de campanha ou de grupo de anúncios](#audience-manager-targets).

### Usar Audience Manager e outros [!DNL Adobe] Segmentos para segmentar ou excluir anúncios {#audience-manager-targets}

* (Anunciantes aceitos com [!DNL Search]) Você pode usar qualquer [!DNL Google Ads] públicos-alvo que foram [criado usando [!DNL Adobe] segmentos](#audience-manager-google-audiences) como metas ou exclusões a nível de campanha ou de grupo de anúncios em seu [!DNL Google Ads] campanhas.

* (Anunciantes com a Advertising Cloud DSP) Você pode usar seu [!DNL Adobe] segmentos como alvos de disposições de anúncios. Opcionalmente, é possível incluir os segmentos em públicos-alvo reutilizáveis, que podem ser usados como alvos ou exclusões para várias disposições.

* (Anunciantes com a Advertising Cloud Creative) Você pode usar seu [!DNL Adobe] segmentos como alvos para criações específicas em suas experiências de publicidade.

>[!NOTE]
>
>Para obter mais informações sobre como criar públicos-alvo no Audience Manager e no Experience Cloud [!DNL Audience Library] interfaces e casos de uso comuns para diferentes tipos de público-alvo, consulte &quot;[Opções de criação de público-alvo](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## Enviar dados de exposição de mídia DSP para o Audience Manager

*Anunciantes somente com DSP*

Os clientes do Advertising Cloud DSP com Adobe Audience Manager podem capturar dados de campanhas de anúncios usando chamadas de pixel para o Audience Manager. Em seguida, você pode usar os dados da campanha para criar características com base em regras, que podem ser usadas para definir novos segmentos para permitir vários casos de uso de DSP, como segmentação mais avançada, gerenciamento de frequência, análise de marketing e insights de relatórios.

Consulte &quot;[Visão geral do envio DSP dados de exposição de mídia para o Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; para obter mais informações.

## Obtenha insights mais ricos sobre a atividade do site com o Audience Analytics

Clientes da Advertising Cloud com [[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) pode enviar dados rastreados pelo Advertising Cloud e segmentos de Audience Manager para [!DNL Analytics] para obter insights enriquecidos sobre a atividade do site.

Para obter mais informações, consulte &quot;[[!DNL Adobe][!DNL Audience Analytics] para clientes da Advertising Cloud](/help/integrations/audience-manager/audience-analytics.md).&quot;
