---
title: Configurações nativas de anúncio de exibição
description: Consulte descrições das configurações de anúncios disponíveis para anúncios nativos.
feature: DSP Ads
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Configurações nativas de anúncio de exibição

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O tipo de anúncio é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de localizar quando você anexar o anúncio a uma disposição, no [!UICONTROL Ads] e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: 15sec Nativo&quot;).

**[!UICONTROL Native Creative]:** Uma imagem de 1200x627 para maximizar o delivery no inventário móvel. Clique em **[!UICONTROL Browse]** e localize o arquivo em seu dispositivo ou rede e clique em **[!UICONTROL Upload]**.

**[!UICONTROL Title]:** Um título atraente para envolver os visualizadores.

**[!UICONTROL Description]:** O corpo do anúncio. O comprimento máximo é de 100 caracteres.

**[!UICONTROL Landing Page]:** O URL no qual o visualizador chega ao clicar no anúncio.

**[!UICONTROL Final Landing Page]:** O [!UICONTROL Landing Page] URL com o necessário [Macros de rastreamento de DSP de publicidade](/help/dsp/campaign-management/macros.md) , se aplicável.

**[!UICONTROL Sponsored By (Advertiser Name)]:** O anunciante do anúncio.

**[!UICONTROL Call to Action]:** (Opcional) A etapa que você deseja que os visualizadores executem quando visualizarem este anúncio.

**[!UICONTROL Advertiser Logo]:** (Opcional) Um logotipo de taxa 1:1 para incluir com o anúncio, para obter mais reconhecimento de marca. Clique em **[!UICONTROL Browse]** e localize o arquivo em seu dispositivo ou rede e clique em **[!UICONTROL Upload]**.

### [!UICONTROL Pixel]

Todos os pixels de rastreamento de evento existentes para a disposição são anexados automaticamente. Você pode desanexar pixels existentes e criar novos pixels, conforme necessário, com base nas suas necessidades de rastreamento para o anúncio individual.

As configurações a seguir se aplicam a cada pixel criado ou editado.

**[!UICONTROL Integration Event]:** O evento que aciona o pixel para ser disparado. Para este tipo de anúncio, use pixels que são acionados no *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se o pixel é um *[!UICONTROL IMG URL]* (arquivo de imagem de pixel 1x1), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** A URL da imagem de pixel, no formato apropriado para a [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** O nome do pixel. Use um nome que o ajude a identificar o pixel com facilidade.

**[!UICONTROL Pixel Provider]:** O provedor de pixel: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* ou *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de anúncios](ad-about.md)
>* [Criar um único anúncio](ad-create.md)
>* [Listar as disposições associadas a um anúncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificações do anúncio](ad-specs.md)
>* [Macros DSP](/help/dsp/campaign-management/macros.md)

