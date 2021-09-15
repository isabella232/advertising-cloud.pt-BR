---
title: Anexar uma publicidade a uma disposição
description: Saiba como anexar um anúncio a uma disposição.
feature: Ads
exl-id: 4d85b89b-217f-46eb-a8b2-27da4c220be7
source-git-commit: fcd55f882f56c9eacd82d554d30364400b99555c
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 1%

---

# Anexar uma publicidade a uma disposição

## Anexe um novo anúncio da exibição [!UICONTROL Ads]

1. No menu principal, clique em **[!UICONTROL Campaigns]**.
1. Clique no nome da campanha.
1. No submenu, clique em **[!UICONTROL Ads]**.
1. Ao lado do nome da publicidade, clique em **.. >[!UICONTROL Add to Placements]**.
1. Na tela Inserir anúncio, siga um destes procedimentos:
   * Para criar uma nova disposição para o anúncio:
      1. Clique em **[!UICONTROL Create New Placement]**.
      1. Insira as [configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md) e clique em **[!UICONTROL Create Placement]**.
   * Para adicionar o anúncio a uma ou mais disposições existentes:
      1. Clique em **[!UICONTROL Select a Placement].**
      1. Siga um destes procedimentos:
         * Para adicionar uma publicidade de cada vez:
            1. Ao lado do nome do anúncio, clique em **[!UICONTROL Select].**
            1. (Opcional) Para cada publicidade adicional que deseja anexar, clique em **[!UICONTROL Attach to Other Placement]**. Ao lado do nome do anúncio, clique em **[!UICONTROL Select].**
         * Para anexar o anúncio a até 20 disposições por vez:
            1. Marque a caixa de seleção ao lado de **Seleção em massa.&quot;
            1. Marque a caixa de seleção ao lado de cada disposição à qual o anúncio será anexado.
            1. Clique em **[!UICONTROL Attach]**.
      1. Na guia Concluir e revisar , selecione uma das seguintes opções:
         * Para retornar à exibição Anúncios, clique em **[!UICONTROL I'm done for now]**.
         * Para anexar o anúncio a outra disposição, clique em **[!UICONTROL Attach To Other Placement]**.

## Anexar um anúncio novo ou existente na exibição [!UICONTROL Placements]

1. No menu principal, clique em **[!UICONTROL Campaigns]**.
1. Clique no nome da campanha.
1. No submenu, clique em **[!UICONTROL Placements]**.
1. Ao lado do nome do posicionamento, clique em **... > [!UICONTROL Attach Ads].**
1. Na tela [!UICONTROL Add Ad to Placement], siga um destes procedimentos:
   * Para criar uma nova publicidade:
      1. Clique em **[!UICONTROL Create a New Ad]**.
      1. Insira as configurações de anúncio para [anúncios de áudio](ad-settings-audio.md), [TV conectada](ad-settings-connected-tv.md), [anúncios de exibição](ad-settings-display.md), [anúncios móveis](ad-settings-mobile.md), [anúncios nativos](ad-settings-native.md) ou [anúncios precedentes](ad-settings-pre-roll.md).
      1. Clique em **[!UICONTROL Save & Submit for Review]**.

         O [ad review](ad-about.md) para o novo anúncio leva de 24 a 48 horas e inclui verificações de categorias confidenciais, clique na funcionalidade de URL e pré-visualize a renderização. A coluna [!UICONTROL Status] indica se o DSP aprovou o anúncio. Anúncios quebrados podem ter um status pendente por mais de 24 a 48 horas, portanto, você tem tempo para corrigir erros antes de serem rejeitados.

         >[!NOTE]
         >
         >Seu anúncio só será veiculado se DSP e a SSP tiverem aprovado o anúncio. Cada PUP tem os seus próprios requisitos e processo de aprovação.
   * Para selecionar anúncios existentes:
      1. Clique em **[!UICONTROL Select an Ad].**
      1. Especifique os anúncios:
         * Para adicionar uma publicidade de cada vez:
            1. Ao lado do nome do anúncio, clique em **[!UICONTROL Select].**
            1. (Opcional) Para cada publicidade adicional que deseja anexar, clique em **[!UICONTROL Add Another Ad]**. Ao lado do nome do anúncio, clique em **[!UICONTROL Select].**
         * Para adicionar até 20 anúncios por vez:
            1. Marque a caixa de seleção ao lado de **[!UICONTROL Bulk Select]**.&quot;
            1. Marque a caixa de seleção ao lado de cada publicidade a ser adicionada.
            1. Clique em **[!UICONTROL Attach]**.
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
      1. Clique em **[!UICONTROL I'm done for now]**.


>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de anúncios](ad-about.md)
>* [Criar uma publicidade](ad-create.md)
>* [Editar uma publicidade](ad-edit.md)
>* [Listar as disposições associadas a um anúncio](ad-list-placements.md)
>* [Editar o agendamento do anúncio para uma disposição](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)

