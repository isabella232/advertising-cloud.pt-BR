---
title: Enviar um anúncio para um contrato PG [!DNL FreeWheel]
description: Saiba como solicitar aprovação para um anúncio para um contrato programático garantido com um editor no FreeWheel.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: c2caed80f0afc0cbe3572d01dc2c89f13ed13712
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Envie um anúncio para um acordo programático garantido para FreeWheel

*Contas com a [!DNL FreeWheel] Permissão programática garantida somente*

Uma vez [aceitar um acordo programático garantido com um editor no FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), incluindo a seleção de um anúncio e a criação do posicionamento padrão programático garantido para uso no negócio, você deve enviar o anúncio ao FreeWheel para aprovação.

>[!PREREQUISITES]
>
>Trabalhe com seu [!DNL Adobe] para garantir que sua [!DNL DSP] a conta tem permissão para usar o [!DNL FreeWheel] fluxo de trabalho programático garantido.

## Copie uma chave de anúncio para usar com o [!DNL FreeWheel] Acordo {#copy-ad-key}

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Ads]**.

1. Clique em  **[!UICONTROL ...]>[!UICONTROL Edit]** ao lado do nome do anúncio.

1. Depois que as configurações de publicidade forem abertas, copie a chave de publicidade alfanumérica no URL exibido na barra de endereços do navegador.

Por exemplo, no URL a seguir, a chave da publicidade é `3NtNC5ZbaGZtqbei8jD3`

`https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

## Envie um anúncio do [!UICONTROL Ads] Exibir

1. [Copie a chave de publicidade para o anúncio](#copy-ad-key).

1. Ao lado do nome da publicidade, clique em  **[!UICONTROL ...]>[!UICONTROL submit to FreeWheel]**.

1. Verifique a ID da transação e insira [o **[!UICONTROL Ad Key]**](#copy-ad-key)e, em seguida, clique em **[!UICONTROL Submit]**.

   O anúncio deve ser enviado e aprovado antes de ser executado.

1. [Verifique o status de envio do anúncio](freewheel-check-status.md).

## Envie um anúncio do [!UICONTROL Deals] Exibir

1. [Copie a chave de publicidade para o anúncio](#copy-ad-key).

1. No menu principal, clique em **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. Na linha de negociação, clique em ![Menu Opções](/help/dsp/assets/options-menu.png) **>[!UICONTROL submit to FreeWheel]**.

1. Verifique a ID da transação e insira [o **[!UICONTROL Ad Key]**](#copy-ad-key)e, em seguida, clique em **[!UICONTROL Submit]**.

   O anúncio deve ser enviado e aprovado antes de ser executado.

1. [Verifique o status de envio do anúncio](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Visão Geral da Configuração de Contratos Programáticos Garantidos em FreeWheel](freewheel-overview.md)
>* [Aceitar um contrato na Caixa de entrada da ID do contrato](deal-id-inbox-accept.md)
>* [Verifique o status dos anúncios em busca de [!DNL FreeWheel] Contratos programáticos garantidos](freewheel-check-status.md)
>* [Códigos de erro para envios de anúncios de FreeWheel](freewheel-error-codes.md)

