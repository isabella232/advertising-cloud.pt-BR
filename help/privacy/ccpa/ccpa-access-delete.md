---
title: 'Suporte de publicidade do Adobe para a Lei de Privacidade do Consumidor da Califórnia : Suporte para acesso e exclusão de dados do consumidor'
description: Saiba mais sobre os tipos de solicitação de dados suportados, a configuração necessária e os valores de campo, além de exemplos de solicitações de acesso à API usando IDs de produto herdadas e campos de dados retornados.
feature: CCPA
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
source-git-commit: e9d9d51302d32b06af805917db2f46e5f6daee62
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 0%

---

# Suporte de publicidade Adobe para a Lei de Privacidade do Consumidor da Califórnia: Suporte para acesso e exclusão de dados do consumidor

*Para [!DNL Adobe Advertising Search]; Adobe Advertising DSP; Adobe Advertising Creative; e Adobe Advertising DCO*

>[!IMPORTANT]
>
>O conteúdo deste documento não é um aconselhamento jurídico e não se destina a substituir tal aconselhamento. Consulte seu advogado para obter conselhos sobre a Lei de Privacidade do Consumidor da Califórnia.

A California Consumer Privacy Act (CCPA) é a nova lei de privacidade da Califórnia, que entrará em vigor em 1º de janeiro de 2020. A CCPA fornece aos residentes da Califórnia novos direitos sobre suas informações pessoais e impõe responsabilidades de proteção de dados a determinadas entidades que realizam negócios na Califórnia. A CCPA dá aos consumidores o direito de acessar e apagar suas informações pessoais, bem como o direito de recusar certas atividades qualificadas como &quot;venda&quot; de informações pessoais a terceiros.

Como empresa, você determinará os dados pessoais que a Adobe Experience Cloud processa e armazena em seu nome.

Como seu provedor de serviços, a Adobe Advertising fornece suporte para que sua empresa cumpra as obrigações da CCPA, aplicáveis ao uso de produtos e serviços de Adobe Advertising, incluindo o gerenciamento de solicitações para acessar e excluir informações pessoais e o gerenciamento de solicitações para recusar a venda de informações pessoais.

Este documento descreve como [!DNL Advertising Search]; Publicidade criativa; Advertising DSP (Demand Side Platform); e [!DNL Advertising DCO] — como prestadores de serviços — apoiem os direitos dos consumidores de acederem e apagarem informações pessoais usando a Adobe [!DNL Experience Platform Privacy Service API] e [!DNL Privacy Service UI].

