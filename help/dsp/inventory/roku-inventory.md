---
title: Usando [!DNL Roku] Inventário
description: 'Saiba mais sobre DSP parceria com disposições específicas do  [!DNL Roku], including inventory options, approved third-party tracking vendors, and best practices for [!DNL Roku]. '
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Usando [!DNL Roku] Inventário

O Advertising Cloud DSP fornece recursos exclusivos para publicidade em [!DNL Roku].

## A Parceria Advertising Cloud DSP e [!DNL Roku]

O Roku e o Advertising Cloud DSP têm uma parceria exclusiva que corresponde seus públicos-alvo [!DNL DSP] a [!DNL Roku] IDs para direcionamento de público-alvo determinístico 1:1 no inventário [!DNL Roku].

Fora do próprio DSP do Roku (OneView), a Advertising Cloud DSP tem acesso exclusivo a esses recursos de direcionamento. O Advertising Cloud DSP também é o único DSP com permissão para medir [!DNL Roku] suprimento ao lado de todo o inventário de TV conectada (CTV). Como [!DNL Roku] não compartilha todos os sinais padrão de RTB e pixel de impressão, nenhum outro DSP pode direcionar ou medir através da fonte de CTV vendida pelo Roku.

## [!DNL Roku] Opções de inventário

Você pode a) configurar IDs de negócios privados diretamente com [!DNL Roku] e inserir os dados da ID de negócios em DSP ou b) visitar a Galeria [!DNL On Demand] para assinar perfis [!DNL Roku]:

>[!NOTE]
>
>[!DNL Roku] O inventário não está disponível em mercados abertos e trocas.

* Para suas ofertas privadas, você [configurará as informações sobre as IDs de negócios em DSP](/help/dsp/inventory/deal-id-create.md) e, em seguida, definirá &quot;[!UICONTROL Roku Network – Audience]&quot; e &quot;[!UICONTROL The Roku Channel – Audience]&quot; em [!DNL Roku] disposições.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* Você pode [assinar a seguinte [!DNL Roku] inventory within the [!DNL On Demand] Galeria](/help/dsp/inventory/on-demand-inventory-subscribe.md) e, em seguida, direcionar qualquer uma das ofertas aprovadas em [!DNL Roku] disposições:

   * &quot;[!UICONTROL Roku Network – Audience]&quot; para inventário no ecossistema [!DNL Roku] com parceiros de conteúdo premium, como [!DNL The CW], [!DNL ABC] e [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel – Audience]&quot; para conteúdo de aplicativo [!DNL Roku] próprio e operado (O&amp;O).

### Vantagens de personalizar mercados privados com [!DNL Roku]

As ofertas privadas permitem que você personalize os parâmetros de negócios de acordo com suas necessidades.

* **Preços negociados:** trabalhe com a equipe  [!DNL Roku] de vendas para negociar e estruturar uma negociação que atenda às suas necessidades de campanha.

* **Prioridade de escala:** os mercados privados (PMPs) recebem prioridade mais alta do que as transações sempre ativas (como  [!DNL On Demand] ofertas).

* **Gerenciamento de frequência:** o limite de frequência  [!DNL Roku] padrão é um (1) e por 30 minutos por usuário, mas você pode personalizar o limite por hora, dia, semana, mês ou todo o período de voo.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]Direcionamento de dados:** [!DNL Roku] os públicos-alvo são criados a partir de sinais de  [!DNL Roku] dispositivo e de TV, dados rastreados por  [!DNL The Roku Channel] (como afinidade de gênero de TV, comportamento de transmissão de TV e status de assinatura de cabo) e dados adicionais do sistema de gerenciamento de relacionamento com o  [!DNL Roku] cliente (CRM).

* **[!DNL Roku]Direcionamento de conteúdo:** as ofertas privadas podem direcionar aplicativos por gênero, aplicação de  de lista de bloqueios de aplicativos, eventos sazonais e temporários e são exibidas  [!DNL The Roku Channel] somente.

## [!DNL Roku] Posicionamentos

Em DSP campanhas, você [criará [!DNL Roku] disposições específicas](/help/dsp/campaign-management/placements/placement-create.md) usando o tipo de disposição &quot;[!UICONTROL Connected TV (Roku)].&quot; Você incluirá [!DNL Roku] disposições em [!DNL Roku] pacotes específicos com metas definidas.

Cada disposição [!DNL Roku] deve ter pelo menos um negócio [!DNL Roku] ou fonte. Para aproveitar a correspondência de público-alvo exclusivo do DSP com [!DNL Roku], inclua um ou mais segmentos de público-alvo que podem ser comparados com o conjunto de dados determinístico [!DNL Roku] (opt-in).

### [!DNL Roku]-Fornecedores de rastreamento de terceiros aprovados

[!DNL Roku] as disposições podem incluir pixels de evento de terceiros e pixels de conversão dos seguintes fornecedores:   [!DNL Acxiom],  [!DNL comScore],  [!DNL Data Plus Math],  [!DNL Experian],  [!DNL Factual],  [!DNL Kantar],  [!DNL Marketing Evolution],  [!DNL Neustar],  [!DNL Nielsen],  [!DNL Nielsen Catalina Solutions],  [!DNL NinthDecimal],  [!DNL Oracle],  [!DNL Placed],  [!DNL Polk] e  [!DNL Research Now].

### Práticas recomendadas por estratégia de posicionamento

A seguir estão as práticas recomendadas para disposições específicas de [!DNL Roku].

Para maximizar o alcance incremental:

* Suprima públicos-alvo expostos em [!DNL Roku O&O] excluindo públicos-alvo que você já acessou usando [!DNL The Roku Channel].

* Suprima públicos-alvo expostos em [!DNL All Roku] excluindo públicos-alvo que você já atingiu na plataforma [!DNL Roku].

Para a configuração mais rápida:

* Direcione ofertas sempre ativas e existentes para [!DNL The Roku Channel] em [[!DNL On Demand] Inventário](/help/dsp/inventory/on-demand-inventory-subscribe.md) para acessar rapidamente [!DNL Roku] o inventário de propriedade e operado.
* Direcione ofertas sempre ativas e existentes para [!DNL Roku Network] em [[!DNL On Demand] Inventário](/help/dsp/inventory/on-demand-inventory-subscribe.md) para alcançar a escala rapidamente na plataforma [!DNL Roku].

Para obter a escala máxima:

* Personalize um [!DNL Roku] mercado privado para acesso priorizado a [!DNL Roku] suprimento a um preço negociado.

>[!MORELIKETHIS]
>
>* [Criar manualmente detalhes da ID do contrato](/help/dsp/inventory/deal-id-create.md)
> * [Assinar e solicitar acesso  [!DNL On Demand] aos contratos de inventário Premium](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Criar uma disposição](/help/dsp/campaign-management/placements/placement-create.md)

