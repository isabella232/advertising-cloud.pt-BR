---
title: Sobre Relatórios Personalizados
description: Saiba mais sobre as opções para criar relatórios personalizados manualmente ou usando modelos de relatório pré-configurados.
feature: DSP Custom Reports
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# Sobre Relatórios Personalizados

Os relatórios personalizados permitem personalizar o conteúdo e a entrega dos dados do relatório usando as dimensões da campanha (como anunciante, posicionamento, sites ou regiões) e as métricas mais importantes para você. Você pode:

* Configure completamente os relatórios de desempenho da campanha em um nível granular.
* Escolha entre templates de relatório pré-configurados e, opcionalmente, personalize-os ainda mais.

Você pode gerar relatórios uma vez ou agendá-los para serem gerados diariamente, semanalmente ou mensalmente às 03:00 no fuso horário especificado. Depois que um relatório é gerado, ele é entregue a cada recipient de email especificado ou vinculado [destinos de relatório](/help/dsp/reports/report-destinations/report-destination-about.md) dos seguintes tipos:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SFTP
* SSL FTP (em beta)

>[!NOTE]
>
>Você também pode visualizar dados sob demanda em todos os níveis de uma campanha (campanha, pacote, disposição ou anúncio) [na visualização de gestão de campanha relevante](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Tipos de relatórios disponíveis

* **[!UICONTROL Custom]:** Este relatório é um modelo em branco que pode ser usado para criar seu próprio relatório personalizado usando a maioria das dimensões e métricas. [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo]e [!UICONTROL Site] os relatórios são variações desse modelo com colunas e dimensões pré-selecionadas para os respectivos casos de uso.

* Modelos de relatório pré-configurados

   * **[!UICONTROL Billing]:** Use este relatório para entender as métricas principais de faturamento, como métricas de gasto para faturamento de mídia por campanha.

      >[!NOTE]
      >
      >Este relatório inclui dados sobre o segmento de faturamento. Se um usuário ou dispositivo receber uma impressão que pertence a vários segmentos, somente um segmento faturável será creditado com a impressão.

   * **[!UICONTROL Conversion]:** Use este relatório para entender o desempenho de suas campanhas com base nas métricas de conversão capturadas por meio do rastreamento de conversão do Adobe Advertising. Este relatório inclui atribuição de multitoque.

   * **[!UICONTROL Device]:** Use esse modelo preenchido previamente para ver as métricas principais por dimensões relacionadas ao dispositivo.

   * **[!UICONTROL Frequency (by Impression)]:** Use esse relatório para entender a distribuição de impressões mostradas para visualizadores únicos (por exemplo, quantos visualizadores únicos viram uma impressão, duas impressões, três impressões e assim por diante). Os dados estão disponíveis por posicionamento ou campanha.

      >[!NOTE]
      >
      >* Os dados estão disponíveis após 1 de março de 2019.
      >* A frequência é estimada com base numa amostragem de dados.
      >* Para alguns inventários, os editores não transmitem um identificador de dispositivo, o que impede o rastreamento de frequência. Este relatório inclui apenas impressões para as quais um identificador de dispositivo estava disponível.


   * **[!UICONTROL Frequency (by App/Site)]:** Use esse relatório para entender quantos usuários únicos foram acessados por aplicativo ou por site. Você também pode ver quantos usuários únicos foram acessados somente por um aplicativo ou site específico (&quot;usuários únicos distintos&quot;).

      >[!NOTE]
      >
      >* Os dados estão disponíveis após 15 de novembro de 2018.
      >* Para um inventário privado, os editores não transmitem um identificador de dispositivo, o que impede o rastreamento de frequência.


   * **[!UICONTROL Geo]**: Use esse modelo preenchido previamente para ver as métricas principais por dimensões geográficas.

   * **[!UICONTROL Margin]:** Use este relatório para ver métricas principais como margem, lucro e outras métricas de gasto por campanha ou disposição.

   * **[!UICONTROL Segment]:** Use esse modelo preenchido previamente para ver as métricas principais por segmento.

      >[!NOTE]
      >
      >* Este relatório tem como objetivo mostrar o desempenho de diferentes segmentos direcionados. Ele usa dados de associação de segmento. Quando uma impressão é enviada para uma pessoa ou dispositivo que pertence a dois ou mais segmentos direcionados, esse relatório inclui uma linha para cada segmento. Por esse motivo, os totais neste relatório podem não corresponder ao delivery real.
      >* Métricas de conversão e dados de meta personalizados para segmentos estão disponíveis após 2 de agosto de 2019. Todos os outros dados para segmentos estão disponíveis a partir de 1 de junho de 2018.


   * **[!UICONTROL Site]:** Por padrão, inclui métricas padrão, total de gasto líquido de mídia e total de gasto líquido faturável por site.

## Relatórios entre contas {#cross-account-reporting}

Qualquer organização com várias contas DSP pode, opcionalmente, habilitar dados entre contas em relatórios personalizados, de acordo com as necessidades da organização. Por exemplo, você pode conceder à Conta A acesso aos dados da Conta B e conceder à Conta B acesso aos dados da Conta C (mas não à Conta A). Para habilitar e configurar esse recurso, entre em contato com seu [!DNL Adobe] equipe da conta.

Depois que o recurso estiver ativado para a sua organização, você poderá [filter](report-settings.md) qualquer um dos seguintes tipos de relatório por conta:  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)]e [!UICONTROL Conversion].

Suas configurações de conta em [!UICONTROL Settings] > [!UICONTROL Account] indicar a) as outras contas cujos dados estão disponíveis para sua conta e b) as outras contas que podem acessar os dados de sua conta.

>[!MORELIKETHIS]
>
>* [Criar um relatório personalizado](/help/dsp/reports/report-create.md)
>* [Configurações personalizadas de relatório](/help/dsp/reports/report-settings.md)
>* [Sobre relatórios na plataforma](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Colunas de Relatório Disponíveis](/help/dsp/reports/report-columns.md)
>* [Sobre [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)

