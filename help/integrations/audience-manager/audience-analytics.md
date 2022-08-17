---
title: '"[!DNL Adobe][!DNL Audience Analytics] para clientes da Advertising Cloud"'
description: Saiba como usar [!DNL Adobe][!DNL Audience Analytics] para casos de uso de publicidade
feature: Integration with Adobe Audience Manager
source-git-commit: d83e36847d0e14bc7e83106c0a221680060c2e58
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# [!DNL Adobe][!DNL Adobe] para clientes da Advertising Cloud

[[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) é uma integração entre o Adobe Audience Manager e a Adobe Analytics que permite que os clientes do Audience Manager enviem segmentos para o [!DNL Analytics] para obter insights enriquecidos sobre a atividade do site.

Os clientes da Advertising Cloud podem se beneficiar usando [!DNL Audience Analytics]. A integração permite:

* Envie dados de exposição da Advertising Cloud diretamente para o [!DNL Analytics] para determinar o impacto da atividade de funil superior na atividade downstream do site.

* Determine os canais de marketing e os pontos de entrada do site a partir dos anúncios de exposição de funil superior.

* Camar a integração com [!DNL Analytics for Advertising Cloud] para incorporar segmentos demográficos de terceiros da [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) com [!DNL Analytics for Advertising Cloud] para obter mais informações sobre perfis de usuário.

   [!DNL Audience Marketplace] O fornece acesso a feeds de dados de terceiros com modelos de assinatura &quot;Ativation&quot;, que permitem aos compradores enviar dados para um destino. Se os dados forem usados em um [!DNL Analytics] e as taxas de ativação não serão aplicadas.

* (Anunciantes com o Advertising Cloud DSP) Adicione segmentos de exposição adicionais para obter insights holísticos do gerenciamento de jornadas.

   O Advertising Cloud DSP pode enviar dados de exposição para o Audience Manager como sinais acionáveis por meio da implementação de pixels de rastreamento de impressões do Adobe Experience Platform ou do Audience Manager. Encaminhamento dos mesmos dados para [!DNL Analytics] permite análise de dados avançada. Consulte &quot;[Visão geral da integração de dados do Advertising Cloud Media com o Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; para obter mais informações.

Para obter mais informações sobre [!DNL Audience Analytics], incluindo os pré-requisitos e o fluxo de trabalho, consulte &quot;[Visão geral do Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## Exemplos de como usar [!DNL Audience Analytics] Dados com dados do Advertising Cloud

A seguir estão exemplos de como você pode usar os dados combinados no [!DNL Analytics] [!DNL Analysis Workspace].

### Veja o impacto da atividade de funil superior na atividade de downstream

Use segmentos de exposição de Audience Manager para ver o impacto da atividade do site de funil superior na atividade downstream do site. Inclua Advertising Cloud ou IDs de macro de terceiros em seus pixels de rastreamento para rastrear o impacto em um nível detalhado, do nível da campanha para o nível do site no qual o usuário foi exposto.

Principais benefícios:

* Acompanhe a exposição por tipos de funil/anúncio e use [!DNL Audience Analytics] para determinar as taxas de entrada e sobreposição com a próxima fase da jornada do cliente.

* Determine o impacto da atividade de funil superior na atividade downstream do site.

* Connect [!DNL Analytics for Advertising Cloud]<!-- which doesn't include the last exposure event --> e [!DNL Audience Analytics] dados <!-- (which includes the user's last exposure event) --> para determinar uma jornada holística do site.

A seguir estão exemplos de relatórios que você pode criar em [!DNL Analysis Workspace].

![Veja o impacto da atividade de funil superior na atividade downstream do site](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Use [!DNL Audience Analytics] Dados de segmento de terceiros para análise de perfil do usuário

Use segmentos de Audience Manager de terceiros para obter uma análise mais detalhada de como os usuários estão interagindo com seu site. Você pode usar as informações para determinar novos públicos-alvo de terceiros para os quais ativar a mídia, com base em como os perfis dos segmentos de terceiros se envolvem com indicadores-chave de desempenho para os sites das campanhas de mídia.

>[!TIP]
> Use o Audience Manager `Audiences ID` e `Audiences Name` dimensões [!DNL Analytics], como qualquer outra dimensão que [!DNL Analytics] coleta.

A seguir estão exemplos de relatórios que você pode criar em [!DNL Analysis Workspace].

![Usar segmentos de terceiros para enriquecer a análise de perfil do usuário](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Integrações do Advertising Cloud com o Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

