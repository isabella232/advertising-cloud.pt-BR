---
title: Configurações de ID de contrato manual
description: Consulte descrições das configurações para IDs de negócios inseridas manualmente.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 0cd5e9e8-2b13-4b1e-a2e0-b8b492f75acf
source-git-commit: 5f39608155f9237fb6d69a7b31c007d1b8d0306f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Configurações de ID de contrato manual

| Seção | Parâmetro | Descrição | Obrigatório | Editável |
|---------|-----------|-------------|----------|----------|
| [Detalhes do contrato] | [!UICONTROL Deal name] | O nome para identificar seu [!UICONTROL Deal ID] no Advertising Cloud DSP. Insira um nome ou selecione [!UICONTROL Auto-name] para permitir que o Advertising Cloud gere um nome com base nos detalhes da negociação.<br><br>Exemplo de um nome gerado automaticamente:  [!DNL *DEAL_ID*  - ID do contrato - Fixo garantido - USD - 5 - 24Cozinha - Privada] | Sim | Sim |
|  | [!UICONTROL External deal ID] | A ID usada pelo editor e pela SSP para identificar essa negociação. | Sim | Não |
|  | [!UICONTROL Publisher] | O nome do editor que está vendendo este inventário. | Sim | Não |
|  | [!UICONTROL SSP] | A plataforma do lado do suprimento (SSP) pela qual esse negócio será executado. | Sim | Não |
|  | [!UICONTROL Media type] | O tipo de mídia que será comprada por meio deste negócio: [!UICONTROL Desktop video], [!UICONTROL Mobile video], [!UICONTROL Connected TV], [!UICONTROL Display] ou [!UICONTROL Audio]. As opções variam de acordo com a SSP.<br><br> Se a negociação permitir vários tipos de mídia, selecione o tipo de mídia para a disposição padrão quando você criar a negociação. Posteriormente, você pode selecionar um tipo de mídia diferente para criar uma nova disposição com o tipo de mídia adicional.<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Sim | Não |
|  | [!UICONTROL Deal type] | O compromisso de negócios e a estrutura de preços:<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: Você e o editor não se comprometeram com um número fixo de deliveries de impressão. A operação especifica o preço mínimo do inventário, embora o CPM possa flutuar e aumentar em função das condições de mercado.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: Você e o editor não se comprometeram com um número fixo de deliveries de impressão. O preço é a uma taxa fixa negociada.</li><li>*[!UICONTROL Guaranteed (fixed)]*: Você e o editor concordaram com um número predefinido de impressões, direcionamento, datas de voo e preço fixo.<br><br><b>Observação:</b> ofertas garantidas exigem datas de voo e um número especificado de impressões na  [!UICONTROL Tracking] seção . Você também precisará criar um posicionamento programático garantido (PG) padrão para o negócio e, como opção, poderá usar o negócio para outras disposições.</li></ul> | Sim | Não |
|  | [!UICONTROL CPM] | O custo negociado por mil impressões (CPM). | Sim | Sim |
|  | [Moeda] | A moeda do negócio.<br><br>Todos os PUP aceitam acordos em USD. Quando o SSP aceitar a moeda da sua conta DSP, essa moeda também estará disponível. | Sim | Não |
|  | [!UICONTROL Billing method] | Todas as IDs de negócios são [!DNL Adobe]-financiadas e -faturadas. A Advertising Cloud pagará todos os fornecedores de mídia disponíveis com base no uso, gerenciará discrepâncias com os fornecedores e enviará uma fatura consolidada para a conta. Esta opção incorre em comissões adicionais, tal como descrito no cartão de crédito da conta. | Sim | Não |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | O endereço de email da conta de usuário que pode acessar a negociação. | Não | Sim |
|  | [!UICONTROL Advertisers that can access this deal] | Os anunciantes específicos na conta que podem acessar este negócio.<br><br><b>Observação:</b> é possível compartilhar a negociação com anunciantes em contas adicionais na  [!UICONTROL Deals] visualização. Na linha de negócios, clique em **[!UICONTROL #]**, clique em **[!UICONTROL share]** e compartilhe a negociação com um endereço de email. | Sim | Sim |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | As datas de início e término do tráfego que usa essa negociação. Essa data é somente para fins de rastreamento e não afeta a entrega do anúncio.<br><br><b>Dica: </b> na  [!UICONTROL Inventory] exibição  [!UICONTROL Deals] >, a  [!UICONTROL Pacing & Budget] coluna mostrará como a negociação está indo para a data de voo e o objetivo de impressão especificados. Se o delivery estiver em um ritmo menor ou maior, entre em contato com o editor para ajustar o volume que ele está enviando por meio da negociação. | Negociações garantidas: Sim<br>Negociações não garantidas: Não | Sim |
|  | [!UICONTROL Impressions] | (Opcional para ofertas não garantidas) O número estimado de impressões que você espera executar usando esse negócio. Esse valor é somente para fins de rastreamento; o editor controla o delivery. | Negociações garantidas: Sim<br>Negociações não garantidas: Não | Sim |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Criar manualmente detalhes da ID do contrato](deal-id-create.md)
>* [Parceiros SSP](ssp-partners.md)

<!-- >* [About Private Inventory](private-inventory-about.md) -->
