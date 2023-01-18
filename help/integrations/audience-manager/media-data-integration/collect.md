---
title: Coletar dados de cliques e impressões de campanhas de publicidade DSP
description: Saiba como capturar impressões baseadas em cookies e eventos de cliques de anúncios de Advertising DSP usando pixels de Audience Manager
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---

# Coletar dados de exposição de mídia de campanhas de publicidade DSP

*Somente anunciantes com DSP publicitária*

*Anunciantes apenas com uma integração Adobe Advertising-Adobe Audience Manager*

Este documento explica como marcar anúncios publicitários DSP para capturar impressões baseadas em cookies e eventos de cliques usando pixels de Audience Manager e tarefas adicionais necessárias para usar os dados.

Os pixels do evento não capturam eventos que ocorrem em ambientes sem cookies, como aplicativos móveis e TV conectada (CTV).

## Etapa 1: Configurar uma fonte de dados no Audience Manager {#set-up-data-source}

No Audience Manager, crie um [fonte de dados](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) para a impressão de DSP e os dados de clique. Incluir a ID da fonte de dados [em cada tag de evento](#implement-dsp-pixels) para que todos os eventos rastreados sejam atribuídos à fonte de dados.

>[!NOTE]
> É possível coletar todas as impressões e dados de cliques para campanhas de publicidade em várias DSP em uma única fonte de dados.

## Etapa 2: Implementar impressão e clicar em pixels do evento nas páginas da Web {#implement-dsp-pixels}

Os anunciantes podem criar e implementar tags de evento para suas próprias marcas. Se necessário, entre em contato com o consultor da Adobe Audience Manager ou com o [!DNL Adobe] gerente de conta para obter suporte.

>[!NOTE]
>
>Se sua organização usar [!DNL Analytics] , talvez você não precise do rastreamento por Audience Manager click. O Adobe Analytics captura sinais de clique e pode enviá-los para o Audience Manager [encaminhamento pelo lado do servidor](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### Sintaxe de pixels

Os pixels do evento devem incluir os seguintes parâmetros.

**Pixels de rastreamento de impressão:**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

com [parâmetros adicionais opcionais](#parameters) com prefixo `&`

**Pixels de rastreamento de cliques:**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

com [parâmetros adicionais opcionais](#parameters) com prefixo `&`

Em que:

* `[Audience Manager customer domain]` é o nome de domínio que enviará impressões ou eventos de clique para [!DNL Adobe].

* `[source id]` é a ID da variável [fonte de dados](#set-up-data-source) em que você rastreará DSP impressões e dados de clique.

* `[redirect URL]` é o URL de redirecionamento codificado duas vezes. Se estiver usando uma ferramenta de codificação online, como www.urlencoder.org, execute a string pelo codificador e codifique novamente o resultado.

* `${TM_CAMPAIGN_ID_NUM}` é a ID numérica da campanha no DSP. Se quiser codificar uma ID de campanha individual em vez de usar a macro de DSP, localize a ID nas configurações da campanha.

* Cada [parâmetro](#key-value-pairs) tem o prefixo `&` e está no formato `d_parameter=parameter_id`, onde `parameter` é substituído pelo par de valor chave para o novo campo. Exemplo: `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Parâmetros como pares de valor-chave {#parameters}

**Formato:**  `d_parameter=parameter_id`

    em que:
    
    * o parâmetro tem o prefixo `&amp;`
    
    * `parameter` é substituído pelo par de valor chave para o novo campo
    
    Exemplo: `&amp;d_placement=${TM_PLACEMENT_ID_NUM}`

Ambos os tipos de pixel podem conter parâmetros adicionais como *pares de valor-chave* para coletar características ou fornecer metadados da campanha (como um nome de disposição ou um nome de campanha) para outros relatórios. Um par de valores chave consiste em dois elementos relacionados: a *key*, que é uma constante que define o conjunto de dados, e um *value*, que é uma variável pertencente ao conjunto.

No par de valores chave, a variável de valor pode ser uma ID codificada ou uma *macro*, que é uma pequena unidade de código autocontido que é substituído dinamicamente pelos valores correspondentes quando a tag do anúncio é carregada para campanha e rastreamento do usuário. Para parâmetros relacionados à campanha, você pode usar [DSP macros](/help/dsp/campaign-management/macros.md) em vez de macros Audience Manager para enviar atributos de campanha junto com a impressão correspondente ou clicar em dados para o Audience Manager, usando um único pixel em todos os anúncios. As macros DSP inseridas nos pixels do evento devem ser valores apropriados para os pares de valores chave incluídos nos pixels. Por exemplo, para a variável `d_placement` chave, você usaria a macro DSP `${TM_PLACEMENT_ID_NUM}` como o valor para capturar IDs de posicionamento geradas pela macro Adobe Advertising.

Para obter uma lista de macros que o Audience Manager suporta para pixels de evento de impressão, consulte &quot;[Captura de dados de impressão da campanha via Pixel Calls](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs).&quot;

Para obter uma lista de macros que o Audience Manager suporta para pixels de evento de clique, consulte &quot;[Captura de dados de cliques da campanha via Pixel Calls](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html).&quot;

>[!TIP]
>
>* A prática recomendada é incluir a campanha, o posicionamento, a criação (publicidade) e as IDs do site, para que você possa usar os atributos da campanha para criar características do Audience Manager.
>* Para criar relatórios do Audience Optimization, são necessários parâmetros adicionais.
>* Nos pares de valores chave, substitua os valores por [DSP macros](/help/dsp/campaign-management/macros.md) assim, você pode usar um único pixel em todos os anúncios em todas as campanhas. Por exemplo, alterar `d_campaign=[%campaignID%]`para `d_campaign=${TM_CAMPAIGN_ID_NUM}` para capturar IDs de campanha geradas pela macro Adobe Advertising.
>* Você pode criar seus próprios parâmetros com valores codificados, se necessário. Exemplo: `d_DSP=AdCloud`


Exemplo de pixel do evento de impressão:

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Onde adicionar os pixels

#### Pixel de rastreamento de impressão

Anexe um pixel de rastreamento de eventos de impressão a todos os anúncios em seu [!DNL DSP] campanhas. Você pode fazer isso em qualquer um dos seguintes lugares:

* No nível de posicionamento, que aplica o pixel por padrão a todos os anúncios no posicionamento. Na seção Rastreamento das configurações de posicionamento, adicione o pixel na [[!UICONTROL Event pixels] campo](/help/dsp/campaign-management/placements/placement-settings.md).

* No nível do anúncio, que substitui qualquer pixel de evento no nível de posicionamento. Nas configurações do anúncio, [crie um pixel de evento na [!UICONTROL Pixel] guia](/help/dsp/campaign-management/ads/ad-edit.md).

* (Para anúncios em um servidor de anúncios de terceiros) No nível do anúncio no servidor de anúncios.

#### Pixel de rastreamento de cliques

No servidor de anúncios, insira o pixel do evento de clique (com o URL codificado anexado) onde você normalmente insere o URL de click-through do anúncio.

## Etapa 3: Tarefas pós-implementação

Depois que as tags de evento forem implementadas, os dados fluirão para os servidores de coleta de dados do Audience Manager. Conclua as seguintes tarefas antes de poder usar os dados nos relatórios.

### Crie um [!DNL Amazon S3] Bucket e fonte de dados

Depois que os dados estiverem nos servidores do Audience Manager, você deverá criar um [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) e, em seguida, uma fonte de dados, para a qual todos os dados de pixel serão enviados. Entre em contato com seu consultor de Audience Manager ou [Atendimento ao cliente](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) se precisar de suporte.

### Criar características e segmentos de Audience Manager

Os dados do evento fluirão para o Audience Manager como [sinais não utilizados](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). Criar manualmente [características com base em regras](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) dos dados assimilados e, em seguida, crie [segmentos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) usar essas características, antes de poder usar os dados nos relatórios.

Exemplo de característica que preenche dados no nível do usuário para usuários expostos a uma criação específica em DSP:

1. Identifique o evento como `d_event = imp`.
1. Identifique a ID criativa na campanha de DSP e, em seguida, a mapeie para a característica como `d_creative=[Creative ID]`.

![Tela de criação de característica](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [Macros DSP](/help/dsp/campaign-management/macros.md)
>* [Visão geral do envio DSP dados de exposição de mídia para o Adobe Audience Manager](overview.md)
>* [Casos de uso](use-cases.md)

