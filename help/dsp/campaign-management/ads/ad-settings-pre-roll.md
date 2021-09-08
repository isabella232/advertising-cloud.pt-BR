---
title: Configurações de anúncio precedente
description: Consulte descrições das configurações de anúncios disponíveis para anúncios precedentes.
feature: Ads
exl-id: 638d5a3d-3dff-40b6-a3ba-7ab3f08282b9
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Configurações de anúncio precedente

## [!UICONTROL Upload or Select Creative]

*Somente novos anúncios*

**[!UICONTROL Transcode to]:**  (alguns usuários, dependendo das permissões; opcional) os formatos que você deseja incluir na tag VAST quando o editor tiver requisitos específicos de arquivo criativo. Os formatos aceitos pela maioria dos editores são selecionados por padrão.

**[!UICONTROL Custom Transcode]:** (Somente usuários beta; não disponível quando Vídeo vertical está selecionado) Indica que o vídeo usa transcódigo personalizado. Se você selecionar essa opção, especifique o formato do arquivo, a taxa de bits do vídeo, o zoom e as dimensões para até três versões de transcodificação personalizadas.

**[!UICONTROL XTrader]:** (alguns usuários, dependendo das permissões) indica que o vídeo usa um ou mais  [!DNL X_TRADER] feeds.

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

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:**  (somente leitura) o tipo de anúncio que você está criando, que corresponde ao tipo de disposição ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de localizar quando anexar o anúncio a uma disposição, na visualização [!UICONTROL Ads] e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: 30sec Preroll&quot;).

**[!UICONTROL Width]|  [!UICONTROL Ad Unit Width]:**  (somente anúncios precedentes padrão e destacáveis) A largura de toda a unidade de anúncio. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Height]|  [!UICONTROL Ad Unit Height]:**  (somente anúncios precedentes padrão e destacáveis) A altura de toda a unidade de anúncio. Essa opção pode ser bloqueada dependendo do tipo de unidade de anúncio selecionada.

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

**[!UICONTROL Wmode]:** (Somente para ativação interativa) O modo de janela:  *[!UICONTROL window]*,  *[!UICONTROL transparent]*, ou  *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:** (Somente antes da exibição interativa) O formato do reprodutor do anúncio para inventário potencial:  *[!UICONTROL VPAID]* ou  *[!UICONTROL VPAID & VAST]*. A capacidade de visualização é sempre medida para VPAID, mas VPAID e VAST incluem inventário que não permite a medição da capacidade de visualização. Lembre-se disso se as métricas de visualização forem importantes para sua campanha.

**[!UICONTROL Clock Number]**: (Apenas antes da exibição interativa; Utilizadas apenas no Reino Unido; disponível somente para usuários com permissão) Um identificador exclusivo usado para garantir que o anúncio correto seja transmitido. Se essa configuração não for aplicável, deixe-a em branco.

### [!UICONTROL Companion]

*Somente anúncios servidos DSP*

Opcionalmente, é possível anexar até três banners complementares com um anúncio. A melhor prática é anexar banners de companheiro sempre que possível.

>[!NOTE]
>
> Nem todos os editores permitem banners de companheiro. Os editores que permitem banners de companheiro não garantem impressões de banner de companheiro.
> Os banners complementares de tags de anúncios de terceiros nem sempre estão disponíveis para visualização.

**\[Caixa de seleção\]:** inclui o banner complementar especificado com o anúncio. Quando a caixa de seleção estiver desativada, o banner complementar não será incluído.

**\[Tamanho do banner\]:** o tamanho do banner complementar:  *[!UICONTROL 300x600 (Skyscraper)]*;  *[!UICONTROL 300x250 (Medium Rectangle)]*, que é o tamanho de anúncio mais comum e recomendado para todos os anúncios;  *[!UICONTROL 300x60 (Small Banner)]*; ou  *[!UICONTROL 728x90 (Leaderboard)]*, que é um tamanho de anúncio menos comum.

**\[Fonte\]:** se você está fazendo upload de seu próprio ativo de banner complementar ou usando uma tag de terceiros.

**Ativo:**  (somente ativos brutos) o ativo de banner complementar. Clique em **[!UICONTROL Browse]**, localize o arquivo no dispositivo ou na rede e clique em **[!UICONTROL Upload]**.

**Tag de anúncio]:[!UICONTROL ** (Anúncios usando somente tags VAST) Uma URL para uma fonte de banner complementar de terceiros.

**[!UICONTROL Final Ad Tag]:** (anúncios usando somente tags VAST) Uma URL para uma fonte de banner complementar de terceiros com o rastreamento necessário do  [Advertising Cloud DSP ](/help/dsp/campaign-management/macros.md) classificado, se aplicável.

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
>* [Práticas recomendadas para projetar sobreposições](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)
>* [Macros Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

