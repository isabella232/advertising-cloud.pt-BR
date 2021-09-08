---
title: Visão geral do gerenciamento de campanhas no Advertising Cloud DSP
description: Saiba mais sobre a hierarquia e os componentes do gerenciamento de campanha.
feature: Packages, Placements, Ads, Creatives
exl-id: c94e08d0-0dd5-4cf9-8df2-9eb4c591375c
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Visão geral do gerenciamento de campanhas no Advertising Cloud DSP

As campanhas do Advertising Cloud DSP têm a seguinte hierarquia:

* Campanha
   * Pacote(s)
      * Disposição(ões)
         * Anúncio(s)
            * Criativo(s)

<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising Cloud DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package will include placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[](/help/dsp/campaign-management/campaigns/campaign-about.md) As campanhas são a estrutura abrangente das configurações de voo. Cada campanha é configurada com um anunciante, datas de início e término, um orçamento geral, uma opção de direcionamento entre dispositivos e limite de frequência padrão e opções de relatórios para visualização, fraude, segurança da marca e verificação de público-alvo. Todas as configurações de nível de campanha se aplicam automaticamente a cada pacote e disposição dentro da campanha.

## [!UICONTROL Packages]

Cada campanha pode conter um ou mais [pacotes](/help/dsp/campaign-management/packages/package-about.md), cada um incluindo um conjunto de disposições.

Use pacotes para agrupar disposições para entrega em um orçamento definido, objetivo de desempenho e estratégia de ritmo personalizado. DSP otimiza pacotes ao transferir orçamentos para as disposições com melhor desempenho no pacote. Você pode organizar os pacotes por formato de disposição, tipo de inventário, provedor de dados, persona ou outras características distinguíveis.

Os pacotes são opcionais, mas recomendados.

## [!UICONTROL Placements]

Um [placement](/help/dsp/campaign-management/placements/placement-about.md) armazena parâmetros de definição de metas para um ou mais anúncios do mesmo tipo de anúncio. Você pode criar uma disposição para uma única campanha ou pacote e, em seguida, atribuir anúncios a ele.

## [!UICONTROL Ads]

[](/help/dsp/campaign-management/ads/ad-about.md) Inclua ativos criativos e URLs de rastreamento. Você pode fazer upload de seus ativos criativos e DSP os anúncios que os usam gratuitamente, ou você pode fazer upload de tags de veiculação de anúncios de terceiros.

Depois que seus anúncios forem configurados, será necessário anexar cada anúncio a uma disposição. Você pode anexar um único anúncio a uma ou mais disposições.

Todos os anúncios ativos e aprovados em um posicionamento ativo em uma campanha ativa são elegíveis para execução com base nos parâmetros de definição de meta de posicionamento.

## [!UICONTROL Creatives]

Você pode fazer upload de arquivos de áudio e vídeo para uso em anúncios para campanhas especificadas.
<!-- add link to [About Creative Management](/help/dsp/campaign-management/creatives/creative-about.md) when it's available-->

Você pode criar um anúncio imediatamente com o anúncio carregado, ou pode criar um anúncio posteriormente na exibição Creative ou Ads.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de campanhas](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Sobre o Gerenciamento de pacotes](/help/dsp/campaign-management/packages/package-about.md)
>* [Sobre o gerenciamento de disposição](/help/dsp/campaign-management/placements/placement-about.md)
>* [Sobre o Gerenciamento de anúncios](/help/dsp/campaign-management/ads/ad-about.md)
>* [Lista de verificação do lançamento da campanha](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Práticas recomendadas para configurar campanhas de desempenho](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Sobre relatórios na plataforma](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Sobre as exibições de dados da campanha](/help/dsp/campaign-management/reports/campaign-data-views-about.md)

