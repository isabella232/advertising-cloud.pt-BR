---
title: Especificar disposições e anúncios para uma ID de contrato
description: Saiba como usar uma venda privada com inserções e anúncios adicionais.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
source-git-commit: 22f5d8279fadfcf79e2cd41566321f423d63eb16
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---

# Especificar disposições e anúncios para uma ID de contrato

Para ofertas não garantidas, você pode especificar a negociação como um destino de inventário para novas disposições do [!UICONTROL Placements] exibir.

Para ofertas programáticas garantidas (PG), você pode criar novas disposições com anúncios especificados na [!UICONTROL Deals] exibir.

Você também pode [anexar novos anúncios a disposições existentes](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) associados à PG e às ofertas não garantidas a qualquer momento.

## Especificar um Acordo não-garantido como um Destino de inventário para uma disposição

* [Crie uma disposição do [!UICONTROL Placements] exibir](/help/dsp/campaign-management/placements/placement-create.md). No [!UICONTROL Inventory Targeting] selecione o negócio privado.

## Anexar disposições e anúncios a um contrato PG

1. No menu principal, clique em **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. Na linha de negociação, clique em  ![Menu Opções](/help/dsp/assets/options-menu.png) **>[!UICONTROL attach a placement]**.

1. No [!UICONTROL Ad & Campaign Selection] selecione as publicidades que serão usadas para a disposição:

       1. Selecione o anunciante, a campanha e o tipo de anúncio. Opcionalmente, selecione um status de publicidade para filtrá-los.
       
       1. Na lista de anúncios disponíveis, marque a caixa de seleção ao lado de cada anúncio que será usado para o negócio.
       
       1. Clique em **[!UICONTROL Apply]**.
   
   1. Na tela de configurações de posicionamento:

      1. Insira o nome da disposição.

      1. (Opcional) Edite o [configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md), incluindo a substituição da oferta padrão, que é automaticamente preenchida com o valor CPM da transação; alteração do intervalo de datas; ou anexar mais anúncios.

      A negociação é automaticamente direcionada na seção Metas de inventário . Todas as outras opções de direcionamento são inaplicáveis.

      1. Clique em **[!UICONTROL Create placement]**.


A disposição começará a ser executada depois que o editor ativar sua ID de negócios PG.

>[!NOTE]
>
> Não é necessário enviar a tag de negócio ao editor para verificação.

>[!MORELIKETHIS]
>
>* [Sobre inventário privado](private-inventory-about.md)
>* [Listar as disposições e anúncios de um contrato privado](/help/dsp/inventory/private-deal-view-placements.md)
>* [Criar manualmente detalhes da ID do contrato](deal-id-create.md)
>* [Configurações de ID de contrato manual](deal-id-settings.md)
>* [Configurar um acordo programático garantido](programmatic-guaranteed-set-up.md)

