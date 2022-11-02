---
title: Configurar testes A/B para anúncios Advertising Cloud DSP no Adobe Target
description: Saiba como configurar um teste A/B no [!DNL Target] para seus anúncios DSP.
source-git-commit: 465f3c18a7d85d54bca5ff2f565694a9b211a7ed
workflow-type: tm+mt
source-wordcount: '1660'
ht-degree: 0%

---

# Configurar testes A/B no Adobe Target para anúncios do Advertising Cloud DSP

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*Anunciantes somente com o Advertising Cloud DSP*

O Adobe Advertising Cloud DSP e o Adobe Target facilitam ainda mais para os profissionais de marketing fornecer uma experiência personalizada e conectada em mídia paga e mensagens no site. Ao compartilhar sinais entre os dois produtos, você pode:

* Diminua as taxas de queda do site ao vincular a exposição de anúncios de clientes de campanhas DSP a suas experiências no site.

* Estabeleça testes A/B espelhando experiências no site com mensagens publicitárias usando dados de exposição do Adobe Audience Manager e público-alvo de clique para feed.

* Meça o impacto das mensagens unificadas em um incentivo objetivo no site com visualizações simples no Adobe Analytics para [!DNL Target].

Consulte as seções a seguir para obter os pré-requisitos e instruções para configurar o rastreamento de click-through e view-through, implementar o compartilhamento de sinal entre DSP e [!DNL Target] e configure uma atividade de teste A/B e configure [!DNL Analytics] Analysis Workspace para exibir os dados de teste.

Em caso de dúvidas adicionais, entre em contato com adcloud_support@adobe.com.

## Pré-requisitos

Esse caso de uso requer os seguintes produtos e integrações:

* [!DNL Target]

