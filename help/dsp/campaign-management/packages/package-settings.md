---
title: Configurações do pacote
description: Consulte descrições das configurações de pacote disponíveis.
feature: DSP Packages
exl-id: b4d415d1-86a5-40bd-b645-1709b267c174
source-git-commit: 6331166f563e1404c077eb848eed049b4eb0706d
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Configurações do pacote

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** O nome do pacote. O comprimento máximo é de 60 caracteres.

**[!UICONTROL Description]:** (Opcional) Uma descrição do pacote.

**[!UICONTROL 3rd Party Billed Fees]:** (Opcional) Uma taxa estática de terceiros a ser rastreada como um custo não faturável:

>[!NOTE]
>
>As comissões faturáveis refletem-se na [!UICONTROL Net CPM] métrica.
* **[!UICONTROL CPM]:** O custo por 1000 impressões (CPM).

* **[!UICONTROL CPM Description]:** Uma descrição da taxa CPM.

Você pode substituir a configuração no nível do pacote na [nível de inserção](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Só de leitura para as embalagens existentes) Em que nível colocar e fixar disposições na embalagem:

* **[!UICONTROL Package level pacing]:** Esta estratégia de ritmo funciona colocando e limitando todas as disposições incluídas como uma *grupo*. Essa estratégia garante que todas as disposições de um determinado pacote sejam otimizadas de forma holística, distribuindo os gastos com base no desempenho e dimensionando para KPIs (indicadores-chave de desempenho) selecionados.

* **[!UICONTROL Placement level pacing]:**  Esta estratégia de ritmo funciona colocando e limitando todas as disposições incluídas *individualmente*. A melhor prática consiste em utilizar esta estratégia apenas para executar transações garantidas do mercado privado.

**[!UICONTROL Flight Dates]:** A data de início e de término do pacote.

Para criar voos de ritmo não par para o pacote, selecione *[!UICONTROL *Activate Custom Flighting]** e configurar os voos personalizados no [!UICONTROL Flighting] abaixo. Depois de ativar o voo personalizado e salvar o pacote, você não pode desativar o voo personalizado.

>[!NOTE]
>
>* As datas de voo devem ser incluídas nas datas de voo da campanha. Além disso, as datas de voo para todas as disposições atribuídas a este pacote devem ser incluídas nessas datas.
> * Não é possível editar a data de início do pacote quando o voo personalizado é ativado.


**[!UICONTROL Budget]:** (Pacotes com ritmo no nível do pacote somente) O limite de orçamento bruto e o intervalo de orçamento.

Para pacotes com voo personalizado, o intervalo de orçamento é sempre *[!UICONTROL All time]*. Para pacotes sem iluminação personalizada, especifique o intervalo de orçamento: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Pacotes com ritmo no nível do pacote e gerenciamento dinâmico de margem apenas) O limite de orçamento bruto para a duração do pacote.

**[!UICONTROL Optimization Goal]:** (Pacotes com ritmo no nível do pacote somente) A meta de otimização do pacote. Veja descrições de cada meta de otimização em [Metas de otimização e como usá-las](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goals]:** (Pacotes com metas de otimização personalizadas somente) A variável [meta personalizada](/help/dsp/optimization/custom-goal-about.md) para o pacote. Para obter mais informações sobre as práticas recomendadas para metas e campanhas personalizadas que as utilizam, consulte  [Práticas recomendadas para criar uma meta personalizada](/help/dsp/optimization/custom-goal-best-practices.md) e [Práticas recomendadas para configurar campanhas de desempenho](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Package Goal Type]:** (Pacotes com metas de otimização personalizadas somente) A finalidade do pacote. Essa configuração ajuda a determinar como otimizar o pacote:

* *[!UICONTROL Prospecting]:* Os pacotes de prospecção se concentram na aquisição de novos clientes.

* *[!UICONTROL Retargeting]:* Os pacotes de redirecionamento se concentram em reexpor visitantes ou clientes anteriores.

