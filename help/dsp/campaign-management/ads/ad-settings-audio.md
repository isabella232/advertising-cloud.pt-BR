---
title: Configurações de anúncio de áudio
description: Consulte descrições das configurações de anúncios disponíveis para anúncios de áudio.
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---

# Configurações de anúncio de áudio

## [!UICONTROL Upload or Select Creative]

*Somente novos anúncios*

**[!UICONTROL Upload Audio]:** Para fazer upload de um ativo bruto no DSP. Ao selecionar essa opção, faça o seguinte:

1. Clique em **[!UICONTROL Choose File]** e localize o arquivo em seu dispositivo ou rede.
1. Insira um título para o arquivo, que será usado no [!UICONTROL Ads] exibir e relatórios.
1. Clique em **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** Para selecionar qualquer criação carregada anteriormente no formato correto na conta.

**[!UICONTROL Advanced: VAST Tag URL]:** Para inserir uma tag VAST de terceiros que contenha ativos criativos e pixels de rastreamento:

1. Clique em ![seta](/help/dsp/assets/compressed.png) ao lado de **[!UICONTROL Advanced: VAST Tag URL]**.
1. No **[!UICONTROL URL]** , insira o URL da tag VAST.
1. Insira um **[!UICONTROL Title]** para o arquivo , que será usado no [!UICONTROL Ads] exibir e relatórios.

>[!TIP]
>
> Para verificar a validade de uma tag VAST, cole-a em um navegador e pressione a **[!UICONTROL Enter]** chave. Se a tag for válida, você verá um arquivo XML que inclui `<VAST>` perto do topo.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado. O padrão é *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome que será fácil de localizar quando você anexar o anúncio a uma disposição, no [!UICONTROL Ads] e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: Áudio de 30 seg&quot;).

**[!UICONTROL Ad Duration]:** A duração do arquivo de áudio. Ele é automaticamente definido como [!UICONTROL 15] ou [!UICONTROL 30], dependendo da unidade de publicidade selecionada.

Esse campo pode ou não ser exibido, dependendo das permissões da conta.

**[!UICONTROL Click URL]:** (Anúncios que usam ativos brutos e somente com banners de exibição; opcional) o URL no qual o visualizador será direcionado ao clicar em um banner de exibição que acompanha seu anúncio.

**[!UICONTROL Final Click URL]:** (Anúncios que usam ativos brutos e somente com banners de exibição; somente leitura) A variável [!UICONTROL Click URL] com as [Macros de rastreamento do Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) , se aplicável.

**[!UICONTROL VAST Tag]:** (Anúncios usando somente tags VAST) Um URL para uma fonte de anúncios de terceiros. Certifique-se de que a tag VAST inclua apenas arquivos de mídia de áudio.

**[!UICONTROL Final VAST Tag]:** (Anúncios usando somente tags VAST) O URL da fonte de anúncios de terceiros com o [Macros de rastreamento do Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) , se aplicável.

**[!UICONTROL Select Rate]:** (Usuários com permissão somente) Uma taxa pré-negociada cobrada por Adobe, ou uma das taxas negociadas e faturadas pelo fornecedor. Para adicionar uma taxa, entre em contato com seu [!DNL Adobe] equipe da conta.

### [!UICONTROL Companion]

*Somente anúncios servidos DSP*

Opcionalmente, é possível anexar até três banners complementares com um anúncio. A melhor prática é anexar banners de companheiro sempre que possível.

>[!NOTE]
>
>* Nem todos os editores permitem banners de companheiro. Os editores que permitem banners de companheiro não garantem impressões de banner de companheiro.
>* Os banners complementares de tags de anúncios de terceiros nem sempre estão disponíveis para visualização.


**\[Caixa de seleção\]:** Inclui o banner complementar especificado com o anúncio. Quando a caixa de seleção estiver desativada, o banner complementar não será incluído.

**\[Tamanho do banner\]:** O tamanho do banner complementar: *[!UICONTROL 300x250]* (usado para [!DNL iHeartRadio], [!DNL Spotify], [!DNL SoundCloud]e [!DNL TuneIn]), *[!UICONTROL 640x640]* (usado para [!DNL Spotify), or *1024x1024]* (usado para [!DNL SoundCloud]).

**\[Origem\]:** A origem do ativo de banner complementar:

* *[!UICONTROL Upload My Own Asset]:* Para fazer upload de seu próprio ativo.
* *[!UICONTROL Use a Third Party Tag]:* Para inserir um iFrame ou uma tag de script de um parceiro de veiculação de anúncios certificado de terceiros.

Use uma tag de terceiros quando quiser rastrear impressões de banner de terceiros.

**[!UICONTROL Asset]:** (Somente ativos brutos) O ativo de banner complementar, no formato GIF, JPG ou PNG. Clique em **[!UICONTROL Browse]** e localize o arquivo em seu dispositivo ou rede e clique em **[!UICONTROL Upload]**.

**[!UICONTROL Click URL]:** (Somente ativos brutos) O URL no qual o visualizador será direcionado ao clicar no banner complementar do anúncio. Ele pode incluir um redirecionamento de clique usando um pixel de rastreamento de cliques de terceiros.

**[!UICONTROL Final Click URL]:** (Somente ativos brutos; somente leitura) O URL de clique com o necessário [Macros de rastreamento do Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) , se aplicável.

**[!UICONTROL Ad Tag]:** (Anúncios usando somente tags de publicidade de terceiros) Uma tag de banner de iFrame ou script para uma fonte de banner complementar de terceiros. Ele deve ser de um parceiro de veiculação de anúncios de terceiros certificado.

**[!UICONTROL Final Ad Tag]:** (Anúncios usando somente tags de publicidade de terceiros) A tag de publicidade com as [Macros de rastreamento do Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) , se aplicável.

### Pixel

Todos os pixels de rastreamento de evento existentes para a disposição são anexados automaticamente. Você pode desanexar pixels existentes e criar novos pixels, conforme necessário, com base nas suas necessidades de rastreamento.

As configurações a seguir se aplicam a cada pixel criado ou editado.

**[!UICONTROL Integration Event]:** O evento que aciona o pixel para ser disparado. Para este tipo de anúncio, use pixels que são acionados no *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se o pixel é um *[!UICONTROL IMG UR]L* (arquivo de imagem de pixel 1x1), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** O URL da imagem de pixel, no formato apropriado para o Tipo de pixel especificado.

**[!UICONTROL Pixel Name]:** O nome do pixel. Use um nome que o ajudará a identificar o pixel com facilidade.

**[!UICONTROL Pixel Provider]:** O provedor de pixel: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* ou *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de anúncios](ad-about.md)
>* [Criar uma publicidade](ad-create.md)
>* [Listar as disposições associadas a um anúncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Tipos de anúncio disponíveis](ad-types.md)
>* [Especificações do anúncio](/help/dsp/assets/ad-specs.pdf)
>* [Macros Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

