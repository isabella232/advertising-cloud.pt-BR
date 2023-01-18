---
title: Importar segmentos do Adobe Audience Manager para o direcionamento de anúncios
description: Saiba como importar seu [!DNL Adobe] públicos-alvo em Advertising DSP e Pesquisar usando Adobe Audience Manager
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%

---

# Importar segmentos do Adobe Audience Manager para o direcionamento de anúncios

DSP publicitárias e [!DNL Advertising Search] Cada um pode obter metadados, dados de hierarquia e dados exclusivos de público-alvo para todos os anúncios ou agências de um anunciante [!DNL Adobe] públicos<!-- segments or audiences? Standardize terms per AAM's docs -->. Isso inclui dados para:

* Segmentos Adobe Audience Manager

* Segmentos do Adobe Analytics publicados na Adobe Experience Cloud

* Segmentos criados no Adobe Experience Cloud usando o [!DNL People core service]

* Segmentos criados no Adobe Experience Platform e enviados para o Adobe Advertising via Audience Manager

Para acessar [!DNL Adobe] públicos-alvo no DSP ou [!DNL Creative], você deve importar os públicos para o DSP. Para acessar [!DNL Adobe] públicos-alvo no [!DNL [!DNL Search]], você deve importar os públicos para o [!DNL [!DNL Search]].

## Pré-requisitos

* O anunciante deve implementar [o [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) versão 2.0 ou superior. O [!DNL Identity Service] O fornece uma ID contínua e universal que identifica os visitantes em todas as soluções do Experience Cloud.

   A implementação inclui adicionar o [!DNL Identity service] código para cada página da Web nos sites do anunciante.

* A organização deve ser [habilitado para serviços de Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) e ter um Experience Cloud [!DNL Organization ID] (anteriormente chamado de [!DNL IMS org ID]).

   O [!UICONTROL Organization ID] O permite que organizações com vários produtos da Adobe Experience Cloud compartilhem dados entre alguns dos produtos.

* (Anunciantes com [!DNL Analytics]) O anunciante deve [implementar [!DNL Analytics] usar `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) versão 1.6.4 ou superior.

* Os visitantes do site do anunciante não incluem um alto volume de [!DNL Apple Safari] usuários.

* (Recomendado quando o anunciante usa Audience Manager e [!DNL Analytics]) Para reduzir as chamadas para cada página da Web, remova o Audience Manager existente [!DNL Data Integration Library] código para coleta de dados e habilitar o encaminhamento pelo lado do servidor para cada [!DNL Analytics] conjunto de relatórios em vez disso. Para obter mais informações, consulte &quot;[Visão geral do encaminhamento pelo lado do servidor](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

* (Recomendado) Para taxas de correspondência mais altas, envie somente dados de site primários para Adobe Advertising. Se o anunciante agrupar dados de terceiros ou dados offline de um sistema de gerenciamento de relacionamento com o cliente, o vazamento de dados poderá reduzir as taxas de correspondência.

## Importar públicos-alvo do Audience Manager para o DSP

### Etapas para importar públicos para DSP

O [!DNL Adobe] As equipes de operações de conta e dados executarão as seguintes etapas.

1. O [!DNL Adobe] a equipe de conta deve configurar a configuração no nível do anunciante &quot;[!UICONTROL Adobe Analytics Cloud].&quot;

1. O [!DNL Adobe] a equipe de conta deve enviar uma solicitação<!-- Submit a request as a JIRA task? --> à equipe de operações de dados<!-- implementation team? --> para importar os segmentos do Audience Manager da organização usando a integração Advertising DSP API nativa.

### O que as alterações resultam em Audience Manager?

A API automaticamente:

* Cria dois destinos DSP no Audience Manager:

   * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* Mapeia os dois destinos para todos os segmentos de Audience Manager, permitindo que o Audience Manager compartilhe os segmentos com a conta do anunciante de DSP associada ao mesmo Experience Cloud [!DNL Organization ID] usado para Audience Manager. <!-- Verify -->

   Como opção, a organização pode remover segmentos desnecessários dos destinos no Audience Manager.

* Adiciona o seguinte pixel de sincronização de cookies do exchange ao contêiner de Audience Manager da organização para melhorar o alcance das campanhas do cliente:

   * Adobe AdCloud: 411 (Isso vem como padrão e automaticamente como parte do [!DNL Identity Service] versão 2.0. Organizações com [!DNL Identity Service] as versões abaixo de 2.0 devem adicionar esse pixel ao contêiner de Audience Manager.

## Importar públicos-alvo do Audience Manager para o [!DNL Search]

### Etapas para importar públicos para [!DNL Search]

[!DNL Adobe] a equipe executará a maioria ou todas as etapas a seguir.

1. O [!DNL Adobe] a equipe de conta deve enviar uma solicitação para a equipe de operações de dados para configurar uma integração entre [!DNL Search] e Audience Manager. Inclua os nomes dos segmentos do Audience Manager para os quais você deseja exportar [!DNL Search].

1. No Audience Manager, configure os destinos para [!DNL Search]:

   1. Crie dois novos destinos: `[!UICONTROL Adobe Media Optimizer (HTTP)]` e `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] é um nome antigo para [!DNL Search].

   1. Especifique os segmentos para cada um dos destinos.

      Com o [!UICONTROL Automatically map all current and future segments] , todos os segmentos são mapeados e sincronizados diariamente.

      O [!UICONTROL Manually map segments] permite mapear manualmente os segmentos para sincronização com o destino do lote (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Nenhum segmento precisa ser mapeado manualmente para o destino HTTP.

1. Within [!DNL Search]ou o [!DNL Search] a equipe de implementação ou um usuário com a função de gerente de cliente de acesso direto deve iniciar a importação de [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Você precisará entrar no Experience Cloud da organização [!DNL Organization ID] ([!DNL IMS org ID]). A ID deve ser a mesma usada para a conta Audience Manager da organização.

### O que as alterações resultam em Audience Manager?

A organização verá dois [!DNL Search] Destinos no Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## Sincronização de dados

A importação inicial demora cerca de 24 horas. Após a importação inicial, os dados são sincronizados em tempo real, com um atraso de um a dois segundos.

<!--
### How DSP Syncs the Data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Adobe Advertising at [!DNL cm.eversttech.net]. Because Adobe Advertising is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html#global-device-ids), also called the [!DNL Device ID].
 
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)

### How Search Syncs the Data
-->

<!-- 
Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

  * The segment is targeted in an Adobe Advertising display ad.

  * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search]):

  * The segment is targeted in an Adobe Advertising search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## Onde encontrar os segmentos sincronizados

### Em DSP

Em DSP, os nomes de segmentos são organizados pela taxonomia de Audience Manager e estão disponíveis com as contagens de associação de segmento correspondentes em:

* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): No [!UICONTROL Adobe Segments] da guia [!UICONTROL Audience Targeting] seção.

* Em [configurações de público](/help/dsp/audiences/audience-settings.md): No [!UICONTROL Adobe Segments] guia .

### Na Advertising Creative

Em [!DNL Creative], os segmentos estão disponíveis nas configurações de experiência para nós do target.

### Em [!DNL Advertising Search]

No [!DNL [!DNL Search]], os segmentos estão disponíveis ao criar um [!DNL Google] público-alvo usando o [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; de [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Para cada [!DNL Google] público-alvo criado, [!DNL Google] O fornece o tamanho do público-alvo.

>[!MORELIKETHIS]
>
>* [Integrações de publicidade do Adobe com o Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

