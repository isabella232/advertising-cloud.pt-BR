---
title: Sobre relatórios na plataforma
description: Saiba mais sobre os dados do relatório incluídos nas visualizações de gerenciamento de campanha.
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: b2393d5e66ba5d3d2dc9816825c05eda076eaad1
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Sobre relatórios na plataforma

<!-- rename "About Performance Reports in Campaign Management Views?" -->
As exibições de gerenciamento de campanha incluem dados abrangentes do relatório. Os relatórios disponíveis ajudam a identificar os pacotes e disposições que estão funcionando bem e aqueles que precisam de sua atenção. Os botões de ação rápida também tornam você mais produtivo.

## Lista de todas as campanhas

O [!UICONTROL Campaigns] a visualização é aberta para uma lista de todas as campanhas dentro da sua conta. O [!UICONTROL Subtotals] mostra a soma ou o valor médio de cada métrica em todas as linhas visíveis.

![Lista de campanhas](/help/dsp/assets/campaigns-list.png)

Por padrão, cada linha de campanha inclui métricas de ritmo e delivery. As métricas de empacotamento incluem [!UICONTROL Gross Spend (Lifetime)], que inclui um indicador do gasto real no target versus o gasto esperado no target em todos os pacotes da campanha, para que você possa identificar campanhas com baixo desempenho imediatamente. Opcionalmente, é possível [alterar a exibição de coluna](column-view-change.md) ou mesmo [criar uma exibição de coluna personalizada](column-view-create.md).

Você pode [personalizar as tabelas de dados](campaign-data-views-about.md) de formas adicionais e [filtrar os dados visíveis](campaign-data-filter.md).

Para visualizar uma campanha com mais detalhes, clique no nome da campanha.

## Relatório de campanha única {#single-campaign-reporting}

Em uma campanha, você pode filtrar dados com base na entidade da campanha: [!UICONTROL Packages], [!UICONTROL Placements]e [!UICONTROL Ads]. Você pode [filtrar os dados visíveis](campaign-data-filter.md) para incluir apenas os pacotes, disposições ou anúncios que você deseja visualizar.

![Guias da entidade da campanha](/help/dsp/assets/campaign-subtabs.png)

Em cada guia de entidade, cada linha inclui as métricas de ritmo e delivery, por padrão, mas é possível [alterar a exibição de coluna](column-view-change.md) ou mesmo [criar uma exibição de coluna personalizada](column-view-create.md) para aplicar em todas as sub-guias da campanha. Você pode [personalizar as tabelas de dados](campaign-data-views-about.md) de outras maneiras. Cada tabela de dados inclui uma [!UICONTROL Subtotals] linha , que mostra a soma ou o valor médio de cada métrica em todas as linhas visíveis.

Para cada campanha, você também pode personalizar gráficos de tendências de séries de tempo com três métricas, que estão disponíveis em cada exibição de entidade. Por padrão, os dados de [!UICONTROL Net Spend], [!UICONTROL Impressions]e [!UICONTROL Net CPM] são incluídos em gráficos separados (gráficos de lista). Como opção, você pode alterar as métricas.

![gráficos de tendências separados para três métricas](/help/dsp/assets/trend-chart-separate.png)

Como opção, também é possível sobrepor as três métricas para fácil detecção de anomalias e áreas nas quais você pode melhorar a escala ou o desempenho.

![gráfico de tendências com sobreposição](/help/dsp/assets/trend-chart.png)

Você pode [personalizar os gráficos de tendências](campaign-data-visualization-manage.md) por campanha e as mesmas métricas são persistentes em todos os gráficos de tendências da campanha.

### Inspetor de posicionamento

Para cada disposição, você pode [abrir uma (exibição detalhada) [!UICONTROL Inspector])](placement-details-view.md), que inclui os seguintes dados detalhados:

* **[!UICONTROL Sites]:** Todos os sites nos quais a disposição foi impressa.

   O [!UICONTROL Sites] A guia inclui recursos de pesquisa e filtro, as mesmas opções padrão e personalizadas de exibição de coluna que estão disponíveis na página principal e uma [!UICONTROL Exclude] em cada linha, para que seja possível excluir rapidamente um site da disposição.

* **[!UICONTROL Ads]:** Todos os anúncios no posicionamento.

   O [!UICONTROL Ads] A guia inclui recursos de pesquisa e filtro, as mesmas opções padrão e personalizadas de exibição de coluna que estão disponíveis na página principal e botões de ação rápida em cada linha, como [!UICONTROL Pause] (para que você possa pausar um anúncio rapidamente).

* **[!UICONTROL Frequency]:** Dados para cada nível de frequência de anúncio para o posicionamento, incluindo:
   * o nível de frequência do anúncio (como &quot;1&quot; para todas as instâncias em que os usuários visualizaram um anúncio uma vez)
   * o número exclusivo estimado de dispositivos/navegadores ou pessoas (dependendo do [!UICONTROL Cross Device Level] para o posicionamento) que receberam impressões no nível de frequência especificado
   * número estimado de impressões no nível de frequência especificado
   * frequência média estimada para o nível de frequência especificado. Esse valor é igual a (Impressões estimadas)/(Únicos estimados).

![Inspetor de posicionamento](/help/dsp/assets/placement-inspector-sites.png)

É possível exportar os dados no [!UICONTROL Sites], [!UICONTROL Ads]ou [!UICONTROL Frequency] para a pasta de download padrão do seu navegador como um relatório no formato XLSM.

### Outros tipos de relatórios no nível da campanha

Para outras quebras de dados, exibir [as páginas herdadas de relatórios no nível da campanha](/help/dsp/campaign-management/campaigns/campaign-view-report.md) from [!UICONTROL Campaigns Classic]. O relatório herdado inclui seções em [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability]e [!UICONTROL Audience Performance] dados.

>[!MORELIKETHIS]
>
>* [Exibir os sites, anúncios e detalhes de frequência de uma disposição](placement-details-view.md)
>* [Sobre as exibições de dados da campanha](campaign-data-views-about.md)
>* [Criar uma exibição de coluna personalizada](column-view-create.md)
>* [Alterar a exibição de coluna](column-view-change.md)
>* [Gerenciar visualizações de dados](campaign-data-visualization-manage.md)
>* [Exportar dados de uma visualização de gerenciamento de campanha](campaign-export-data.md)
>* [Exibir um relatório detalhado de uma campanha](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

