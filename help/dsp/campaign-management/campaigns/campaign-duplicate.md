---
title: Duplicação de uma campanha
description: Saiba como duplicar uma campanha.
feature: DSP Campaigns
exl-id: 2bb4030d-22b0-4a16-aeed-35f64a19df6a
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# Duplicação de uma campanha

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplique uma campanha para criar uma nova campanha com configurações semelhantes. É possível:

* Duplique a campanha do anunciante original ou de outro
* Opcionalmente, duplique os pacotes e disposições originais
* Modificar as datas de lançamento da nova campanha

Consulte &quot;[O que não é duplicado](#campaign-not-duplicated)&quot; para obter uma lista de configurações de posicionamento que não estão duplicadas.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Ao lado do nome da campanha, clique em **... >[!UICONTROL Duplicate]**.

1. Especifique as novas configurações de campanha:

   1. Insira o nome da nova campanha e a data de término da prova.

   1. (Opcional) Altere as configurações padrão.

      Por padrão, a nova campanha é atribuída ao anunciante original, tem um cronograma de envio que começa no dia atual e inclui os pacotes e disposições originais.

1. Clique em **[!UICONTROL Submit]**.

## O que não é duplicado {#campaign-not-duplicated}

Todas as configurações das disposições originais são duplicadas, exceto:

* Configurações do experimento
* (Se você alterar as datas de voo) Programação de anúncio personalizada
* (Se você não anexar anúncios) Peso de anúncio personalizado e agendamento
* Disposições por defeito para ofertas programáticas garantidas (PG) e disposições para [!UICONTROL Simple Ad Serving] negociações
* (Se você copiar disposições para uma campanha diferente):
   * Meta geográfica
   * pixels do evento
   * Anúncios
   * Nível de posicionamento [!DNL DoubleVerify Authentic Brand Safety] segmentos (que substituem os segmentos no nível do anunciante)

>[!MORELIKETHIS]
>
>* [Sobre o Campaign Management](campaign-about.md)
>* [Criar uma campanha](campaign-create.md)
>* [Editar uma campanha](campaign-edit.md)
>* [Configurações da campanha](campaign-settings.md)

