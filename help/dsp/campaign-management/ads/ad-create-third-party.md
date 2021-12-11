---
title: Criar vários anúncios de terceiros
description: Saiba como criar vários anúncios de terceiros de uma só vez.
feature: DSP Ads
exl-id: 83d35d27-1ab6-4fcf-877f-650a2dc6975a
source-git-commit: 19d6a2edf07eecf874537dd9d356737ed9156bd9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Criar vários anúncios de terceiros

Você pode criar até 500 anúncios de terceiros de cada vez, carregando tags que apontam para ativos criativos hospedados em servidores de anúncios de terceiros. Você pode incluir o rastreamento de pixels para as publicidades.<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

Você pode fazer upload de [!DNL DoubleClick] e [!DNL Flashtalking] folhas de tags ou um arquivo preenchido manualmente usando o modelo fornecido.

Para criar um único anúncio de terceiros, consulte [Criar uma publicidade](ad-create.md).

>[!TIP]
>
> A prática recomendada é usar anúncios de terceiros veiculados com segurança usando HTTPS. Os URLs fornecidos usando HTTPS começam com &quot;https&quot;.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha na qual o anúncio será incluído.

1. Acima da tabela de dados, clique em **[!UICONTROL Create]**. Na seção Tipos de anúncio do menu, clique em **[!UICONTROL Bulk upload ads]**.

1. Selecione o servidor de publicidade no qual o anúncio está hospedado: *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]* ou *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] e [!DNL Flashtalking] anúncios) Selecione o tipo de tag a ser usado para cada ativo de vídeo e para cada ativo de exibição. As opções disponíveis variam de acordo com o servidor de publicidade.

1. (Anúncios em todos os servidores de anúncios, exceto [!DNL DoubleClick] e [!DNL Flashtalking]) **[!UICONTROL Download this template]** para baixar um modelo em [!DNL Microsoft Excel] formato de planilha (XLSX), que pode ser preenchido com dados de publicidade e salvo localmente. As colunas necessárias incluem [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag]e [!UICONTROL Ad Types].

1. Clique em **[!UICONTROL Upload]** e selecione um arquivo nos formatos .xlsx ou .xls do dispositivo ou rede.

   Para [!DNL DoubleClick] e [!DNL Flashtalking] publicidades, faça upload de folhas de tags não editadas do servidor de anúncios. Para outros servidores de anúncios, use o modelo baixado na Etapa 3.

1. Após concluir o upload, clique em **[!UICONTROL Start Building Ads]**.

1. Revise os detalhes e o status de cada anúncio:

   1. Revise o status de cada anúncio, que é baseado em verificações de validação na tag carregada.
   1. (Opcional) Siga um destes procedimentos para cada anúncio:
      * Para visualizar uma publicidade, clique em ![play](/help/dsp/assets/play.png) na linha publicidade.
      * Para editar os detalhes da publicidade, clique em ![editar](/help/dsp/assets/edit.png), edite os detalhes e clique em **Salvar**.
      * Para remover uma publicidade, clique em **[!UICONTROL X]** na linha publicidade.

1. Clique em **[!UICONTROL Create *N *Anúncio(s)]**.

1. Siga um destes procedimentos:

   * Clique em **[!UICONTROL Done]**.

   * (Se um anúncio for rejeitado; (opcional) Para editar o registro de anúncio e reenviar o anúncio para revisão:
      1. Clique no nome da publicidade.
      1. Edite as configurações do anúncio.
      1. Clique em **[!UICONTROL Save & submit for review]**.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de anúncios](ad-about.md)
>* [Criar uma publicidade](ad-create.md)
>* [Tipos de anúncio disponíveis](ad-types.md)
>* [Especificações do anúncio](/help/dsp/assets/ad-specs.pdf)
>* [Vídeo: Como fazer upload em massa de tags de anúncios de terceiros](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)

