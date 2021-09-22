---
title: Configurações de anúncio nativo
description: Consulte descrições das configurações de anúncios disponíveis para anúncios nativos.
feature: DSP Ads
exl-id: 3ae59e63-ae64-41b2-8734-3df2da020c7c
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Configurações de anúncio nativo

## [!UICONTROL Upload or Select Creative]

*Somente anúncios de vídeo novos (mas não de exibição)*

**[!UICONTROL Upload Audio]:** Para fazer upload de um ativo bruto no DSP. Ao selecionar essa opção, faça o seguinte:

1. Clique em **[!UICONTROL Choose File]** e localize o arquivo no dispositivo ou na rede.
1. Insira um título para o arquivo, que será usado na exibição [!UICONTROL Ads] e nos relatórios.
1. Clique em **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** para selecionar qualquer criação carregada anteriormente no formato correto na conta.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:**  (somente leitura) o tipo de anúncio que você está criando, que corresponde ao tipo de disposição ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O tipo de anúncio (exibição nativa) ou o título do vídeo (formatos de vídeo) é usado por padrão, mas é possível alterar o nome.

>[!TIP]
>
> Use um nome fácil de localizar quando anexar o anúncio a uma disposição, na visualização [!UICONTROL Ads] e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: 15sec Nativo&quot;).

**[!UICONTROL Native Creative]:** uma imagem de 1200x627 para maximizar o delivery no inventário móvel. Para anúncios de vídeo, essa será a imagem exibida antes da reprodução do vídeo nativo. Clique em **[!UICONTROL Browse]**, localize o arquivo no dispositivo ou na rede e clique em **[!UICONTROL Upload]**.

**[!UICONTROL Title]:** um título atraente que engajará os visualizadores.

**[!UICONTROL Description]:** para anúncios de vídeo, este é um breve resumo do anúncio. Para anúncios de exibição, esse é o corpo do anúncio. O comprimento máximo é de 100 caracteres.

**[!UICONTROL Landing Page]:** o URL no qual o visualizador será direcionado ao clicar no anúncio.

**[!UICONTROL Final Landing Page]:** o  [!UICONTROL Landing Page] URL com o rastreamento  [Advertising Cloud DSP necessário ](/help/dsp/campaign-management/macros.md) classificado, se aplicável.

**[!UICONTROL Sponsored By (Advertiser Name)]:** O anunciante do anúncio.

**[!UICONTROL Call to Action]:** (opcional) a etapa que você deseja que os visualizadores executem quando visualizarem esse anúncio.

**[!UICONTROL Advertiser Logo]:** (opcional) um logotipo com a proporção de 1:1 para incluir no anúncio, para obter mais reconhecimento de marca. Clique em **[!UICONTROL Browse]**, localize o arquivo no dispositivo ou na rede e clique em **[!UICONTROL Upload]**.

### [!UICONTROL Pixel]

Todos os pixels de rastreamento de evento existentes para a disposição são anexados automaticamente. Você pode desanexar os pixels existentes e criar novos pixels, conforme necessário, com base nas suas necessidades de rastreamento.

As configurações a seguir se aplicam a cada pixel criado ou editado.

**[!UICONTROL Integration Event]:** o evento que aciona o pixel para ser disparado. Para esse tipo de anúncio, use pixels que são acionados no *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** se o pixel é um  *[!UICONTROL IMG URL]* (arquivo de imagem de pixel 1x1),  *[!UICONTROL HTML]*, ou  *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** o URL da imagem de pixel, no formato apropriado para o especificado  [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** O nome do pixel. Use um nome que o ajudará a identificar o pixel com facilidade.

**[!UICONTROL Pixel Provider]:** O provedor de pixel:  *[!UICONTROL None]*,  *[!UICONTROL Nielsen]*, ou  *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de anúncios](ad-about.md)
>* [Criar uma publicidade](ad-create.md)
>* [Listar as disposições associadas a um anúncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Tipos de anúncio disponíveis](ad-types.md)
>* [Especificações do anúncio](/help/dsp/assets/ad-specs.pdf)
>* [Macros Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

