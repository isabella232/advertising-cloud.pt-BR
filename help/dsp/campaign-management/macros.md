---
title: Macros Advertising Cloud DSP
description: Consulte as macros disponíveis para rastreamento geral e rastrear cliques em anúncios de terceiros.
feature: Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Macros Advertising Cloud DSP

Uma macro é um comando curto ou abreviado para uma instrução e geralmente segue o formato `${MACRO_NAME}`. O servidor de publicidade da Advertising Cloud DSP executa macros quando o anúncio é veiculado ou clicado.

As macros são usadas mais frequentemente durante o tráfico de código criativo ou metadados de terceiros e personalizados (como pixels de terceiros).

## Macros de rastreamento geral

Use macros de rastreamento geral em todos os tipos de anúncios e tags para retornar dados específicos, conforme necessário.

| Macro | Descrição |
| --------------- | ---------------------- |
| `${USER_ID}` | Identificador de usuário para todos os tipos de dispositivo. |
| `${TM_RANDOM}` | Cachebuster: um número aleatório entre 1 e 1000000 |
| `${TM_PLACEMENT_ID_NUM}` | A ID de posicionamento |
| `${TM_SITE_URL_URLENC}` | O URL transmitido na solicitação de licitação; Codificado por URL |
| `${TM_SITE_DOMAIN_URLENC}` | O subdomínio de página analisado a partir do URL na solicitação de licitação; Codificado por URL |

{style=&quot;table-layout:auto&quot;}

## Clique em Macros para anúncios de exibição de terceiros

Para rastrear com precisão os cliques de anúncios usando tags de exibição de terceiros, DSP requer uma macro de clique de exibição. É necessária apenas uma versão da macro; a macro relevante depende do tipo de tag.

| Macro | Descrição |
| --------------- | ---------------------- |
| `${TM_CLICK_URL}` | Redirecionar URL que permite que servidores de publicidade rastreiem e contem cliques em anúncios na plataforma |
| `${TM_CLICK_URL_URLENC}` | Redirecionar URL que permite que servidores de publicidade que exigem codificação de URL acompanhem e contem cliques de anúncio na plataforma |

{style=&quot;table-layout:auto&quot;}

DSP insere automaticamente macros de clique de exibição em uma tag de exibição ao:

* Exportar tags de publicidade de um parceiro de servidor de publicidade da Advertising Cloud <!-- [Needs PM confirmation.] -->
* Carregar tags de anúncio [!DNL Flashtalking] ou [!DNL Google DoubleClick for Advertisers] em massa diretamente no DSP

Se uma macro de clique estiver ausente durante a criação de um anúncio de exibição, o DSP exibe uma mensagem de aviso, que solicita a inserção manual da macro de clique de exibição apropriada na área correta da tag.

>[!MORELIKETHIS]
>
>* [Configurações de anúncio de áudio](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Configurações de anúncio de áudio](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Configurações de anúncio de áudio](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Configurações de anúncio de áudio](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Configurações de anúncio de áudio](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Configurações de anúncio de áudio](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)

