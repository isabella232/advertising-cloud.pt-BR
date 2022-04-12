---
title: Sobre o Gerenciamento de anúncios no Advertising Cloud DSP
description: Saiba mais sobre o gerenciamento de anúncios.
feature: DSP Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 0%

---

# Sobre o Gerenciamento de anúncios no Advertising Cloud DSP

<!-- add "The Ads View (Dashboard?)" section -->

O Advertising Cloud DSP suporta a entrega de anúncios por meio de tags de veiculação de anúncios de terceiros (como Google, Flashtalk ou Sizmek) para vários tipos de anúncios e o upload direto de ativos para anúncios de exibição nativos. Você pode fazer upload de tags de terceiros individualmente ou em massa. Os uploads em massa usam folhas de tags de parceiros ou um modelo de tag em massa.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Depois que seus anúncios forem configurados, será necessário anexar cada anúncio a uma disposição, que inclui os parâmetros de definição de metas (como geografia, público-alvo, dispositivo e segmentação de inventário) que controlarão o desempenho da sua campanha. Você pode anexar um único anúncio a uma ou várias disposições.

## Tipos de anúncio disponíveis {#ad-types}

Todos os tipos de anúncios a seguir estão disponíveis no Advertising Cloud DSP. Para obter as especificações completas para cada tipo de anúncio, consulte o [Especificações do anúncio](ad-specs.md).

* **Anúncios de áudio (somente de terceiros)**: Os anúncios de áudio são reproduzidos entre conteúdo em sites de editores digitais e podem ser executados de forma independente como arquivos de áudio ou junto a banners associados. O áudio é o melhor uso para conscientizar a marca e se envolver com públicos móveis. Os principais indicadores de desempenho para áudio incluem [!UICONTROL Completion Rate] e [!UICONTROL Cost per Completion].

* **Exibir anúncios (somente de terceiros)**: Anúncios de exibição são imagens animadas ou estáticas exibidas em navegadores da Web ou em aplicativos. Clicar na unidade de anúncio leva o usuário para um site ou microsite com marca. A exibição é mais bem usada para impulsionar CPMs eficientes, aumentar a associação de mensagens, adicionar pontos de contato adicionais de marca ou produto e empurrar os usuários para baixo no funil de compra. Inclusão dos principais indicadores de desempenho para exibição [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions]e [!UICONTROL Cost per Conversion]. DSP suporta uma grande variedade de tamanhos de anúncio de banner de exibição.

* **Anúncios do Mobile (somente de terceiros)**: Os anúncios móveis podem estar em vídeo precedente (VAST, MRAID) ou em formato de exibição padrão. O vídeo antes da exibição do Mobile pode ser de reprodução automática ou de clique para reprodução e é melhor usado para alcançar os visualizadores em todas as telas. O monitor padrão Mobile é uma imagem estática exibida em navegadores da Web móveis ou em aplicativos e é melhor usado para complementar as compras de vídeo digital, a associação de mensagens de unidade e adicionar outras marcas ou pontos de contato do produto. Os anúncios móveis também podem funcionar como aquisições em tela inteira ou como intersticiais móveis, que são anúncios móveis de tela inteira e de alto impacto que são mais usados para desenvolver o conhecimento da marca para públicos móveis e gerar conversões.

* **Anúncios de exibição nativos (somente primários)**: Anúncios nativos são suportados no formato de exibição padrão. Os anúncios nativos incluem um título e/ou título, descrição, logotipo e imagem. Os elementos do anúncio são combinados e renderizados para corresponder ao estilo de página do editor, de modo que o anúncio seja combinado com o conteúdo orgânico do editor e gere maior engajamento. O nativo é melhor usado para conscientização da marca e para aumentar a visualização do público-alvo e as taxas de engajamento com a publicidade amigável para o visualizador. Os principais indicadores de desempenho incluem [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions]e [!UICONTROL Cost Per Conversion].

* **Anúncios precedentes (somente de terceiros)**: Os anúncios precedentes (VAST e VPAID) são mostrados antes do conteúdo de vídeo premium e proporcionam uma experiência imersiva e envolvente do visualizador. O vídeo precedente pode ser interativo, conter recursos de mídia avançada e incluir sobreposições, sobreposições e chamadas de ação. Os principais indicadores de desempenho para anúncios de vídeo precedentes incluem [!UICONTROL Video Completion Rate] e [!UICONTROL Viewability Rate].

* **Anúncios de TV conectados (somente de terceiros)**: Os anúncios de TV conectados são exibidos antes e durante o conteúdo de vídeo de TV premium. Todo o inventário da TV conectada é executado em dispositivos de TV, o que significa que o vídeo é reproduzido automaticamente em um ambiente de tela cheia e dormente que os visualizadores não podem ignorar. A TV conectada é o formato de vídeo digital mais próximo dos comerciais da TV. Inclusão dos principais indicadores de desempenho para TV conectada [!UICONTROL Completion Rate].

## Aprovações de anúncio do Advertising Cloud DSP

Quando você cria uma publicidade, a Advertising Cloud DSP a analisa para categorias confidenciais, clica na funcionalidade do URL e visualiza a renderização.

Inicialmente, você verá um ponto vermelho no [!UICONTROL Status] coluna. O processo de revisão normalmente leva de 24 a 48 horas. Um anúncio quebrado, no entanto, pode ter um status pendente por mais de 48 horas, portanto, você tem tempo para corrigir erros antes que o anúncio seja rejeitado. Os anúncios rejeitados incluem um motivo para a rejeição.

Quando DSP aprovar um anúncio, você verá um ponto verde na coluna Status .

![indicador de homologação em [!UICONTROL Status] column](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Seu anúncio só será veiculado se DSP e a SSP tiverem aprovado o anúncio. Cada PUP tem os seus próprios requisitos e processo de aprovação.

>[!MORELIKETHIS]
>
>* [Criar um único anúncio](ad-create.md)
>* [Criar vários anúncios de terceiros](ad-create-multiple.md)
>* [Especificações do anúncio](ad-specs.md)

