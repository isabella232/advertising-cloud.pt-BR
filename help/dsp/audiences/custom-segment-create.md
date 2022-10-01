---
title: Criar e implementar um segmento personalizado
description: Saiba como criar e implementar um segmento personalizado para rastrear usuários expostos a anúncios ou usuários que visitam suas páginas da Web.
feature: DSP Segments
exl-id: 691903e2-773e-4205-837e-822f435f57a7
source-git-commit: ea9c5ba9263be2c1607d682ac035caae70621020
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# Criar e implementar um segmento personalizado

Você pode coletar seus próprios dados de público-alvo primários criando e implementando um segmento personalizado do Advertising Cloud. Você pode usar o segmento para rastrear a) usuários expostos a anúncios de computadores, dispositivos móveis e dispositivos CTV e b) usuários que visitam páginas da Web específicas. Posteriormente, é possível redirecionar os usuários do segmento com anúncios adicionais ou impedir que os usuários do segmento recebam anúncios adicionais.

>[!NOTE]
>
>Para rastrear as IDs de usuários das solicitações de cancelamento da venda do consumidor no seu site, de acordo com a California Consumer Privacy Act (CCPA), crie um [Segmento de não participação na venda do CCPA](ccpa-opt-out-segment-create.md).

1. Crie o segmento:

   1. No menu principal, clique em **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. Acima da tabela de dados, clique em **[!UICONTROL Create]**.

   1. Insira um **[!UICONTROL Segment Name]**.

   1. Para o **[!UICONTROL Segment Type]**, selecione *[!UICONTROL Custom]*.

   1. Insira o **[!UICONTROL Segment Window]**, que é o número de dias em que o cookie de um usuário permanece no segmento.

      A janela padrão é de 45 dias. Insira um valor de 1 (1) a 365.

   1. Clique em **[!UICONTROL Save]**.

1. Copie e implemente tags para rastrear o segmento, conforme necessário:

   1. Retornar para **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   2. Segure o cursor sobre a linha de segmento e clique em **[!UICONTROL Get Pixel]**.

      * Para rastrear visitantes de desktop e de dispositivos móveis em uma página da Web:

         1. Copie a tag de rastreamento da exibição de página, que é rotulada como &quot;[!UICONTROL Desktop or mobile websites].&quot;

         1. Forneça a tag para o anunciante ou contato do site para implantação.

            O departamento de TI do anunciante ou outro grupo pode precisar agendar ou ser informado sobre a implantação da tag.
      * Para rastrear usuários expostos a uma unidade de anúncio em dispositivos de desktop, móveis ou CTV:

         1. Copie a tag de rastreamento de impressão, que é rotulada como &quot;[!UICONTROL Desktop or mobile ads].&quot;


1. Adicione a tag ao [!UICONTROL Pixel] para cada anúncio relevante ou para o [!UICONTROL Event Pixels] da seção [[!UICONTROL Tracking] configurações para cada posicionamento relevante](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

Depois que uma tag de rastreamento é implementada, você pode usar o segmento nos públicos-alvo ou exclusões para qualquer disposição.

>[!TIP]
>
>Acompanhe o tamanho do segmento à medida que os usuários são acompanhados.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de público-alvo](audience-about.md)
>* [Editar informações de segmento](segment-edit.md)
>* [Excluir um segmento](segment-delete.md)
>* [Exibir pixels de rastreamento para um segmento](segment-view-pixels.md)
>* [Compartilhar ou parar de compartilhar um segmento](segment-share.md)
>* [Criar e implementar um [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Criar um público-alvo reutilizável](reusable-audience-create.md)
>* [Fornecedores de dados de terceiros disponíveis](third-party-data-providers.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)

