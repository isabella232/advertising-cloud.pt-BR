---
title: Configurações personalizadas de relatório
description: Consulte descrições das configurações personalizadas do relatório.
feature: DSP Custom Reports
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 0%

---

# Configurações personalizadas de relatório

**[!UICONTROL Name]** O nome do relatório. O comprimento máximo é de 180 caracteres.

**[!UICONTROL Report Type]** O tipo de relatório: *[!UICONTROL Custom]* (que inclui a maioria das opções disponíveis), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*,  *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*,  *[!UICONTROL Segment]* ou *[!UICONTROL Site]*.

## [!UICONTROL Apply Filters] Seção

**[!UICONTROL Timezone]:** O fuso horário para relatórios.

**[!UICONTROL Observe Daylight Savings Time]:** Considera o Horário de verão nos horários relatados.

**\[Intervalo de datas\]:** O intervalo de datas para o qual gerar dados. O número de dias disponíveis varia de acordo com o relatório e as dimensões selecionadas. Escolha um:

* **[!UICONTROL Previous N days]:** Inclui dados de um número específico de dias antes de hoje.

* **[!UICONTROL Custom]:** Inclui dados entre datas de início e término específicas. Para relatar dados até o dia anterior, selecione **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]:** Inclui dados do mês anterior.

**[!UICONTROL Add Filters]:** (Opcional) Dimensões adicionais pelas quais filtrar os dados, independentemente das dimensões serem incluídas como colunas no relatório: *[!UICONTROL Account]*,\* *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Placement]*, *[!UICONTROL Ad]*, *[!UICONTROL Ad Type]*, *[!UICONTROL Video]*, *[!UICONTROL Video Duration]*, *[!UICONTROL Country]* e *[!UICONTROL Package]*.

