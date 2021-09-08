---
title: Visão geral de [!DNL Analytics for Advertising Cloud]
description: Visão geral de [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Visão geral de [!DNL Analytics for Advertising Cloud]

*Anunciantes com Advertising Cloud DSP e Advertising Cloud Search*

[!DNL Analytics for Advertising Cloud] O integra o Adobe Analytics e o Adobe Advertising Cloud para estender e aprimorar os recursos de cada produto.

A integração permite que os anunciantes rastreiem as interações do site de click-through e view-through em suas [!DNL Analytics] instâncias, permitindo que as marcas vejam como o gasto de publicidade leva ao envolvimento do site e aos objetivos críticos dos negócios.

Além disso, o Advertising Cloud pode acessar os vastos dados primários que [!DNL Analytics] coleta usando tags [!DNL Analytics] já existentes no site. Isso permite um gerenciamento de jornadas mais robusto, remarketing próprio e relatórios de site de mídia paga. A Advertising Cloud pode usar ainda mais os dados [!DNL Analytics] para otimização de gastos e lances.

Quando usado corretamente, [!DNL Analytics for Advertising Cloud] esvazia as linhas entre duas funções tradicionais: gerenciamento de jornadas de publicidade (o ato de enviar usuários para o site por meio de anúncios) e entender o envolvimento do site por meio de análises da web.

Prestações primárias:

* Envie [!DNL Analytics] segmentos diretamente para o Advertising Cloud para remarketing de site próprio.
* Use [!DNL Analytics] eventos personalizados e padrão como sinais de conversão para otimizar a publicidade de mídia paga.
* Tire proveito do [!DNL Analytics] Analysis Workspace para entender melhor os pontos de entrada do site e o comportamento da visita.
* Habilite uma colaboração mais estreita entre analistas da Web e equipes de mídia paga.
* Use IDs de view-through e click-through persistentes do Advertising Cloud em [!DNL Analytics] para entender o envolvimento do site.
* Aprimore relatórios de mídia paga tradicionais no Analysis Workspace com métricas personalizadas, dimensões personalizadas e atividade do site que não podem ser obtidas ao exportar dados ou pixels para servidores de publicidade ou outros DSP.
* Aproveite o [!DNL Analytics] código já existente no seu site para rastreamento e otimização no Advertising Cloud.

>[!TIP]
>
> Assista a [introdução ao vídeo para [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Uso do Analytics para relatórios de mídia paga

[!DNL Analytics for Advertising Cloud] melhora os relatórios e informações sobre como sua publicidade direciona o comportamento do site, permitindo que você:

* Use IDs de view-through e click-through persistentes do Advertising Cloud em [!DNL Analytics] para entender o envolvimento do site.
* Tire proveito do Analysis Workspace para entender melhor os pontos de entrada do site e o comportamento da visita. Você pode acessar dados dimensionais de mídia e de evento pagos, que incluem nomes de entidades de campanha do Advertising Cloud (até disposições e anúncios) e suas métricas associadas, como cliques, impressões e custo.

Para usar [!DNL Analytics] como ferramenta de relatórios de mídia paga, sua organização precisa de um logon do Experience Cloud com acesso ao Analysis Workspace. Sua equipe do Advertising Cloud ajudará você a mapear os dados do Advertising Cloud para conjuntos de relatórios individuais no Analysis Workspace. É possível enviar dados do Advertising Cloud para qualquer conjunto de relatórios, mas você deve estar ciente dos conjuntos de relatórios que foram mapeados para o Advertising Cloud e aqueles que não foram mapeados. Dependendo do conjunto de relatórios, isso pode alterar os dados relatados.

[As Advertising Cloud IDs  [!DNL Analytics]](ids.md) no funcionam como outras eVars, com uma expiração persistente e personalizada. Por padrão, a janela de lookback de atribuição é definida como 60 dias durante a implementação do Advertising Cloud. Para alterar essa configuração, trabalhe com seu gerente de conta do Adobe.

As dimensões do Advertising Cloud são anexadas com o sufixo &quot;(ID do AMO)&quot; (como &quot;Tipo de anúncio (ID do AMO)&quot;). Consulte &quot;[Métricas do Advertising Cloud no Analysis Workspace](advertising-cloud-metrics-in-analytics.md)&quot; para obter uma lista das dimensões disponíveis.

>[!NOTE]
>
> Ao exibir dados do Advertising Cloud (ou qualquer conjunto de dados) em [!DNL Analytics], esteja ciente de que as métricas e os relatórios se baseiam nas regras definidas em [!DNL Analytics]. Os dados podem ser diferentes do que você vê em outros sistemas de relatórios, como relatórios do servidor de anúncios, relatórios [!DNL DSP] ou relatórios do mecanismo de pesquisa. Para entender as diferenças de dados em [!DNL Analytics], é necessário saber quando os dados do eVar expiram, o que define uma visita, o que é considerado atribuição de último toque versus atribuição persistente total e outros fatores. Para obter mais informações, consulte [Variações de dados esperadas entre [!DNL Analytics] e Advertising Cloud](data-variances.md).

## Uso do Analytics para potencializar campanhas e Portfolio do Advertising Cloud

Sem exigir pixels adicionais, [!DNL Analytics for Advertising Cloud] permite melhor otimização e segmentação mais fácil do público-alvo ao enviar dois sinais principais para a Advertising Cloud:

* Métricas de conversão a serem usadas como sinais de lance:
   * métricas padrão, como [!UICONTROL Revenue] e [!UICONTROL Cart Views].
   * métricas de envolvimento do site, como exibição de página e métricas de visita.
   * métricas de receita personalizadas.
   * métricas de receita reservada.
* Segmentos criados em [!DNL Analytics] e publicados no Experience Cloud.

   Você pode usar [!DNL Analytics] segmentos para o redirecionamento de site próprio em [!DNL DSP] e anúncios de pesquisa paga.

   (Somente Advertising Cloud Search) Os anunciantes com [!DNL Analytics], mas não o Audience Manager, também podem criar públicos-alvo baseados em tags do site do Google (listas de remarketing) e públicos-alvo de correspondência do cliente (listas de clientes) a partir de [!DNL Analytics] segmentos que são compartilhados com o Experience Cloud.

### Métricas de conversão do site como sinais de lance

Você pode usar os eventos padrão e personalizados de [!DNL Analytics] para criar objetivos ponderados no Advertising Cloud. Os objetivos informam as decisões de licitação dos seus [!DNL DSP] pacotes e dos portfólios de pesquisa.

>[!NOTE]
>
> Você não pode mapear métricas calculadas de [!DNL Analytics] para o Advertising Cloud.

Sua equipe do Advertising Cloud ajudará você a identificar e mapear os eventos aplicáveis ao desempenho de mídia paga para o Advertising Cloud, onde eles aparecerão em [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

Consulte &quot;[Métricas do Analytics no Advertising Cloud](analytics-data-in-advertising-cloud.md)&quot; para obter uma lista das métricas disponíveis.

### Segmentos do Analytics para redirecionamento de site

O Advertising Cloud pode assimilar [!DNL Analytics] segmentos para fins de remarketing para anúncios Advertising Cloud DSP e [!DNL Search] usando a integração Experience Cloud Audiences nativa entre [!DNL Analytics] e Experience Cloud.

Para acessar os segmentos [!DNL Analytics], uma conta de anunciante precisa ter o [Serviço de ID do Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) habilitado. Quando o Serviço de ID é ativado, todos os segmentos de Experience Cloud (incluindo segmentos criados em [!DNL Analytics] e publicados no Experience Cloud, segmentos criados no Adobe Audience Manager, segmentos criados no Experience Cloud usando o [!DNL People core service] e segmentos criados no Adobe Experience Platform e enviados para o Advertising Cloud via Audience Manager) ficam disponíveis no Advertising Cloud assim que são processados.

[!DNL Analytics] segmentos estão disponíveis em 24 horas e são atualizados diariamente.

Para obter mais informações sobre o serviço Experience Cloud Audiences, consulte [Experience Cloud Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Exemplos de como usar a integração

### Uso de dados do Advertising Cloud no Analysis Workspace

Para saber como usar seus dados do Advertising Cloud para criar relatórios visuais no Analysis Workspace, assista ao vídeo &quot;[Introdução ao Workspace e Relatórios](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html)&quot;.

### Criação de painéis do Advertising Cloud

Para saber como rastrear seus dados do Advertising Cloud em relação às suas metas no Analysis Workspace, assista ao vídeo &quot;[Create Advertising Cloud Dashboards with Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html)&quot;.

### Usar a Advertising Cloud ID para análise de entrada do site

Para ver como criar um relatório de entrada do site do Advertising Cloud para monitorar dia da semana, hora do dia, navegador e influências geográficas, consulte o vídeo &quot;[Criar relatórios de entrada do site do Advertising Cloud](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html)&quot;.

>[!MORELIKETHIS]
>
>* [Vídeo: Introdução ao [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [Pré-requisitos e informações-chave para implementação [!DNL Analytics for Advertising Cloud]](prerequisites.md)
>* [Advertising Cloud IDs usadas pelo Analytics](ids.md)
>* [Código JavaScript do Analytics para Advertising Cloud](/help/integrations/analytics/javascript.md)
>* [Variações de dados esperadas  [!DNL Analytics] entre o e o Advertising Cloud](data-variances.md)
>* [Métricas do Advertising Cloud no Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Dados no Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

