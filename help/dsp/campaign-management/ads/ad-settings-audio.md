---
title: Configurações de anúncio de áudio
description: Consulte descrições das configurações de anúncios disponíveis para anúncios de áudio.
feature: Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Configurações de anúncio de áudio

## [!UICONTROL Upload or Select Creative]

*Somente novos anúncios*

**[!UICONTROL Upload Audio]:** Para fazer upload de um ativo bruto no DSP. Ao selecionar essa opção, faça o seguinte:

1. Clique em **[!UICONTROL Choose File]** e localize o arquivo no dispositivo ou na rede.
1. Insira um título para o arquivo, que será usado na exibição [!UICONTROL Ads] e nos relatórios.
1. Clique em **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** para selecionar qualquer criação carregada anteriormente no formato correto na conta.

**[!UICONTROL Advanced: VAST Tag URL]:** para inserir uma tag VAST de terceiros que contenha ativos criativos e pixels de rastreamento:

1. Clique em ![seta](/help/dsp/assets/compressed.png) ao lado de **[!UICONTROL Advanced: VAST Tag URL]**.
1. No campo **[!UICONTROL URL]**, insira o URL da tag VAST.
1. Insira um **[!UICONTROL Title]** para o arquivo, que será usado na exibição [!UICONTROL Ads] e nos relatórios.

>[!TIP]
>
> Para verificar a validade de uma tag VAST, cole-a em um navegador e pressione a tecla **[!UICONTROL Enter]**. Se a tag for válida, você verá um arquivo XML que inclui `<VAST>` próximo à parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:**  (somente leitura) o tipo de anúncio que você está criando, que corresponde ao tipo de disposição ao qual o anúncio pode ser anexado. O padrão é *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de localizar quando anexar o anúncio a uma disposição, na visualização [!UICONTROL Ads] e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: Áudio de 30 seg&quot;).

**[!UICONTROL Ad Duration]:** a duração do arquivo de áudio. Ele é automaticamente definido como [!UICONTROL 15] ou [!UICONTROL 30], dependendo da unidade de anúncio selecionada.

Esse campo pode ou não ser exibido, dependendo das permissões da conta.

**[!UICONTROL Click URL]:** (anúncios que usam ativos brutos e somente com banners de exibição; opcional) o URL no qual o visualizador será direcionado ao clicar em um banner de exibição que acompanha seu anúncio.

**[!UICONTROL Final Click URL]:** (anúncios que usam ativos brutos e somente com banners de exibição; somente leitura) O  [!UICONTROL Click URL] com o rastreamento  [Advertising Cloud DSP necessário ](/help/dsp/campaign-management/macros.md) classificado, se aplicável.

**[!UICONTROL VAST Tag]:** (anúncios usando somente tags VAST) Um URL para uma fonte de anúncio de terceiros. Certifique-se de que a tag VAST inclua apenas arquivos de mídia de áudio.

**[!UICONTROL Final VAST Tag]:** (anúncios usando somente tags VAST) O URL da fonte de anúncio de terceiros com o rastreamento necessário do  [Advertising Cloud DSP ](/help/dsp/campaign-management/macros.md) classificado, se aplicável.

**[!UICONTROL Select Rate]:**  (usuários somente com permissão) Uma taxa pré-negociada cobrada pelo Adobe ou uma das taxas que você negociou e será cobrada pelo fornecedor. Para adicionar uma taxa, entre em contato com o gerente de conta do Adobe.

### [!UICONTROL Companion]

*Somente anúncios servidos DSP*

Opcionalmente, é possível anexar até três banners complementares com um anúncio. A melhor prática é anexar banners de companheiro sempre que possível.

>[!NOTE]
>
>* Nem todos os editores permitem banners de companheiro. Os editores que permitem banners de companheiro não garantem impressões de banner de companheiro.
>* Os banners complementares de tags de anúncios de terceiros nem sempre estão disponíveis para visualização.


**\[Caixa de seleção\]:** inclui o banner complementar especificado com o anúncio. Quando a caixa de seleção estiver desativada, o banner complementar não será incluído.

**\[Tamanho do banner\]:** o tamanho do banner complementar:  *[!UICONTROL 300x250]* (usado para  [!DNL iHeartRadio],  [!DNL Spotify],  [!DNL SoundCloud], e  [!DNL TuneIn]),  *[!UICONTROL 640x640]* (usado para  [!DNL Spotify), or *1024x1024]* (usado para  [!DNL SoundCloud]).

**\[Origem\]:** A origem do ativo de banner complementar:

* *[!UICONTROL Upload My Own Asset]:* para fazer upload de seu próprio ativo.
* *[!UICONTROL Use a Third Party Tag]:* para inserir um iFrame ou tag de script de um parceiro de veiculação de anúncios de terceiros certificado.

Use uma tag de terceiros quando quiser rastrear impressões de banner de terceiros.

**[!UICONTROL Asset]:**  (somente ativos brutos) o ativo de banner complementar, no formato GIF, JPG ou PNG. Clique em **[!UICONTROL Browse]**, localize o arquivo no dispositivo ou na rede e clique em **[!UICONTROL Upload]**.

**[!UICONTROL Click URL]:**  (somente ativos brutos) o URL no qual o visualizador será direcionado ao clicar no banner complementar do anúncio. Ele pode incluir um redirecionamento de clique usando um pixel de rastreamento de cliques de terceiros.

**[!UICONTROL Final Click URL]:**  (somente ativos brutos; somente leitura) O URL de clique com o rastreamento  [Advertising Cloud DSP necessário ](/help/dsp/campaign-management/macros.md) classificado, se aplicável.

**[!UICONTROL Ad Tag]:** (anúncios usando somente tags de anúncios de terceiros) Uma tag de banner de iFrame ou script para uma fonte de banner complementar de terceiros. Ele deve ser de um parceiro de veiculação de anúncios de terceiros certificado.

**[!UICONTROL Final Ad Tag]:** (anúncios usando somente tags de anúncios de terceiros) A tag do anúncio com o rastreamento necessário do  [Advertising Cloud DSP foi ](/help/dsp/campaign-management/macros.md) analisada, se aplicável.

### Pixel

Todos os pixels de rastreamento de evento existentes para a disposição são anexados automaticamente. Você pode desanexar os pixels existentes e criar novos pixels, conforme necessário, com base nas suas necessidades de rastreamento.

As configurações a seguir se aplicam a cada pixel criado ou editado.

**[!UICONTROL Integration Event]:** o evento que aciona o pixel para ser disparado. Para esse tipo de anúncio, use pixels que são acionados no *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** se o pixel é um arquivo de imagem de pixel  *[!UICONTROL IMG UR]L*  (1x1),  *[!UICONTROL HTML]*, ou  *[!UICONTROL JavaScript URL]*.

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

