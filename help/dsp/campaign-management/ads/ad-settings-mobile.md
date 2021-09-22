---
title: Configurações de anúncio móvel
description: Consulte descrições das configurações de anúncios disponíveis para anúncios móveis.
feature: DSP Ads
exl-id: f67c4ba0-1011-4ad6-bd36-98c312b81b67
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '1335'
ht-degree: 0%

---

# Configurações de anúncio móvel

## [!UICONTROL Upload or Select Creative]

*Somente novos formatos de anúncios de vídeo móveis*

**[!UICONTROL Vertical video]:** (Não disponível quando  [!UICONTROL Custom Transcode] está selecionado) Indica que o vídeo está vertical (modo retrato).

**[!UICONTROL Transcode to]:**  (alguns usuários, dependendo das permissões; opcional) os formatos que você deseja incluir na tag VAST quando o editor tiver requisitos específicos de arquivo criativo. Os formatos aceitos pela maioria dos editores são selecionados por padrão.

**[!UICONTROL Custom Transcode]:** (Somente usuários beta; não disponível quando Vídeo vertical está selecionado) Indica que o vídeo usa transcódigo personalizado. Se você selecionar essa opção, especifique o formato do arquivo, a taxa de bits do vídeo, o zoom e as dimensões para até três versões de transcodificação personalizadas.

**[!UICONTROL XTrader]:** (alguns usuários, dependendo das permissões) indica que o vídeo usa mais um  [!DNL X_TRADER] feed.

**[!UICONTROL Upload Video]:** Para fazer upload de um ativo bruto no DSP. Ao selecionar essa opção, faça o seguinte:

1. Clique em **[!UICONTROL Choose File]** e localize o arquivo no dispositivo ou na rede.
1. Insira um título para o arquivo, que será usado na exibição [!UICONTROL Ads] e nos relatórios.
1. Clique em **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Video]:** para selecionar qualquer criação carregada anteriormente no formato correto na conta.

**[!UICONTROL Advanced: VAST Tag URL]:** (Alguns tipos de anúncios) Para inserir uma tag VAST de terceiros que contenha ativos criativos e pixels de rastreamento:

1. Clique em ![seta](/help/dsp/assets/compressed.png) ao lado de **[!UICONTROL Advanced: VAST Tag URL]**.
1. No campo **[!UICONTROL URL]**, insira o URL da tag VAST.
1. Insira um **[!UICONTROL Title]** para o arquivo, que será usado na exibição [!UICONTROL Ads] e nos relatórios.

>[!TIP]
>
> Para verificar a validade de uma tag VAST, cole-a em um navegador e pressione a tecla **[!UICONTROL Enter]**. Se a tag for válida, você verá um arquivo XML que inclui `<VAST>` próximo à parte superior.

**[!UICONTROL Advanced: 3rd party Ad Tag]:** (Alguns tipos de anúncios) Para inserir uma tag de anúncio de terceiros que contenha ativos criativos e pixels de rastreamento:

1. Clique em ![seta](/help/dsp/assets/compressed.png) ao lado de **[!UICONTROL Advanced: #3rd party Ad Tag]**.
1. Insira um **[!UICONTROL Ad Title]** para o arquivo, que será usado na exibição [!UICONTROL Ads] e nos relatórios.
1. No campo **[!UICONTROL Ad Tag]** , insira a tag de anúncio.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: Anúncios de exibição em dispositivos móveis

**[!UICONTROL Ad Type]:**  (somente leitura) o tipo de anúncio que você está criando, que corresponde ao tipo de disposição ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de localizar quando anexar o anúncio a uma disposição, na exibição Anúncios e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: 300x250 Gamer&quot;).

**\[Origem de anúncio\]**: Se a Advertising Cloud DSP está veiculando o anúncio (*[!UICONTROL Adobe served]*) ou se você está usando um servidor de anúncios de terceiros (*[!UICONTROL 3rd party]*).

**[!UICONTROL Creative type]:**  (somente anúncios veiculados no Adobe) se o ativo é um ativo  *[!UICONTROL Image]* ou um  *[!UICONTROL HTML5]* ativo.

**[!UICONTROL Asset]|  [!UICONTROL HTML5 Asset]:**  (somente anúncios veiculados por Adobe) Um arquivo de imagem ou ativo HTML5 zipado para upload, dependendo do tipo de criação. Clique em **[!UICONTROL Browse]**, localize o arquivo no dispositivo ou na rede e clique em **[!UICONTROL Upload]**.

