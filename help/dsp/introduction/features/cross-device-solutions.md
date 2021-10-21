---
title: Soluções entre dispositivos
description: Saiba mais sobre recursos entre dispositivos.
feature: DSP Introduction
exl-id: 29f8ec41-35a6-4a29-a638-82a2929a8fe6
source-git-commit: e0713f3717a684fb5ef2808d7de769424b8972d2
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 0%

---

# Soluções entre dispositivos

Integrações do Advertising Cloud DSP com [!DNL LiveRamp] e [!DNL Adobe Device Co-op] permita estender seu público-alvo para todos os dispositivos conhecidos de uma pessoa, não apenas os dispositivos que sua marca rastreou. As integrações também fornecem limite de frequência e medição de atribuição em todos os dispositivos.

Ao usar um gráfico de dispositivos com base em pessoas, é possível:

* Combine públicos-alvo em canais e dispositivos para fornecer anúncios para pessoas e residências, em vez de dispositivos.
* Equilíbrio e exposição por meio da compreensão e limitação da frequência entre indivíduos.
* Testar estratégias que expõem e convertem públicos-alvo em canais ou dispositivos.

## Benefícios de cada gráfico de dispositivos

* [!DNL Adobe Device Co-op]:
   * Fornece um pool de aceitação dos dados determinísticos e probabilísticos dos anunciantes do Adobe participantes
   * Fornece conexões de ID de cookie potentes fornecidas por visitantes da Web móveis e de desktop
   * Inclui dados predominantemente dos Estados Unidos e Canadá
   * Não tem taxas de uso

* [!DNL LiveRamp] gráfico de dispositivos:
   * Fornece um pool de dados determinístico, incluindo dados offline do cliente
   * Fornece cobertura uniforme entre IDs de cookies e IDs de dispositivos móveis
   * Inclui dados predominantemente dos Estados Unidos
   * É gratuito para limite de frequência e medição de atribuição
   * Preço de US$ 0,35 CPM para impressões estendidas (impressões que são fornecidas apenas com o uso da variável [!DNL LiveRamp] gráfico de dispositivos em vez de em dispositivos encontrados nos segmentos de público-alvo direcionados)

      A taxa é refletida no seu cartão de taxa de conta.

## Gerenciamento de frequência com base em pessoas

O gerenciamento de frequência com base em pessoas permite especificar limites de frequência no nível da pessoa, em vez do nível do dispositivo, para o controle de exposição da mídia verdadeiro.

### Ativar o gerenciamento de frequência com base em pessoas

* **Campanhas:** Ao criar uma nova campanha, você pode especificar uma [!UICONTROL Cross-Device Level] configuração. Ativar &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People],&quot; e selecionar um gráfico de dispositivos. O gráfico de dispositivos especificado é usado para o direcionamento entre dispositivos no nível de posicionamento e para o gerenciamento de frequência com base em pessoas no nível de campanha, pacote e posicionamento. Os limites de frequência se aplicam a todos os dispositivos conhecidos de uma pessoa.

Para obter mais informações, consulte [Configurações da campanha](/help/dsp/campaign-management/campaigns/campaign-settings.md).

Depois de salvar uma campanha, você não pode alterar sua [!UICONTROL Cross Device Level] configuração.

* **Pacotes:**  Opcionalmente, é possível definir limites de frequência adicionais no nível do pacote. DSP respeitará o limite de frequência mais restrito na hierarquia da campanha.

* **Disposições:** Opcionalmente, é possível definir limites de frequência adicionais no nível de posicionamento. DSP respeitará o limite de frequência mais restrito na hierarquia da campanha.

## Direcionamento baseado em pessoas

O direcionamento com base em pessoas permite encontrar clientes em computadores e dispositivos móveis.

### Ativar direcionamento com base em pessoas

* **Campanhas:** Ao criar uma nova campanha, você pode especificar uma [!UICONTROL Cross-Device Level] configuração. Ativar &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People],&quot; e selecionar um gráfico de dispositivos. O gráfico de dispositivos especificado é usado para o direcionamento entre dispositivos no nível de posicionamento e para o gerenciamento de frequência com base em pessoas.

