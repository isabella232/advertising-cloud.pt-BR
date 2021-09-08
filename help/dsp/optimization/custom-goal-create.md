---
title: Criar uma meta personalizada
description: Criar uma meta personalizada
feature: Optimization
exl-id: 440ded21-92d3-41ad-839f-ebc8376aa932
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Criar uma meta personalizada

>[!TIP]
>
>Consulte as [práticas recomendadas para criar metas personalizadas](custom-goal-best-practices.md) para obter dicas sobre como configurar suas metas personalizadas.

1. Faça logon no Advertising Cloud Search em (empresas dos EUA) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) ou (empresas em todos os outros países) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. Certifique-se de que as métricas que deseja incluir na meta foram rastreadas, estão disponíveis no produto e incluem um nome de exibição:
   1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.
   1. Localize a métrica e verifique se **[!UICONTROL Show in UI and Reports]** está ativado para a métrica.
   1. Se a métrica não tiver um valor na coluna **[!UICONTROL Display Name]**, clique na célula, digite o nome de exibição e clique em **[!UICONTROL Apply].**
1. Crie a meta personalizada como um *objetivo*:
   1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Optimization] >[!UICONTROL Objectives]**.
   1. Na barra de ferramentas, clique em **[!UICONTROL Create objective].**
   1. Insira as configurações do objetivo:
      1. No campo **[!UICONTROL Change Objective Name]**, insira o nome do objetivo.

         O nome do objetivo será mostrado na lista [!UICONTROL Custom Goals] nas configurações do pacote Advertising Cloud DSP.

      1. Associe propriedades ao objetivo:

         >[!NOTE]
         >
         > Todas as propriedades de transação rastreadas para o anunciante são listadas por padrão na lista [!UICONTROL Available Properties].

         * Para importar um arquivo CSV com propriedades e seus pesos, clique em **[!UICONTROL Import]** e localize o arquivo a ser importado.

            As propriedades importadas já devem existir para o anunciante; os nomes não fazem distinção entre maiúsculas e minúsculas.

            As propriedades importadas substituirão as propriedades existentes especificadas.

         * Para especificar manualmente a primeira propriedade com o peso padrão (1), selecione em uma lista de todas as propriedades de transação rastreadas para o anunciante.

         * Para adicionar manualmente outra propriedade com o peso padrão (1), clique em **[!UICONTROL +]** .

            >[!TIP]
            >
            > Para procurar uma propriedade na lista, digite uma string de qualquer lugar dentro do nome da propriedade.

         * Para adicionar manualmente várias propriedades, clique em **[!UICONTROL Add Multiple Properties].** Para cada propriedade que deseja adicionar, clique no nome da propriedade na  [!UICONTROL Available Properties] coluna e arraste-a para a  [!UICONTROL Added Properties] coluna . Quando terminar de adicionar propriedades, clique em **[!UICONTROL Add]**.

            >[!TIP]
            >
            >* Para procurar uma propriedade na lista, insira uma string de qualquer lugar dentro do nome da propriedade no campo de entrada.
            >* Para filtrar a lista para excluir propriedades excluídas nos relatórios, selecione a opção **[!UICONTROL Hide properties excluded from reports].**


         * (Quando o objetivo contém várias propriedades) Para alterar o peso de uma propriedade em relação às outras propriedades no objetivo, insira valores no(s) campo(s) **[!UICONTROL Weight]** .
      1. Na parte inferior das configurações, clique em **[!UICONTROL Save]**.


Depois de criar um objetivo, você pode atribuí-lo a um pacote Advertising Cloud DSP como uma meta personalizada quando a meta de otimização for &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; ou &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot;.

>[!TIP]
>
>Para um desempenho <!-- optimum? Or optimization won't happen at all w/out it? -->otimizado, as métricas combinadas na meta personalizada (objetivo) devem totalizar pelo menos 10 conversões por dia. Caso contrário, a prática recomendada é adicionar outros eventos de suporte (propriedades de transação), como páginas de produto ou início de aplicativo, ao objetivo. Consulte [Práticas recomendadas para criar uma meta personalizada](custom-goal-best-practices.md) para obter diretrizes.

>[!MORELIKETHIS]
>
>* [Sobre as metas personalizadas](custom-goal-about.md)
>* [Práticas recomendadas para criar uma meta personalizada](custom-goal-best-practices.md)
>* [Metas de otimização e como usá-las](optimization-goals.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
> * [Como o DSP otimiza suas campanhas](optimization-how-dsp-optimizes-campaigns.md)

