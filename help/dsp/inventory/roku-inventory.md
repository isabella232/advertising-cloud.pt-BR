---
title: Usando [!DNL Roku] Inventário
description: 'Saiba mais sobre DSP parceria com a [!DNL Roku], incluindo opções de inventário, fornecedores de rastreamento de terceiros aprovados e práticas recomendadas para [!DNL Roku]disposições específicas. '
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: 39f491a39bdc9d8dd820eb4c69594dda71d8b3c2
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Usando [!DNL Roku] Inventário

O Advertising Cloud DSP fornece recursos exclusivos para a publicidade em [!DNL Roku].

## A Advertising Cloud DSP e [!DNL Roku] Parceria

O Roku e a Advertising Cloud DSP têm uma parceria exclusiva que corresponde a sua [!DNL DSP] públicos-alvo para [!DNL Roku] IDs para direcionamento de público-alvo determinístico 1:1 em [!DNL Roku] inventário.

Fora do próprio DSP do Roku (OneView), a Advertising Cloud DSP tem acesso exclusivo a esses recursos de direcionamento. O Advertising Cloud DSP também é o único DSP com permissão para medir [!DNL Roku] fornecimento ao lado de todas as outras existências de TV ligada (CTV). Porque [!DNL Roku] O não compartilha todos os sinais padrão de RTB e pixel de impressão, nenhum outro DSP pode direcionar ou medir através do fornecimento de CTV vendido pelo Roku.

## [!DNL Roku] Opções de inventário

Você pode a) configurar IDs de negócios privados diretamente com o [!DNL Roku] e insira os dados da ID do negócio em DSP ou b) visite a [!DNL On Demand] Galeria para assinar [!DNL Roku] perfis:

>[!NOTE]
>
>[!DNL Roku] O inventário não está disponível em mercados abertos e trocas.

* Para suas ofertas privadas, [configurar informações sobre as IDs de negócios no DSP](/help/dsp/inventory/deal-id-create.md) e, em seguida, direcionar &quot;[!UICONTROL Roku Network – Audience]&quot; e &quot;[!UICONTROL The Roku Channel – Audience]&quot; [!DNL Roku] disposições.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* Você pode [assine o seguinte [!DNL Roku] no inventário [!DNL On Demand] Galeria](/help/dsp/inventory/on-demand-inventory-subscribe.md)e, em seguida, direcione qualquer uma das ofertas aprovadas dentro do [!DNL Roku] disposições:

   * &quot;[!UICONTROL Roku Network – Audience]&quot; para inventário em todo o [!DNL Roku] ecossistema com parceiros de conteúdo premium, como [!DNL The CW], [!DNL ABC]e [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel – Audience]&quot; para [!DNL Roku] conteúdo de aplicativo próprio e operado (O&amp;O).

### Vantagens de personalizar mercados privados com [!DNL Roku]

As ofertas privadas permitem que você personalize os parâmetros de negócios de acordo com suas necessidades.

* **Preços negociados:** Trabalhe com a [!DNL Roku] equipe de vendas para negociar e estruturar um negócio que atenda às suas necessidades de campanha.

* **Prioridade da escala:** Os mercados privados (PMPs) recebem prioridade mais alta do que as transações sempre ativas (como [!DNL On Demand] acordos).

* **Gerenciamento de frequência:** O [!DNL Roku] o limite de frequência padrão é um (1) e por 30 minutos por usuário, mas você pode personalizar o limite por hora, dia, semana, mês ou todo o período de voo.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]Direcionamento de dados:** [!DNL Roku] os públicos-alvo são criados a partir de [!DNL Roku] sinais de dispositivo e de TV, dados rastreados por [!DNL The Roku Channel] (como afinidade de gênero de TV, comportamento de transmissão de TV e status de assinatura a cabo) e dados adicionais da [!DNL Roku] sistema de gerenciamento de relacionamento com o cliente (CRM).

* **[!DNL Roku]Direcionamento de conteúdo:** As ofertas privadas podem direcionar aplicativos por gênero, aplicação de  de lista de bloqueios de aplicativos, eventos sazonais e temporários e programas dentro de [!DNL The Roku Channel] somente.

## [!DNL Roku] Posicionamentos

Em campanhas DSP, [criar [!DNL Roku]-disposições específicas](/help/dsp/campaign-management/placements/placement-create.md) usando o tipo de posicionamento &quot;[!UICONTROL Connected TV (Roku)].&quot; Incluir [!DNL Roku] disposições em [!DNL Roku]Pacotes específicos do , com metas definidas.

Cada [!DNL Roku] inserção deve direcionar pelo menos um [!DNL Roku] negócio ou fonte. Para usar a correspondência de público-alvo exclusivo do DSP com [!DNL Roku], inclua um ou mais segmentos de público-alvo que podem ser comparados com a variável [!DNL Roku] conjunto de dados determinísticos (opt-in).

### [!DNL Roku]-Fornecedores de rastreamento de terceiros aprovados

[!DNL Roku] as disposições podem incluir pixels de evento de terceiros e pixels de conversão dos seguintes fornecedores:  [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]e [!DNL Research Now].

### Práticas recomendadas por estratégia de posicionamento

Estas são as práticas recomendadas para [!DNL Roku]disposições específicas.

Para maximizar o alcance incremental:

* Suprimir públicos-alvo expostos em [!DNL Roku O&O] excluindo públicos-alvo que você já acessou usando [!DNL The Roku Channel].

* Suprimir públicos-alvo expostos em [!DNL All Roku] excluindo públicos-alvo que você já acessou na [!DNL Roku] plataforma.

Para a configuração mais rápida:

* Direcionamento de ofertas sempre ativas e existentes para [!DNL The Roku Channel] em [[!DNL On Demand] Inventário](/help/dsp/inventory/on-demand-inventory-subscribe.md) para acessar rapidamente [!DNL Roku] inventário próprio e explorado.
* Direcionamento de ofertas sempre ativas e existentes para [!DNL Roku Network] em [[!DNL On Demand] Inventário](/help/dsp/inventory/on-demand-inventory-subscribe.md) para atingir rapidamente a escala na [!DNL Roku] plataforma.

Para obter a escala máxima:

* Personalize uma [!DNL Roku] private marketplace para acesso priorizado a [!DNL Roku] fornecimento a um preço negociado.

>[!MORELIKETHIS]
>
>* [Criar manualmente detalhes da ID do contrato](/help/dsp/inventory/deal-id-create.md)
> * [Assinar e solicitar acesso a [!DNL On Demand] Contratos de inventário premium](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Criar uma disposição](/help/dsp/campaign-management/placements/placement-create.md)

