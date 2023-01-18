---
title: Sobre o [!UICONTROL Deal ID Inbox]
description: Saiba mais sobre o [!UICONTROL Deal ID inbox] , que permite aceitar ofertas privadas que você já negociou com editores no [!DNL FreeWheel], [!DNL Google Authorized Buyers] (anteriormente conhecido como [!DNL AdX]), and [!DNL Magnite DV+] (anteriormente [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---

# Sobre o [!UICONTROL Deal ID Inbox]

O DSP de publicidade [!UICONTROL Deal ID inbox] O permite que você configure rapidamente ofertas que DSP importou de editores por meio de plataformas do lado do suprimento (SSPs) para que você não precise configurar cada negócio manualmente. Você pode aceitar as ofertas de inventário privado garantidas e não garantidas que já negociou com editores em [!DNL FreeWheel], [!DNL Google Authorized Buyers] (anteriormente conhecido como [!DNL AdX]), e [!DNL Magnite DV+] (anteriormente [!DNL Rubicon]) do [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>A DSP de publicidade é a primeira DSP a ser integrada à [!DNL FreeWheel] API.

No [!UICONTROL Deal ID inbox], você pode ver os detalhes da venda à medida que o editor os vê, acelerar a configuração da venda e evitar erros de entrada manual.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.
   
You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP atualiza automaticamente todos os detalhes do negócio diariamente às 4:30 EST. Ele também atualiza tudo [!DNL FreeWheel] negócios e atualiza negócios existentes de [!DNL Google] e [!DNL Magnite DV+] Por hora. Você também pode atualizar manualmente os detalhes do negócio para preencher novas ofertas a qualquer momento.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>Para acordos programáticos garantidos através de [!DNL Google Authorized Buyers], você deve entregar pelo menos 90% do seu orçamento, caso contrário sua conta perderá o acesso a [!DNL Google] nas [!UICONTROL Deal ID inbox].

## Implementar o [!UICONTROL Deal ID Inbox]

Para receber suas ofertas na [!UICONTROL Deal ID inbox], suas contas do SSP devem mapear a conta de DSP da organização para a conta do SSP. DSP compartilhará os nomes de conta da organização com os PUPs relevantes. Entre em contato com seu [!DNL Adobe] para obter instruções.

Durante as negociações de negócios, diga ao editor para enviar o contrato para seu comprador em vez de para a conta de DSP principal. O identificador da transação pode ser um nome ou uma ID, dependendo da PUP.

## Ações possíveis

* **Revisar negociações** para verificar se a SSP enviou o editor correto, as datas de voo, o CPM e outros detalhes do negócio. Se o editor tiver cometido um erro, entre em contato com o DSP para que ele possa corrigir e reenviar o negócio.

* **Aceitar ofertas** depois de revisar, e elas não serão mais exibidas na variável [!UICONTROL Deal ID inbox]. Os negócios aceitos são listados em [!UICONTROL Inventory] > [!UICONTROL Deals] e estão prontas para direcionar nas disposições dos anunciantes.

* **Ignorar ofertas** que não são necessárias ou não são solicitadas. Os negócios ignorados são movidos para a variável [!UICONTROL Ignored Deals] na guia [!UICONTROL Deal ID inbox], que serve como um arquivo. DSP não alerta SSPs e editores quando você ignora um negócio.

* **Modificar detalhes de ofertas já aceitas** from [!UICONTROL Inventory] > [!UICONTROL Deals] (não no [!UICONTROL Deal ID inbox]). Da mesma forma, quando os editores enviam alterações a ofertas, os anunciantes são responsáveis pela implementação dessas alterações no [!UICONTROL Inventory] > [!UICONTROL Deals] porque a variável [!UICONTROL Deal ID inbox] não sincroniza alterações dos SSPs após a configuração das ofertas.

## Que tipos de negócios não podem ser aceitos?

Quando uma listagem de negócios não inclui uma ![Aceitar](/help/dsp/assets/accept.png) ou um [!UICONTROL Accept] não é possível aceitá-lo do [!UICONTROL Deal ID inbox]. Em vez disso, você pode [criar os detalhes da ID de negócios manualmente](/help/dsp/inventory/deal-id-create.md).

Você não pode aceitar os seguintes tipos de ofertas:

* [!DNL Google] acordos que não estão em USD.

* [!DNL Magnite DV+] acordos que não estão em USD

* [!DNL FreeWheel] ofertas que não estão na moeda da sua conta.

* Contratos que têm data final antes de hoje.

* Antigo [!DNL Magnite DV+] ofertas rotuladas como &quot;vários tipos de mídia&quot;.

Os detalhes do negócio incluem o motivo pelo qual o negócio não está disponível para aceitar.

>[!MORELIKETHIS]
>
>* [Aceitar um contrato na Caixa de entrada da ID do contrato](deal-id-inbox-accept.md)
>* [Visão geral dos recursos de inventário](inventory-overview.md)

