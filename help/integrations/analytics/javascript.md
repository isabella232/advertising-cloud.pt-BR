---
title: Código JavaScript para [!DNL Analytics for Advertising Cloud]
description: Código JavaScript para [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Código JavaScript para [!DNL Analytics for Advertising Cloud]

*Anunciantes somente com uma integração Advertising Cloud-Adobe Analytics*

*Anunciantes somente com o Advertising Cloud DSP*

Para o Advertising Cloud DSP, a integração [!DNL Analytics for Advertising Cloud] rastreia as interações de view-through e click-through do site. As visitas de click-through são rastreadas pelo código padrão do Adobe Analytics nas suas páginas da Web; o código [!DNL Analytics] captura os parâmetros da ID do AMO e da ID do EF no URL da página de aterrissagem e os rastreia em suas respectivas eVars reservadas. Você pode rastrear visitas de view-through implantando duas linhas de código JavaScript nas suas páginas da Web.

Na primeira exibição de página de uma visita ao site, o código JavaScript do Advertising Cloud verifica se o visitante já viu ou clicou em um anúncio. Se o usuário tiver entrado no site anteriormente por meio de um click-through ou não tiver visto um anúncio, o visitante será ignorado. Se o visitante tiver visto um anúncio e não tiver entrado no site por meio de um click-through durante o conjunto [click lookback window](/help/integrations/analytics/prerequisites.md#lookback-a4adc) no Advertising Cloud, o código JavaScript do Advertising Cloud usará o [Experience Cloud ID Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) para gerar uma ID adicional (`SDID`), que é usada para unir dados do Advertising Cloud à ocorrência do Adobe Analytics do visitante. A Adobe Analytics consulta a Advertising Cloud para a AMO ID e a EF ID associadas à exposição do anúncio. A AMO ID e as EF IDs são preenchidas nas respectivas eVars. Esses valores persistem por um período designado (por padrão, 60 dias).

[!DNL Analytics] envia métricas de tráfego do site (como exibições de página, visitas e tempo gasto) e qualquer evento  [!DNL Analytics]  personalizado ou padrão para a Advertising Cloud por hora, usando a EF ID como chave. Essas [!DNL Analytics] métricas são executadas pelo sistema de atribuição do Advertising Cloud para conectar as conversões ao histórico de cliques e exposições.

>[!NOTE]
>
>A lógica de rastreamento do JavaScript do Advertising Cloud ocorre no lado do Adobe e, portanto, praticamente não afeta o tempo de carregamento da página.
>
>Por outro lado, a lógica do conector de dados [!DNL DCM] para [!DNL Analytics] (usando [!DNL Google Campaign Manager 360]) para Advertising Cloud DSP ocorre no lado do cliente. A costura do lado do cliente atrasa o carregamento da página e aumenta o risco de perda de dados. Isso ocorre porque o [!DNL Analytics] JavaScript deve fazer ping [!DNL DoubleClick] e esperar [!DNL DoubleClick] para retornar os últimos dados de clique/impressão para [!DNL Analytics]. Quando sua equipe [!DNL DSP] configura o conector de dados [!DNL DCM], você deve especificar por quanto tempo está disposto a atrasar a página.

## Implantação do código JavaScript

A biblioteca do JavaScript consiste em duas linhas que permitem que [!DNL Analytics] e o Advertising Cloud se comuniquem entre si. Se a integração [!DNL Analytics for Advertising Cloud] foi concluída durante a implementação do Advertising Cloud, você deve ter recebido esse código com instruções sobre como implantá-la.

Se você ainda não tiver o código, entre em contato com a equipe de suporte da Advertising Cloud.

### Onde colocar o código

A função [!DNL Analytics for Advertising Cloud] do JavaScript deve vir após o Serviço de ID do Experience Cloud, mas antes do código de Medição de Aplicativo do Analytics para que a ID adicional (`SDID`) possa ser incluída na chamada do Analytics.

![Inserção de código](/help/integrations/assets/a4adc-code-placement.png)

### Validando a implantação do código

Você pode executar a validação usando qualquer tipo de ferramenta de sniffer de pacote (como [!DNL Charles], [!DNL Fiddler] ou [!DNL Chrome Developer Tools]) comparando os valores das quatro IDs entre a solicitação que vai para o Advertising Cloud e a solicitação que vai para [!DNL Analytics], conforme descrito abaixo.

#### Como confirmar o código com [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Abra [!DNL Chrome Developer Tools] e clique na guia **Rede**.
1. Carregue uma página do site que contenha o [!DNL Analytics for Advertising Cloud] JavaScript.
1. Filtre a guia [!UICONTROL Network] por `last` e revise duas linhas:

   ![Filtragem na última](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * A primeira linha é a chamada para a biblioteca do JavaScript e é intitulada `last-event-tag-latest.min.js`.
   * A segunda linha é a chamada que envia a solicitação para a Advertising Cloud. Começa da seguinte maneira: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Se você não vir a chamada para o Advertising Cloud, talvez não seja a primeira exibição de página de sua visita. Para fins de teste, você pode remover o cookie para que a próxima chamada seja a primeira exibição de página para a visita correspondente:

      1. Na guia Application , encontre o cookie `adcloud` e verifique se o cookie contém `_les_v` (última visita) com um valor de `y` e um carimbo de data e hora de época UTC que expira em 30 minutos.
      1. Exclua o cookie `ad cloud` e atualize a página.
1. Filtre em `/b/ss` para ver a ocorrência do Analytics.

   ![Filtragem em  `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. Compare os valores de ID entre as duas ocorrências. Todos os valores estarão nos parâmetros da string de consulta, exceto a ID do conjunto de relatórios na ocorrência do Analytics, que é o caminho do URL imediatamente após `/b/ss/`.

   | ID | Parâmetro do Analytics | Parâmetro Advertising Cloud |
   |--- |--- |--- |
   | Org. Experience Cloud IMS | `mcorgid` | `_les_imsOrgid` |
   | ID de dados complementares | sdid | `_les_sdid` |
   | Conjunto de relatórios do Analytics | O valor após `/b/ss/` | `_les_rsid` |
   | ID de visitante Experience Cloud | mid | `_les_mid` |

   Se os valores de ID corresponderem, a implementação do JavaScript será confirmada. O Advertising Cloud enviará ao servidor [!DNL Analytics] todos os detalhes de rastreamento de click-through ou view-through, se existirem.

#### Como confirmar o código com [!DNL Adobe Experience Cloud Debugger]

1. Abra o [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html) em sua página inicial.
1. Vá para a guia [!UICONTROL Network] .
1. Na barra de ferramentas [!UICONTROL Solutions Filter], clique em [!UICONTROL Advertising Cloud] e [!UICONTROL Analytics].
1. Na linha de parâmetro [!UICONTROL Request URL – Hostname], localize `lasteventf-tm.everesttech.net`.
1. Na linha [!UICONTROL Request – Parameters*] , faça a auditoria dos sinais gerados, de modo semelhante à Etapa 3 em &quot;[Como confirmar o código com [!DNL Chrome Developer Tools]](#validate-js-chrome)&quot;.
   * Verifique se o parâmetro `SDID` corresponde ao `Supplemental Data ID` no filtro Adobe Analytics.
   * Se o código não estiver sendo gerado, verifique se o cookie do Advertising Cloud foi removido na guia [!UICONTROL Application]. Depois de removido, atualize a página e repita o processo.

   ![Auditoria do código  [!DNL Analytics for Advertising Cloud] JavaScript em  [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Visão geral da [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Pré-requisitos e informações-chave para implementação [!DNL Analytics for Advertising Cloud]](prerequisites.md)