* *[!UICONTROL Other]:* Todos os outros fins.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Pacotes com metas de otimização personalizadas somente) Outro pacote cujos dados históricos são usados como entrada para otimizar o pacote.

**[!UICONTROL Target]:** (Pacotes com ritmo no nível do pacote somente) A meta do target, que é usada para rastrear o desempenho.

>[!NOTE]
>
>Este campo é apenas um referencial e não é usado para a tomada de decisão.

**[!UICONTROL Frequency Cap]:** (Pacotes com ritmo no nível do pacote somente) O número de vezes que um dispositivo ou pessoa exclusiva (dependendo do [!UICONTROL Cross Device Level] para a campanha) pode ser veiculada como anúncio do pacote. As opções incluem *[!UICONTROL Unlimited]* ou um valor específico por dia, semana ou mês.

>[!NOTE]
>
>* Você pode definir limites de frequência nos níveis de campanha, pacote e disposição. DSP respeita o limite de frequência mais rigoroso na hierarquia da campanha.
>* A prática recomendada é definir limites de frequência para prospecção e redirecionamento no nível do pacote.
> * Limites de frequência mais altos resultam em gastos e impressões mais altos, mas em menor alcance. Os limites de frequência mais baixos resultam em menos gasto e impressões, mas maior alcance.


**[!UICONTROL Pace on]:** (Pacotes com ritmo de nível de pacote somente) O que é baseado em:

* *[!UICONTROL Budget]:* (Padrão) Essa opção fornece o máximo de impressões possível dentro do orçamento do pacote alocado.

* *[!UICONTROL Impressions]:* Essa opção fornece impressões até que uma quantidade especificada seja alcançada em um intervalo especificado. Ao selecionar essa opção, especifique o número de impressões e o intervalo: *O tempo todo,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Pacotes com pacing no nível do pacote somente) Como acompanhar e entregar em todo o voo:

* *[!UICONTROL Even]:* Os pacotes são fornecidos uniformemente ao longo de cada voo, com um objetivo de 50% da entrega na primeira metade do voo.

* *[!UICONTROL Slightly Ahead]:* (O padrão) Acelera a entrega para que esteja 55 a 65% completo na metade da duração do voo.

* *[!UICONTROL Frontload]:* Acelera a entrega para que esteja 65 a 75% completo na metade do voo.

* *[!UICONTROL Aggressive Frontload]:* Acelera a entrega para que esteja 75 a 85% completo na metade do voo.

**[!UICONTROL Intraday pacing]:** (Pacotes com pacing no nível do pacote somente) Como acompanhar e entregar em cada dia no voo:

* *[!UICONTROL Even]:* (O padrão) Dimensiona o delivery com base na disponibilidade do inventário. Geralmente, mais anúncios são entregues por hora no dia, quando o volume do leilão é maior e menos anúncios são entregues de manhã e à noite.

* *[!UICONTROL ASAP]:* Acelera a entrega para o dobro da velocidade de *Mesmo*.

   >[!CAUTION]
   >
   >Essa opção pode afetar negativamente o desempenho. Use-o somente quando estiver priorizando totalmente o delivery e gastando em relação à otimização de desempenho.

## [!UICONTROL Flighting]

(Pacotes com ritmo no nível do pacote e com &quot;[!UICONTROL Activate Custom Flighting]&quot; ativado) Períodos de voo personalizados dentro do total [!UICONTROL Flight Dates] especificados na [!UICONTROL Goals & Budget] seção.

Para cada voo, insira a data de início, a data de término e o número alvo de impressões. Para adicionar outro voo, clique em **[!UICONTROL Add Flight]**.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de pacotes](package-about.md)
>* [Criar um pacote](package-create.md)
>* [Editar um pacote](package-edit.md)
>* [Anexar uma disposição a um pacote](package-attach-placement.md)
>* [Perguntas frequentes sobre o Campaign Management](/help/dsp/campaign-management/campaign-management-faq.md)

