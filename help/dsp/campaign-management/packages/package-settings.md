---
title: Configurações do pacote
description: Consulte descrições das configurações de pacote disponíveis.
feature: Packages
exl-id: b4d415d1-86a5-40bd-b645-1709b267c174
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Configurações do pacote

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** o nome do pacote. O comprimento máximo é de 60 caracteres.

**[!UICONTROL Description]:** (opcional) uma descrição do pacote.

**[!UICONTROL 3rd Party Billed Fees]:** (Opcional) Uma taxa de terceiros estática a ser rastreada como um custo não faturável:

>[!NOTE]
>
>As tarifas faturáveis são refletidas na métrica [!UICONTROL Net CPM].
* **[!UICONTROL CPM]:** o custo por 1000 impressões (CPM).

* **[!UICONTROL CPM Description]:** uma descrição da taxa CPM.

Você pode substituir a configuração de nível de pacote no [nível de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Só de leitura para as embalagens existentes) Em que nível colocar e fixar disposições na embalagem:

* **[!UICONTROL Package level pacing]:** essa estratégia de ritmo funciona colocando e limitando todas as disposições incluídas como um  *grupo*. Essa estratégia garante que todas as disposições de um determinado pacote sejam otimizadas de forma holística, distribuindo os gastos com base no desempenho e dimensionando para KPIs (indicadores-chave de desempenho) selecionados.

* **[!UICONTROL Placement level pacing]:**  essa estratégia de ritmo funciona colocando e limitando todas as disposições incluídas  *individualmente*. A melhor prática consiste em utilizar esta estratégia apenas para executar transações garantidas do mercado privado.

**[!UICONTROL Flight Dates]:** A data de início e de término do pacote.

Como opção, para criar voos não regulares para o pacote, selecione *[!UICONTROL *Activate Custom Flighting]** e configure os voos personalizados na seção [!UICONTROL Flighting] abaixo. Depois de ativar o voo personalizado e salvar o pacote, você não pode desativar o voo personalizado.

>[!NOTE]
>
>* As datas de voo devem ser incluídas nas datas de voo da campanha. Além disso, as datas de voo para todas as disposições atribuídas a este pacote devem ser incluídas nessas datas.
> * Não é possível editar a data de início do pacote quando o voo personalizado é ativado.


**[!UICONTROL Budget]:**  (pacotes com ritmo no nível do pacote somente) O limite de orçamento bruto e o intervalo de orçamento.

Para pacotes com voo personalizado, o intervalo de orçamento é sempre *[!UICONTROL All time]*. Para pacotes sem iluminação personalizada, especifique o intervalo de orçamento: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Pacotes com ritmo no nível do pacote e gerenciamento dinâmico de margens apenas) O limite bruto do orçamento para a duração do pacote.

**[!UICONTROL Optimization Goal]:**  (pacotes com ritmo no nível do pacote somente) A meta de otimização do pacote. Consulte descrições de cada meta de otimização em [Metas de otimização e Como usá-las](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goals]:** (Pacotes com metas de otimização personalizadas somente) O objetivo  [personalizado ](/help/dsp/optimization/custom-goal-about.md) do pacote. Para obter mais informações sobre as práticas recomendadas para metas e campanhas personalizadas que as usam, consulte [Práticas recomendadas para criar uma meta personalizada](/help/dsp/optimization/custom-goal-best-practices.md) e [Práticas recomendadas para configurar campanhas de desempenho](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Package Goal Type]:**  (pacotes com metas de otimização personalizadas somente) a finalidade do pacote. Essa configuração ajuda a determinar como otimizar o pacote:

* *[!UICONTROL Prospecting]:* Os pacotes de prospecção se concentram na aquisição de novos clientes.

* *[!UICONTROL Retargeting]:* os pacotes de redirecionamento se concentram em reexpor visitantes ou clientes anteriores.

* *[!UICONTROL Other]:* Todos os outros fins.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:**  (pacotes com metas de otimização personalizadas somente) outro pacote cujos dados históricos são usados como entrada para otimizar o pacote.

**[!UICONTROL Target]:**  (pacotes com ritmo no nível do pacote somente) a meta do target, que é usada para rastrear o desempenho.

>[!NOTE]
>
>Este campo é apenas um referencial e não é usado para a tomada de decisão.

**[!UICONTROL Frequency Cap]:** (pacotes com ritmo no nível do pacote somente) o número de vezes que um dispositivo ou pessoa exclusiva (dependendo do especificado  [!UICONTROL Cross Device Level]) pode ser veiculada nos anúncios do pacote. As opções incluem *[!UICONTROL Unlimited]* ou uma quantidade específica por dia, semana ou mês.

>[!NOTE]
>
>* Você pode definir limites de frequência nos níveis de campanha, pacote e disposição. DSP respeita o limite de frequência mais rigoroso na hierarquia da campanha.
>* A prática recomendada é definir limites de frequência para prospecção e redirecionamento no nível do pacote.
> * Limites de frequência mais altos resultam em gastos e impressões mais altos, mas em menor alcance. Os limites de frequência mais baixos resultam em menos gasto e impressões, mas maior alcance.


**[!UICONTROL Pace on]:** (Pacotes apenas com ritmo de nível de pacote) O que é baseado em:

* *[!UICONTROL Budget]:* (padrão) essa opção fornece o máximo de impressões possível dentro do orçamento do pacote alocado.

* *[!UICONTROL Impressions]:* essa opção fornece impressões até que uma quantidade específica seja alcançada em um intervalo especificado. Ao selecionar essa opção, especifique o número de impressões e o intervalo: *Tempo inteiro,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Pacing Fill Strategy]:** (Pacotes com pacing no nível do pacote somente) Como carregar e fornecer:

* *[!UICONTROL Even]:* Os pacotes são distribuídos uniformemente em cada voo, com um target de 50% do delivery na primeira metade do voo.

* *[!UICONTROL Slightly Ahead]:* (o padrão) acelera a entrega para que esteja 55 a 65% completo na metade da duração do voo.

* *[!UICONTROL Frontload]:* acelera a entrega para que esteja 65 a 75% completo na metade do voo.

* *[!UICONTROL Aggressive Frontload]:* acelera a entrega para que esteja 75 a 85% completo na metade do voo.

## [!UICONTROL Flighting]

(Pacotes com ritmo no nível do pacote e com &quot;[!UICONTROL Activate Custom Flighting]&quot; ativado) Períodos de voo personalizados dentro do [!UICONTROL Flight Dates] geral especificado na seção [!UICONTROL Goals & Budget].

Para cada voo, insira a data de início, a data de término e o número alvo de impressões. Para adicionar outro voo, clique em **[!UICONTROL Add Flight]**.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de pacotes](package-about.md)
>* [Criar um pacote](package-create.md)
>* [Editar um pacote](package-edit.md)
>* [Anexar uma disposição a um pacote](package-attach-placement.md)
>* [Perguntas frequentes sobre o gerenciamento de campanhas](/help/dsp/campaign-management/campaign-management-faq.md)

