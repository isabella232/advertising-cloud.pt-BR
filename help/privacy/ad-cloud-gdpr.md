---
title: Suporte da Adobe Advertising Cloud para o Regulamento Geral sobre a Proteção de Dados
description: Saiba mais sobre os tipos de solicitação de dados suportados, a configuração necessária e os valores de campo, e exemplos de solicitações de acesso à API usando IDs de produto herdadas e campos de dados retornados
feature: GDPR
exl-id: 304d88d0-d63d-4b32-8d4d-c61ba2409adc
source-git-commit: 2e0395dc1e5aa52adc83c1aaea49793fd5555390
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 0%

---

# Suporte da Adobe Advertising Cloud para o Regulamento Geral sobre a Proteção de Dados

*Para Adobe Advertising Cloud Search, Adobe Advertising Cloud Creative, Adobe Advertising Cloud DSP e Adobe Media Optimizer DCO*

>[!IMPORTANT]
>
>O conteúdo deste documento não é um aconselhamento jurídico e não se destina a substituir tal aconselhamento. Consulte seu advogado para obter aconselhamento sobre o Regulamento Geral sobre a Proteção de Dados.

O Regulamento Geral sobre a Proteção de Dados (GDPR), uma lei em vigor desde 25 de maio de 2018, concede a todos os indivíduos (titulares de dados) dentro das fronteiras da União Europeia (UE) o controle de seus dados pessoais e simplifica o ambiente regulamentar para os negócios internacionais. Esta lei se aplica a todas as empresas (controladores de dados) que oferecem bens ou serviços para monitorar o comportamento ou coletar dados pessoais de indivíduos dentro das fronteiras da UE no momento em que seus dados pessoais são processados, independentemente da localização comercial do controlador de dados.

A Adobe Experience Cloud atua como um processador de dados para quaisquer dados pessoais que recebe e armazena em nome de seus clientes. Como controlador de dados, você determinará os dados pessoais que a Adobe Experience Cloud processa e armazena em seu nome.

Este documento descreve como o Advertising Cloud Search, Advertising Cloud Creative, Advertising Cloud DSP (Demand Side Platform) e Media Otimizer DCO oferecem suporte aos direitos de acesso e exclusão de dados do GDPR de seus titulares de dados usando a API do Adobe Experience Platform Privacy Service e a interface do usuário do Privacy Service.

