---
title: Criar manualmente detalhes da ID do contrato
description: Saiba como inserir detalhes manualmente para uma ID de contrato.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: cd9763a7-99d4-4881-9df9-b4e24c55be0f
source-git-commit: 593bfc03d2dd182b817be9eac4792dfd690132a2
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Criar manualmente detalhes da ID do contrato

1. No menu principal, clique em **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. Acima da tabela de dados, clique em **[!UICONTROL Create]** e selecione **[!UICONTROL Deal ID]**.

1. Insira o [configurações de negócios](deal-id-settings.md):

   1. No [!UICONTROL Deal ID basics] especifique os detalhes do negócio e os anunciantes que podem acessá-lo. Para ofertas garantidas, você também deve especificar as datas de voo planejadas e a estimativa de impressões, somente para fins de rastreamento.

   1. (Somente usuários administradores; opcional) na [!UICONTROL Technical] edite as configurações padrão conforme necessário.

   1. Clique em **[!UICONTROL Save]**.

1. (Somente ofertas garantidas) Selecione os anúncios que serão usados para a negociação e crie um posicionamento programático padrão garantido (PG).

   As disposições PPG padrão garantem que seu negócio sempre retorne uma licitação para cada solicitação de licitação. Se você não criar uma disposição PPG padrão, quaisquer disposições que direcionem o negócio não colocarão ofertas, a menos que estejam configuradas corretamente. Você sempre deve criar uma disposição PPG padrão. No [!UICONTROL Placements] exibição, as disposições padrão do PG têm uma [!UICONTROL Sub-type] valor da coluna de &quot;[!UICONTROL PG Default].&quot;

   Opcionalmente, você pode usar a negociação como um destino de inventário em disposições adicionais, mas deve configurá-las corretamente para colocar ofertas.

   1. No [!UICONTROL Ad & Campaign Selection] selecione os anúncios que serão usados para o negócio:

      1. Selecione o anunciante, a campanha e o tipo de anúncio. Opcionalmente, selecione um status de publicidade para filtrá-los.

      1. Na lista de anúncios disponíveis, marque a caixa de seleção ao lado de cada anúncio que será usado para o negócio.

      1. Clique em **[!UICONTROL Apply]**.
   1. Na tela de configurações de posicionamento:

      1. Insira o nome da disposição.

      1. (Opcional) Edite o [configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md), incluindo a substituição da oferta padrão, que é automaticamente preenchida com o valor CPM da transação; alteração do intervalo de datas; ou anexar mais anúncios.

      A negociação é automaticamente direcionada na seção Metas de inventário . Todas as outras opções de direcionamento são inaplicáveis.

      1. Clique em **[!UICONTROL Create placement]**.



Após criar a negociação, você pode usar a negociação como destino de inventário para várias disposições.

>[!NOTE]
>
> Não é necessário enviar a tag de negócio ao editor para verificação.

>[!TIP]
>
>* No [!UICONTROL Inventory] > [!UICONTROL Deals] , a [!UICONTROL Pacing & Budget] mostra como a negociação está indo para a data de voo e o objetivo de impressão especificados.
>
>* Se o delivery estiver em um ritmo menor ou maior, entre em contato com o editor para ajustar o volume que ele está enviando por meio da negociação.


>[!MORELIKETHIS]
>
>* [Configurações de ID de contrato manual](deal-id-settings.md)
>* [Configurar um acordo programático garantido](programmatic-guaranteed-set-up.md)
>* [Envie um anúncio para um acordo programático garantido com o [!DNL FreeWheel]](freewheel-submit.md)
>* [Sobre contratos programáticos garantidos](programmatic-guaranteed-about.md)

<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->