**[!UICONTROL Click URL]:**  (somente anúncios veiculados por Adobe) o URL no qual o visualizador será direcionado ao clicar no anúncio.

**[!UICONTROL Final Click URL]:**  (somente anúncios de Adobe servido; somente leitura) O URL de clique com o rastreamento  [Advertising Cloud DSP necessário ](/help/dsp/campaign-management/macros.md) classificado, se aplicável.

**[!UICONTROL Display Code]:**  (somente anúncios de terceiros) o URL do ativo criativo de terceiros. Qualquer parâmetro [timestamp] e [[timestamp]] será substituído por valores reais.

**[!UICONTROL Final Display Code]:**  (somente anúncios de terceiros) o URL do ativo criativo de terceiros, com o rastreamento necessário do  [Advertising Cloud DSP ](/help/dsp/campaign-management/macros.md) sincronizado, se aplicável.

### [!UICONTROL Basic]: Anúncios de vídeo

**[!UICONTROL Ad Type]:**  (somente leitura) o tipo de anúncio que você está criando, que corresponde ao tipo de disposição ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de localizar quando anexar o anúncio a uma disposição, na exibição Anúncios e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: 30sec (Pré-etiqueta de Telefone&quot;).

**[!UICONTROL Width]|  [!UICONTROL Ad Unit Width]:** A largura da unidade de anúncio inteira. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Height]|  [!UICONTROL Ad Unit Height]:** A altura de toda a unidade de anúncio. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Player X]:** A coordenada X para a unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Y]:** A coordenada Y para a unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Width]:** a largura da unidade de anúncio inteira. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

É o mesmo que o campo **[!UICONTROL Width]** .

**[!UICONTROL Player Height]:** a altura da unidade de anúncio inteira. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

É o mesmo que o campo **[!UICONTROL Height]** .

**[!UICONTROL Show Controls]:** onde incluir controles de vídeo para o anúncio:  *[!UICONTROL Under]*,  *[!UICONTROL Over]*,  *[!UICONTROL Bottom]* ou  *[!UICONTROL None]* (o padrão).

**[!UICONTROL Preserve Aspect Ratio]:** manter as proporções de largura e altura do vídeo (*[!UICONTROL Yes]*) ou esticar o vídeo para preencher o espaço disponível (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Alguns tipos de anúncios) A quantidade de segundos para atrasar a aparência do botão de fechamento.

**[!UICONTROL Click URL]:**  (somente anúncios veiculados por Adobe) o URL no qual o visualizador será direcionado ao clicar no anúncio.

**[!UICONTROL Final Click URL]:**  (somente anúncios de Adobe servido; somente leitura) O  [!UICONTROL Click URL] com o rastreamento  [Advertising Cloud DSP necessário ](/help/dsp/campaign-management/macros.md) classificado, se aplicável.

**[!UICONTROL VAST Tag]:** (anúncios usando somente tags VAST; somente leitura) A tag VAST de terceiros inserida como ativo criativo.

**[!UICONTROL Final VAST Tag]:** (anúncios usando somente tags VAST; somente leitura) A tag VAST de terceiros inserida como o ativo criativo com o rastreamento necessário do  [Advertising Cloud DSP ](/help/dsp/campaign-management/macros.md) se for aplicável.

**[!UICONTROL Wmode]:**  (Alguns tipos de anúncios) O modo da janela:  *[!UICONTROL window]*,  *[!UICONTROL transparent]*, ou  *[!UICONTROL opaque]*.

### [!UICONTROL Teaser]

*Formatos de toque para reprodução móvel para anúncios DSP*

**[!UICONTROL Asset]:** A imagem do teaser ou o ativo de vídeo:

* Para selecionar sua própria imagem, clique em **[!UICONTROL Choose File],** localize o arquivo em seu dispositivo ou rede e clique em **[!UICONTROL Upload Image]**.

   A prática recomendada é usar uma imagem com as mesmas dimensões da unidade de anúncio.

* Para selecionar uma imagem do anúncio, clique em **[!UICONTROL Choose Thumbnail]**.

Requisitos para teasers de imagem estática:

