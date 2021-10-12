---
title: Sobre o [!UICONTROL Deal ID Inbox]
description: Saiba mais sobre o recurso [!UICONTROL Deal ID inbox], que permite aceitar ofertas privadas que já negociou com editores em [!DNL FreeWheel], [!DNL Google Authorized Buyers] (formerly known as [!DNL AdX]), and [!DNL Magnite DV+] (anteriormente [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: 8046ec79ec24f47fe33e49c6097e44dbba450f1f
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Sobre o [!UICONTROL Deal ID Inbox]

DSP [!UICONTROL Deal ID inbox] permite que você configure rapidamente as ofertas que a Advertising Cloud DSP importou de editores por meio de plataformas do lado do suprimento (SSPs), de modo que não seja necessário configurar cada negócio manualmente. Você pode aceitar as ofertas de inventário privado garantidas e não garantidas que já negociou com editores em [!DNL FreeWheel], [!DNL Google Authorized Buyers] (anteriormente conhecido como [!DNL AdX]) e [!DNL Magnite DV+] (anteriormente [!DNL Rubicon]) no [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>O Advertising Cloud DSP é o primeiro DSP a ser integrado à API [!DNL FreeWheel].

No [!UICONTROL Deal ID inbox], você pode ver os detalhes do negócio conforme seu editor os vê, acelerar sua configuração de negócio e evitar erros de entrada manual.

DSP atualiza automaticamente todos os detalhes do negócio diariamente às 4:30 EST. Ele também atualiza todas as [!DNL FreeWheel] negociações e atualiza as ofertas existentes de [!DNL Google] e [!DNL Magnite DV+] por hora. Você também pode atualizar manualmente os detalhes do negócio para preencher novas ofertas a qualquer momento.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>Para ofertas programáticas garantidas por meio de [!DNL Google Authorized Buyers], você deve entregar pelo menos 90% do seu orçamento, caso contrário sua conta perderá o acesso a [!DNL Google] ofertas no [!UICONTROL Deal ID inbox].

## Implementar o [!UICONTROL Deal ID Inbox]

Para receber suas ofertas no [!UICONTROL Deal ID inbox], suas contas do SSP devem mapear a conta de DSP de sua organização para a conta do SSP. DSP compartilhará os nomes de conta da organização com os PUPs relevantes. Entre em contato com o gerente de conta do Adobe para obter instruções.

Durante as negociações de negócios, diga ao editor para enviar o contrato para seu comprador em vez de para a conta de DSP principal. O identificador da transação pode ser um nome ou uma ID, dependendo da PUP.

## Ações possíveis

* **Revise** os adiamentos para verificar se a SSP enviou o editor correto, as datas de voo, o CPM e outros detalhes do negócio. Se o editor tiver cometido um erro, entre em contato com o DSP para que ele possa corrigir e reenviar o negócio.

* **Aceite** adiantes de revisar e eles não aparecerão mais no  [!UICONTROL Deal ID inbox]. As ofertas aceitas são listadas em [!UICONTROL Inventory] > [!UICONTROL Deals] e estão prontas para o direcionamento dentro das disposições dos anunciantes.

* **Ignore** as transações que não são necessárias ou que não são solicitadas. As ofertas ignoradas são movidas para a guia [!UICONTROL Ignored Deals] dentro do [!UICONTROL Deal ID inbox], que serve como um arquivo. DSP não alerta SSPs e editores quando você ignora ofertas.

* **Modifique os detalhes de** ofertas já aceitas de  [!UICONTROL Inventory] >  [!UICONTROL Deals] (não no  [!UICONTROL Deal ID inbox]). Da mesma forma, quando os editores enviam alterações a ofertas, os anunciantes são responsáveis por implementar essas alterações em [!UICONTROL Inventory] > [!UICONTROL Deals] porque o [!UICONTROL Deal ID inbox] não sincroniza as alterações das SSPs após a configuração das ofertas.

## Que tipos de negócios não podem ser aceitos?

Quando uma listagem de negócios não inclui um ícone ![Accept](/help/dsp/assets/accept.png) ou um botão [!UICONTROL Accept], você não pode aceitá-la do [!UICONTROL Deal ID inbox]. Em vez disso, você pode [criar os detalhes da ID de negócios manualmente](/help/dsp/inventory/deal-id-create.md).

Você não pode aceitar os seguintes tipos de ofertas:

* [!DNL Google] acordos que não estão em USD.

* [!DNL Magnite DV+] acordos que não estão em USD

* [!DNL FreeWheel] ofertas que não estão na moeda da sua conta.

* Contratos que têm data final antes de hoje.

* Ofertas antigas [!DNL Magnite DV+] que eram rotuladas como &quot;vários tipos de mídia&quot;.

Os detalhes do negócio incluem o motivo pelo qual o negócio não está disponível para aceitar.

>[!MORELIKETHIS]
>
>* [Aceitar um contrato na Caixa de entrada da ID do contrato](deal-id-inbox-accept.md)
>* [Visão geral dos recursos de inventário](inventory-overview.md)