Para obter mais informações sobre o que o GDPR significa para sua empresa, consulte [GDPR e seu negócio](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Tipos de solicitação de dados compatíveis com o Advertising Cloud

O Adobe Experience Platform fornece a capacidade de as empresas concluírem as seguintes tarefas:

* Acesse os dados a nível de cookie de um titular de dados ou os dados a nível de ID do dispositivo (para anúncios em aplicativos móveis) em [!DNL Search], [!DNL Creative], [!DNL DSP]ou [!DNL DCO].
* Excluir dados a nível de cookie armazenados em [!DNL Search], [!DNL Creative], [!DNL DSP]ou [!DNL DCO] para titulares de dados que utilizem um navegador; ou excluir dados a nível de ID armazenados em [!DNL DSP] para titulares de dados que usam aplicativos em dispositivos móveis.
* Verifique o status de uma ou todas as solicitações existentes.

## Configuração necessária para enviar solicitações para o Advertising Cloud

Para fazer solicitações de acesso e exclusão de dados para o Advertising Cloud, é necessário:

1. Implante uma biblioteca do JavaScript para recuperar e remover os cookies do titular dos dados. A mesma biblioteca, `AdobePrivacy.js`, é usada para todas as soluções da Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >As solicitações para algumas soluções da Adobe Experience Cloud não exigem a biblioteca do JavaScript, mas as solicitações para a Advertising Cloud exigem.

   Você deve implantar a biblioteca na página da Web da qual o titular dos dados pode enviar solicitações de acesso e exclusão, como o portal de privacidade da sua empresa. A biblioteca ajuda a recuperar cookies do Adobe (ID do namespace: `gsurferID`) para que você possa enviar essas identidades como parte das solicitações de acesso e exclusão por meio da API do Adobe Experience Platform Privacy Service.

   Quando o titular dos dados solicita a exclusão de dados pessoais, a biblioteca também exclui o cookie do titular dos dados do navegador.

   >[!NOTE]
   >
   >A exclusão de dados pessoais é diferente da exclusão, que impede o direcionamento de um usuário final com segmentos de público-alvo. No entanto, quando um titular de dados solicita a exclusão de dados pessoais do [!DNL Creative], [!DNL DSP]ou [!DNL DCO], a biblioteca também envia uma solicitação ao Advertising Cloud para excluir o titular dos dados do direcionamento por segmento. Para anunciantes com [!DNL Search], recomendamos que você forneça aos titulares dos dados um link para [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), que explica como recusar o direcionamento do segmento de público-alvo.

1. Identifique a ID da organização do Experience Cloud e verifique se está vinculada às contas da Advertising Cloud.

   Uma ID de Experience Cloud da organização é uma sequência de 24 caracteres alfanuméricos anexada com &quot;@AdobeOrg&quot;. A maioria dos clientes do Experience Cloud recebeu uma ID da organização. Se a sua equipe de marketing ou o administrador interno do sistema do Adobe não souber a ID da organização ou não tiver certeza se ela foi fornecida, entre em contato com o Atendimento ao cliente do Adobe em gdprsupport@adobe.com. Você precisará da ID da organização para enviar solicitações à API de Privacidade usando o `imsOrgID` namespace.

   >[!IMPORTANT]
   >
   >Entre em contato com o representante da Advertising Cloud de sua empresa para confirmar que todas as contas da Advertising Cloud de sua organização, incluindo [!DNL DSP] contas ou anunciantes, [!DNL Search] contas e [!DNL Creative] ou [!DNL DCO] contas — são vinculadas à ID da organização do Experience Cloud.

1. Use a variável [API do Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (para solicitações automatizadas) ou [Interface do usuário do Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (para solicitações ad-hoc) para enviar solicitações de acesso e exclusão à Advertising Cloud em nome dos titulares dos dados e verificar o status das solicitações existentes.

   Para anunciantes que têm um aplicativo móvel para interagir com titulares de dados e lançar campanhas com a DSP, será necessário baixar os SDKs móveis prontos para privacidade do Experience Cloud. Os SDKs móveis permitem que controladores de dados definam sinalizadores de status de recusa, recuperem a ID de dispositivo do titular dos dados (ID de namespace: deviceID) e enviar solicitações para a API do Privacy Service. Seu aplicativo móvel exigirá uma versão 4.15.0 ou superior do SDK.

   Ao enviar uma solicitação de acesso do titular dos dados, a API do Privacy Service retorna as informações do titular dos dados com base no cookie ou na ID do dispositivo especificada, que deve ser retornada ao titular dos dados.

   Ao enviar uma solicitação de exclusão do titular dos dados, a ID do cookie ou a ID do dispositivo e todos os dados de custo, clique e receita associados ao cookie são excluídos do servidor.

   >[!NOTE]
   Se sua empresa tiver várias IDs de organização do Experience Cloud, você deverá enviar solicitações de API separadas para cada uma. No entanto, você pode fazer uma solicitação de API para várias subsoluções da Advertising Cloud ([!DNL Search], [!DNL Creative], [!DNL DSP]e [!DNL DCO]), com uma conta por subsolução.

Todas essas etapas são necessárias para o Advertising Cloud. Para obter mais informações sobre essas e outras tarefas relacionadas que você precisa executar usando a Adobe Experience Platform Privacy Service e onde encontrar os itens que você precisará, consulte [www.adobe.io/apis/cloudplatform/gdpr.html](https://www.adobe.io/apis/experienceplatform/gdpr.html).

## Valores de campo obrigatórios em solicitações JSON do Advertising Cloud

&quot;contexto da empresa&quot;:

* `"namespace": **imsOrgID**`
* `"value":` &lt;*seu valor da ID da organização IMS*>

`"users":`

* `"key":` &lt;*geralmente o nome do titular dos dados*>

* `"action":` ou `**access**` ou `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (que indica a variável [!DNL adcloud] espaço do cookie)

   * `"value":` &lt;*o valor da ID de cookie do titular dos dados real, como recuperado de`AdobePrivacy.js`*>

* `"include": **adCloud**` (que é o Adobe product que se aplica à solicitação)

* `"regulation": **gdpr**` (que é o regulamento de privacidade que se aplica à solicitação)

## Exemplo de solicitação enviada pelo titular dos dados usando uma ID de usuário do Advertising Cloud recuperada de `AdobePrivacy.js`

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
    "regulation":"gdpr"
}
}
```

## Campos de dados retornados para solicitações de acesso

Veja a seguir um exemplo de resposta de acesso para o Advertising Cloud.

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
