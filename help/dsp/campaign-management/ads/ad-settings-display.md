---
title: Exibir configurações do anúncio
description: Consulte descrições das configurações de anúncios disponíveis para anúncios de exibição.
feature: DSP Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Exibir configurações do anúncio

As configurações a seguir são para anúncios de exibição padrão. Você também pode veicular anúncios de vídeo de clique para reprodução para anúncios de exibição, mas não recomendamos fazê-lo porque nem muitos editores os suportam.

## [!UICONTROL Ad Options]

### Básico

**[!UICONTROL Ad Type]:**  (somente leitura) o tipo de anúncio que você está criando, que corresponde ao tipo de disposição ao qual o anúncio pode ser anexado. O padrão é *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de localizar quando anexar o anúncio a uma disposição, na visualização [!UICONTROL Ads] e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: 300x250 Gamer&quot;).

**\[Origem de anúncio\]**: Se a Advertising Cloud DSP está veiculando o anúncio (*[!UICONTROL Adobe served]*) ou se você está usando um servidor de anúncios de terceiros (*[!UICONTROL 3rd party]*).

**[!UICONTROL This is an expandable Banner]:**  (somente anúncios de terceiros) Indica que o anúncio é um anúncio de banner expansível. As configurações de expansão relacionadas determinam qual inventário comprar, portanto, certifique-se de que elas reflitam o comportamento do anúncio.

**[!UICONTROL Expansion Method]:** (Somente anúncios de banner expansíveis de terceiros) Se o banner se expande  *[!UICONTROL Click]* ou  *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:**  (somente anúncios de banner expansíveis de terceiros) A direção em que o anúncio se expande:  *[!UICONTROL Up]*,  *[!UICONTROL Down]*,  *[!UICONTROL Left]* ou  *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:**  (somente anúncios de banner expansíveis de terceiros) O fornecedor certificado para o qual o anúncio está disponível:  *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]),  *[!UICONTROL Flashtalking]*,  *[!UICONTROL Sizmek]* ou  *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:**  (somente anúncios de terceiros) o URL do ativo criativo de terceiros. Qualquer parâmetro [timestamp] e [[timestamp]] será substituído por valores reais.

**[!UICONTROL Final Display Code]:**  (somente anúncios de terceiros) o URL do ativo criativo de terceiros, com o rastreamento necessário do  [Advertising Cloud DSP ](/help/dsp/campaign-management/macros.md) sincronizado, se aplicável.

**[!UICONTROL Creative type]:**  (somente anúncios veiculados no Adobe) se o ativo é um ativo  *[!UICONTROL Image]* ou um  *[!UICONTROL HTML5]* ativo.

**[!UICONTROL Asset]|  [!UICONTROL HTML5 Asset]:**  (somente anúncios veiculados por Adobe) Um arquivo de imagem ou ativo HTML5 zipado para upload, dependendo do tipo de criação. Clique em **[!UICONTROL Browse]**, localize o arquivo no dispositivo ou na rede e clique em **[!UICONTROL Upload]** ou **[!UICONTROL Upload Image]**.

**[!UICONTROL Ad Size]:** a largura e a altura do anúncio. Deve ser um [tamanho de anúncio de exibição padrão suportado](/help/dsp/assets/ad-specs.pdf). Você pode inserir manualmente o tamanho do anúncio antes de fazer upload do anúncio ou inserir um [!UICONTROL Display Code]. Se você não inserir o tamanho do anúncio, as dimensões da publicidade carregada ou da tag do anúncio serão inseridas automaticamente como somente leitura. Observe que a publicidade não será salva se as dimensões não estiverem em Telas padrão como tamanhos - por exemplo, 301x250 em vez de 300x250.

>[!IMPORTANT]
>
> O tamanho do anúncio declarado nos campos de largura e altura será correspondido por solicitações de ofertas recebidas. Você pode enfrentar problemas de entrega se as dimensões do anúncio não corresponderem ao tamanho do anúncio declarado.

**[!UICONTROL Click URL]:**  (somente anúncios veiculados por Adobe) o URL no qual o visualizador será direcionado ao clicar no anúncio.

**[!UICONTROL Final Click URL]:**  (somente anúncios de Adobe servido; somente leitura) O  [!UICONTROL Click URL] com o rastreamento  [Advertising Cloud DSP necessário ](/help/dsp/campaign-management/macros.md) classificado, se aplicável.

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
>* [Listar as disposições associadas a um anúncio](ad-list-placements.md)
>* [Tipos de anúncio disponíveis](ad-types.md)
>* [Especificações do anúncio](/help/dsp/assets/ad-specs.pdf)
>* [Macros Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