Para obter informações sobre como a Advertising DSP suporta o direito do consumidor de recusar a venda de informações pessoais, consulte [Suporte de publicidade Adobe para a Lei de Privacidade do Consumidor da Califórnia: Suporte ao cancelamento da adesão do consumidor](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

Para obter mais informações sobre os serviços de privacidade do Adobe para CCPA, consulte o [Centro de privacidade do Adobe](https://www.adobe.com/privacy/ccpa.html).

## Tipos de solicitação de dados suportados para publicidade Adobe

O Adobe Experience Platform fornece a capacidade de as empresas concluírem as seguintes tarefas:

* Acesse os dados a nível de cookie de um consumidor ou os dados a nível de ID do dispositivo (para anúncios em aplicativos móveis) em [!DNL Search], [!DNL Creative], [!DNL DSP]ou [!DNL DCO].
* Excluir dados a nível de cookie armazenados em [!DNL Search], [!DNL Creative], [!DNL DSP]ou [!DNL DCO] para consumidores que utilizem um browser; ou excluir dados a nível de ID armazenados em [!DNL DSP] para consumidores que utilizam aplicativos em dispositivos móveis.
* Verifique o status de uma ou todas as solicitações existentes.

## Configuração necessária para enviar solicitações de publicidade do Adobe Advertising

Para fazer solicitações de acesso e exclusão de informações pessoais do consumidor da Adobe Advertising, você precisará:

1. Implante uma biblioteca JavaScript para recuperar e remover os cookies do cliente. A mesma biblioteca, `AdobePrivacy.js`, é usada para todas as soluções da Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >As solicitações para algumas soluções do Experience Cloud não exigem a biblioteca JavaScript, mas as solicitações para a Adobe Advertising exigem-na.

   Você deve implantar a biblioteca na página da Web da qual seus clientes podem enviar solicitações de acesso e exclusão, como o portal de privacidade da sua empresa. A biblioteca ajuda a recuperar cookies do Adobe (ID do namespace: `gsurferID`) para que você possa enviar essas identidades como parte das solicitações de acesso e exclusão por meio do [!DNL Adobe Experience Platform Privacy Service API].

   Quando o cliente solicita a exclusão de dados pessoais, a biblioteca também exclui o cookie do cliente do navegador do cliente.

   >[!NOTE]
   >
   >A exclusão de dados pessoais é diferente da recusa, que impede o direcionamento de um usuário final com segmentos de público-alvo. No entanto, quando um consumidor solicita a exclusão de dados pessoais do [!DNL Creative], [!DNL DSP]ou [!DNL DCO], a biblioteca também envia uma solicitação para a Adobe Advertising para excluir o cliente do direcionamento de segmentos. Para anunciantes com [!DNL Search], recomendamos que você forneça aos clientes um link para [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse), que explica como recusar o direcionamento do segmento de público-alvo.

1. Identifique a ID da organização do Experience Cloud e verifique se ela está vinculada às contas do Adobe Advertising.

   Uma ID de Experience Cloud da organização é uma sequência de 24 caracteres alfanuméricos anexada com &quot;@AdobeOrg&quot;. A maioria dos clientes do Experience Cloud recebeu uma ID da organização. Se a sua equipe de marketing ou o administrador interno do sistema do Adobe não souber a ID da organização ou não tiver certeza se ela foi fornecida, entre em contato com o Atendimento ao cliente do Adobe em gdprsupport@adobe.com. Você precisará da ID da organização para enviar solicitações à API de Privacidade usando o `imsOrgID` namespace.

   >[!IMPORTANT]
   >
   >Entre em contato com o representante de publicidade Adobe da sua empresa para confirmar que todas as contas de publicidade Adobe da sua organização, incluindo [!DNL DSP] contas ou anunciantes, [!DNL Search] contas e [!DNL Creative] ou [!DNL DCO] contas — são vinculadas à ID da organização do Experience Cloud.

1. Use a variável [API do Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (para solicitações automatizadas) ou [Interface do usuário do Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (para pedidos ad-hoc) para enviar pedidos de acesso e de eliminação de informações pessoais à Adobe Advertising em nome dos consumidores e para verificar o estado dos pedidos existentes.

   Para anunciantes que têm um aplicativo móvel para interagir com clientes e lançar campanhas com [!DNL DSP], será necessário baixar os SDKs móveis prontos para privacidade para o Experience Cloud. Os Mobile SDKs permitem que as empresas definam sinalizadores de status de opção de não participação, recupere a ID de dispositivo do consumidor (ID de namespace: `deviceID`) e enviar solicitações para a API do Privacy Service. Seu aplicativo móvel exigirá uma versão 4.15.0 ou superior do SDK.

   Ao enviar uma solicitação de acesso do consumidor, a API do Privacy Service retorna as informações do consumidor com base no cookie ou na ID do dispositivo especificada, que você deve retornar ao consumidor.

   Ao enviar uma solicitação de exclusão do consumidor, a ID do cookie ou a ID do dispositivo e todos os dados de custo, clique e receita associados ao cookie são excluídos do servidor.

   >[!NOTE]
   Se sua empresa tiver várias IDs de organização do Experience Cloud, você deverá enviar solicitações de API separadas para cada uma. No entanto, você pode fazer uma solicitação de API para várias subsoluções de Adobe Advertising ([!DNL Search], [!DNL Creative], [!DNL DSP]e [!DNL DCO]), com uma conta por subsolução.

Todas essas etapas são necessárias para receber suporte da Adobe Advertising. Para obter mais informações sobre essas e outras tarefas relacionadas que você precisa executar usando a Adobe Experience Platform Privacy Service e onde encontrar os itens que você precisará, consulte [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Valores de campo obrigatórios em solicitações JSON de publicidade do Adobe

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*sua ID da organização do Experience Cloud*>

&quot;users&quot;:

* `"key":` &lt;*geralmente o nome do cliente*>

* `"action":` ou `**access**` ou `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (que indica o espaço do cookie da adcloud)

   * `"value":` &lt;*o valor da ID de cookie do cliente real, como recuperado de`AdobePrivacy.js`*>

* `"include": **adCloud**` (que é o Adobe product que se aplica à solicitação)

* `"regulation": **ccpa**` (que é o regulamento de privacidade que se aplica à solicitação)

## Exemplo de solicitação enviada por um consumidor usando uma ID de usuário de publicidade Adobe recuperada do AdobePrivacy.js

```
{
"companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
  "userIDs":[
      {
         "namespace":"411",
         "value":"Wqersioejr-wdg",
         "type":"namespaceId",
         "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"ccpa"
}
}
```

## Campos de dados retornados para solicitações de acesso

A seguir encontra-se um exemplo de resposta de acesso a informações pessoais para Adobe Advertising.

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
