---
title: Configurações de anúncio precedente
description: Consulte descrições das configurações de anúncios disponíveis para anúncios precedentes.
feature: DSP Ads
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# Configurações de anúncio precedente

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
> Use um nome que será fácil de localizar quando você anexar o anúncio a uma disposição, no [!UICONTROL Ads] e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: 30sec Preroll&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** (Somente anúncios precedentes padrão e ignoráveis) A largura de toda a unidade de anúncio. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** (Somente anúncios precedentes padrão e ignoráveis) A altura de toda a unidade de anúncio. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Player X]:** A coordenada X para a unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Y]:** A coordenada Y para a unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Width]:** A largura da unidade de anúncio inteira. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

Este campo é igual ao **[!UICONTROL Width]** campo.

**[!UICONTROL Player Height]:** A altura da unidade de anúncio inteira. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

É o mesmo que o **[!UICONTROL Height]** campo.

**[!UICONTROL Show Controls]:** Onde incluir controles de vídeo para o anúncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* ou *[!UICONTROL None]* (padrão).

**[!UICONTROL Preserve Aspect Ratio]:** Manter as proporções de largura e altura do vídeo (*[!UICONTROL Yes]*) ou para estender o vídeo para preencher o espaço disponível (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Anúncios que usam somente tags VAST; somente leitura) A tag VAST de terceiros inserida como fonte de anúncio.

**[!UICONTROL Final VAST Tag]:** (Anúncios que usam somente tags VAST; somente leitura) A tag VAST de terceiros inserida como fonte de anúncio com o necessário [Macros de rastreamento de DSP de publicidade](/help/dsp/campaign-management/macros.md) , se aplicável.

**[!UICONTROL Wmode]:** (Somente para ativação interativa) O modo de janela: *[!UICONTROL window]*, *[!UICONTROL transparent]* ou *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:** (Somente antes da exibição interativa) O formato do reprodutor do anúncio para inventário potencial: *[!UICONTROL VPAID]* ou *[!UICONTROL VPAID & VAST]*. A capacidade de visualização é sempre medida para VPAID, mas VPAID e VAST incluem inventário que não permite a medição da capacidade de visualização. Considere esta distinção se as métricas de visualização forem importantes para sua campanha.

**[!UICONTROL Clock Number]**: (Apenas antes da exibição interativa; Utilizadas apenas no Reino Unido; disponível somente para usuários com permissão) Um identificador exclusivo usado para garantir que o anúncio correto seja transmitido. Se essa configuração não for aplicável, deixe-a em branco.

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

