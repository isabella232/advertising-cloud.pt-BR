---
title: Criar uma fonte de público-alvo para ativar públicos-alvo primários
description: Saiba como criar uma fonte para importar públicos para sua conta ou conta de anunciante.
feature: DSP Audiences
exl-id: 16eb7cdb-4364-4e94-ba73-0f2d4d200cb9
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Criar uma fonte de público-alvo para ativar públicos-alvo primários

*Recurso beta*

<!-- Will this remain for admin users/Adobe account teams only? -->

Crie uma fonte para importar públicos para sua conta de DSP ou para uma conta de anunciante. Atualmente, é possível importar públicos do [o [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html).

>[!NOTE]
>
>Depois de criar uma fonte para a variável [!DNL Real-Time CDP], será necessário ativar o [!DNL Real-Time CDP] públicos-alvo por meio do destino Adobe Advertising DSP dentro de [!DNL Real-Time CDP] para começar a importá-los. Consulte [as etapas no fluxo de trabalho de ativação](source-about.md#workflow-sources).

1. No menu principal, clique em **[!UICONTROL Audiences] > [!UICONTROL Sources (BETA)].

1. Clique em [!UICONTROL Add Source].

1. No [!UICONTROL Select a Type] selecione o tipo de origem.

   *[!UICONTROL RT-CDP]*: Esse tipo de fonte, para [o [!DNL Adobe Real-Time Customer Data Profile]](source-about.md), é a única opção.

1. Especifique a [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* ou *[!UICONTROL Account]*.

1. Insira o restante [configurações de origem](source-settings.md).

   Mantenha uma cópia do [!UICONTROL Source Key] que é gerado. Você precisará do valor posteriormente.

1. Clique em **[!UICONTROL Save]**.

1. No Experience Platform, crie uma conexão de destino de DSP de publicidade usando o [!UICONTROL Source Key] que foi gerada nas configurações de origem do DSP.

Para obter instruções sobre como ativar a conexão de destino DSP, selecionar segmentos e acessar permissões de controle, consulte &quot;[Conexão Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

>[!MORELIKETHIS]
>
>* [Configurações de origem do público-alvo](source-settings.md)
>* [Sobre a ativação de segmentos autenticados de fontes de público-alvo](source-about.md)
>* [Ativar segmentos autenticados de parceiros de ID duráveis](source-durable-id.md)<!-- title?-->
>* [Conexão Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)

