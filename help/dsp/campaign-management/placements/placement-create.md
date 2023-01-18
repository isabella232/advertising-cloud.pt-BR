---
title: Criar uma disposição
description: Saiba como criar uma disposição.
feature: DSP Placements
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 1%

---

# Criar uma disposição

>[!TIP]
>
>Crie disposições com base em metas de campanha específicas ou necessidades de relatórios.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha na qual a disposição será incluída.

1. Acima da tabela de dados, clique em **[!UICONTROL Create]**. No [!UICONTROL Placement Types] no menu, clique no tipo de posicionamento.

   O tipo de disposição determina o tipo de anúncio que a disposição pode incluir.

1. Insira o [configurações de posicionamento](placement-settings.md):

   1. Especifique a [!UICONTROL Basics] configurações.

   1. No [!UICONTROL Goals] especifique a [!UICONTROL Gross Budget] e, opcionalmente, especifique metas adicionais de posicionamento.

      Alguns campos têm valores padrão que podem ser substituídos.

      Se o pacote ao qual o posicionamento é atribuído tiver ritmo no nível do pacote, suas metas e configurações de posicionamento refletirão as configurações do pacote.

   1. (Opcional) Na seção [!UICONTROL Geo-Targeting] restringir os locais incluídos ou excluídos.

      Se você não identificar locais específicos, todos os locais serão direcionados.

      >[!NOTE]
      >
      >Locais de cidade e DMA não estão disponíveis para inserções do Roku.

   1. No [!UICONTROL Inventory Targeting] , restrinja as fontes de inventário para incluir ou excluir.

      Para a maioria dos tipos de disposição, todos os tipos de inventário e todas as fontes para cada tipo são incluídos por padrão. Para [!DNL Roku] disposições, você deve especificar o tipo de inventário e as fontes.

   1. (Opcional) Na seção [!UICONTROL Site Targeting] , restrinja os sites que deseja direcionar e especifique os sites que deseja excluir.

   1. (Opcional) Na seção [!UICONTROL Audience Targeting] seção:

      1. Restrinja o público-alvo. Isso inclui selecionar segmentos de público-alvo para direcionar na disposição.

         Para [!DNL] Disposições do Roku, você pode aproveitar [Correspondência de público-alvo único da DSP com [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) incluindo um ou mais segmentos de público-alvo que podem ser combinados com a variável [!DNL Roku] conjunto de dados determinísticos (opt-in).
   1. (Para campanhas com definição de metas entre dispositivos em nível de pessoas; (opcional) Quando a disposição segmentar um ou mais públicos específicos, ative o direcionamento entre dispositivos com base em pessoas para a disposição.

      O direcionamento entre dispositivos com base em pessoas é fornecido por [!DNL LiveRamp] usando somente dados dos EUA. O serviço está disponível para todos os anunciantes em US$ 0,35 CPM para impressões que são entregues usando o [!DNL LiveRamp] gráfico de dispositivos (ou seja, para dispositivos não encontrados nos segmentos de público-alvo direcionados).

   1. (Opcional) Na seção [!DNL Brand Safety and Media Targeting] , aplique restrições de segurança da marca para suas disposições.

   1. (Opcional) Na seção [!DNL Tracking] , insira pixels de evento de terceiros ou pixels de conversão para anúncios no posicionamento.

      >[!NOTE]
      >
      >([!DNL Roku] disposições) Fornecedores de pixel de terceiros aprovados por [!DNL Roku] incluir [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]e [!DNL Research Now].


1. Clique em **[!UICONTROL Create Placement]**.

1. (Opcional) Anexe anúncios à disposição:

   1. Clique em **[!UICONTROL Attach an ad]**.

   1. Siga um destes procedimentos:
   * Para criar uma nova publicidade:

      1. Clique em **[!UICONTROL Create a New Ad].**

      1. Especifique as configurações de anúncio para [anúncios de áudio](/help/dsp/campaign-management/ads/ad-settings-audio.md), [TV conectada](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [anúncios de exibição](/help/dsp/campaign-management/ads/ad-settings-display.md), [anúncios móveis](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [anúncios nativos](/help/dsp/campaign-management/ads/ad-settings-native.md), [anúncios precedentes](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)ou [anúncios de vídeo universais](/help/dsp/campaign-management/ads/ad-settings-universal-video.md).

      1. Clique em **[!UICONTROL Save & Submit for Review]**.

      1. (Opcional) Para cada publicidade adicional que você deseja criar para a disposição, clique em **[!UICONTROL Attach Another Ad]** e repita as Etapas 1 a 3.

      1. Se você não quiser anexar nenhum anúncio existente, clique em **[!UICONTROL I'm done for now]**.
   * Para anexar anúncios existentes na campanha:

      1. Clique em **[!UICONTROL Select an Ad]**.

      1. Siga um destes procedimentos:

         * Para adicionar uma publicidade de cada vez:

            1. Ao lado do nome da publicidade, clique em **[!UICONTROL Select].**

            1. (Opcional) Para cada publicidade adicional que deseja anexar, clique em **[!UICONTROL Attach Another Ad]** e repita o processo.
         * Para adicionar até 20 anúncios por vez:

            1. Marque a caixa de seleção acima da lista de anúncios.

            1. Marque a caixa de seleção ao lado de cada publicidade a ser adicionada.

            1. Clique em **[!UICONTROL Attach]**.

            1. Ao lado do nome da publicidade, clique em **[!UICONTROL Select]**.
      1. (Opcional) Para substituir o período de voo padrão e a rotação de anúncios para anúncios específicos na disposição:

         1. Clique em **[!UICONTROL Custom Schedule Ads]**.

         1. Siga um destes procedimentos:

            * Para adicionar um voo, clique em **[!UICONTROL Add Flight]** e, em seguida, especifique a data de início e a data de término.

            * Para adicionar um voo existente a um anúncio, clique em **[!UICONTROL +]** na linha de anúncio da coluna flight.

            * Para remover um voo existente de um anúncio, clique em **[!UICONTROL x]** na linha de anúncio da coluna flight.

            * (Quando vários anúncios tiverem o mesmo voo) Para girar os anúncios de forma desigual, clique em **[!UICONTROL Even Rotation]** nas informações de voo e, em seguida, insira o peso relativo pelo qual girar cada anúncio, como uma porcentagem.

               Os pesos totais devem ser iguais a 100.
         1. No canto superior direito, clique em **[!UICONTROL Continue]**.

         1. Revise os detalhes do voo e clique em **[!UICONTROL Save & Finish]**.






>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de disposição](placement-about.md)
>* [Editar uma disposição](placement-edit.md)
>* [Editar o agendamento do anúncio para uma disposição](placement-edit-ad-schedule.md)
>* [Pausar ou ativar uma disposição](placement-pause-activate.md)
>* [Exibir o log de alterações para uma disposição](placement-change-log.md)
>* [Configurações de posicionamento](placement-settings.md)
>* [Atalhos de teclado](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)

   >*[Solução de problemas de desempenho](/help/dsp/optimization/troubleshooting-performance.md)
>* [Vídeo: Como criar uma disposição de exibição padrão](https://video.tv.adobe.com/v/340454)

