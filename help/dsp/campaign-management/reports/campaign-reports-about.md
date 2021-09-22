---
title: Sobre relatórios na plataforma
description: Saiba mais sobre os dados do relatório incluídos nas visualizações de gerenciamento de campanha.
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: c1441fb6fddf56a0f0346a967da49efa0fb602ff
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 0%

---

# Sobre relatórios na plataforma

<!-- rename "About Performance Reports in Campaign Management Views?" -->
As exibições de gerenciamento de campanha incluem dados abrangentes do relatório. Os relatórios disponíveis ajudam a identificar os pacotes e disposições que estão funcionando bem e aqueles que precisam de sua atenção. Os botões de ação rápida também tornam você mais produtivo.

## Lista de todas as campanhas

A visualização [!UICONTROL Campaigns] é aberta a uma lista de todas as campanhas dentro de sua conta. A linha [!UICONTROL Subtotals] mostra a soma ou o valor médio de cada métrica em todas as linhas visíveis.

![Lista de campanhas](/help/dsp/assets/campaigns-list.png)

Por padrão, cada linha de campanha inclui métricas de ritmo e delivery. As métricas de pacotes incluem [!UICONTROL Gross Spend (Lifetime)], que inclui um indicador do gasto real no target versus o gasto esperado no target em todos os pacotes da campanha, para que você possa identificar campanhas com baixo desempenho imediatamente. Opcionalmente, é possível [alterar a exibição de coluna](column-view-change.md) ou até [criar uma exibição de coluna personalizada](column-view-create.md).

Você pode [personalizar ainda mais as tabelas de dados](campaign-data-views-about.md) de formas adicionais e [filtrar os dados visíveis](campaign-data-filter.md).

Para visualizar uma campanha com mais detalhes, clique no nome da campanha.

## Relatório de campanha única

