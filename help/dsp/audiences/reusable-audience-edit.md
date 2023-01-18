---
title: Editar um público-alvo reutilizável
description: Saiba como editar um público-alvo reutilizável.
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Editar um público-alvo reutilizável

Ao editar um público-alvo usado em quaisquer disposições ou outros públicos reutilizáveis, as alterações são aplicadas imediatamente a essas disposições e públicos-alvo.<!-- verify -->

1. No menu principal, clique em **[!UICONTROL Audiences]>[!UICONTROL All audiences]**.

1. Segure o cursor sobre a linha de público-alvo e clique em **[!UICONTROL Edit]**.

1. Edite as configurações do público-alvo de qualquer uma das seguintes maneiras:

   >[!NOTE]
   >
   >Se você editar a lógica do segmento de público-alvo, detalhe [dados de tamanho do público](audience-about.md) é atualizado no painel direito.

   * (Opcional) Para editar o **[!UICONTROL Audience Name]** click ![Editar](/help/dsp/assets/edit.png) ao lado do nome do público-alvo, insira um nome de público-alvo exclusivo e clique em **[!UICONTROL Apply]**.

   * (Opcional) Para editar manualmente a lógica do segmento, usando segmentos disponíveis no [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments]e [!UICONTROL Saved Audiences] guias](audience-settings.md), faça o seguinte.

      * Para adicionar um segmento a um grupo de segmentos existente:
      1. Clique no grupo de segmentos no painel direito.

      1. (Opcional) Altere a lógica do grupo para *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, conforme necessário.

         *[!UICONTROL Exclude All]* não está disponível para o primeiro grupo de segmentos. Para um público-alvo que inclui apenas exclusões, crie este público-alvo como *[!UICONTROL Include Any]* e, em uma disposição, selecione esse público-alvo no menu Públicos excluídos .

      1. Localize o novo segmento no painel esquerdo e marque a caixa de seleção ao lado do nome do segmento.

         O grupo de segmentos é atualizado automaticamente com o novo segmento.
   * Para adicionar um novo grupo de segmentos:

      1. Clique em **[!UICONTROL + New Group]** no painel direito.

      1. (Opcional) Altere a lógica entre o grupo anterior e o novo grupo para *[!UICONTROL And]* ou *[!UICONTROL Or]*, conforme necessário.

      1. Localize os segmentos do novo grupo no painel esquerdo e marque as caixas de seleção ao lado dos nomes dos segmentos.

      1. (Opcional) Altere a lógica do grupo para *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, conforme necessário.
   * Para usar a lógica de segmento de um público-alvo existente:

      1. Copie a lógica do segmento do público-alvo existente de qualquer uma das seguintes maneiras:

         * Na exibição Todos os públicos , mantenha o cursor sobre a linha de público-alvo e clique em **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * Nas configurações do público-alvo existente, na parte superior do painel lógico do segmento, clique em **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * Em um editor de texto, crie manualmente a lógica do segmento usando IDs de segmento alfanumérico e [Sintaxe booleana](audience-segment-logic-syntax.md)e copie-o para a área de transferência.
      1. Clique em **[!UICONTROL paste in an audience rule to begin building]**, cole a lógica de segmento existente no campo de entrada e clique em **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Se o público-alvo já incluir qualquer lógica de segmento, colar na nova lógica de segmento substituirá a lógica existente.





1. Clique em **[!UICONTROL Save]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Continue]**.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de público-alvo](audience-about.md)
>* [Criar um público-alvo reutilizável](reusable-audience-create.md)
>* [Duplicar um público-alvo reutilizável](reusable-audience-duplicate.md)
>* [Exibir detalhes sobre um público-alvo reutilizável](reusable-audience-view-details.md)
>* [Compartilhar um público-alvo reutilizável](reusable-audience-share.md)
>* [Exportar um público-alvo reutilizável](reusable-audience-export.md)
>* [Copiar a chave do segmento para um público-alvo reutilizável para a área de transferência](reusable-audience-clipboard.md)
>* [Excluir um público-alvo reutilizável](reusable-audience-delete.md)
>* [Configurações de público-alvo](audience-settings.md)
>* [Sintaxe para lógica de segmento do público-alvo](audience-segment-logic-syntax.md)
>* [Fornecedores de dados de terceiros disponíveis](third-party-data-providers.md)

