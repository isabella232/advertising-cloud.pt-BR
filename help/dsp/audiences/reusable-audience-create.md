---
title: Criar um público-alvo reutilizável
description: Saiba como criar públicos-alvo reutilizáveis que consistem em segmentos de público-alvo e outros públicos-alvo salvos.
feature: Audiences
exl-id: 48e3dc4c-6e2d-452c-8d69-7e6211d808e0
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Criar um público-alvo reutilizável

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

Você pode salvar e gerenciar públicos reutilizáveis, que são grupos de segmentos de público-alvo e até outros públicos salvos, que podem ser usados como alvos ou exclusões para várias disposições.

1. No menu principal, clique em **[!UICONTROL Audiences]>[!UICONTROL All Audiences]**.

1. Acima da tabela de dados, clique em **[!UICONTROL Create]**.

1. Insira um [!UICONTROL Audience Name] exclusivo.

1. (Opcional) Desmarque a opção para **[!UICONTROL Share with all advertisers in my account]**.

   Quando você compartilha um público, o público-alvo fica disponível como um destino ou exclusão para todos os anunciantes dentro da conta. No entanto, os segmentos individuais no público-alvo estão disponíveis apenas para usuários aos quais os segmentos são compartilhados. Por exemplo, se você compartilhar um público-alvo contendo segmentos do Adobe Analytics com um anunciante que não está mapeado para a mesma conta [!DNL Analytics], o segmento não será visualizado nesse público-alvo para esse anunciante. Somente os segmentos disponíveis para esse anunciante serão visualizados no público-alvo.

1. Clique em **[!UICONTROL Save]**.

1. Crie o público-alvo:

   >[!NOTE]
   >
   >À medida que você constrói o público-alvo, os [dados do tamanho do público-alvo](audience-about.md) detalhados são atualizados no painel direito.

   * Para criar manualmente a lógica do segmento, usando segmentos disponíveis nas guias [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments] e [!UICONTROL Saved Audiences]](audience-settings.md), faça o seguinte:

      * Para adicionar o primeiro segmento, localize o segmento no painel esquerdo e marque a caixa de seleção ao lado do nome do segmento.

      * Para adicionar um segmento a um grupo de segmentos existente:

         1. Clique no grupo de segmentos no painel direito.

         1. (Opcional) Altere a lógica do grupo para *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, conforme necessário.

            *[!UICONTROL Exclude All]* não está disponível para o primeiro grupo de segmentos. Para um público-alvo que inclua apenas exclusões, crie esse público-alvo como *[!UICONTROL Include Any]* e, em uma disposição, selecione-o no menu Públicos excluídos .

         1. Localize o novo segmento no painel esquerdo e marque a caixa de seleção ao lado do nome do segmento.

            O grupo de segmentos é atualizado automaticamente com o novo segmento.
      * Para adicionar um novo grupo de segmentos:

         1. Clique em **[!UICONTROL + New Group]** no painel direito.

         1. (Opcional) Altere a lógica entre o grupo anterior e o novo para *[!UICONTROL And]* ou *[!UICONTROL Or]*, conforme necessário.

         1. Localize os segmentos do novo grupo no painel esquerdo e marque as caixas de seleção ao lado dos nomes dos segmentos.

         1. (Opcional) Altere a lógica do grupo para *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, conforme necessário.
   * Para usar a lógica de segmento de um público-alvo existente:

      1. Copie a lógica do segmento do público-alvo existente de qualquer uma das seguintes maneiras:

         * Na exibição Todos os públicos , mantenha o cursor sobre a linha de público-alvo e clique em **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * Nas configurações do público-alvo existente, na parte superior do painel lógico do segmento, clique em **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * Em um editor de texto, crie manualmente a lógica do segmento usando IDs de segmento alfanumérico e [Sintaxe booleana](audience-segment-logic-syntax.md), e copie-a na área de transferência.
      1. Clique em **[!UICONTROL paste in an audience rule to begin building]**, cole a lógica de segmento existente no campo de entrada e clique em **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Se o público-alvo já incluir qualquer lógica de segmento, colar na nova lógica de segmento substituirá a lógica existente.




1. Clique em **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de público-alvo](audience-about.md)
>* [Configurações de público-alvo](audience-settings.md)
>* [Sintaxe para lógica de segmento do público-alvo](audience-segment-logic-syntax.md)
>* [Fornecedores de dados de terceiros disponíveis](third-party-data-providers.md)
>* [Criar e implementar um segmento personalizado](custom-segment-create.md)
>* [Criar e implementar um  [!UICONTROL CCPA Opt-Out-of-Sale] segmento](ccpa-opt-out-segment-create.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)