Para obter mais informações, consulte [Configurações da campanha](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **Disposições:** Quando você seleciona públicos-alvo para uma disposição em uma campanha com um gráfico de dispositivos especificado, uma [!UICONTROL Cross-Device Targeting] permite estender sua definição de metas em todos os dispositivos conhecidos de uma pessoa (de acordo com o gráfico de dispositivos especificado nas configurações da campanha), até mesmo em dispositivos que não estão nos segmentos especificados.

### Configurar relatórios para direcionamento com base em pessoas

Você pode incluir as seguintes métricas em relatórios personalizados:

* **Impressões estendidas:** (No [!UICONTROL Build Your Report] seção sob [!UICONTROL Metrics] > [!UICONTROL Std. Metrics]) O volume de impressões incrementais fornecidas por meio do aproveitamento de um gráfico de dispositivos (e não encontradas nos segmentos originais do público-alvo). Essa métrica também é usada para calcular as tarifas aplicáveis associadas ao uso de um gráfico de dispositivos de terceiros.

   Para determinar o custo de suas impressões estendidas durante um período de tempo, execute um relatório personalizado que inclua a variável [!UICONTROL Extended Impressions] e multiplique o número total de impressões estendidas por $0.00035 (US$0.35/1000 impressões).

   O custo agregado também é incluído na variável [!UICONTROL Billable Other Net Spend] coluna (em [!UICONTROL Metrics] > [!UICONTROL Spend]), embora essa métrica também inclua outras tarifas de campanha que você pode ter adicionado.

* **Gráfico de dispositivos:** (No [!UICONTROL Build Your Report] seção sob [!UICONTROL Dimensions] > [!UICONTROL Campaign]) O gráfico de dispositivos selecionado para uma campanha, pacote ou disposição específico.

## Medição de atribuição baseada em pessoas

*Anunciantes com rastreamento de conversão do Advertising Cloud somente*

Com a atribuição baseada em pessoas, você pode atribuir conversões que ocorreram em um dispositivo diferente daquele no qual a exposição da mídia ocorreu. A medição de atribuição baseada em pessoas está disponível em DSP, Advertising Cloud Search e Advertising Cloud Creative para anunciantes que implementaram pixels de conversão do Advertising Cloud em seus sites.

### Ativar a medição de atribuição baseada em pessoas

Se você deseja ativar a medição de atribuição entre dispositivos, entre em contato com seu [!DNL Adobe] gerente de conta. Para [!DNL Adobe Device Co-op] , você precisará fornecer sua assinatura [!DNL Adobe Device Co-op] contrato e Experience Cloud [!DNL Organization ID] (anteriormente chamado de [!DNL IMS org ID]).

Para ver se uma conta de anunciante está configurada para usar um gráfico de dispositivos para medição de atribuição:

1. No menu principal, clique em **[!UICONTROL Settings]>[!UICONTROL Advertiser]**.
1. Mantenha o cursor sobre a linha do anunciante e clique em **[!UICONTROL Edit]**.
1. No [!UICONTROL Integrations] das configurações do anunciante, veja se a variável [!UICONTROL Cross-Device Attribution] está ativa.

   Para integrações ativas, o gráfico do dispositivo é indicado.

### Configurar relatórios de conversão para atribuição de conversão entre dispositivos

#### Configurações do relatório de conversão

Quando um gráfico de dispositivos é ativado para medição de atribuição, a variável [!UICONTROL Conversion] O relatório inclui uma [!UICONTROL Cross-Device Breakout] , que permite incluir até três colunas separadas para cada métrica de conversão, incluindo:

* &lt;*Conversão*>[!UICONTROL (tp)]: Inclui o total de conversões (total de pessoas), que inclui conversões de mesmo dispositivo e conversões entre dispositivos (se aplicável). No relatório, &quot;[!UICONTROL (tp)]&quot; é anexado ao nome da métrica de conversão, ao tipo de regra e aos tipos de conversão no caminho de conversão (por exemplo, &quot;Responses(le)(tl)(tp)&quot;).

* &lt;*Conversão*>[!UICONTROL (sd)]: (Opcional) Inclui apenas conversões para as quais apenas um único dispositivo foi rastreado no caminho de conversão. No relatório, &quot;[!UICONTROL (sd)]&quot; é anexado ao nome da métrica de conversão, ao tipo de regra e aos tipos de conversão no caminho de conversão (por exemplo, &quot;Responses(le)(tl)(sd)&quot;.

* &lt;*Conversão*>[!UICONTROL (xd)]: (Opcional) Inclui apenas conversões para as quais mais de um dispositivo foi rastreado no caminho de conversão. No relatório, &quot;[!UICONTROL (xd)]&quot; é anexado ao nome da métrica de conversão, ao tipo de regra e aos tipos de conversão no caminho de conversão (por exemplo, &quot;Responses(le)(tl)(xd)&quot;.

#### Como interpretar o relatório de conversão

Se você classificar a porcentagem do total de conversões que são entre dispositivos ([!UICONTROL (xd)]/[!UICONTROL (tl)]) de alto a baixo, você entenderá o que está gerando conversões entre dispositivos acima da média. Você pode usar isso para informar sua estratégia de criação ou direcionamento para corresponder mensagens e investimento em canal ao comportamento do usuário.

* Pacotes - Veja quais pacotes direcionam a maioria das conversões totais e quais têm uma alta porcentagem de conversões entre dispositivos. Isso pode ajudá-lo a entender onde se concentrar os gastos.

* Disposições - Compare o desempenho da disposição e a atribuição (por exemplo, um anúncio da Web para dispositivos móveis pode gerar conversões no desktop). Sem um gráfico de dispositivos para atribuição, você pode perder o impacto de uma disposição da Web móvel nas conversões da área de trabalho ou ela pode ser enterrada se a maioria dos usuários converter na área de trabalho e não na Web móvel.

* Anúncios - Descubra quais anúncios impulsionam conversões mais altas e quantificar seu valor e impacto em navegadores da Web e ambientes de aplicativos móveis.

* Sites - Otimize em todos os sites, em vez de excluir manualmente os sites completamente. Se um site gerar conversões entre dispositivos, você poderá ver em quais dispositivos esse comportamento ocorre.

* Ofertas - Melhore a otimização manual verificando quais ofertas de inventário oferecem conversões entre dispositivos e, em seguida, decidindo se você deve expandir seu direcionamento para incluir mais dispositivos e canais nessas negociações.

>[!MORELIKETHIS]
>
>* [Configurações do relatório](/help/dsp/reports/report-settings.md)
>* [Configurações da campanha](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)

