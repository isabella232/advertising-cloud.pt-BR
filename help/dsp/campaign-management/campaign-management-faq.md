---
title: Perguntas frequentes sobre o Campaign Management
description: Saiba mais sobre o gerenciamento de campanhas, incluindo o período de latência para alterações e o que acontece quando você faz alterações no orçamento durante um voo.
feature: DSP Packages, DSP Placements
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Perguntas frequentes sobre o Campaign Management

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Latência das alterações na configuração

* Quando você altera uma configuração de posicionamento ou pacote, quando a alteração entrará em vigor?

   As alterações nas configurações normalmente entrarão em vigor imediatamente, mas podem levar até 12 horas.

   Se for o último dia do delivery, faça alterações no início do dia para que DSP tenha tempo suficiente para recalibrar o pacote com base nas alterações. Por exemplo, se você mudar de ritmo uniforme para ritmo de carregamento prévio, DSP precisará reavaliar como ele distribuirá o gasto durante o restante do voo. Não faça esse tipo de mudança se você tiver apenas uma hora para entregar no último dia do voo.

## Atualizações do orçamento no meio do voo

* Quando você faz uma alteração em uma disposição, quanto DSP leva para realocar o orçamento do pacote?

   A alocação de orçamento é baseada no desempenho da disposição, que é avaliado usando uma média de 14 dias. Alterações em uma disposição resultam em alterações na alocação do orçamento somente quando causam alterações no desempenho durante a média de 14 dias.

   Quando o desempenho muda, o DSP realoca o orçamento do pacote entre as disposições de acordo durante o próximo ciclo de otimização de orçamento, que ocorre em cerca de meia-noite (00:00) no fuso horário da campanha.

* Como o orçamento é realocado quando uma disposição é removida de um pacote e adicionada a outro pacote?

   Todo o histórico de gastos de um posicionamento é anexado ao posicionamento e se move com ele de pacote em pacote.

   Quando você remove um posicionamento de um pacote, ele não tem mais histórico dos gastos do posicionamento. O orçamento do pacote se tornará (orçamento do pacote - orçamento de posicionamento removido) / intervalo de tempo restante em andamento. O orçamento do pacote é então alocado para as disposições restantes no pacote.

   Da mesma forma, se você adicionar a mesma disposição a um pacote diferente, o DSP considerará o histórico de gastos da disposição quando ela alocar orçamento para todas as disposições no novo pacote.

* Como o ritmo do pacote muda no último dia de um voo?

   No último dia de um voo, o dia é reduzido de 24 horas para 23 horas para que o orçamento do pacote não seja excedido. Além disso, a estratégia de preenchimento de ritmo do pacote muda automaticamente para &quot;[!UICONTROL Frontload],&quot; mesmo que esteja definido como &quot;[!UICONTROL even].&quot; Isso significa que 65% do orçamento diário deve ser entregue até às 11h30 EST.

>[!MORELIKETHIS]
>
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Práticas recomendadas para configurar campanhas de desempenho](/help/dsp/optimization/campaign-best-practices-performance.md)

