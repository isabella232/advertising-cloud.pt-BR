---
title: Configurações universais de anúncio de vídeo
description: Consulte descrições das configurações de anúncios disponíveis para anúncios de vídeo universais.
feature: DSP Ads
source-git-commit: 2d344d2ae0438433eb679a5f31f471c2eac4fe26
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Configurações universais de anúncio de vídeo

*Abra o recurso beta*

## [!UICONTROL Insert Ad Tag]

*Somente novos anúncios*

**[!UICONTROL URL]:** O URL da tag VAST.

**[!UICONTROL Title]:** Um título para o arquivo, que está no [!UICONTROL Ads] exibir e relatórios.

>[!TIP]
>
> Para verificar a validade de uma tag VAST, cole-a em um navegador e pressione a **[!UICONTROL Enter]** chave. Se a tag for válida, você verá um arquivo XML que inclui `<VAST>` perto do topo.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome que será fácil de localizar quando você anexar o anúncio a uma disposição, no [!UICONTROL Ads] e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: Vídeo universal de 30 seg&quot;).

**[!UICONTROL Show Controls]:** Onde incluir controles de vídeo para o anúncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* ou *[!UICONTROL None]* (padrão).

**[!UICONTROL Preserve Aspect Ratio]:** Manter as proporções de largura e altura do vídeo (*[!UICONTROL Yes]*) ou para estender o vídeo para preencher o espaço disponível (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Anúncios que usam somente tags VAST; somente leitura) A tag VAST de terceiros inserida como fonte de anúncio.

**[!UICONTROL Final VAST Tag]:** (Anúncios que usam somente tags VAST; somente leitura) A tag VAST de terceiros inserida como fonte de anúncio com o necessário [Macros de rastreamento do Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) , se aplicável.

**[!UICONTROL Wmode]:** O modo da janela: *[!UICONTROL window]*, *[!UICONTROL transparent]* ou *[!UICONTROL opaque]*. Se essa configuração não for aplicável, deixe-a em branco.

**[!UICONTROL Video Format]:** O formato do reprodutor de anúncio para o inventário potencial: *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]* ou *[!UICONTROL VAST]*. A possibilidade de visualização é sempre medida para [!UICONTROL VPAID], mas [!UICONTROL VPAID & VAST] O inclui inventário que não permite a avaliação da capacidade de visualização. Considere esta distinção se as métricas de visualização forem importantes para sua campanha.

Use *[!UICONTROL VAST]*, que não permite a avaliação da capacidade de visualização, quando você direciona a TV conectada ou o inventário que exige rigorosamente apenas o formato VAST (geralmente de fontes de fornecimento como Google Ad Manager, Appnexus, SpotX e Freewheel).

**[!UICONTROL Clock Number]**: (Utilizado apenas no Reino Unido; disponível somente para usuários com permissão) Um identificador exclusivo usado para garantir que o anúncio correto seja transmitido. Se essa configuração não for aplicável, deixe-a em branco.

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
>* [Macros Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

