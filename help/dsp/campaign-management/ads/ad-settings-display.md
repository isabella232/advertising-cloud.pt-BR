---
title: Exibir configurações do anúncio
description: Consulte descrições das configurações de anúncios disponíveis para anúncios de exibição.
feature: DSP Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# Exibir configurações do anúncio

As configurações a seguir são para anúncios de exibição padrão.

## [!UICONTROL Ad Options]

### Básico

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado. O padrão é *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome que será fácil de localizar quando você anexar o anúncio a uma disposição, no [!UICONTROL Ads] e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: 300x250 Gamer&quot;).

**\[Origem de anúncio\]**: (Somente leitura) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (Somente anúncios de terceiros) Indica que o anúncio é um anúncio de banner expansível. As configurações de expansão relacionadas determinam qual inventário comprar, portanto, certifique-se de que elas reflitam o comportamento do anúncio.

**[!UICONTROL Expansion Method]:** (Somente anúncios de banner expansíveis de terceiros) Se o banner se expande *[!UICONTROL Click]* ou *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (Somente anúncios de banner expansíveis de terceiros) A direção em que o anúncio se expande: *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]* ou *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (Somente anúncios de banner expansíveis de terceiros) O fornecedor certificado para o qual o anúncio está disponível: *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]* ou *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (Somente anúncios de terceiros) O URL do ativo criativo de terceiros. Qualquer [timestamp] e [[timestamp]] parâmetros serão substituídos por valores reais.

**[!UICONTROL Final Display Code]:** (Somente anúncios de terceiros) O URL do ativo criativo de terceiros, com o [Macros de rastreamento do Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) , se aplicável.

**[!UICONTROL Ad Size]:** A largura e a altura do anúncio. Deve ser um [tamanho de anúncio de exibição padrão suportado](ad-specs.md). Você pode inserir manualmente o tamanho do anúncio antes de fazer upload do anúncio ou inserir um [!UICONTROL Display Code]. Se você não inserir o tamanho do anúncio, as dimensões da publicidade carregada ou da tag do anúncio serão inseridas automaticamente como somente leitura. Observe que a publicidade não será salva se as dimensões não estiverem em Telas padrão como tamanhos - por exemplo, 301x250 em vez de 300x250.

>[!IMPORTANT]
>
> O tamanho do anúncio declarado nos campos de largura e altura será correspondido por solicitações de ofertas recebidas. Você pode enfrentar problemas de entrega se as dimensões do anúncio não corresponderem ao tamanho do anúncio declarado.

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
>* [Listar as disposições associadas a um anúncio](ad-list-placements.md)
>* [Especificações do anúncio](ad-specs.md)
>* [Macros Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

