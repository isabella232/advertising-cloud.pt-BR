---
title: 'Ativar segmentos autenticados de parceiros de ID duráveis '
description: Saiba mais sobre como ativar públicos autenticados por meio de uma solução de ID durável.
feature: DSP Audiences
source-git-commit: 8550b539676588c3a6bc07abe088b38bd4251725
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Ativar segmentos autenticados de parceiros de ID duráveis

*Recurso beta*

Para ativar públicos autenticados por meio de uma solução de ID duradoura no Advertising Cloud DSP, os segmentos devem ser traduzidos em [!DNL RampIDs], que são reconhecíveis em um ambiente de oferta. Você pode conseguir isso ao:

* Como aproveitar a integração do DSP com o [!DNL Adobe Real-Time Customer Data Profile (CDP)] e [!DNL Adobe-LiveRamp Retrieval API].

* Enviar manualmente segmentos autenticados para DSP a partir do [!DNL LiveRamp] [!DNL Connect] painel.

## Tarefas

1. Para qualquer uma das opções, entre em contato com `adcloud-support@adobe.com` para ativar as seguintes configurações no DSP, o que permitirá direcionar segmentos autenticados em campanhas DSP uma vez [todas as etapas no fluxo de trabalho de ativação estão concluídas](source-about.md#workflow-sources):

   1. [!DNL LiveRamp] [!DNL RampID] configuração da campanha antes do compartilhamento de segmentos a partir de [!DNL Real-Time CDP].

   1. O nível da conta &quot;[!UICONTROL LiveRamp segments]&quot;.

1. (Os usuários compartilham manualmente segmentos autenticados de [!DNL LiveRamp]) Complete as etapas na seção [!DNL LiveRamp] [!DNL Connect] painel:

   1. Ativar o bloco de destino **[!DNL AAC API 1P Onboarding]**.

   1. Definir [!DNL Identifier Settings] para **[!DNL Ramp ID]** somente.

      ![Configurações do identificador](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Opcional) Se você ainda quiser receber identificadores baseados em cookies, crie um segundo [!DNL AAC API 1P Onboarding] bloco de destino com &quot;[!DNL Cookies],&quot;[!DNL IDFA],&quot; e &quot;[!DNL AAID]&quot; selecionado.

## Práticas recomendadas para teste e validação de dados

* **Target [!DNL RampID]segmentos baseados em cookies e em campanhas separadas.**

   * As configurações de campanha permitem que apenas um identificador seja priorizado.

   * Atualmente, [!DNL RampIDs] não são recuperáveis durante eventos no site. Isso significa que determinadas metas personalizadas, como o CPA mais baixo e o ROAS, não estão disponíveis com o uso de segmentos autenticados. Use segmentos baseados em cookies somente se você tiver um KPI de desempenho restritivo.

* **Crie uma disposição em ambas as [!DNL RampID] e campanhas baseadas em cookies.**

   * Direcione os segmentos compartilhados a partir de [!DNL LiveRamp] usando o processo de ativação de segmento padrão.

   * Trabalhe com a equipe de suporte da Advertising Cloud para validar a distribuição de dados adequada.

Para saber mais sobre a integração do DSP com o [!DNL LiveRamp], contato `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>*[Sobre a ativação de segmentos autenticados de fontes de público-alvo](source-about.md)
>* [Criar uma fonte de público-alvo para ativar públicos-alvo primários](source-create.md)
>* [Configurações de origem do público-alvo](source-settings.md)
>* [Conexão Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)