* [[!DNL Analytics] para Advertising Cloud](/help/integrations/analytics/overview.md) integração<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] para [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integração

* Audience Manager (necessário somente para o teste de view-through)

## Etapa 1: Configurar a estrutura Click-through {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Estrutura de click-through](/help/integrations/assets/target-ct-framework.png)

Ao adicionar DSP macros a um URL de click-through (o URL exibido quando um usuário clica em um anúncio e atinge a página de aterrissagem), o DSP captura automaticamente a chave de posicionamento ao incluir ```${TM_PLACEMENT_ID}``` no URL de click-through. Essa macro captura a chave de posicionamento alfanumérico e não a ID de posicionamento numérica.

![URL de click-through anexado ao URL da página de aterrissagem](/help/integrations/assets/target-ct-url.jpg)

### Adicionar DSP macros aos URLs de click-through

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

No Flash ou Google Campaign Manager 360, atualize manualmente o URL de click-through para cada anúncio para incluir as macros necessárias para capturar variáveis de ID do AMO. As variáveis da ID do AMO são usadas para enviar dados de clique ao Adobe Analytics e compartilhar chaves de posicionamento para testes A/B. Consulte as seguintes páginas para obter instruções:

* [Anexar [!DNL Analytics for Advertising Cloud] Macros para [!DNL Flashtalking] Tags de anúncio](/help/integrations/analytics/macros-flashtalking.md)

* [Anexar [!DNL Analytics for Advertising Cloud] Macros para [!DNL Google Campaign Manager 360] Tags de anúncio](/help/integrations/analytics/macros-google-campaign-manager.md)

Entre em contato com a equipe de conta do DSP e o Grupo de soluções de publicidade (aac-advertising-solutions-group@adobe.com) para recuperar a chave de posicionamento necessária e finalizar a configuração, e para garantir que cada URL de click-through seja preenchido com a chave de posicionamento.

## Etapa 2: Configurar a estrutura de view-through usando o Audience Manager {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Estrutura de view-through](/help/integrations/assets/targetr-vt-framework.png)

Ao adicionar um pixel de evento de impressão de Audience Manager em suas tags de publicidade e configurações de posicionamento, você pode criar um segmento de teste para obter oportunidades adicionais de teste de view-through.

1. Implemente um pixel de evento de impressão de Audience Manager nas tags de anúncios e nas configurações de posicionamento DSP.

   Para obter instruções, consulte &quot;[Coletar dados de exposição de mídia das campanhas do Advertising Cloud DSP](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   Certifique-se de adicionar [DSP macros](/help/dsp/campaign-management/macros.md) para capturar todos os dados que você deseja que o pixel do evento de impressão retorne, incluindo `${TM_PLACEMENT_ID_NUM}` para a ID de disposição numérica.

   >[!NOTE]
   >
   >Os URLs de rastreamento de cliques incluem a variável `${TM_PLACEMENT_ID}` macro para a chave de posicionamento alfanumérico, em vez de `${TM_PLACEMENT_ID_NUM}` para a ID de disposição numérica.

1. Configure um segmento de Audience Manager a partir dos dados de impressão do DSP:

   1. Ir para **Audience Manager** > **Dados de público-alvo** > **Sinais** e selecione o **Pesquisar** na parte superior esquerda.

   1. Insira o **Chave** e **Valor** para o sinal que determina em qual nível os usuários do segmento são agrupados. Use um [chave com suporte](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=en) com um valor que corresponde a uma macro adicionada ao pixel do evento de impressão de Audience Manager.

      Por exemplo, para agrupar usuários para uma disposição específica, use a variável `d_placement` chave. Para o valor, use uma ID de posicionamento numérico real (como 2501853 na captura de tela acima) capturada pela macro de DSP `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

      Se o campo Contagem total mostrar contagens de usuários para o par de valores chave, o que indica que o pixel foi colocado corretamente e os dados estão fluindo, você poderá continuar para a próxima etapa.
   ![Sinais de pesquisa](/help/integrations/assets/target-am-signals.png)

1. [Criar uma característica com base em regras](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) para criação de segmentos no Audience Manager.

   1. Nomeie a característica para identificá-la facilmente nas atividades de teste. Armazene a característica na pasta que você preferir.

   1. No **Fonte de dados** , selecione **Ad Cloud**.

   1. No Construtor de expressões, adicione ```d_event``` no campo Chave e ```imp``` no **Valor** , selecione **Adicionar regra** e, em seguida, salve a característica.

   ![Captura de tela de uma característica com base em regras](/help/integrations/assets/target-am-trait.png)

1. Configure um segmento de teste no Audience Manager:

   1. Na parte superior da página, acesse **Dados de público-alvo** > **Características** e pesquise o nome completo da característica. Marque a caixa de seleção ao lado do nome da característica e clique em **Criar segmento**.

   1. Nomeie o segmento, selecione `Ad Cloud` como **Fonte de dados** e, em seguida, salve o segmento.

      O Audience Manager divide automaticamente o segmento em um grupo de controle que recebe a experiência padrão de página de aterrissagem e um grupo de teste que recebeu uma experiência personalizada no site.
   ![Captura de tela de um segmento de teste](/help/integrations/assets/target-am-segment.png)

## Etapa 3: Configurar uma atividade de &quot;Teste A/B&quot; no Target

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

As instruções a seguir destacam informações relacionadas ao caso de uso do DSP. Para obter instruções completas, consulte &quot;[Criar um teste A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html).&quot;

1. [Faça logon no Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. No **Atividades** listar, clique em **Criar atividade** > **Teste A/B**.

   ![Criar uma atividade de Teste A/B](/help/integrations/assets/target-create-ab.png)

1. No **Inserir URL da atividade*** , insira o URL da página de aterrissagem do teste.

   ![Inserir campo URL da atividade](/help/integrations/assets/target-create-ab-url.png)

   >[!NOTE]
   >
   >Você pode usar vários URLs para testar a entrada do site de view-through. Para obter mais informações, consulte &quot;[Atividade multipáginas](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; Você pode identificar facilmente as principais entradas por URL de página criando um [Relatório de entrada do site](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) no Analytics.

1. No **Meta** , insira a métrica de sucesso do teste.

   >[!NOTE]
   >
   >Certifique-se de que [!DNL Analytics] está habilitado como fonte de dados no [!DNL Target]e que o conjunto de relatórios correto está selecionado.

1. Defina as **Prioridade** para `High` ou `999` para evitar conflitos, quando os usuários do segmento de teste recebem uma experiência no site incorreta.

1. Within **Configurações da geração de relatórios**, selecione o **Nome da empresa** e **Conjunto de relatórios** conectada à sua conta DSP.

   Para obter dicas adicionais sobre relatórios, consulte &quot;[Relatório de práticas recomendadas e solução de problemas](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

1. No **Intervalo de datas** , insira as datas inicial e final apropriadas para o teste.

1. Adicione públicos à atividade:

   1. Escolha a [segmento criado anteriormente no Audience Manager para testar públicos-alvo de view-through](#view-through-framework).

      ![Adicionar públicos à atividade](/help/integrations/assets/target-create-ab-audiences.png)

   1. Selecionar **Páginas do site** > **Página de aterrissagem** > **Query** e insira a tecla de posicionamento DSP no **Valor** para usar os parâmetros da cadeia de caracteres de consulta do Target para públicos-alvo de click-through.

      ![Captura de tela de um público-alvo de clique](/help/integrations/assets/target-click-audience.jpg)

1. Para o **Método de alocação de tráfego**, selecione **Manual (Padrão)** e divida o público-alvo 50/50.

1. Salve a atividade.

1. Use [!DNL Target] [Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) para fazer alterações de design no modelo da landing page de teste A/B.

   * Experiência A: Não edite porque é a experiência padrão/de controle da página de aterrissagem sem personalização.

   * Experiência B: Use o [!DNL Target] interface do usuário para personalizar o modelo de página de aterrissagem com base nos ativos incluídos no teste (como títulos, cópia, posicionamento de botões e criações).
   >[!NOTE]
   >
   >Por exemplo, casos de uso de testes criativos para testes criativos, entre em contato com a equipe de conta.

## Etapa 4: Configure seu [!DNL Analytics for Target] Analysis Workspace em [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) é uma integração entre soluções que permite aos anunciantes criar [!DNL Target] com base em [!DNL Analytics] métricas de conversão e segmentos de público-alvo e, em seguida, meça os resultados usando [!DNL Analytics] como fonte de relatórios. Todos os relatórios e segmentações dessa atividade são baseados em [!DNL Analytics] coleta de dados.

Para obter mais informações sobre [!DNL Analytics for Target], incluindo um link para instruções de implementação, consulte[Adobe Analytics como origem de relatório do Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Configure o [!DNL Analytics for Target] Painel

No Analysis Workspace, configure a variável [!DNL Analytics for Target panel] para analisar sua [!DNL Target] atividades e experiências. Lembre-se dos seguintes pontos importantes e informações sobre seus relatórios.

#### Métricas

* Crie um painel dentro do espaço de trabalho específico para a campanha, pacote ou disposição do Advertising Cloud para o qual o teste foi executado. Use as visualizações de resumo para mostrar as métricas do Advertising Cloud no mesmo relatório que o desempenho do teste do Target.

* Priorize o uso de métricas no site (como visitas e conversões) para medir o desempenho.

* Entenda que as métricas de mídia agregada do Advertising Cloud (como impressões, cliques e custos) não podem corresponder às métricas do Target.

#### Dimension

As seguintes dimensões pertencem a [!DNL Analytics for Target]:

* **Atividades do Target**: Nome do teste A/B

* **Experiências do Target**: Nomes das experiências de página de aterrissagem usadas na atividade

* **Atividade do Target** > **Experiência**: O nome da atividade e da experiência na mesma linha

### Solução de problemas do Analytics para [!DNL Target] Dados

No Analysis Workspace, se você observar que os dados de atividade e experiências são mínimos ou não estão sendo preenchidos, faça o seguinte:

* Verifique se a mesma ID de dados complementares (SDID) é usada para o Target e o Analytics. Você pode verificar os valores de SDID usando o [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) na página de aterrissagem para a qual a campanha está direcionando os usuários.

[Valores de ID de dados complementares (SDID) no Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Na mesma página de aterrissagem, verifique se a) o Nome do host mostrado no Adobe Debugger em Soluções> Target corresponde a b) o Servidor de rastreamento mostrado em [!DNL Target] para a atividade (em Metas e configurações > Configurações da geração de relatórios).

   [!DNL Analytics For Target] exige um [!DNL Analytics] servidor de rastreamento a ser enviado em chamadas de [!DNL Target] para [!DNL Modstats] servidor de coleta de dados do Analytics.&lt;!— apenas &quot;para o Analytics?&quot;>

[Valor do nome do host no Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valor do servidor de rastreamento no Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Leitura adicional

* [Integração do Target ao Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html)- Explica como configurar relatórios do Target no Analysis Workspace.
* [Visão geral do teste A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Descreve atividades de teste A/B, que podem ser usadas com anúncios de DSP.
* [Experiências e ofertas](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Explicações [!DNL Target] ferramentas para determinar o conteúdo no site ao qual DSP usuários de teste são expostos.
* [Sinais, características e segmentos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - Define algumas das ferramentas do Audience Manager que podem ajudar com DSP teste de view-through.
* [Visão geral do Analytics para Advertising Cloud](https://experienceleague.adobe.com/docs/advertising-cloud/integrations/analytics/overview.html) - Apresenta o Analytics for Advertising Cloud, que permite rastrear as interações de click-through e view-through do site nas instâncias do Analytics.

<!-- 
>[!MORELIKETHIS]
>
>* 
-->