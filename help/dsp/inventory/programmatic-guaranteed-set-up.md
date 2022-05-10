---
title: Configurar um acordo programático garantido
description: Saiba como configurar um negócio programático garantido (PG) que você negociou com um editor.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 9e371606-5428-4635-9653-7dc43449e489
source-git-commit: 3c9822890e96035fc9e44f8832efcc2889a8cb5f
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Configurar um acordo programático garantido

*[Somente plataformas compatíveis do lado do suprimento](programmatic-guaranteed-about.md)*

Depois de negociar um negócio programático garantido (PG) com um editor suportado, você pode configurar a negociação no DSP usando o [!DNL Deal ID inbox] ou inserindo manualmente os detalhes da negociação.

>[!NOTE]
>
> Para ofertas PG, o editor lida com todo o ritmo do orçamento, limite de orçamento e definição de metas. Todos os SSPs que permitem o PG por DSP confirmam que o editor pode configurar o limite de orçamento.
>
> Configuração de acordos programáticos garantidos com editores em [!DNL FreeWheel] O requer permissões e etapas adicionais. Consulte &quot;[Visão geral da configuração de contratos programáticos garantidos no [!DNL FreeWheel]](freewheel-overview.md)&quot; para obter mais informações.

## Configure um acordo programático garantido usando o [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

Esse é o método preferido para [!DNL FreeWheel], [!DNL Google Authorized Buyers]e [!DNL Magnite DV+].

1. [Aceite o negócio](deal-id-inbox-accept.md).

1. Depois de salvar o negócio, selecione os anúncios que serão usados para o negócio e crie uma disposição padrão programática garantida (PG), conforme solicitado.

   Criar uma disposição PPG padrão para a venda é obrigatório para fornecer 100% de sua compra. Esse tipo de disposição não tem direcionamento, portanto, DSP pode retornar um lance para cada solicitação de lance do editor.

   * Se estiver aceitando uma única venda, você será automaticamente redirecionado para o fluxo de trabalho de criação de disposição padrão do PG.

      Todos [!DNL FreeWheel] os acordos são propostos como um acordo único.

   * Se estiver aceitando uma proposta com várias IDs de negócios PG, identifique cada disposição padrão PG que precisa criar. Depois de criar todas as disposições necessárias, o botão continuar é ativado.

1. (Opcional) Direcione a negociação PG em disposições adicionais PG ou não-PG clicando em ![Menu Opções](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Um negócio pode direcionar várias disposições que suportam qualquer combinação de tipos de mídia (como TV conectada, desktop e áudio).

## Configurar manualmente um acordo programático garantido

Use este método para todos os outros SSPs.

1. [Configurar manualmente os detalhes da ID de negócios](deal-id-create.md).

1. Depois de salvar o negócio, selecione os anúncios que serão usados para o negócio e crie uma disposição padrão PG, conforme solicitado.

   Criar uma disposição padrão PG para a venda é obrigatório para fornecer 100% de sua compra. Esse tipo de disposição não tem direcionamento, portanto, DSP pode retornar um lance para cada solicitação de lance do editor.

1. (Opcional) Direcione a negociação PG em disposições adicionais PG ou não-PG clicando em ![Menu Opções](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Um negócio pode direcionar várias disposições que suportam qualquer combinação de tipos de mídia (como TV conectada, desktop e áudio).

>[!MORELIKETHIS]
>
>* [Sobre contratos programáticos garantidos](programmatic-guaranteed-about.md)
>* [Dicas para negociar um acordo programático garantido](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Envie um anúncio para um acordo programático garantido com o [!DNL FreeWheel]](freewheel-submit.md)
>* [Aceitar um contrato na Caixa de entrada da ID do contrato](deal-id-inbox-accept.md)
>* [Criar manualmente detalhes da ID do contrato](deal-id-create.md)
>* [Parceiros SSP](ssp-partners.md)
>* [Visão geral dos recursos de inventário](inventory-overview.md)