\* *[!UICONTROL Account]* está disponível para os seguintes tipos de relatório somente quando sua organização está configurada para [relatório entre contas](report-about.md#cross-account-reporting):  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)]e [!UICONTROL Conversion]. Entre em contato com seu [!DNL Adobe] equipe de contas para obter mais informações sobre relatórios entre contas.

Para aplicar um ou mais filtros, faça o seguinte:

* Selecione uma dimensão, selecione o operador (*igual* ou *não é igual*) e, em seguida, selecione o valor aplicável. Por exemplo, para retornar dados apenas de anúncios precedentes, especifique &quot;[!UICONTROL Ad Type equals Preroll].&quot;
* (Opcional) Adicione critérios adicionais ao filtro.
* (Opcional) Adicione filtros adicionais, cada um com um ou mais critérios.

## [!UICONTROL Build Your Report] Seção

**[!UICONTROL Select To Add As Report Headers]:**  As colunas de dados, ou cabeçalhos, a serem incluídos no relatório. Para adicionar uma coluna, expanda a categoria e marque a caixa de seleção ao lado do nome da coluna. Todas as métricas indisponíveis estão desativadas. As categorias de dados disponíveis incluem:

* [!UICONTROL  Dimensions]
* [!UICONTROL Metrics]
* [!UICONTROL Conversion Metrics] (classificado pelo anunciante)
* [!UICONTROL Custom Goals] (classificado pelo anunciante)

**[!UICONTROL Drag to Re-Order Report Headers Below]:** A ordem dos cabeçalhos da coluna. Você pode arrastar e soltar qualquer coluna para personalizar a ordem.

## [!UICONTROL Multi-Touch Conversion Options] Seção

**[!UICONTROL Format]:** Se um relatório será gerado em *[!UICONTROL CSV]* (valores separados por vírgula) ou *[!UICONTROL Tab]* Formato (valores separados por tabulação).

**[!UICONTROL Report Headers]:** Se *[!UICONTROL Include]* ou *[!UICONTROL Do Not Include]* cabeçalhos da coluna.

**[!UICONTROL Attribution Rule Settings]:** (Todos [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]e [!UICONTROL Site] relatórios com [!UICONTROL Conversion Metrics] ou [!UICONTROL Custom Goals] colunas; publicitários com rastreamento de conversão de Adobe Advertising somente) No relatório, como atribuir dados de conversão em uma série de eventos que levam a uma conversão. Você pode escolher mais de uma regra se quiser comparar diferenças entre elas.

>[!NOTE]
>
>Os caminhos de conversão incluem impressões e cliques nas janelas de pesquisa de impressões ou cliques do anunciante, que estão configuradas em [!DNL Adobe Advertising Search]. Os cliques recebem preferência por impressões durante a atribuição da conversão. Todos os cliques em um caminho de conversão recebem crédito total com base na regra de atribuição. As impressões recebem crédito somente quando nenhum clique é rastreado no caminho de conversão.

* *[!UICONTROL Last Event]:* Atribui conversões ao último clique ou impressão no caminho de conversão.

* *[!UICONTROL Weight Last More]:* Atribui conversões a todos os eventos no caminho de conversão, mas dá mais peso ao último evento e menos peso sucessivamente aos eventos anteriores.

* *[!UICONTROL Even Distribution]:* Atribui conversões igualmente a cada evento no caminho de conversão.

* *[!UICONTROL Weight First More]:* Atribui conversões a todos os eventos no caminho de conversão, mas dá mais peso ao primeiro evento e menos peso sucessivamente aos eventos a seguir.

* *[!UICONTROL First Event]:* Atribui conversões ao primeiro clique ou impressão no caminho de conversão.

* *[!UICONTROL U-shaped]:* Atribui a conversão a todos os eventos no caminho de conversão, mas atribui mais peso ao primeiro e ao último eventos, com sucessivamente menos peso aos eventos no meio do caminho de conversão.

* *[!UICONTROL Display Only]:*  Atribui conversões ao último clique DSP ou impressão no caminho de conversão. Isso inclui vídeo e anúncios de TV conectados e exclui cliques em [!DNL Adobe Advertising Search] anúncios.

* *[!UICONTROL Social Only]:* Obsoleto

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

**[!UICONTROL Paths as Columns]:**  (Todos [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]e [!UICONTROL Site] relatórios com [!UICONTROL Conversion Metrics] ou [!UICONTROL Custom Goals] colunas) Quais tipos de conversões relatar quando eventos anteriores ocorreram no mesmo dispositivo. É possível incluir até três tipos. Para cada tipo selecionado, uma coluna separada é incluída para cada métrica de conversão e é anexada com o sufixo especificado ([!UICONTROL (tl)], [!UICONTROL (ct)]ou [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Inclui conversões atribuídas a cliques (CT para click-through) e a impressões (VT para view-through). As conversões atribuídas a impressões são multiplicadas pelo peso de view-through especificado. O peso de view-through padrão é de 100%, o que significa que as conversões atribuídas a impressões são contadas como 100% do valor das conversões atribuídas aos cliques.

* *[!UICONTROL With Clicks (CT)]:* Inclui apenas conversões atribuídas a cliques.

* *[!UICONTROL Impressions Only (VT)]:* Inclui apenas conversões que foram atribuídas a impressões porque nenhum clique foi rastreado no caminho de conversão.

**[!UICONTROL Conversion Reporting Based On]:**  Como relatar dados de conversão:

* *[!UICONTROL Conversion Timestamp]:* (O padrão) As conversões serão associadas à data de conversão.

* *[!UICONTROL Event Timestamp]:* As conversões serão relatadas com base na data da impressão ou do clique que causou a conversão, conforme determinado pelo [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] Seção

**[!UICONTROL Destination Type]:** Escolha um dos seguintes tipos de destino:

* *[!UICONTROL S3]:* Para enviar o relatório concluído para um ou mais [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]), que você especificará na **[!UICONTROL Destination Name]** campo.
* *[!UICONTROL sFTP]:* Para enviar o relatório concluído para um ou mais locais SFTP, que você especificará na variável **[!UICONTROL Destination Name]** campo.
* *[!UICONTROL FTP]:* Para enviar o relatório concluído para um ou mais locais FTP, que você especificará na variável **[!UICONTROL Destination Name]** campo.
* *[!UICONTROL FTP SSL](Atualmente em Beta):* Para enviar o relatório concluído para um ou mais locais FTP SSL, que você especificará na variável **[!UICONTROL Destination Name]** campo.
* *[!UICONTROL Email]:* Especificação dos endereços de email para os quais enviar relatórios concluídos ou notificações se o relatório for cancelado por causa de erros. Para especificar vários endereços, separe-os com vírgulas ou espaços.

>[!NOTE]
>
> Não é possível alterar o tipo de destino depois de salvar o relatório.

**[!UICONTROL Destination Name]:** (Tipos de destino SSL S3, FTP, sFTP e FTP apenas) Os nomes dos destinos do relatório para os quais o relatório personalizado será enviado.

* Para especificar um destino existente, selecione um nome de destino na lista. Você pode selecionar vários nomes de destino separadamente.

* Para criar um novo destino:

   1. Clique em **Adicionar novo destino**.

   1. Insira o [configurações de destino do relatório](/help/dsp/reports/report-destinations/report-destination-settings.md)e clique em **Salvar**.

   1. De volta às configurações do relatório, clique em **Atualizar nomes de destino.**

      O novo destino agora está disponível na lista de destinos existentes e, como opção, é possível adicioná-lo ao relatório.

**[!UICONTROL Frequency]:** (Para cada [!UICONTROL Destination Name] Com que frequência enviar o relatório para o destino: *[!UICONTROL Once]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]* ou *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] Seção

**[!UICONTROL Send & Save]:** Quando enviar o relatório: *[!UICONTROL On Schedule]* ou *[!UICONTROL Run Now]*. Os relatórios agendados serão entregues até às 09:00, no fuso horário da conta.

>[!NOTE]
>
>Você pode [executar um relatório personalizado a qualquer momento](report-run-now.md) do [!UICONTROL Reports] exibir.

>[!MORELIKETHIS]
>
>* [Sobre Relatórios Personalizados](/help/dsp/reports/report-about.md)
>* [Criar um relatório personalizado](/help/dsp/reports/report-create.md)
>* [Duplicar um relatório personalizado](/help/dsp/reports/report-copy.md)
>* [Editar um relatório personalizado](/help/dsp/reports/report-edit.md)
>* [Executar um relatório personalizado](/help/dsp/reports/report-run-now.md)
>* [Configurações personalizadas de relatório](/help/dsp/reports/report-settings.md)
>* [Sobre destinos de relatórios](/help/dsp/reports/report-destinations/report-destination-about.md)

* [Colunas de Relatório Disponíveis](/help/dsp/reports/report-columns.md)
