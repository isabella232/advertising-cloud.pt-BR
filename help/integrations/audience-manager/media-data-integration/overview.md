---
title: Visão geral do envio DSP dados de exposição de mídia para o Adobe Audience Manager
description: Saiba como usar pixels de Audience Manager event para capturar dados de nível de impressão e de cliques de campanhas do Advertising Cloud DSP
feature: Integration with Adobe Audience Manager
source-git-commit: e861fc53ba14d783c763b291cdc618e5f1d4124f
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# Visão geral do envio DSP dados de exposição de mídia para o Adobe Audience Manager

*Anunciantes somente com o Advertising Cloud DSP*

*Anunciantes somente com uma integração Advertising Cloud-Adobe Audience Manager*

Os clientes do Advertising Cloud DSP com Adobe Audience Manager podem usar pixels de Audience Manager event para capturar dados de nível de impressão e dados de nível de clique de campanhas DSP. Os pixels do evento enviam os dados como sinais acionáveis para o Audience Manager. Esses sinais permitem vários casos de uso de DSP, como segmentação mais avançada, gerenciamento de frequência, análise de marketing e insights de relatórios.

DSP não cobra que você envie esses sinais para o Audience Manager. No entanto, você paga os custos padrão de ingestão de Audience Manager com base nas chamadas do servidor, de acordo com seu contrato de Audience Manager. O Audience Manager remove eventos duplicados que são rastreados de duas maneiras diferentes, de modo que cada evento é cobrado apenas uma vez.

>[!NOTE]
>
> O Audience Manager também oferece suporte à captura de dados de arquivos de log do servidor de publicidade, o que oferece menos flexibilidade. Esse processo não é abordado nesta documentação.

## Benefícios principais

* DSP os dados da campanha fluem para o Audience Manager em tempo real e você pode usá-los para criar características baseadas em regras que você usa para definir segmentos.

* Os segmentos estão disponíveis para direcionamento imediatamente após a qualificação de característica do usuário e segmento, reforçando os esforços de direcionamento em tempo real.

* Você pode aproveitar os dados da campanha para casos de uso como limite de frequência entre anúncios, redirecionamento de usuários que foram expostos a campanhas anteriores e análise do comportamento downstream do site e pontos de entrada.

* Os dados agregados fornecem uma visão unificada do desempenho da campanha, ajudam a identificar caminhos de conversão personalizados e podem ser usados para melhorar a sequência de eventos que levam a conversões por meio do Audience Manager [!DNL Audience Optimization Reports] ou através de uma [[!DNL Audience Analytics] integração com o Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md).

## Como os dados são rastreados

A impressão de Audience Manager e os pixels do evento de clique são baseados em cookies. Os pixels não capturam eventos que ocorrem em ambientes sem cookies, como aplicativos móveis e TV conectada (CTV).

### Pixels de rastreamento de impressão

O Audience Manager acompanha os dados de impressão de um anúncio quando você anexa um pixel de rastreamento de evento transparente de 1xl ao anúncio. O pixel do evento é carregado sempre que o anúncio é veiculado a um usuário e carregado pelo navegador da Web. O pixel é carregado de um subdomínio específico do cliente de [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), que é um domínio herdado para o Audience Manager, e contém parâmetros como pares de valores chave. A chamada de evento coleta dados de impressão e conversão e os envia para os servidores de coleta de dados do Audience Manager.

### Pixels de rastreamento de cliques

O Audience Manager rastreia cliques de forma semelhante às impressões, exceto que não carrega o pixel do evento transparente sempre que o anúncio é veiculado. Em vez disso, os dados de clique são rastreados no URL de click-through do anúncio. O anúncio aponta para um subdomínio específico do cliente de [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), que é um domínio herdado do Audience Manager, para processamento pelos servidores de coleta de dados do Audience Manager. Em seguida, o servidor redireciona o usuário para a página de aterrissagem desejada. O URL contém parâmetros como pares de valores chave.

>[!NOTE]
>
>Se sua organização usar [!DNL Analytics] , talvez você não precise do rastreamento por Audience Manager click. O Adobe Analytics captura sinais de clique e pode enviá-los para o Audience Manager [encaminhamento pelo lado do servidor](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

>[!MORELIKETHIS]
>
>* [Coletar dados de cliques e impressões de campanhas do Advertising Cloud DSP](collect.md)
>* [Casos de uso](use-cases.md)

