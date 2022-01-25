---
title: 'Suporte da Adobe Advertising Cloud para a Lei de Privacidade do Consumidor da Califórnia : Suporte para cancelamento da venda do consumidor'
description: Saiba mais sobre o suporte para capturar solicitações de cancelamento da venda do consumidor.
feature: CCPA
exl-id: 2c0cd4f5-798f-479a-99cd-f555cd676766
source-git-commit: adb3118d291d110e653a62cc1a323410b1a596b2
workflow-type: tm+mt
source-wordcount: '1031'
ht-degree: 0%

---

# Suporte da Adobe Advertising Cloud para a Lei de Privacidade do Consumidor da Califórnia: Suporte ao cancelamento da venda do consumidor

*Para Adobe Advertising Cloud Demand Side Platform*

>[!IMPORTANT]
>
>O conteúdo deste documento não é um aconselhamento jurídico e não se destina a substituir tal aconselhamento. Consulte seu advogado para obter conselhos sobre a Lei de Privacidade do Consumidor da Califórnia.

A California Consumer Privacy Act (CCPA) é a nova lei de privacidade da Califórnia, que entrará em vigor em 1º de janeiro de 2020. A CCPA fornece aos residentes da Califórnia novos direitos sobre suas informações pessoais e impõe responsabilidades de proteção de dados a determinadas entidades que realizam negócios na Califórnia. A CCPA dá aos consumidores o direito de acessar e excluir seus dados, bem como o direito de recusar certas atividades qualificadas como &quot;venda&quot; de informações pessoais a terceiros.

Como empresa, você determinará os dados pessoais que a Adobe Experience Cloud processa e armazena em seu nome.

Como seu provedor de serviços, a Adobe Advertising Cloud fornece suporte para que sua empresa cumpra as obrigações da CCPA aplicáveis ao uso de produtos e serviços da Advertising Cloud, incluindo o gerenciamento de solicitações do consumidor para acessar e excluir informações pessoais e o gerenciamento de solicitações do consumidor para recusar a venda de informações pessoais.

Este documento descreve como o Adobe Advertising Cloud Demand Side Platform (DSP), como um provedor de serviços, suporta o direito do consumidor de recusar a &quot;venda&quot; de &quot;informações pessoais&quot;, conforme cada termo é definido pela CCPA. Ele inclui informações sobre como comunicar solicitações de não participação na venda ao Advertising Cloud e como recuperar relatórios das solicitações de não participação na venda de sua organização.

Para obter informações sobre como o Advertising Cloud Search, Advertising Cloud Creative, Advertising Cloud DSP (Demand Side Platform) e o DCO do Media Otimizer oferecem suporte aos direitos de acesso e exclusão de informações pessoais dos consumidores, consulte [Suporte da Adobe Advertising Cloud para a Lei de Privacidade do Consumidor da Califórnia: Suporte para acesso e exclusão de dados do consumidor](/help/privacy/ad-cloud-ccpa-access-delete.md).

