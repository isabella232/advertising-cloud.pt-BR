---
title: Configurações de anúncio de áudio
description: Consulte descrições das configurações de anúncios disponíveis para anúncios de áudio.
feature: DSP Ads
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Configurações de anúncio de áudio

## [!UICONTROL Insert Ad Tag]

*Somente novos anúncios*

**[!UICONTROL URL]**: O URL da tag VAST.

**[!UICONTROL Title]**: Um nome para o arquivo, que será usado na variável [!UICONTROL Ads] exibir e relatórios.

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

**[!UICONTROL VAST Tag]:** (Anúncios usando somente tags VAST) Um URL para uma fonte de anúncios de terceiros. Certifique-se de que a tag VAST inclua apenas arquivos de mídia de áudio.

**[!UICONTROL Final VAST Tag]:** (Anúncios usando somente tags VAST) O URL da fonte de anúncios de terceiros com o [Macros de rastreamento de DSP de publicidade](/help/dsp/campaign-management/macros.md) , se aplicável.

**[!UICONTROL Select Rate]:** (Usuários com permissão somente) Uma taxa pré-negociada cobrada por Adobe, ou uma das taxas negociadas e faturadas pelo fornecedor. Para adicionar uma taxa, entre em contato com seu [!DNL Adobe] equipe da conta.

### Pixel

Todos os pixels de rastreamento de evento existentes para a disposição são anexados automaticamente. Você pode desanexar pixels existentes e criar novos pixels, conforme necessário, com base nas suas necessidades de rastreamento para o anúncio individual.

As configurações a seguir se aplicam a cada pixel criado ou editado.

**[!UICONTROL Integration Event]:** O evento que aciona o pixel para ser disparado. Para este tipo de anúncio, use pixels que são acionados no *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se o pixel é um *[!UICONTROL IMG UR]L* (arquivo de imagem de pixel 1x1), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** O URL da imagem de pixel, no formato apropriado para o Tipo de pixel especificado.

**[!UICONTROL Pixel Name]:** O nome do pixel. Use um nome que o ajude a identificar o pixel com facilidade.

**[!UICONTROL Pixel Provider]:** O provedor de pixel: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* ou *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de anúncios](ad-about.md)
>* [Criar um único anúncio](ad-create.md)
>* [Listar as disposições associadas a um anúncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificações do anúncio](ad-specs.md)
>* [Macros DSP](/help/dsp/campaign-management/macros.md)

