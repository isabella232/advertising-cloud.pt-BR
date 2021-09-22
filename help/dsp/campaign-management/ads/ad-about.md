---
title: Sobre o Gerenciamento de anúncios no Advertising Cloud DSP
description: Saiba mais sobre o gerenciamento de anúncios.
feature: DSP Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# Sobre o Gerenciamento de anúncios no Advertising Cloud DSP

<!-- add "The Ads View (Dashboard?)" section -->

O Advertising Cloud DSP oferece duas maneiras de veicular seus anúncios:

* A Advertising Cloud DSP disponibilizará seus anúncios gratuitamente quando você fizer upload de seus próprios ativos (como banners de exibição, ativos de vídeo, arquivos de áudio ou URLs) diretamente para o DSP. Para ativos DSP servidos, você tem acesso a recursos adicionais, como sobreposições.

* Se você usar um servidor de publicidade de terceiros (como Google, Flashtalk ou Sizmek), é possível fazer upload de tags de veiculação de anúncios de terceiros para DSP individualmente ou em massa. O recurso de upload em massa requer que você a) faça o upload das planilhas de tags DoubleClick e Flashtalk ou b) faça o download de um modelo, insira suas tags no modelo e faça novamente o upload do modelo.<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Depois que seus anúncios forem configurados, será necessário anexar cada anúncio a uma disposição, que inclui os parâmetros de definição de metas (como geografia, público-alvo, dispositivo e segmentação de inventário) que controlarão o desempenho da sua campanha. Você pode anexar um único anúncio a uma ou várias disposições.

## Tipos de anúncio disponíveis

* Áudio
* TV conectada
* Exibir
* Celular
* Nativo
* Precedente

Para obter mais informações sobre esses tipos de anúncios, consulte [Tipos de anúncio disponíveis](ad-types.md) e as [Especificações de anúncio](/help/dsp/assets/ad-specs.pdf) completas.

## Recursos de anúncios especiais

Os recursos a seguir estão disponíveis somente para anúncios veiculados DSP.

### Banners complementares

Os banners complementares são servidos juntamente com [anúncios precedentes](ad-settings-pre-roll.md) ou (com alguns editores) [anúncios de áudio](ad-settings-audio.md) e podem ajudar a reforçar a associação de marca e mensagem.

>[!NOTE]
>
>* Nem todos os editores permitem banners de companheiro. Os editores que permitem banners de companheiro não garantem impressões de banner de companheiro.
>* Os banners complementares de tags de anúncios de terceiros nem sempre estão disponíveis para visualização.


Você pode fazer upload de seu próprio ativo de banner complementar ou fazer upload de uma tag de banner de iFrame ou script de terceiros de um parceiro de veiculação de anúncios certificado de terceiros.

### Sobreposições

As sobreposições ajudam com a marca persistente em todo o vídeo e podem gerar cliques adicionais. O recurso de sobreposição está disponível para [anúncios antes da exibição interativos](ad-settings-pre-roll.md) e para [anúncios móveis em formatos interativos e de toque para reprodução](ad-settings-mobile.md).

Consulte as [Práticas recomendadas para projetar sobreposições](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)

### Teasers

Um teaser é uma imagem atraente que atrai o visualizador para reproduzir um anúncio. Os teasers se aplicam apenas aos formatos de anúncio de toque para reprodução móvel.

## Aprovações de anúncio do Advertising Cloud DSP

Quando você cria uma publicidade, a Advertising Cloud DSP a analisa para categorias confidenciais, clica na funcionalidade do URL e visualiza a renderização.

Inicialmente, você verá um ponto vermelho na coluna [!UICONTROL Status]. O processo de revisão normalmente leva de 24 a 48 horas. Um anúncio quebrado, no entanto, pode ter um status pendente por mais de 48 horas, portanto, você tem tempo para corrigir erros antes que o anúncio seja rejeitado. Os anúncios rejeitados incluem um motivo para a rejeição.

Quando DSP aprovar um anúncio, você verá um ponto verde na coluna Status .

![indicador de aprovação na  [!UICONTROL Status] coluna](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Seu anúncio só será veiculado se DSP e a SSP tiverem aprovado o anúncio. Cada PUP tem os seus próprios requisitos e processo de aprovação.

>[!MORELIKETHIS]
>
>* [Criar uma publicidade](ad-create.md)
>* [Criar vários anúncios de terceiros](ad-create-third-party.md)
>* [Tipos de anúncio disponíveis](ad-types.md)
>* [Especificações do anúncio](/help/dsp/assets/ad-specs.pdf)

