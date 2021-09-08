---
title: Pré-requisitos e informações principais para implementar [!DNL Analytics for Advertising Cloud]
description: Pré-requisitos e informações principais para implementar [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Pré-requisitos e informações principais para implementar [!DNL Analytics for Advertising Cloud]

*Anunciantes com Advertising Cloud DSP e Advertising Cloud Search*

Analise as informações a seguir antes de integrar o Advertising Cloud com o Adobe Analytics.

## Requisitos para relatórios de dados do Advertising Cloud em [!DNL Analytics]

* Serviço de identidade do Experience Cloud: `visitorAPI.js` versão 2.0 ou superior
* Qualquer versão do Adobe Analytics (incluindo [!DNL Prime], [!DNL Premium] ou [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` versão 2.1 ou superior

>[!TIP]
>
>Para melhorar a fidelidade dos dados, use a versão mais recente do Experience Cloud Identity Service com suporte a CNAME, bem como a versão mais recente do Analytics AppMeasurement para JavaScript.

## Requisitos para compartilhar segmentos do Analytics com a Advertising Cloud

* Serviço de identidade do Experience Cloud: `visitorAPI.js` versão 2.1 ou superior
* Adobe Analytics: `!DNL appMeasurement.js` versão 1.8 ou superior

## Requisitos para relatórios de dados [!DNL Analytics] no Advertising Cloud

Forneça à equipe de implementação da Advertising Cloud o seguinte:

* A ID do conjunto de relatórios [!DNL Analytics] que será usada para relatórios sobre a atividade de mídia paga e para alimentar a atividade do site para otimização e relatórios no Advertising Cloud
* A ID da organização da Experience Cloud (ID da organização) da empresa.

Você pode encontrar ambas as IDs na tela [Summary do Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html).

![Tela Resumo do Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Dados no Advertising Cloud {#lookback-a4adc}

Como os dados [!DNL Analytics] são enviados ao Advertising Cloud para relatórios e otimização, eles estão sujeitos às regras de atribuição, incluindo as janelas de retrospectiva de impressão e clique, que são configuradas para o anunciante no Advertising Cloud.

![configurações da janela de pesquisa no nível do anunciante no Advertising Cloud](/help/integrations/assets/a4adc-lookbacks.png)

* Janela de retrospectiva de clique da atribuição do Advertising Cloud: O número de dias após o primeiro clique em que o clique pode ser atribuído a uma conversão. Por padrão, esse valor é de 60 dias; o máximo é 90 dias
* Janela de retrospectiva de impressão de atribuição do Advertising Cloud: O número de dias após uma impressão de anúncio em que a impressão pode ser atribuída a uma conversão. Por padrão, esse valor é de 14 dias; o máximo é 30 dias

   >[!NOTE]
   >
   > A janela de retrospectiva de impressão é específica do Advertising Cloud, não [!DNL Analytics for Advertising Cloud], do relatório.

O JavaScript [!DNL Analytics for Advertising Cloud] usa essas configurações para determinar até que ponto uma entrada view-through ou uma entrada click-through para o site é válida. Para obter mais informações sobre como view-throughs e click-throughs são determinados, consulte &quot;[Advertising Cloud IDs Usadas pelo Analytics](ids.md)&quot;.

## Dados do Advertising Cloud em [!DNL Analytics]

[!DNL Analytics] O define Advertising Cloud IDs (AMO IDs) na ocorrência do Analytics, sujeitas à configuração de persistência de eVar do anunciante, que se aplica a click-throughs e view-throughs. A configuração de persistência é configurada no back-end do Advertising Cloud e o gerente de conta do Adobe pode alterá-la.

* [!DNL Analytics for Advertising Cloud] Expiração do eVar: 60 dias por padrão para IDs do AMO

>[!NOTE]
>
>Para segmentar dados para um período diferente, você pode [configurar segmentos personalizados](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) com diferentes janelas de pesquisa no Analysis Workspace.

## Ambientes de anúncio compatíveis

* Pesquisar
* Exibir
* Vídeo
* Vídeo online
* Nativo

Entre em contato com o gerente de conta do Adobe para obter os ambientes de publicidade mais recentes com suporte em cada canal.

## O que você deve saber antes da implementação

* Nenhum custo adicional é cobrado por essa integração, nem chamadas de servidor resultam em tarifas adicionais [!DNL Analytics] ou do Advertising Cloud.

* [!DNL Analytics for Advertising Cloud] é independente do servidor de anúncios: um view-through ou click-through pode ocorrer de qualquer servidor de publicidade e as IDs adequadas são geradas na entrada do site.

* A integração transmite somente [!DNL Analytics] eventos padrão e personalizados para o Advertising Cloud para otimização de lances de mídia paga e esforços de publicidade subsequentes. Ele não transmite [!DNL Analytics] segmentos, métricas calculadas e eVars para o Advertising Cloud para otimização de lance.

* O Advertising Cloud cria IDs persistentes em [!DNL Analytics] com base no último anúncio clicado ou exibido antes do usuário entrar no site, com base nas [janelas de pesquisa de cliques e view-through](#lookback-a4adc) configuradas no Advertising Cloud. Se um visitante do site tiver ambos os tipos de interações de entrada do site em seu perfil e o clique estiver dentro do período de pesquisa, a ID de click-through do visitante substituirá a ID de view-through do relatório do site.

* [!DNL Analytics for Advertising Cloud] o rastreamento de conversão no Adobe Analytics usa uma janela de lookback de rastreamento configurável (60 dias por padrão). Os relatórios do Advertising Cloud refletem as conversões e o envolvimento do site até o final dessa janela de lookback de rastreamento.

* Todos os tipos de anúncios são suportados. No entanto, nem todos os ambientes de publicidade são compatíveis.

   Por exemplo, anúncios de TV conectados (CTV) não são rastreados porque nenhum clique ocorre na CTV e nenhuma conversão pode ocorrer no mesmo dispositivo. No entanto, se o anúncio for visualizado em um ambiente de desktop, alguns dados de view-through de entrada do site podem ser rastreados.

* [!DNL Analytics] no momento, as conversões são rastreadas e atribuídas somente a um visitante no mesmo dispositivo.

* [!DNL Analytics for Advertising Cloud] não suporta conversões de view-through no aplicativo.

* O rastreamento de view-through não é compatível com anunciantes que usam uma implementação de encaminhamento pelo lado do servidor de [!DNL Analytics].

### ID suplementar

Depois que o Serviço de identidade do Experience Cloud é implementado em um site, as ocorrências que contêm dados de [!DNL Analytics] ou Advertising Cloud contêm uma ID complementar.

Exemplo: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Para uma integração precisa de dados, todas as chamadas do Advertising Cloud usadas por uma atividade [!DNL Analytics for Advertising Cloud] para fornecer conteúdo ou registrar a métrica de meta devem ter uma ocorrência [!DNL Analytics] correspondente que compartilha a mesma ID adicional.

Ao solucionar problemas em [!DNL Analytics], confirme se a ID adicional está presente para ocorrências de [!DNL Analytics]. No [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html), você pode ver essa ID na guia Advertising Cloud como o parâmetro `sdid`.

>[!NOTE]
>
> Essa implementação funciona de forma semelhante à integração [!DNL Analytics for Target].

>[!MORELIKETHIS]
>
>* [Visão geral da [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Código JavaScript do Analytics para Advertising Cloud](/help/integrations/analytics/javascript.md)

