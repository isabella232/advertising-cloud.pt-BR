---
title: "Criar um [!UICONTROL Simple Ad Serving] Acordo"
description: "Saiba como criar um pixel de rastreamento para um [!UICONTROL Simple Ad Serving] acordo."
feature: DSP Simple Ad Serving
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Crie um [!UICONTROL Simple Ad Serving] Acordo

1. No menu principal, clique em **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. Acima da tabela de dados, clique em **[!UICONTROL Create]** e selecione **[!UICONTROL Simple Ad Serving]**.

1. Insira o [configurações de negócios](simple-deal-settings.md):

   1. No [!UICONTROL Select Ad Source] , especifique informações sobre o publicador, anunciante e campanha, e tipo de anúncio, e clique em **[!UICONTROL Next]**.

   1. No [!UICONTROL Select Ad(s)] especifique uma publicidade a ser usada como proxy em DSP:

      1. Siga um destes procedimentos:

         * Para anúncios existentes, selecione os anúncios a serem usados.

         * Para novos anúncios, crie um proxy [anúncio de terceiros](/help/dsp/campaign-management/ads/ad-create-multiple.md).
      >[!NOTE]
      > DSP não exibe os anúncios especificados. O editor serve o anúncio.

      1. Clique em **[!UICONTROL Next]**.
   1. Em Detalhes do feed, edite os detalhes do feed e clique em **[!UICONTROL Next]**.

      DSP gera automaticamente uma disposição, chamada &quot;Disposição SAS - &lt;*nome da transação*>,&quot; para o anúncio. No posicionamento, o negócio é automaticamente direcionado no [!UICONTROL Inventory Targets] seção. Todas as outras opções de direcionamento são inaplicáveis.



1. Envie os pixels de rastreamento de eventos para o editor para implementação de uma das seguintes maneiras:

   * (Opcional) Na [!UICONTROL Activate Tag with Publisher] , envie a tag comercial para o editor.

      Quando você conclui as etapas anteriores, o DSP gera uma mensagem de email que pode ser enviada para o editor. A mensagem inclui os detalhes da negociação, um link do qual será recuperada a tag da negociação e um código de autorização para o link.

      1. Revise os detalhes da negociação e execute um dos seguintes procedimentos:

         * Para colar as informações em uma mensagem de email em um aplicativo de email no seu dispositivo, clique em **[!UICONTROL Email & Done]** e selecione o aplicativo de email. O [!UICONTROL CC:] é pré-preenchido com um [!DNL Adobe] endereço de suporte. Você pode enviar a mensagem para o contato apropriado do editor.

         * Para copiar as informações para a área de transferência, clique em **[!UICONTROL Copy Email].** Em seguida, você pode colar manualmente o conteúdo em uma mensagem de email e enviá-lo para o contato apropriado do editor. Você deve incluir uma cópia (CC:) para `publisher-support-global@adobe.com`. Quando terminar de copiar a mensagem, clique em **[!UICONTROL Email & Done]**.
      1. (Se necessário) Siga as instruções do editor para ver se a tag inclui as macros apropriadas, para que a tag funcione com o servidor de anúncios do editor.
   * (Opcional) Envie manualmente os pixels de rastreamento de eventos para o editor:

      1. Na linha de negócios dentro do [!UICONTROL Deals] exibir, clique em ![Menu Opções](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         Os pixels do evento incluem um [!UICONTROL Clickthrough] pixel e um [!UICONTROL Impression] pixel. Anúncios de vídeo e áudio também incluem pixels de evento por quartil concluído (de [!UICONTROL 25% Complete] para [!UICONTROL 100% Complete]).

      1. Copie os pixels de rastreamento de eventos e forneça-os ao editor.



>[!MORELIKETHIS]
>
>* [Sobre [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] Configurações](simple-deal-settings.md)
>* [Exibir um relatório detalhado de um contrato](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