* Formato: GIF, JPEG, PNG
* Tamanho da imagem: 300x250
* Tamanho do arquivo: 50 KB ou menos
* Recomendado: ação de chamada, imagem reconhecível, logotipo da marca

Requisitos para teasers de vídeo:

* Tipo de arquivo: MOV, MP4
* Tamanho do arquivo: Menos de 2 MB
* Duração: 7-10seg
* Recomendado: imagens, faces, cortes rápidos reconhecíveis

### [!UICONTROL Overlays]

*Formatos interativos antes da exibição e móveis interativos e de toque para reprodução para anúncios DSP-veiculados*

As configurações a seguir se aplicam a cada sobreposição criada ou editada.

**[!UICONTROL Asset]:**  (somente ativos brutos) O ativo de imagem de sobreposição. O arquivo deve estar em formato GIF, JPG ou PNG de quadro único e o tamanho máximo da imagem é menor que 2 MB. Para fazer upload do ativo, clique em **[!UICONTROL Browse]**, localize o arquivo no dispositivo ou na rede e clique em **[!UICONTROL Upload]**.

>[!TIP]
>
>Consulte as [Práticas recomendadas para projetar sobreposições](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)

**[!UICONTROL Click URL]:**  o URL no qual o visualizador será direcionado ao clicar em uma sobreposição para sua publicidade.

**[!UICONTROL X]:** A coordenada X para a sobreposição. Selecione a posição inicial da sobreposição e insira o número de pixels da posição inicial (como 10px A partir do centro). A prática recomendada é usar *Do centro*, o que impede que a sobreposição se movimente com tamanhos de player diferentes em sites do editor.

**[!UICONTROL Y]:** A coordenada Y para a sobreposição. Selecione a posição inicial da sobreposição e insira o número de pixels da posição inicial (como 10px a partir do topo). A prática recomendada é especificar uma coordenada *[!UICONTROL From Bottom]* ou *[!UICONTROL From Top],*, dependendo da posição na qual você deseja que a sobreposição seja exibida no anúncio.

**[!UICONTROL Layer]:** a camada na qual a sobreposição será exibida. O vídeo e cada sobreposição estarão em camadas separadas.

* *[!UICONTROL 2 through 5]:* na frente do vídeo, mas atrás de outras sobreposições.

* *[!UICONTROL 1]:* na frente do vídeo.

* *[!UICONTROL 0]:* na mesma camada do vídeo. O vídeo será reduzido para preencher o espaço restante. Não recomendado para Pré-implantação interativa.

* *[!UICONTROL -1]:* Por trás do vídeo.

* *[!UICONTROL -2 through -5]:* atrás do vídeo, mas na frente de outras sobreposições.

* *[!UICONTROL Background]:* atrás do vídeo e de outras sobreposições. A sobreposição será dimensionada para a largura e a altura completas do vídeo, e a taxa de proporção não será preservada.

### [!UICONTROL Endcap]

Obsoleto

### [!UICONTROL Pixel]

Todos os pixels de rastreamento de evento existentes para a disposição são anexados automaticamente. Você pode desanexar os pixels existentes e criar novos pixels, conforme necessário, com base nas suas necessidades de rastreamento.

As configurações a seguir se aplicam a cada pixel criado ou editado.

**[!UICONTROL Integration Event]:** o evento que aciona o pixel para ser disparado. Para esse tipo de anúncio, use pixels que são acionados no *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** se o pixel é um  *[!UICONTROL IMG URL]* (arquivo de imagem de pixel 1x1),  *[!UICONTROL HTML]*, ou  *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** o URL da imagem de pixel, no formato apropriado para o especificado  [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** O nome do pixel. Use um nome que o ajudará a identificar o pixel com facilidade.

**[!UICONTROL Pixel Provider]:** O provedor de pixel:  *[!UICONTROL None]*,  *[!UICONTROL Nielsen]*, ou  *[!UICONTROL Comscore]*.

### [!UICONTROL Sharing]

Obsoleto

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de anúncios](ad-about.md)
>* [Criar uma publicidade](ad-create.md)
>* [Listar as disposições associadas a um anúncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Tipos de anúncio disponíveis](ad-types.md)
>* [Especificações do anúncio](/help/dsp/assets/ad-specs.pdf)
>* [Práticas recomendadas para projetar sobreposições](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)
>* [Macros Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

