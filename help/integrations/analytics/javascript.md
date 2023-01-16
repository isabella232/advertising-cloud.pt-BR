---
title: Código JavaScript para [!DNL Analytics for Advertising]
description: Código JavaScript para [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# Código JavaScript para [!DNL Analytics for Advertising]

*Anunciantes apenas com uma integração Adobe Advertising-Adobe Analytics*

*Somente anunciantes com DSP publicitária*

Para DSP de publicidade, a variável [!DNL Analytics for Advertising] a integração acompanha as interações de view-through e click-through do site. As visitas de click-through são rastreadas pelo código padrão do Adobe Analytics nas suas páginas da Web; o [!DNL Analytics] O código captura os parâmetros AMO ID e EF ID no URL da página de aterrissagem e os rastreia em suas respectivas eVars reservadas. Você pode rastrear visitas de view-through implantando um trecho de JavaScript nas suas páginas da Web.

Na primeira exibição de página de uma visita ao site, o código JavaScript de publicidade do Adobe verifica se o visitante já viu ou clicou em um anúncio. Se o usuário tiver entrado no site anteriormente por meio de um click-through ou não tiver visto um anúncio, o visitante será ignorado. Se o visitante viu um anúncio e não entrou no site por meio de um click-through durante a [janela de retrospectiva de clique](/help/integrations/analytics/prerequisites.md#lookback-a4adc) definido em Adobe Advertising, em seguida, o código JavaScript de anúncio do Adobe (a) usa a variável [Serviço de ID de Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) para gerar uma ID complementar (`SDID`) ou b) usa a Adobe Experience Platform [!DNL Web SDK] `generateRandomID` para gerar um `[!DNL StitchID]`. Qualquer ID é usada para unir dados do Adobe Advertising à ocorrência do Adobe Analytics do visitante. A Adobe Analytics, então, consulta a Adobe Advertising para a AMO ID e a EF ID associadas à exposição do anúncio. A AMO ID e as EF IDs são preenchidas nas respectivas eVars. Esses valores persistem por um período designado (por padrão, 60 dias).

[!DNL Analytics] envia métricas de tráfego do site (como exibições de página, visitas e tempo gasto) e qualquer [!DNL Analytics] eventos personalizados ou padrão para Adobe Advertising por hora, usando a EF ID como chave. Esses [!DNL Analytics] As métricas são executadas pelo sistema de atribuição Adobe Advertising para conectar as conversões ao histórico de cliques e exposições.

>[!NOTE]
>
>A lógica de rastreamento do JavaScript de publicidade do Adobe ocorre no lado do Adobe e, portanto, praticamente não afeta o tempo de carregamento da página.
>
>Por outro lado, a lógica da variável [!DNL DCM] conector de dados para [!DNL Analytics] (usando [!DNL Google Campaign Manager 360]) para DSP de publicidade ocorre no lado do cliente. A costura do lado do cliente atrasa o carregamento da página e aumenta o risco de perda de dados. Isso ocorre porque a variável [!DNL Analytics] O JavaScript deve ser ping [!DNL DoubleClick] e esperar por [!DNL DoubleClick] para retornar os dados do último clique/impressão para [!DNL Analytics]. Quando o [!DNL DSP] equipe configura o [!DNL DCM] do conector de dados, você deve especificar por quanto tempo deseja atrasar a página.

## Implantação do código JavaScript

A biblioteca JavaScript consiste em duas linhas que permitem [!DNL Analytics] e Adobe Advertising para se comunicar entre si. Se a variável [!DNL Analytics for Advertising] A integração foi concluída durante a implementação do Adobe Advertising, então você já deve ter recebido esse código com instruções sobre como implantá-la.

### O código

#### Implementações que usam o serviço de identidade do Experience Cloud `visitorAPI.js` código

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

#### Implementações que usam o Experience Platform [!DNL Web SDK] `alloy.js`código

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

### Onde colocar o código

O [!DNL Analytics for Advertising] A função JavaScript deve vir após o Serviço de ID do Experience Cloud, mas antes do código de medição de aplicativo do Analytics, para que a ID adicional (`SDID`) ou `[!DNL StitchID]` pode ser incluído na sua chamada do Analytics.

![Inserção de código](/help/integrations/assets/a4adc-code-placement.png)

### Validando a implantação do código

Você pode executar a validação usando qualquer tipo de ferramenta de sniffer de pacote (como [!DNL Charles], [!DNL Fiddler]ou [!DNL Chrome Developer Tools]), comparando os valores das quatro IDs entre a solicitação que vai para a Adobe Advertising e a solicitação que vai para [!DNL Analytics], conforme descrito abaixo.

#### Como confirmar o código com [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Abrir [!DNL Chrome Developer Tools] e clique no botão **Rede** guia .

1. Carregar uma página de site que contenha a variável [!DNL Analytics for Advertising] JavaScript.

1. Filtre o [!UICONTROL Network] tab by `last` e revisar duas linhas:

   ![Filtragem na última](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * A primeira linha é a chamada para a biblioteca JavaScript e é intitulada `last-event-tag-latest.min.js`.
   * A segunda linha é a chamada que envia a solicitação para a Adobe Advertising. Começa da seguinte maneira: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Se você não vir a chamada para Adobe Advertising, talvez não seja a primeira exibição de página de sua visita. Para fins de teste, você pode remover o cookie para que a próxima chamada seja a primeira exibição de página para a visita correspondente:

      1. Na guia Aplicativo , localize a variável `adcloud` e verifique se o cookie contém `_les_v` (última visita) com um valor de `y` e um carimbo de data e hora da época UTC que expira em 30 minutos.
      1. Exclua o `ad cloud` e atualize a página.

1. (Implementações que usam o serviço de identidade do Experience Cloud) `visitorAPI.js` código) Filtrar em `/b/ss` para ver a ocorrência do Analytics.

   ![Filtragem em `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementações que usam o Experience Platform [!DNL Web SDK] `alloy.js`código) Filtrar em `/interact` para verificar se a carga da solicitação para a rede de borda contém `advertisingStitchID`.

   ![Filtragem em `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Compare os valores de ID entre as duas ocorrências. Todos os valores estarão nos parâmetros da string de consulta, exceto a ID do conjunto de relatórios na ocorrência do Analytics, que é o caminho do URL imediatamente após `/b/ss/`.

   | ID | Parâmetro do Analytics | Rede Edge | Parâmetro de publicidade Adobe |
   | --- | --- | --- | --- |
   | Org. Experience Cloud IMS | `mcorgid` |  | `_les_imsOrgid` |
   | ID de dados complementares | sdid |  | `_les_sdid` |
   | Identificação do título | stitchId | `advertisingStitchID` nos termos do `_adcloud` propriedade |  |
   | Conjunto de relatórios do Analytics | O valor após `/b/ss/` |  | `_les_rsid` |
   | ID de visitante Experience Cloud | mid |  | `_les_mid` |

   Se os valores de ID corresponderem, a implementação do JavaScript será confirmada. A Adobe Advertising enviará a variável [!DNL Analytics] qualquer servidor de rastreamento de click-through ou view-through, caso existam.

#### Como confirmar o código com [!DNL Adobe Experience Cloud Debugger]

1. Abra o [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) na sua página inicial.
1. Vá para o [!UICONTROL Network] guia .
1. No [!UICONTROL Solutions Filter] barra de ferramentas, clique em [!UICONTROL Adobe Advertising] e [!UICONTROL Analytics].
1. No [!UICONTROL Request URL – Hostname] linha de parâmetro, localizar `lasteventf-tm.everesttech.net`.
1. No [!UICONTROL Request – Parameters] , audite os sinais gerados, de modo semelhante à Etapa 3 em &quot;[Como confirmar o código com [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (Implementações que usam o serviço de identidade do Experience Cloud) `visitorAPI.js` código) Certifique-se de que a variável `Sdid` corresponde ao parâmetro `Supplemental Data ID` no filtro Adobe Analytics.
   * (Implementações que usam o Experience Platform [!DNL Web SDK] `alloy.js`código) Certifique-se de que o valor da variável `advertisingStitchID` corresponde ao parâmetro `Sdid` enviado para a rede Experience Platform Edge.
   * Se o código não estiver sendo gerado, verifique se o cookie Adobe Advertising foi removido no [!UICONTROL Application] guia . Depois de removido, atualize a página e repita o processo.

   ![Auditoria [!DNL Analytics for Advertising] Código JavaScript em [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Visão geral da [!DNL Analytics for Advertising]](overview.md)
>* [Pré-requisitos e informações-chave para implementação [!DNL Analytics for Advertising]](prerequisites.md)

