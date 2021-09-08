---
title: Criar manualmente detalhes da ID do contrato
description: Saiba como inserir detalhes manualmente para uma ID de contrato.
feature: Private Inventory, Deal IDs
exl-id: cd9763a7-99d4-4881-9df9-b4e24c55be0f
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Criar manualmente detalhes da ID do contrato

1. No menu principal, clique em **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. Acima da tabela de dados, clique em **[!UICONTROL Create]** e selecione **[!UICONTROL Deal ID]**.

1. Insira as [configurações de negócios](deal-id-settings.md):

   1. Na seção [!UICONTROL Deal ID basics] , especifique os detalhes do negócio e os anunciantes que podem acessar o negócio. Para ofertas garantidas, você também deve especificar as datas de voo planejadas e a estimativa de impressões, somente para fins de rastreamento.

   1. (Somente usuários administradores; opcional) Na seção [!UICONTROL Technical], edite as configurações padrão conforme necessário.

   1. Clique em **[!UICONTROL Save]**.

1. (Somente ofertas garantidas) Selecione os anúncios que serão usados para a negociação e crie um posicionamento programático padrão garantido (PG).

   As disposições PPG padrão garantem que seu negócio sempre retorne uma licitação para cada solicitação de licitação. Se você não criar uma disposição PPG padrão, quaisquer disposições que direcionem o negócio não colocarão ofertas, a menos que estejam configuradas corretamente. Você sempre deve criar uma disposição PPG padrão. Na visualização [!UICONTROL Placements], as disposições PPG padrão têm um valor de coluna [!UICONTROL Sub-type] de &quot;[!UICONTROL PG Default].&quot;

   Opcionalmente, você pode usar a negociação como um destino de inventário em disposições adicionais, mas deve configurá-las corretamente para colocar ofertas.

   1. Nas configurações [!UICONTROL Ad & Campaign Selection], selecione os anúncios que serão usados para o negócio:

      1. Selecione o anunciante, a campanha e o tipo de anúncio.

      1. Na lista de anúncios disponíveis, marque a caixa de seleção ao lado de cada anúncio que será usado para o negócio.

      1. Clique em **[!UICONTROL Apply]**.
   1. Na tela de configurações de posicionamento:

      1. Insira o nome da disposição.

      1. (Opcional) Edite as [configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md), incluindo a substituição do lance padrão, que é preenchido automaticamente com o valor CPM do negócio; alteração do intervalo de datas; ou anexar mais anúncios.

      A negociação é automaticamente direcionada na seção Metas de inventário . Todas as outras opções de direcionamento são inaplicáveis.

      1. Clique em **[!UICONTROL Create placement]**.



Após criar a negociação, você pode usar a negociação como destino de inventário para várias disposições.

>[!NOTE]
>
> Não é necessário enviar a tag de negócio ao editor para verificação.

>[!TIP]
>
>* Na exibição [!UICONTROL Inventory] > [!UICONTROL Deals], a coluna [!UICONTROL Pacing & Budget] mostra como a negociação está indo para a data de voo e o objetivo de impressão especificados.
>
>* Se o delivery estiver em um ritmo menor ou maior, entre em contato com o editor para ajustar o volume que ele está enviando por meio da negociação.


>[!MORELIKETHIS]
>
>* [Configurações de ID de contrato manual](deal-id-settings.md)
>* [Configurar um acordo programático garantido](programmatic-guaranteed-set-up.md)
>* [Envie um anúncio para um acordo programático garantido com o [!DNL FreeWheel]](freewheel-submit.md)
>* [Sobre contratos programáticos garantidos](programmatic-guaranteed-about.md)

