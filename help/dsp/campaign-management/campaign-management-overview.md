---
title: Visão geral do Campaign Management em DSP de publicidade
description: Saiba mais sobre a hierarquia e os componentes do gerenciamento de campanha.
feature: DSP Packages, DSP Placements, DSP Ads
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Visão geral do Campaign Management em DSP de publicidade

DSP campanhas têm a seguinte hierarquia:

* Campanha
   * Pacote(s)
      * Disposição(ões)
         * Anúncio(s)

<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package will include placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Campanhas](/help/dsp/campaign-management/campaigns/campaign-about.md) são o quadro geral das definições de voo. Cada campanha é configurada com um anunciante, datas de início e término, um orçamento geral, uma opção de direcionamento entre dispositivos e limite de frequência padrão e opções de relatórios para visualização, fraude, segurança da marca e verificação de público-alvo. Todas as configurações de nível de campanha se aplicam automaticamente a cada pacote e disposição dentro da campanha.

## [!UICONTROL Packages]

Cada campanha pode conter um ou mais [pacotes](/help/dsp/campaign-management/packages/package-about.md), cada qual inclui um conjunto de disposições.

Use pacotes para agrupar disposições para entrega em um orçamento definido, objetivo de desempenho e estratégia de ritmo personalizado. DSP otimiza pacotes ao transferir orçamentos para as disposições com melhor desempenho no pacote. Você pode organizar os pacotes por formato de disposição, tipo de inventário, provedor de dados, persona ou outras características distinguíveis.

Os pacotes são opcionais, mas recomendados.

## [!UICONTROL Placements]

A [placement](/help/dsp/campaign-management/placements/placement-about.md) armazena parâmetros de definição de metas para um ou mais anúncios do mesmo tipo de anúncio. Você pode criar uma disposição para uma única campanha ou pacote e, em seguida, atribuir anúncios a ele.

## [!UICONTROL Ads]

[Anúncios](/help/dsp/campaign-management/ads/ad-about.md) inclua ativos criativos e URLs de rastreamento. Você pode fazer upload de publicidade de terceiros veiculando tags individualmente ou em massa usando folhas de tags de parceiros ou o modelo de tag em massa. Você também pode criar manualmente anúncios de exibição nativos para DSP a serem exibidos.

Depois que seus anúncios forem configurados, será necessário anexar cada anúncio a uma disposição. Você pode anexar um único anúncio a uma ou mais disposições.

Todos os anúncios ativos e aprovados em um posicionamento ativo em uma campanha ativa são elegíveis para execução com base nos parâmetros de definição de meta de posicionamento.

>[!MORELIKETHIS]
>
>* [Sobre o Campaign Management](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Sobre o Gerenciamento de pacotes](/help/dsp/campaign-management/packages/package-about.md)
>* [Sobre o gerenciamento de disposição](/help/dsp/campaign-management/placements/placement-about.md)
>* [Sobre o Gerenciamento de anúncios](/help/dsp/campaign-management/ads/ad-about.md)
>* [Lista de verificação do lançamento da campanha](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Práticas recomendadas para configurar campanhas de desempenho](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Sobre relatórios na plataforma](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Sobre as exibições de dados da campanha](/help/dsp/campaign-management/reports/campaign-data-views-about.md)
>* [Vídeo: Estrutura da conta DSP e interface do usuário](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/dsp/ui.html)