Em uma campanha, você pode filtrar dados com base na entidade da campanha: [!UICONTROL Packages], [!UICONTROL Placements] e [!UICONTROL Ads]. Você pode filtrar ainda mais os dados visíveis](campaign-data-filter.md) para incluir apenas os pacotes, disposições ou anúncios que deseja visualizar.[

![Guias da entidade da campanha](/help/dsp/assets/campaign-subtabs.png)

Em cada guia de entidade, cada linha inclui as métricas de ritmo e entrega, por padrão, mas você pode [alterar a exibição de coluna](column-view-change.md) ou até mesmo [criar uma exibição de coluna personalizada](column-view-create.md) para aplicar em todas as sub-guias da campanha. Você pode [personalizar ainda mais as tabelas de dados](campaign-data-views-about.md) de maneiras adicionais. Cada tabela de dados inclui uma linha [!UICONTROL Subtotals], que mostra a soma ou o valor médio de cada métrica em todas as linhas visíveis.

Para cada campanha, você também pode personalizar gráficos de tendências de séries de tempo com três métricas, que estão disponíveis em cada exibição de entidade. Por padrão, os dados para [!UICONTROL Net Spend], [!UICONTROL Impressions] e [!UICONTROL Net CPM] são incluídos em gráficos separados (gráficos de listas). Como opção, você pode alterar as métricas.

![gráficos de tendências separados para três métricas](/help/dsp/assets/trend-chart-separate.png)

Como opção, também é possível sobrepor as três métricas para fácil detecção de anomalias e áreas nas quais você pode melhorar a escala ou o desempenho.

![gráfico de tendências com sobreposição](/help/dsp/assets/trend-chart.png)

Você pode [personalizar os gráficos de tendências](campaign-data-visualization-manage.md) por campanha e as mesmas métricas são persistentes em todos os gráficos de tendências da campanha.

### Inspetor de posicionamento

Para cada disposição, você pode [abrir uma (visualização detalhada [!UICONTROL Inspector])](placement-details-view.md), que inclui os seguintes dados aprofundados:

* **[!UICONTROL Sites]:** Todos os sites nos quais a disposição foi impressa.

   A guia [!UICONTROL Sites] inclui recursos de pesquisa e filtro, as mesmas opções padrão e personalizadas de exibição de coluna que estão disponíveis na página principal e um botão [!UICONTROL Exclude] em cada linha, para que você possa excluir rapidamente um site da disposição.

* **[!UICONTROL Ads]:** todos os anúncios no posicionamento.

   A guia [!UICONTROL Ads] inclui recursos de pesquisa e filtro, as mesmas opções padrão e personalizadas de exibição de coluna que estão disponíveis na página principal e botões de ação rápida em cada linha, como [!UICONTROL Pause] (para que você possa pausar um anúncio rapidamente).

* **[!UICONTROL Frequency]:** Dados para cada nível de frequência de anúncio para a disposição, incluindo:
   * o nível de frequência do anúncio (como &quot;1&quot; para todas as instâncias em que os usuários visualizaram um anúncio uma vez)
   * o número exclusivo estimado de dispositivos/navegadores ou pessoas (dependendo do [!UICONTROL Cross Device Level] especificado para a disposição) que receberam impressões no nível de frequência especificado
   * número estimado de impressões no nível de frequência especificado
   * frequência média estimada para o nível de frequência especificado. Esse valor é igual a (Impressões estimadas)/(Únicos estimados).

* **[!UICONTROL Inventory]:** informações para todas as ofertas direcionadas pela disposição em uma única visualização.

A guia Inventário inclui recursos de pesquisa e filtro, as mesmas opções padrão e personalizadas de exibição de coluna que estão disponíveis na página principal e botões de ação rápida em cada linha, como Editar e Exibir Relatório. A guia Inventário ajuda na solução rápida de problemas ao mostrar estatísticas de desempenho, como Leilões, Ofertas, Taxa de Ganho etc.

# Solução de problemas do inventário

| Problema | Causa Possível | Ações a serem tomadas |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | O Publisher não iniciou o envio de pedidos de licitação | Entre em contato com o editor para ativar a negociação |
|  | Problemas de configuração de negócios como inserir uma ID de negócios externa incorreta, etc. | Confirme os detalhes da negociação e edite a negociação |
| [!UICONTROL Non-zero Auctions but no Bids] | O direcionamento da disposição não corresponde às solicitações de oferta recebidas do negócio. <br><br> Por exemplo, a disposição pode ser direcionada para uma geografia diferente da necessária por negociação | Edite as configurações de posicionamento adequadas para evitar incompatibilidades de direcionamento com o negócio |
|  | O posicionamento não tem um anúncio ativo ou o tipo de mídia correto, conforme exigido pelo negócio | Criar/anexar anúncio com o tipo de mídia correto à disposição |
|  | A disposição não tem orçamento adequado | Edite o orçamento de disposição adequadamente para permitir lances em solicitações recebidas |
|  | As datas de envio da disposição não se sobrepõem às datas de entrega da impressão como por negócio | Editar as datas de voo para a disposição |
| [!UICONTROL Low Win Rate] | O lance máximo no posicionamento é definido abaixo do mínimo exigido pelo negócio (limite mínimo ou fixo) | Editar lance máximo no posicionamento adequado |
|  | A disposição usa filtros pré-lances que limitam | Reduza os limites dos filtros pré-lances para permitir mais lances |
|  | O direcionamento de público-alvo no posicionamento é muito restritivo | Verifique se os públicos-alvo especificados têm suficientes usuários ativos e expanda o público-alvo, se possível |

![Inspetor de posicionamento](/help/dsp/assets/placement-inspector-sites.png)

Você pode exportar os dados na guia [!UICONTROL Sites], [!UICONTROL Ads] ou [!UICONTROL Frequency] para a pasta de download padrão do navegador como um relatório no formato XLSM.

### Outros tipos de relatórios no nível da campanha

Para outros detalhamentos de dados, visualize [as páginas de relatórios herdadas no nível da campanha](/help/dsp/campaign-management/campaigns/campaign-view-report.md) de [!UICONTROL Campaigns Classic]. O relatório herdado inclui seções nos dados [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability] e [!UICONTROL Audience Performance].

>[!MORELIKETHIS]
>
>* [Exibir os sites, anúncios e detalhes de frequência de uma disposição](placement-details-view.md)
>* [Sobre as exibições de dados da campanha](campaign-data-views-about.md)
>* [Criar uma exibição de coluna personalizada](column-view-create.md)
>* [Alterar a exibição de coluna](column-view-change.md)
>* [Gerenciar visualizações de dados](campaign-data-visualization-manage.md)
>* [Exportar dados de uma visualização de gerenciamento de campanha](campaign-export-data.md)
>* [Exibir um relatório detalhado de uma campanha](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

