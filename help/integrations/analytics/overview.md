---
title: Visão geral da [!DNL Analytics for Advertising Cloud]
description: Visão geral da [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# Visão geral da [!DNL Analytics for Advertising Cloud]

*Anunciantes com Advertising Cloud DSP e Advertising Cloud Search*

[!DNL Analytics for Advertising Cloud] O integra o Adobe Analytics e o Adobe Advertising Cloud para estender e aprimorar os recursos de cada produto.

A integração permite que os anunciantes rastreiem as interações de click-through e view-through do site em seus [!DNL Analytics] , permitindo que as marcas vejam como o investimento em publicidade leva ao envolvimento do site e aos objetivos críticos de negócios.

Além disso, o Advertising Cloud pode acessar os grandes dados primários que [!DNL Analytics] coleta usando [!DNL Analytics] tags já no site. Isso permite um gerenciamento de jornadas mais robusto, remarketing próprio e relatórios de site de mídia paga. A Advertising Cloud pode usar ainda mais a variável [!DNL Analytics] dados para otimização de gastos e lances.

Quando devidamente utilizado, [!DNL Analytics for Advertising Cloud] borra as linhas entre duas funções tradicionais: gerenciamento de jornadas de publicidade (o ato de enviar usuários para o site por meio de anúncios) e entender o envolvimento do site por meio de análises da web.

Prestações primárias:

* Enviar [!DNL Analytics] segmentos diretamente no Advertising Cloud para remarketing de site próprio.
* Use [!DNL Analytics] eventos personalizados e padrão como sinais de conversão para otimizar a publicidade de mídia paga.
* Tire proveito de [!DNL Analytics] Analysis Workspace para entender melhor os pontos de entrada do site e o comportamento da visita.
* Habilite uma colaboração mais estreita entre analistas da Web e equipes de mídia paga.
* Usar IDs de view-through e click-through persistentes do Advertising Cloud em [!DNL Analytics] para entender a participação do site.
* Aprimore relatórios de mídia paga tradicionais no Analysis Workspace com métricas personalizadas, dimensões personalizadas e atividade do site que não podem ser obtidas ao exportar dados ou pixels para servidores de publicidade ou outros DSP.
* Tire proveito de [!DNL Analytics] O código já está no seu site para rastreamento e otimização no Advertising Cloud.

>[!TIP]
>
> Assista a [introdução ao vídeo [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Uso do Analytics para relatórios de mídia paga

[!DNL Analytics for Advertising Cloud] melhora os relatórios e informações sobre como sua publicidade direciona o comportamento do site, permitindo que você:

* Usar IDs de view-through e click-through persistentes do Advertising Cloud em [!DNL Analytics] para entender a participação do site.
* Tire proveito do Analysis Workspace para entender melhor os pontos de entrada do site e o comportamento da visita. Você pode acessar dados dimensionais de mídia e de evento pagos, que incluem nomes de entidades de campanha do Advertising Cloud (até disposições e anúncios) e suas métricas associadas, como cliques, impressões e custo.

Para usar [!DNL Analytics] como ferramenta de relatórios de mídia paga, sua organização precisa de um login do Experience Cloud com acesso ao Analysis Workspace. Sua equipe do Advertising Cloud ajudará você a mapear os dados do Advertising Cloud para conjuntos de relatórios individuais no Analysis Workspace. É possível enviar dados do Advertising Cloud para qualquer conjunto de relatórios, mas você deve estar ciente dos conjuntos de relatórios que foram mapeados para o Advertising Cloud e aqueles que não foram mapeados. Dependendo do conjunto de relatórios, isso pode alterar os dados relatados.

[Advertising Cloud IDs no [!DNL Analytics]](ids.md) funciona como outras eVars, com uma expiração persistente e personalizada. Por padrão, a janela de lookback de atribuição é definida como 60 dias durante a implementação do Advertising Cloud. Para alterar essa configuração, trabalhe com seu [!DNL Adobe] equipe da conta.

As dimensões do Advertising Cloud são anexadas com o sufixo &quot;(ID do AMO)&quot; (como &quot;Tipo de anúncio (ID do AMO)&quot;). Consulte &quot;[Métricas do Advertising Cloud no Analysis Workspace](advertising-cloud-metrics-in-analytics.md)&quot; para obter uma lista das dimensões disponíveis.

>[!NOTE]
>
> Ao exibir dados do Advertising Cloud (ou qualquer conjunto de dados) em [!DNL Analytics]esteja ciente de que as métricas e os relatórios se baseiam nas regras definidas no [!DNL Analytics]. Os dados podem ser diferentes do que você vê em outros sistemas de relatórios, como relatórios de servidor de anúncios, [!DNL DSP] ou relatórios do mecanismo de pesquisa. Para entender as diferenças de dados no [!DNL Analytics], é necessário saber quando os dados do eVar expiram, o que define uma visita, o que é considerado atribuição de último toque versus atribuição persistente total e outros fatores. Para obter mais informações, consulte [Variações de dados esperadas entre [!DNL Analytics] e Advertising Cloud](data-variances.md).

## Uso do Analytics para potencializar campanhas e Portfolio do Advertising Cloud

Sem exigir pixels adicionais, [!DNL Analytics for Advertising Cloud] permite melhor otimização e segmentação mais fácil do público-alvo, enviando dois sinais principais para o Advertising Cloud:

* Métricas de conversão a serem usadas como sinais de lance:
   * métricas padrão, como [!UICONTROL Revenue] e [!UICONTROL Cart Views].
   * métricas de envolvimento do site, como exibição de página e métricas de visita.
   * métricas de receita personalizadas.
   * métricas de receita reservada.
* Segmentos criados em [!DNL Analytics] e publicados no Experience Cloud.

   Você pode usar [!DNL Analytics] segmentos para redirecionamento de site próprio em [!DNL DSP] e anúncios de pesquisa pagos.

   (Somente para Advertising Cloud Search) Anunciantes com [!DNL Analytics] mas não o Audience Manager também pode criar públicos-alvo baseados em tags do site da Google (listas de remarketing) e públicos-alvo de correspondência do cliente (listas de clientes) de [!DNL Analytics] segmentos que são compartilhados com o Experience Cloud.

### Métricas de conversão do site como sinais de lance

Você pode usar os eventos padrão e personalizados de [!DNL Analytics] para criar objetivos ponderados no Advertising Cloud. Os objetivos informam as decisões de licitação para seus [!DNL DSP] pacotes e portfólios de pesquisa.

>[!NOTE]
>
> Não é possível mapear métricas calculadas do [!DNL Analytics] no Advertising Cloud.

Sua equipe do Advertising Cloud ajudará você a identificar e mapear os eventos aplicáveis ao desempenho de mídia paga para o Advertising Cloud, onde eles aparecerão em [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

Consulte &quot;[Métricas do Analytics no Advertising Cloud](analytics-data-in-advertising-cloud.md)&quot; para obter uma lista de métricas disponíveis.

### Segmentos do Analytics para redirecionamento de site

O Advertising Cloud pode assimilar [!DNL Analytics] segmentos para fins de remarketing para Advertising Cloud DSP e [!DNL Search] anúncios que usam a integração de Experience Cloud Audiences nativa entre [!DNL Analytics] e Experience Cloud.

Para acessar o [!DNL Analytics] segmentos, uma conta do anunciante precisa ter a variável [Serviço de ID de Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) habilitado. Quando o Serviço de ID estiver ativado, todos os segmentos de Experience Cloud (incluindo segmentos criados em [!DNL Analytics] e publicados no Experience Cloud, segmentos criados no Adobe Audience Manager, segmentos criados no Experience Cloud usando o [!DNL People core service]e os segmentos criados no Adobe Experience Platform e enviados para o Advertising Cloud via Audience Manager) ficam disponíveis no Advertising Cloud assim que são processados.

[!DNL Analytics] segmentos estão disponíveis em 24 horas e são atualizados diariamente.

Para obter mais informações sobre o serviço Experience Cloud Audiences, consulte [Públicos-alvo do Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Exemplos de como usar a integração

### Uso de dados do Advertising Cloud no Analysis Workspace

Para saber como você pode usar seus dados do Advertising Cloud para criar relatórios visuais no Analysis Workspace, assista ao vídeo &quot;[Introdução ao Workspace e Relatórios](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### Criação de painéis do Advertising Cloud

Para saber como rastrear os dados do Advertising Cloud em relação às metas no Analysis Workspace, assista ao vídeo &quot;[Criar painéis do Advertising Cloud com o Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Usar a Advertising Cloud ID para análise de entrada do site

Para ver como criar um relatório de entrada do site do Advertising Cloud para monitorar dia da semana, hora do dia, navegador e influências geográficas, consulte o vídeo &quot;[Criar relatórios de entrada do site da Advertising Cloud](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [Vídeo: Introdução ao [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [Pré-requisitos e informações-chave para implementação [!DNL Analytics for Advertising Cloud]](prerequisites.md)
>* [Advertising Cloud IDs usadas pelo Analytics](ids.md)
>* [Código JavaScript do Analytics para Advertising Cloud](/help/integrations/analytics/javascript.md)
>* [Variações de dados esperadas entre [!DNL Analytics] e Advertising Cloud](data-variances.md)
>* [Métricas do Advertising Cloud no Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Dados no Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

