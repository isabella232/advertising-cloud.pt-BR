---
title: Práticas recomendadas para criar uma meta personalizada
description: Conheça as práticas recomendadas para criar metas personalizadas para definir seus eventos de sucesso.
feature: DSP Optimization, DSP Best Practices
exl-id: 54b16325-4b72-48a3-a2e0-4e342229211c
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Práticas recomendadas para criar uma meta personalizada

## Metas personalizadas com uma única propriedade

Os exemplos a seguir mostram como configurar metas que direcionam uma única propriedade (métrica).

### Exemplo de uma campanha com o &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; Objetivo de otimização

Se a meta da campanha for receita ([!UICONTROL Highest ROAS - Custom Goal]), sua meta personalizada (objetivo) incluirá o &quot;[!UICONTROL Revenue]&quot;propriedade com um peso de 1 (1).

![exemplo de uma meta personalizada do ROAS com uma única propriedade](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] de um equivale a um valor de um para cada $1 da receita rastreada.
>
> Por exemplo, uma conversão de $250 com um peso de um é relatada como $250. Se a métrica de conversão receber um peso de 0,5, a conversão de $250 será relatada como $125 em Adobe Advertising ($250 Conversion * 0,5) [!UICONTROL Property Weight] = US$125).

### Exemplo de uma campanha com o &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot; Objetivo de otimização

Se a meta da campanha for o menor custo por aquisição (CPA) e exigir apenas um evento bem-sucedido, você incluirá essa métrica (no exemplo a seguir, &quot;Envio de aplicativo&quot;). A prática recomendada é definir o peso como um (1).

![exemplo de uma meta personalizada de CPA com uma única propriedade](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] de um equivale a um valor de um para cada conversão rastreada.
>
> Por exemplo, se 10 conversões de Envio de aplicativo forem rastreadas, 10 conversões de Envio de aplicativo serão relatadas.  Se a métrica de conversão receber um peso de 0,5, então as 10 conversões serão relatadas como cinco (5) em Adobe Advertising (10 Conversões * 0,5 [!UICONTROL Property Weight] = 5).

## Metas personalizadas com várias propriedades

Há dois cenários nos quais você usaria várias propriedades em uma meta personalizada:

* Sua meta da campanha tem vários eventos bem-sucedidos. Por exemplo, talvez você esteja anunciando mais de uma ação no site e todos estão sendo atribuídos à meta do CPA. O objetivo de exemplo a seguir inclui três propriedades separadas (Download de PDF, Entre em contato conosco e Cadastre-se de email), cada uma com um peso de uma (1), que informa ao [!DNL Adobe Sensei] algoritmo que cada uma das propriedades tem importância igual. Se você incluir propriedades com custos ou importância variáveis, será possível ajustar os pesos relativos de acordo.

   ![exemplo de uma meta personalizada com várias propriedades](/help/dsp/assets/custom-goal-multiple-properties.png)

* A única propriedade na meta personalizada não está atingindo o mínimo de 10 conversões por dia necessárias para um desempenho otimizado. Isso pode ocorrer devido ao gasto diário mínimo ou a um número limitado de conversões naturais. Adicionar outras propriedades de suporte à meta personalizada pode ajudar você a atingir o limite de 10 conversões por dia. Dez eventos de suporte podem ajudar um pacote a atingir o limite de 10 dias, mesmo quando cada um de seus pesos estiver abaixo de um (1). Mas talvez você não precise adicionar tantos eventos.

   Ao adicionar propriedades de suporte a uma meta personalizada, avalie-as de acordo com sua importância relativa para o evento de sucesso principal e lembre-se da quantidade de pontos de dados. Isso permite que o algoritmo Adobe Sensei equilibre várias propriedades e otimize sua meta.

   O objetivo de exemplo a seguir inclui três propriedades, cada uma com um peso diferente: Envio de aplicativo = 1, Início do aplicativo = 0.1 e Página inicial do anunciante = 0.01. Isso significa que cada conversão de Envio de aplicativo tem o mesmo valor para sua empresa que uma média de 10 conversões de Início do aplicativo e 100 conversões de Página inicial do anunciante.

   ![exemplo de uma meta personalizada com várias propriedades](/help/dsp/assets/custom-goal-multiple-properties2.png)

   Se, em vez disso, você tiver ponderado as visitas da página inicial igualmente nos envios de aplicativo, a quantidade naturalmente maior de visitas da página inicial poderá sobrecarregar sua meta e inclinar-se para as visitas da página inicial.<!--reword-->

>[!MORELIKETHIS]
>
>* [Sobre as metas personalizadas](custom-goal-about.md)
>* [Criar uma meta personalizada](custom-goal-create.md)
>* [Metas de otimização e como usá-las](optimization-goals.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
> * [Como o DSP otimiza suas campanhas](optimization-how-dsp-optimizes-campaigns.md)

