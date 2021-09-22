---
title: Configurações do anúncio de TV conectado
description: Consulte descrições das configurações de anúncios disponíveis para anúncios de TV conectados.
feature: DSP Ads
exl-id: 4daae9e4-27eb-4496-9186-f33aebd8daae
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# Configurações do anúncio de TV conectado

## [!UICONTROL Upload or Select Creative]

*Somente novos anúncios*

**[!UICONTROL Upload Audio]:** Para fazer upload de um ativo bruto no DSP. Ao selecionar essa opção, faça o seguinte:

1. Clique em **[!UICONTROL Choose File]** e localize o arquivo no dispositivo ou na rede.
1. Insira um título para o arquivo, que será usado na exibição [!UICONTROL Ads] e nos relatórios.
1. Clique em **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** para selecionar qualquer criação carregada anteriormente no formato correto na conta.

**[!UICONTROL Advanced: VAST Tag URL]:** (Alguns tipos de anúncios) Para inserir uma tag VAST de terceiros que contenha ativos criativos e pixels de rastreamento:

1. Clique em ![seta](/help/dsp/assets/compressed.png) ao lado de **[!UICONTROL Advanced: VAST Tag URL]**.
1. No campo **[!UICONTROL URL]**, insira o URL da tag VAST.
1. Insira um **[!UICONTROL Title]** para o arquivo, que será usado na exibição Anúncios e nos relatórios.

>[!TIP]
>
> Para verificar a validade de uma tag VAST, cole-a em um navegador e pressione a tecla **[!UICONTROL Enter]**. Se a tag for válida, você verá um arquivo XML que inclui `<VAST>` próximo à parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:**  (somente leitura) o tipo de anúncio que você está criando, que corresponde ao tipo de disposição ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de localizar quando anexar o anúncio a uma disposição, na visualização [!UICONTROL Ads] e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: 30sec CTV&quot;).

**[!UICONTROL Width | Ad Unit Width]:** a largura da unidade de anúncio inteira. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Height | Ad Unit Height]:** a altura da unidade de anúncio inteira. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Player X]:** A coordenada X para a unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Y]:** A coordenada Y para a unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Width]:** a largura da unidade de anúncio inteira. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

É o mesmo que o campo **[!UICONTROL Width]** .

**[!UICONTROL Player Height]:** a altura da unidade de anúncio inteira. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

É o mesmo que o campo **[!UICONTROL Height]** .

**[!UICONTROL Show Controls]:** onde incluir controles de vídeo para o anúncio:  *[!UICONTROL Under]*,  *[!UICONTROL Over]*,  *[!UICONTROL Bottom]* ou  *[!UICONTROL None]* (o padrão).

**[!UICONTROL Preserve Aspect Ratio]:** manter as proporções de largura e altura do vídeo (*[!UICONTROL Yes]*) ou esticar o vídeo para preencher o espaço disponível (*[!UICONTROL No]*).

**[!UICONTROL Click URL]:**  (somente anúncios veiculados por Adobe) o URL no qual o visualizador será direcionado ao clicar no anúncio.

**[!UICONTROL Final Click URL]:**  (somente anúncios de Adobe servido; somente leitura) O  [!UICONTROL Click URL] com o rastreamento  [Advertising Cloud DSP necessário ](/help/dsp/campaign-management/macros.md) classificado, se aplicável.

**[!UICONTROL VAST Tag]:** (anúncios usando somente tags VAST; somente leitura) A tag VAST de terceiros inserida como fonte de anúncio.

**[!UICONTROL Final VAST Tag]:** (anúncios usando somente tags VAST; somente leitura) A tag VAST de terceiros inserida como fonte de anúncio com o rastreamento  [Advertising Cloud DSP necessário ](/help/dsp/campaign-management/macros.md) classificado, se aplicável.

**[!UICONTROL Clock Number]**: (Utilizado apenas no Reino Unido; disponível somente para usuários com permissão) Um identificador exclusivo usado para garantir que o anúncio correto seja transmitido. Se essa configuração não for aplicável, deixe-a em branco.

### [!UICONTROL Pixel]

Todos os pixels de rastreamento de evento existentes para a disposição são anexados automaticamente. Você pode desanexar os pixels existentes e criar novos pixels, conforme necessário, com base nas suas necessidades de rastreamento.

As configurações a seguir se aplicam a cada pixel criado ou editado.

**[!UICONTROL Integration Event]:** o evento que aciona o pixel para ser disparado. Para esse tipo de anúncio, use pixels que são acionados no *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** se o pixel é um  *[!UICONTROL IMG URL]* (arquivo de imagem de pixel 1x1),  *[!UICONTROL HTML]*, ou  *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** o URL da imagem de pixel, no formato apropriado para o Tipo de pixel especificado.

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

