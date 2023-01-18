---
title: Pré-requisitos e informações-chave para implementação [!DNL Analytics for Advertising]
description: Pré-requisitos e informações-chave para implementação [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Pré-requisitos e informações-chave para implementação [!DNL Analytics for Advertising]

*Anunciantes com DSP de publicidade e[!DNL Advertising Search]*

Analise as informações a seguir antes de integrar a publicidade Adobe com o Adobe Analytics.

## Requisitos para relatórios de dados de publicidade do Adobe em [!DNL Analytics]

* Uma das seguintes opções:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Serviço de identidade do Experience Cloud: `visitorAPI.js` versão 2.0 ou superior
* Qualquer versão do Adobe Analytics (incluindo [!DNL Prime], [!DNL Premium]ou [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` versão 2.1 ou superior

>[!TIP]
>
>Para melhorar a fidelidade dos dados, use a versão mais recente de cada biblioteca.

## Requisitos para compartilhar segmentos do Analytics com a publicidade do Adobe

* Serviço de identidade do Experience Cloud: `visitorAPI.js` versão 2.1 ou superior
* Adobe Analytics: `!DNL appMeasurement.js` versão 1.8 ou superior

## Requisitos para a apresentação de relatórios [!DNL Analytics] Dados na publicidade do Adobe

Forneça à equipe de implementação Adobe Advertising o seguinte:

* O [!DNL Analytics] a ID do conjunto de relatórios que será usada para relatórios sobre a atividade de mídia paga e para alimentar a atividade do site para otimização e relatórios na Adobe Advertising
* A ID da organização da Experience Cloud (ID da organização) da empresa.

Você pode encontrar ambas as IDs no [Guia Resumo do Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Tela Resumo do Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Dados na publicidade do Adobe {#lookback-a4adc}

Porque [!DNL Analytics] Os dados são enviados ao Adobe Advertising para relatórios e otimização, eles estão sujeitos às regras de atribuição, incluindo as janelas de pesquisa de impressão e cliques, que são configuradas para o anunciante no Adobe Advertising.

![configurações da janela de pesquisa no nível do anunciante no Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Janela de pesquisa de clique de atribuição de anúncio do Adobe: O número de dias após o primeiro clique em que o clique pode ser atribuído a uma conversão. Por padrão, esse valor é de 60 dias; o máximo é 90 dias
* Janela de retrospectiva de impressão de atribuição de Adobe Advertising: O número de dias após uma impressão de anúncio em que a impressão pode ser atribuída a uma conversão. Por padrão, esse valor é de 14 dias; o máximo é 30 dias

   >[!NOTE]
   >
   > A janela de retrospectiva de impressão é específica do Adobe Advertising, não [!DNL Analytics for Advertising], relatórios.

O [!DNL Analytics for Advertising] O JavaScript usa essas configurações para determinar até que ponto uma entrada view-through ou uma entrada click-through para o site é válida. Para obter mais informações sobre como os view-throughs e click-throughs são determinados, consulte &quot;[IDs de publicidade do Adobe usadas pelo Analytics](ids.md).&quot;

## Dados de publicidade do Adobe em [!DNL Analytics]

[!DNL Analytics] define IDs de publicidade do Adobe (AMO IDs) na ocorrência do Analytics, sujeitas à configuração de persistência de eVar do anunciante, que se aplica a click-throughs e view-throughs. A configuração de persistência é configurada no back-end do Adobe Advertising e sua [!DNL Adobe] a equipe de conta pode alterá-la.

* [!DNL Analytics for Advertising] Expiração do eVar: 60 dias por padrão para IDs do AMO

>[!NOTE]
>
>Para segmentar dados para um período diferente, é possível [configurar segmentos personalizados](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) com janelas de pesquisa diferentes no Analysis Workspace.

## Ambientes de anúncio compatíveis

* Pesquisar
* Exibir
* Vídeo
* Vídeo online
* Nativo

Entre em contato com seu [!DNL Adobe] equipe da conta para obter os ambientes de anúncios compatíveis mais recentes em cada canal.

## O que você deve saber antes da implementação

* A equipe de implementação Adobe Advertising irá configurar a integração.

* Nenhum custo adicional é cobrado por essa integração, nem chamadas de servidor resultam em outros [!DNL Analytics] ou Adobe Advertising.

* [!DNL Analytics for Advertising] é independente do servidor de anúncios: um view-through ou click-through pode ocorrer de qualquer servidor de publicidade e as IDs adequadas são geradas na entrada do site.

* A integração passa somente [!DNL Analytics] eventos padrão e personalizados para Adobe Advertising para otimização de lances de mídia paga e esforços de publicidade subsequentes. Não passa [!DNL Analytics] segmentos, métricas calculadas e eVars para Adobe Advertising para otimização de lances.

* A publicidade Adobe cria IDs persistentes no [!DNL Analytics] com base no último anúncio clicado ou visualizado antes do usuário entrar no site, com base no [janelas de pesquisa de cliques e view-through](#lookback-a4adc) configurado em Adobe Advertising. Se um visitante do site tiver ambos os tipos de interações de entrada do site em seu perfil e o clique estiver dentro do período de pesquisa, a ID de click-through do visitante substituirá a ID de view-through do relatório do site.

* [!DNL Analytics for Advertising] o rastreamento de conversão no Adobe Analytics usa uma janela de lookback de rastreamento configurável (60 dias por padrão). Os relatórios de Adobe Advertising refletem conversões de site e envolvimento ao final desta janela de lookback de rastreamento.

* Todos os tipos de anúncios são suportados. No entanto, nem todos os ambientes de publicidade são compatíveis.

   Por exemplo, anúncios de TV conectados (CTV) não são rastreados porque nenhum clique ocorre na CTV e nenhuma conversão pode ocorrer no mesmo dispositivo. No entanto, se o anúncio for visualizado em um ambiente de desktop, alguns dados de view-through de entrada do site podem ser rastreados.

* [!DNL Analytics] no momento, as conversões são rastreadas e atribuídas somente a um visitante no mesmo dispositivo.

* [!DNL Analytics for Advertising] não suporta conversões de view-through no aplicativo.

* O rastreamento de view-through não é compatível com anunciantes que usam uma implementação de encaminhamento pelo lado do servidor de [!DNL Analytics].

### ID suplementar

Depois que o serviço de identidade do Experience Cloud é implementado para um site, as ocorrências que contêm dados de [!DNL Analytics] ou Adobe Advertising contém uma ID complementar.

Exemplo: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Para obter uma integração precisa de dados, todas as chamadas de Adobe Advertising usadas por um [!DNL Analytics for Advertising] atividade para fornecer conteúdo ou registrar a métrica de meta deve ter uma [!DNL Analytics] ocorrência que compartilha a mesma ID complementar.

Quando você estiver solucionando problemas no [!DNL Analytics]confirme se a ID adicional está presente para [!DNL Analytics] ocorrências. No [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html), você pode ver essa ID na guia Adobe Advertising como a variável `sdid` parâmetro.

>[!NOTE]
>
> Essa implementação funciona de forma semelhante à [!DNL Analytics for Target] integração.

>[!MORELIKETHIS]
>
>* [Visão geral da [!DNL Analytics for Advertising]](overview.md)
>* [Código JavaScript para Analytics para publicidade](/help/integrations/analytics/javascript.md)