Para obter mais informações sobre os serviços de privacidade do Adobe para CCPA, consulte o [Centro de privacidade do Adobe](https://www.adobe.com/privacy/ccpa.html).

## Comunicar solicitações de recusa de venda do consumidor ao Advertising Cloud

Você pode comunicar solicitações de cancelamento de venda do consumidor usando:

* um segmento de cancelamento de venda do CCPA criado no Advertising Cloud DSP
* a API do Adobe Experience Platform Privacy Service

### Método 1: Comunicar as solicitações de recusa de venda do CCPA usando um [!UICONTROL CCPA Opt-Out-of-Sale] Segmento no Advertising Cloud DSP

>[!NOTE]
>
>Os usuários permanecem indefinidamente em segmentos de opção de não participação na CCPA.

1. Faça logon na conta do anunciante no Advertising Cloud DSP em [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Crie um segmento de cancelamento de venda do CCPA e implemente o pixel do segmento para capturar as solicitações de cancelamento](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Método 2: Comunicar as solicitações de recusa de venda do CCPA usando a API do Adobe Experience Platform Privacy Service

*Os anunciantes atribuíram uma Adobe Experience Cloud [!DNL Organization ID] ([!DNL IMS Org ID]somente )*

1. Implante uma biblioteca JavaScript para recuperar os cookies do cliente. A mesma biblioteca, `AdobePrivacy.js`, é usada para todas as soluções da Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >As solicitações para algumas soluções da Adobe Experience Cloud não exigem a biblioteca do JavaScript, mas as solicitações para a Advertising Cloud exigem.

   Você deve implantar a biblioteca na página da Web da qual seus clientes podem enviar solicitações de recusa de venda, como o portal de privacidade da sua empresa. A biblioteca ajuda a recuperar cookies do Adobe (ID do namespace: `gsurferID`) para enviar essas identidades como parte das solicitações de não participação na venda por meio da API do Adobe Experience Platform Privacy Service.

1. Identifique a ID da organização IMS e verifique se ela está vinculada às contas da Advertising Cloud.

   Uma ID de organização IMS é uma sequência de 24 caracteres alfanuméricos anexada com @AdobeOrg. A maioria dos clientes do Adobe Experience Cloud recebeu uma ID organizacional IMS. Se a equipe de marketing ou o administrador interno do sistema do Adobe não souber a ID organizacional IMS da organização ou não tiver certeza se ela foi fornecida, entre em contato com o Atendimento ao cliente do Adobe em gdprsupport@adobe.com. Você precisará da ID de organização IMS para enviar solicitações à API de privacidade.

   >[!IMPORTANT]
   >
   >Entre em contato com o representante da Advertising Cloud de sua empresa para confirmar que todas as contas da Advertising Cloud de sua organização, incluindo [!DNL DSP] contas ou anunciantes, [!DNL Search] contas e [!DNL Creative] ou [!DNL DCO] contas — estão vinculadas à ID da organização IMS.

1. Use a API do Adobe Experience Platform Privacy Service para [enviar solicitações de cancelamento de venda](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) à Advertising Cloud em nome dos consumidores e para verificar o estado dos pedidos existentes.

   Consulte o Apêndice abaixo para obter um exemplo de uma solicitação de recusa de venda.

   >[!NOTE]
   Se sua empresa tiver várias IDs de organização do serviço da Adobe Experience Cloud Identity Management (IDs de organização IMS), você deverá enviar solicitações de API separadas para cada uma. No entanto, você pode fazer uma solicitação de API para várias subsoluções da Advertising Cloud ([!DNL Search], [!DNL Creative], [!DNL DSP]e [!DNL DCO]), com uma conta por subsolução.

Todas essas etapas são necessárias para receber suporte da Advertising Cloud. Para obter mais informações sobre essas e outras tarefas relacionadas que você precisa executar usando a Adobe Experience Platform Privacy Service e onde encontrar os itens que você precisará, consulte [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Recuperação de Relatórios de Consumidores que Enviaram Solicitações de Não Venda

O Advertising Cloud gera relatórios mensais de IDs que os clientes enviaram para solicitações de não participação na venda da conta. Cada relatório está disponível como um arquivo de texto separado por tabulações compactado no formato GZIP. Os dados consolidam solicitações capturadas por meio de segmentos de não participação na venda do CCPA criados no Advertising Cloud DSP e quaisquer envios feitos por meio da API do Privacy Service. As IDs de usuário capturadas nos segmentos de não participação na venda do CCPA são identificadas por segmento e pelo anunciante. Os relatórios são gerados no primeiro de cada mês do mês anterior. Por exemplo, a lista mensal de usuários para junho está disponível em 1 de julho.

Você pode recuperar links para os relatórios mensais criados nos três meses anteriores, dentro do Advertising Cloud DSP ou usando a Advertising Cloud [!DNL Trafficking API]. Cada link é válido por sete dias, mas é atualizado sempre que um cliente tenta recuperar um.

### Método 1: Recuperar relatórios de cancelamento de venda do consumidor no Advertising Cloud DSP

1. Faça logon na conta do anunciante no Advertising Cloud DSP em [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Recuperar os relatórios](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Método 2: Recuperar relatórios de não participação do consumidor usando a Advertising Cloud [!DNL Trafficking API]

Esse recurso está disponível para organizações que usam a variável [!DNL Trafficking API]. Consulte a documentação do [!DNL Trafficking API] para obter mais informações.

Se sua organização não usar a variável [!DNL Trafficking API] mas está interessado em mais informações, entre em contato com seu [!DNL Adobe] gerente de conta.

## Apêndice: Exemplo [!UICONTROL CCPA Opt-Out-of-Sale] Solicitação para usuários da API do Privacy Service

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["AdCloud"],
    "regulation": "ccpa"
}'
```

em que:

* `"namespace": "AdCloud"` indica que `AdCloud` espaço do cookie e o valor correspondente é a ID do cookie do cliente, como recuperada de `AdobePrivacy.js`
* `"include": ["AdCloud"]` indica que a solicitação se aplica ao Advertising Cloud
