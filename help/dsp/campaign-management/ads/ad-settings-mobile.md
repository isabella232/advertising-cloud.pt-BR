---
title: Configurações de anúncio móvel
description: Consulte descrições das configurações de anúncios disponíveis para anúncios móveis.
feature: DSP Ads
exl-id: f67c4ba0-1011-4ad6-bd36-98c312b81b67
source-git-commit: 68af6b1846a37689dce0ca13a05cc1611b1f35a9
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---

# Configurações de anúncio móvel

## [!UICONTROL Insert Ad Tag]

*Somente novos formatos de anúncios de vídeo móveis*

**[!UICONTROL URL]** ou **[!UICONTROL Ad Tag]**: Uma tag de anúncio VAST de terceiros ou tag de anúncio que contém ativos criativos e pixels de rastreamento

**[!UICONTROL Ad Title]** ou **[!UICONTROL Title]**: Um nome para o anúncio usado no [!UICONTROL Ads] exibir e relatórios.

>[!TIP]
>
> Para verificar a validade de uma tag VAST, cole-a em um navegador e pressione a **[!UICONTROL Enter]** chave. Se a tag for válida, você verá um arquivo XML que inclui `<VAST>` perto do topo.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: Anúncios de exibição do Mobile

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome que será fácil de localizar quando você anexar o anúncio a uma disposição, na exibição Anúncios e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: 300x250 Gamer&quot;).

**\[Origem de anúncio\]**: (Somente leitura) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** O URL do ativo criativo de terceiros. Qualquer [timestamp] e [[timestamp]] parâmetros serão substituídos por valores reais.

**[!UICONTROL Final Display Code]:** O URL do ativo criativo de terceiros, com o [Macros de rastreamento do Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) , se aplicável.

### [!UICONTROL Basic]: Anúncios de vídeo

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome que será fácil de localizar quando você anexar o anúncio a uma disposição, na exibição Anúncios e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: 30sec (Pré-etiqueta de Telefone&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** A largura da unidade de anúncio inteira. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** A altura da unidade de anúncio inteira. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Player X]:** A coordenada X para a unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Y]:** A coordenada Y para a unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Width]:** A largura da unidade de anúncio inteira. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

É o mesmo que o **[!UICONTROL Width]** campo.

**[!UICONTROL Player Height]:** A altura da unidade de anúncio inteira. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

É o mesmo que o **[!UICONTROL Height]** campo.

**[!UICONTROL Show Controls]:** Onde incluir controles de vídeo para o anúncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* ou *[!UICONTROL None]* (padrão).

**[!UICONTROL Preserve Aspect Ratio]:** Manter as proporções de largura e altura do vídeo (*[!UICONTROL Yes]*) ou para estender o vídeo para preencher o espaço disponível (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Alguns tipos de anúncios) A quantidade de segundos para atrasar a aparência do botão Fechar.

**[!UICONTROL VAST Tag]:** (Anúncios que usam somente tags VAST; somente leitura) A tag VAST de terceiros inserida como ativo criativo.

**[!UICONTROL Final VAST Tag]:** (Anúncios que usam somente tags VAST; somente leitura) A tag VAST de terceiros inserida como o ativo criativo com o necessário [Macros de rastreamento do Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) , se aplicável.

**[!UICONTROL Wmode]:** (Alguns tipos de anúncios) O modo da janela: *[!UICONTROL window]*, *[!UICONTROL transparent]* ou *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

Todos os pixels de rastreamento de evento existentes para a disposição são anexados automaticamente. Você pode desanexar pixels existentes e criar novos pixels, conforme necessário, com base nas suas necessidades de rastreamento para o anúncio individual.

As configurações a seguir se aplicam a cada pixel criado ou editado.

**[!UICONTROL Integration Event]:** O evento que aciona o pixel para ser disparado. Para este tipo de anúncio, use pixels que são acionados no *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se o pixel é um *[!UICONTROL IMG URL]* (arquivo de imagem de pixel 1x1), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** A URL da imagem de pixel, no formato apropriado para a [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** O nome do pixel. Use um nome que o ajude a identificar o pixel com facilidade.

**[!UICONTROL Pixel Provider]:** O provedor de pixel: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* ou *[!UICONTROL Comscore]*.

### [!UICONTROL Sharing]

Obsoleto

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de anúncios](ad-about.md)
>* [Criar um único anúncio](ad-create.md)
>* [Listar as disposições associadas a um anúncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificações do anúncio](/help/dsp/assets/ad-specs.pdf)
>* [Macros Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

