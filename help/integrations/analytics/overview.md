---
title: Visão geral da [!DNL Analytics for Advertising]
description: Visão geral da [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 0%

---

# Visão geral da [!DNL Analytics for Advertising]

*Anunciantes com DSP de publicidade e[!DNL Advertising Search]*

[!DNL Analytics for Advertising] O integra Adobe Analytics e Adobe Advertising para estender e aprimorar os recursos de cada produto.

A integração permite que os anunciantes rastreiem as interações de click-through e view-through do site em seus [!DNL Analytics] , permitindo que as marcas vejam como o investimento em publicidade leva ao envolvimento do site e aos objetivos críticos de negócios.

Além disso, a Adobe Advertising pode acessar os vastos dados primários que [!DNL Analytics] coleta usando [!DNL Analytics] tags já no site. Isso permite um gerenciamento de jornadas mais robusto, remarketing próprio e relatórios de site de mídia paga. A publicidade do Adobe pode usar ainda mais a variável [!DNL Analytics] dados para otimização de gastos e lances.

Quando devidamente utilizado, [!DNL Analytics for Advertising] borra as linhas entre duas funções tradicionais: gerenciamento de jornadas de publicidade (o ato de enviar usuários para o site por meio de anúncios) e entender o envolvimento do site por meio de análises da web.

Prestações primárias:

* Enviar [!DNL Analytics] segmentos diretamente para Adobe Advertising para remarketing de site próprio.
* Use [!DNL Analytics] eventos personalizados e padrão como sinais de conversão para otimizar a publicidade de mídia paga.
* Tire proveito de [!DNL Analytics] Analysis Workspace para entender melhor os pontos de entrada do site e o comportamento da visita.
* Habilite uma colaboração mais estreita entre analistas da Web e equipes de mídia paga.
* Usar IDs de view-through e click-through persistentes do Adobe Advertising no [!DNL Analytics] para entender a participação do site.
* Aprimore relatórios de mídia paga tradicionais no Analysis Workspace com métricas personalizadas, dimensões personalizadas e atividade do site que não podem ser obtidas ao exportar dados ou pixels para servidores de publicidade ou outros DSP.
* Tire proveito de [!DNL Analytics] O código já está no seu site para rastreamento e otimização dentro do Adobe Advertising.

>[!TIP]
>
> Assista a [introdução ao vídeo [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Uso do Analytics para relatórios de mídia paga

[!DNL Analytics for Advertising] melhora os relatórios e informações sobre como sua publicidade direciona o comportamento do site, permitindo que você:

* Usar IDs de view-through e click-through persistentes do Adobe Advertising no [!DNL Analytics] para entender a participação do site.
* Tire proveito do Analysis Workspace para entender melhor os pontos de entrada do site e o comportamento da visita. Você pode acessar dados dimensionais de mídia e de evento pagos, que incluem nomes de entidade de campanha Adobe Advertising (até disposições e anúncios) e suas métricas associadas, como cliques, impressões e custo.

Para usar [!DNL Analytics] como ferramenta de relatórios de mídia paga, sua organização precisa de um login do Experience Cloud com acesso ao Analysis Workspace. Sua equipe de publicidade do Adobe ajudará você a mapear os dados de publicidade do Adobe para conjuntos de relatórios individuais no Analysis Workspace. É possível enviar dados de publicidade do Adobe para qualquer conjunto de relatórios, mas você deve estar ciente dos conjuntos de relatórios que foram mapeados para publicidade do Adobe e aqueles que não foram mapeados. Dependendo do conjunto de relatórios, isso pode alterar os dados relatados.

[IDs de publicidade do Adobe em [!DNL Analytics]](ids.md) funciona como outras eVars, com uma expiração persistente e personalizada. Por padrão, a janela de lookback de atribuição é definida como 60 dias durante a implementação do Adobe Advertising. Para alterar essa configuração, trabalhe com seu [!DNL Adobe] equipe da conta.

As dimensões de Adobe Advertising são anexadas com o sufixo &quot;(ID do AMO)&quot; (como &quot;Tipo de anúncio (ID do AMO)&quot;). Consulte &quot;[Métricas de publicidade do Adobe no Analysis Workspace](advertising-metrics-in-analytics.md)&quot; para obter uma lista das dimensões disponíveis.

>[!NOTE]
>
> Ao exibir dados de Adobe Advertising (ou qualquer conjunto de dados) em [!DNL Analytics]esteja ciente de que as métricas e os relatórios se baseiam nas regras definidas no [!DNL Analytics]. Os dados podem ser diferentes do que você vê em outros sistemas de relatórios, como relatórios de servidor de anúncios, [!DNL DSP] ou relatórios do mecanismo de pesquisa. Para entender as diferenças de dados no [!DNL Analytics], é necessário saber quando os dados do eVar expiram, o que define uma visita, o que é considerado atribuição de último toque versus atribuição persistente total e outros fatores. Para obter mais informações, consulte [Variações de dados esperadas entre [!DNL Analytics] e publicidade Adobe](data-variances.md).

## Uso do Analytics para potencializar campanhas e Portfolio publicitárias do Adobe

Sem exigir pixels adicionais, [!DNL Analytics for Advertising] permite melhor otimização e segmentação mais fácil do público-alvo, enviando dois sinais principais para o Adobe Advertising:

* Métricas de conversão a serem usadas como sinais de lance:
   * métricas padrão, como [!UICONTROL Revenue] e [!UICONTROL Cart Views].
   * métricas de envolvimento do site, como exibição de página e métricas de visita.
   * métricas de receita personalizadas.
   * métricas de receita reservada.
* Segmentos criados em [!DNL Analytics] e publicados no Experience Cloud.

   Você pode usar [!DNL Analytics] segmentos para redirecionamento de site próprio em [!DNL DSP] e anúncios de pesquisa pagos.

   ([!DNL Search] somente) Anunciantes com [!DNL Analytics] mas não o Audience Manager também pode criar públicos-alvo baseados em tags do site da Google (listas de remarketing) e públicos-alvo de correspondência do cliente (listas de clientes) de [!DNL Analytics] segmentos que são compartilhados com o Experience Cloud.

### Métricas de conversão do site como sinais de lance

Você pode usar os eventos padrão e personalizados de [!DNL Analytics] para criar objetivos ponderados na Adobe Advertising. Os objetivos informam as decisões de licitação para seus [!DNL DSP] pacotes e portfólios de pesquisa.

>[!NOTE]
>
> Não é possível mapear métricas calculadas do [!DNL Analytics] em Adobe Advertising.

Sua equipe de Adobe Advertising ajudará você a identificar e mapear os eventos aplicáveis ao desempenho da mídia paga para a Adobe Advertising, onde eles aparecerão em [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

Consulte &quot;[Métricas do Analytics na publicidade do Adobe](analytics-data-in-advertising.md)&quot; para obter uma lista de métricas disponíveis.

### Segmentos do Analytics para redirecionamento de site

A publicidade do Adobe pode assimilar [!DNL Analytics] segmentos para fins de remarketing para DSP de publicidade e [!DNL Search] anúncios que usam a integração de Experience Cloud Audiences nativa entre [!DNL Analytics] e Experience Cloud.

Para acessar o [!DNL Analytics] segmentos, uma conta do anunciante precisa ter a variável [Serviço de ID de Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) habilitado. Quando o Serviço de ID estiver ativado, todos os segmentos de Experience Cloud (incluindo segmentos criados em [!DNL Analytics] e publicados no Experience Cloud, segmentos criados no Adobe Audience Manager, segmentos criados no Experience Cloud usando o [!DNL People core service]e os segmentos criados no Adobe Experience Platform e enviados para o Adobe Advertising via Audience Manager) tornam-se disponíveis no Adobe Advertising assim que são processados.

[!DNL Analytics] segmentos estão disponíveis em 24 horas e são atualizados diariamente.

Para obter mais informações sobre o serviço Experience Cloud Audiences, consulte [Públicos-alvo do Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Exemplos de como usar a integração

### Uso de dados de publicidade do Adobe no Analysis Workspace

Para saber como você pode usar seus dados de publicidade do Adobe para criar relatórios visuais no Analysis Workspace, assista ao vídeo &quot;[Introdução ao Workspace e Relatórios](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### Criação de painéis de publicidade do Adobe

Para saber como rastrear seus dados de Adobe Advertising em relação às suas metas no Analysis Workspace, assista ao vídeo &quot;[Criar Painéis de publicidade do Adobe com o Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Uso da ID de publicidade do Adobe para análise de entrada do site

Para ver como criar um relatório de entrada do site de publicidade do Adobe para monitorar dia da semana, hora do dia, navegador e influências geográficas, consulte o vídeo &quot;[Criar relatórios de entrada de site de publicidade do Adobe](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [Vídeo: Introdução ao [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [Pré-requisitos e informações-chave para implementação [!DNL Analytics for Advertising]](prerequisites.md)
>* [IDs de publicidade do Adobe usadas pelo Analytics](ids.md)
>* [Código JavaScript para Analytics para publicidade](/help/integrations/analytics/javascript.md)
>* [Variações de dados esperadas entre [!DNL Analytics] e publicidade Adobe](data-variances.md)
>* [Métricas de publicidade do Adobe no Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Dados na publicidade do Adobe](/help/integrations/analytics/analytics-data-in-advertising.md)

