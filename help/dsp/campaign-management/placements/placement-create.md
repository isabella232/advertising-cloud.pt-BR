---
title: Criar uma disposição
description: Saiba como criar uma disposição.
feature: DSP Placements
exl-id: 4e37b571-9af4-4897-bff2-035a5f2600a5
source-git-commit: 608774723f865c22bfdd5c911ac818600a495114
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Criar uma disposição

>[!TIP]
>
>Crie disposições com base em metas de campanha específicas ou necessidades de relatórios.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha na qual a disposição será incluída.

1. Acima da tabela de dados, clique em **[!UICONTROL Create]**. Na seção [!UICONTROL Placement Types] do menu, clique no tipo de posicionamento.

   O tipo de disposição determina o tipo de anúncio que a disposição pode incluir.

1. Insira as [configurações de posicionamento](placement-settings.md):

   1. Especifique as configurações de [!UICONTROL Basics].

   1. Na seção [!UICONTROL Goals] , especifique o [!UICONTROL Gross Budget] e, opcionalmente, especifique metas de posicionamento adicionais.

      Alguns campos têm valores padrão que podem ser substituídos.

      Se o pacote ao qual o posicionamento é atribuído tiver ritmo no nível do pacote, suas metas e configurações de posicionamento refletirão as configurações do pacote.

   1. (Opcional) Na seção [!UICONTROL Geo-Targeting] , restrinja os locais incluídos ou excluídos.

      Se você não identificar locais específicos, todos os locais serão direcionados.

      >[!NOTE]
      >
      >Locais de cidade e DMA não estão disponíveis para inserções do Roku.

   1. Na seção [!UICONTROL Inventory Targeting], restrinja as fontes de inventário para incluir ou excluir.

      Para a maioria dos tipos de disposição, todos os tipos de inventário e todas as fontes para cada tipo são incluídos por padrão. Para disposições [!DNL Roku], você deve especificar o tipo de inventário e as fontes.

   1. (Opcional) Na seção [!UICONTROL Site Targeting] , restrinja os sites que deseja direcionar e especifique os sites que deseja excluir.

   1. (Opcional) Na seção [!UICONTROL Audience Targeting] :

      1. Restrinja o público-alvo. Isso inclui selecionar segmentos de público-alvo para direcionar na disposição.

         Para [!DNL] disposições do Roku, você pode aproveitar a correspondência de público-alvo exclusivo do DSP com [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) ao incluir um ou mais segmentos de público-alvo que podem ser comparados com o conjunto de dados determinístico do [!DNL Roku] (opt-in) do.[
   1. (Para campanhas com definição de metas entre dispositivos em nível de pessoas; (opcional) Quando a disposição segmentar um ou mais públicos específicos, ative o direcionamento entre dispositivos com base em pessoas para a disposição.

      O direcionamento entre dispositivos com base em pessoas é fornecido por [!DNL LiveRamp] usando somente dados dos EUA. O serviço está disponível para todos os anunciantes em US$ 0,35 CPM para impressões que são entregues usando o gráfico de dispositivos [!DNL LiveRamp] (ou seja, para dispositivos não encontrados nos segmentos de público-alvo direcionados).

   1. (Opcional) Na seção [!DNL Brand Safety and Media Targeting] , aplique restrições de segurança da marca para suas disposições.

   1. (Opcional) Na seção [!DNL Tracking] , insira pixels de evento de terceiros ou pixels de conversão para anúncios na disposição.

      >[!NOTE]
      >
      >([!DNL Roku] disposições) Fornecedores de pixel de terceiros aprovados por [!DNL Roku] incluem [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], a13/>, [!DNL Placed], [!DNL Polk] e [!DNL Research Now].[!DNL Oracle]


1. Clique em **[!UICONTROL Create Placement]**.

1. (Opcional) Anexe anúncios à disposição:

   1. Clique em **[!UICONTROL Attach an ad]**.

   1. Siga um destes procedimentos:
   * Para criar uma nova publicidade:

      1. Clique em **[!UICONTROL Create a New Ad].**

      1. Especifique as configurações de anúncio para [anúncios de áudio](/help/dsp/campaign-management/ads/ad-settings-audio.md), [TV conectada](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [anúncios de exibição](/help/dsp/campaign-management/ads/ad-settings-display.md), [anúncios móveis](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [anúncios nativos](/help/dsp/campaign-management/ads/ad-settings-native.md) ou [anúncios precedentes](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md).

      1. Clique em **[!UICONTROL Save & Submit for Review]**.

      1. (Opcional) Para cada publicidade adicional que deseja criar para a disposição, clique em **[!UICONTROL Attach Another Ad]** e repita as Etapas 1-3.

      1. Se não quiser anexar nenhum anúncio existente, clique em **[!UICONTROL I'm done for now]**.
   * Para anexar anúncios existentes na campanha:

      1. Clique em **[!UICONTROL Select an Ad]**.
      1. Siga um destes procedimentos:
         * Para adicionar uma publicidade de cada vez:
            1. Ao lado do nome do anúncio, clique em **[!UICONTROL Select].**
            1. (Opcional) Para cada publicidade adicional que deseja anexar, clique em **[!UICONTROL Attach Another Ad]** e repita o processo.
         * Para adicionar até 20 anúncios por vez:
            1. Marque a caixa de seleção acima da lista de anúncios.
            1. Marque a caixa de seleção ao lado de cada publicidade a ser adicionada.
            1. Clique em **[!UICONTROL Attach]**.
            1. Ao lado do nome da publicidade, clique em **[!UICONTROL Select]**.
      1. (Opcional) Para substituir o período de voo padrão e a rotação de anúncios para anúncios específicos na disposição:
         1. Clique em **[!UICONTROL Custom Schedule Ads]**.

         1. Siga um destes procedimentos:

            * Para adicionar um voo, clique em **[!UICONTROL Add Flight]** e especifique a data de início e de término.

            * Para adicionar um voo existente a um anúncio, clique em **[!UICONTROL +]** na linha de anúncio da coluna de voo.

            * Para remover um voo existente de um anúncio, clique em **[!UICONTROL x]** na linha de anúncio da coluna de voo.

            * (Quando vários anúncios tiverem o mesmo voo) Para girar os anúncios de maneira desigual, clique em **[!UICONTROL Even Rotation]** nas informações de voo e insira o peso relativo pelo qual girar cada anúncio, como uma porcentagem.

               Os pesos totais devem ser iguais a 100.
         1. No canto superior direito, clique em **[!UICONTROL Continue]**.

         1. Revise os detalhes do voo e clique em **[!UICONTROL Save & Finish]**.




>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de disposição](placement-about.md)
>* [Editar uma disposição](placement-edit.md)
>* [Editar o agendamento do anúncio para uma disposição](placement-edit-ad-schedule.md)
>* [Pausar ou ativar uma disposição](placement-pause-activate.md)
>* [Configurações de posicionamento](placement-settings.md)
>* [Atalhos de teclado](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)

   >*[Resolução de Problemas de Desempenho](/help/dsp/optimization/troubleshooting-performance.md)

