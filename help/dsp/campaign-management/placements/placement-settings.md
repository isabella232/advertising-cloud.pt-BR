---
title: Configurações de posicionamento
description: Consulte descrições das configurações de posicionamento disponíveis.
feature: DSP Placements
exl-id: 36097132-e589-4d49-bf86-54f61eae5b67
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '3281'
ht-degree: 0%

---

# Configurações de posicionamento

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** O nome da disposição.

>[!TIP]
>Use uma convenção de nomenclatura que faça sentido para sua situação. Uma convenção de nomenclatura sugerida é &quot;*\&lt;Nome da Campanha\>: \&lt;Ad Unit\>: \&lt;Duração\>: \&lt;Targeting\>*.&quot;

**[!UICONTROL Status]:** O status da disposição:  *[!UICONTROL Active]* (o padrão) ou  *[!UICONTROL Paused]*.

>[!TIP]
>A prática recomendada é pausar a disposição até que você esteja pronto para iniciá-la.

**[!UICONTROL Details]:**  (somente leitura) o tipo de anúncio aplicável, a conta que está criando ou criando a disposição e a campanha principal. Para ver mais detalhes, clique em **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** abre uma lista de modelos de disposição existentes. Para preencher automaticamente as configurações de direcionamento a partir de um modelo:

1. Siga um destes procedimentos:

   * Para reutilizar todo o target de um modelo, marque a caixa de seleção ao lado do nome do modelo.

   * Para reutilizar tipos de alvos individuais a partir de um modelo, expanda o nome do modelo e marque a caixa de seleção ao lado dos tipos de alvo que deseja reutilizar.

1. Clique em **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:**  (somente formatos de anúncio de vídeo) A duração do anúncio e/ou as especificações do anúncio, que são usadas para calcular a projeção de Previsão à direita. Os campos variam de acordo com o tipo de anúncio.

**[!UICONTROL Placement tags]:** (Opcional) Palavras-chave ou apelidos para ajudar a localizar essa disposição.

## Metas

**[!UICONTROL Package]:** (opcional) um pacote ao qual a disposição é atribuída. Clique em ![Edit](/help/dsp/assets/edit.png) para selecionar um pacote existente ou criar um novo pacote. Quando você atribui a disposição a um pacote, a seção [!UICONTROL Goals] é atualizada com as datas de voo, o objetivo da entrega e o orçamento do pacote.

**[!UICONTROL Flight Dates]:** a data de início e de término da disposição. Anúncios aprovados são elegíveis para serem executados durante o voo, quando a disposição estiver ativa e for atribuída a um pacote ativo ou campanha.

As datas do pacote (quando aplicável) ou da campanha são preenchidas automaticamente por padrão.

>[!NOTE]
>
>* As datas de voo devem ser incluídas nas datas de voo da campanha e nas datas de voo do pacote.


### Disposições atribuídas a pacotes com Pacote no nível do pacote

**[!UICONTROL Placement Funding]:** Como orçar para a disposição:

* *[!UICONTROL Optimize based on performance]:* controla o orçamento no nível do pacote.
* *[!UICONTROL Set a fixed budget cap]:* permite definir um orçamento de disposição diário, semanal, mensal ou sempre. Insira um valor e a duração (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Max Bid]:** o máximo a ser pago por 1000 impressões.

**[!UICONTROL Placement Pre-bid Filters]:** Até cinco limites de KPI (como uma métrica mínima de visibilidade ou taxa de click-through) que devem ser atendidos para que a licitação ocorra. Você pode usar filtros pré-lances como táticas de otimização, mas entender que cada regra pode limitar as oportunidades nas quais essa disposição pode lance. Para adicionar ou editar filtros:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Siga um destes procedimentos:
   * Para adicionar um filtro:
      1. Clique em **[!UICONTROL Add Filter]**.
      1. Ao lado de **[!UICONTROL Only bid if]**, selecione uma métrica e insira um valor.
   * Para remover um filtro, clique em **[!UICONTROL X]** na linha de filtro.
1. Clique em **[!UICONTROL Save]**.

Consulte descrições de cada filtro pré-lance em &quot;[Filtros pré-lances de nível de posicionamento e Como usá-los](/help/dsp/optimization/optimization-pre-bid-filters.md)&quot;.

### Todas as outras disposições

**[!UICONTROL Budget Goal]:** o limite bruto do orçamento e o intervalo do orçamento (*[!UICONTROL All time]*,  *[!UICONTROL Daily]*,  *[!UICONTROL Weekly]*,  *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:**  (Disposições em campanhas somente com gerenciamento de margem) O limite bruto do orçamento e o intervalo do orçamento (*[!UICONTROL All time]*,  *[!UICONTROL Daily]*,  *[!UICONTROL Weekly]*,  *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:**  A meta de otimização do pacote. Consulte descrições de cada meta de otimização em &quot;[Metas de otimização e Como usá-las](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** a meta, que é usada para rastrear o desempenho.

>[!NOTE]
>
>Este campo é apenas um referencial e não é usado para a tomada de decisão.

**[!UICONTROL Pace on]:** Em que ritmo será baseado:

* **[!UICONTROL Budget goal]:** (padrão) essa opção fornece o máximo de impressões possível dentro do orçamento alocado.

* **[!UICONTROL Impressions]:** essa opção fornece impressões até que uma quantidade específica seja alcançada em um intervalo especificado. Ao selecionar essa opção, especifique o número de impressões e o intervalo: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** o máximo a ser pago por 1000 impressões.

**[!UICONTROL Pacing Fill Strategy]:** (Pacotes com pacing no nível do pacote somente) Como carregar e fornecer:

* *[!UICONTROL Even]:* (o padrão) Os pacotes são distribuídos uniformemente em cada voo, com um target de 50% do delivery na primeira metade do voo.

* *[!UICONTROL Frontload]:* acelera a entrega para que esteja entre 65 e 75% completo na metade do voo.

* *[!UICONTROL Aggressive Frontload]:* acelera a entrega para que esteja 75 a 85% completo na metade do voo.

**[!UICONTROL Placement Pre-bid Filters]:** (Opcional) Até cinco filtros que devem ser atendidos para que a licitação ocorra. Você pode usar filtros pré-lances como táticas de otimização, mas lembre-se de que cada regra pode limitar as oportunidades nas quais essa disposição pode lance. Para adicionar ou editar filtros:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Siga um destes procedimentos:
   * Para adicionar um filtro:
      1. Clique em **[!UICONTROL Add Filter]**.
      1. Ao lado de **[!UICONTROL Only bid if]**, selecione uma métrica e insira um valor.
   * Para remover um filtro, clique em **[!UICONTROL X]** na linha de filtro.
1. Clique em **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Opcional) Locais específicos nos quais incluir ou excluir anúncios na disposição. Se você não especificar nenhuma localização, todas as localizações serão direcionadas.

>[!NOTE]
>
>Locais de cidade e DMA não estão disponíveis para inserções do Roku.

Para especificar localizações:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Siga um destes procedimentos:
   * Para incluir ou excluir um País, Estado, Cidade, DMA, Distrito Legislativo Federal ou Distrito Legislativo do Estado:
      1. Selecione o tipo de local na coluna esquerda.
      1. (Conforme necessário) Clique em um local para expandi-lo.
      1. Ao lado do local, clique em *[!UICONTROL Include]* para incluí-lo como target ou *[!UICONTROL Exclude]* para excluí-lo como target.
   * Para procurar um código postal e incluir ou excluir todos os resultados selecionados:
      1. Clique em **[!UICONTROL Search Postal Code]**.
      1. Selecione o país.
      1. Insira o nome da cidade e clique em ![Edit](/help/dsp/assets/search.png).
      1. Clique no resultado de pesquisa correto.
      1. Clique em *[!UICONTROL Include All]* para incluir todos os locais como alvos ou *[!UICONTROL Exclude All]* para excluir todos os locais como alvos.
   * Para inserir ou colar códigos postais e incluir ou excluir todos:
      1. Clique em **[!UICONTROL Paste Postal Code]**.
      1. Selecione o país.
      1. Insira ou cole até 1000 códigos postais.
Inclua um código postal por linha ou insira vários valores separados por vírgulas ou guias.
      1. Clique em *[!UICONTROL Include All]* para incluir todos os locais como alvos ou *[!UICONTROL Exclude All]* para excluir todos os locais como alvos.
   * Para remover um local da lista [!UICONTROL Included] ou [!UICONTROL Excluded], clique em **[!UICONTROL X]** ao lado do local na coluna direita.
1. Clique em **[!UICONTROL Done]**.

>[!NOTE]
>
>* Nem todos os países têm localizações de Estado, Cidade ou Código Postal.
>* A DMA (área de mercado designada), os Distritos Legislativos Federais e os Distritos Legislativos Estaduais estão disponíveis apenas para os Estados Unidos.


## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Fontes de inventário para incluir ou excluir como alvos. Para a maioria dos tipos de disposição, todos os tipos de inventário e todas as fontes para cada tipo são incluídos por padrão. Para disposições [!DNL Roku], você deve especificar o tipo de inventário e as fontes. Você pode escolher entre os seguintes tipos de inventário:

* [!UICONTROL Public]: (Todos os tipos de disposição exceto Roku) Todo o inventário de troca aberto ao qual a Advertising Cloud tem acesso. É possível incluir e excluir o inventário público.

   É possível exibir a lista por origem ou por feed. Ao exibir a lista por feed, é possível pesquisar por nome de feed, chave de feed ou uma tag característica selecionada.

* [!UICONTROL Private] |  [!UICONTROL Roku Private]: Suas ofertas privadas existentes (ou  [!DNL Roku] ofertas privadas existentes para  [!DNL Roku] disposições) com editores que você configurou em DSP. É possível incluir, mas não excluir, o inventário público.

   Você pode pesquisar a lista por palavra-chave, chave, ID da transação ou tag personalizada.

* [!UICONTROL On Demand] |  [!UICONTROL Roku On Demand]: Todo o  [inventário [!UICONTROL On Demand]  premium não garantido (ou ofertas ](/help/dsp/inventory/on-demand-inventory-about.md) Roku para  [!UICONTROL On Demand] [!DNL] disposições) no qual você se inscreveu  [!DNL Roku]   [!DNL DSP]. Você pode incluir e excluir o inventário [!UICONTROL On Demand].

   É possível exibir a lista por origem ou por feed. Ao exibir a lista por feed, você pode pesquisar por nome de feed, chave de feed ou uma região do editor, tag de categoria ou tag característica selecionada.

Para especificar o direcionamento de inventário:

* Para excluir um tipo de inventário, desmarque a caixa de seleção ao lado do nome.
* Para direcionar um tipo de inventário:
   1. Marque a caixa de seleção ao lado do nome do tipo de inventário.
   1. (Opcional) Altere as fontes para incluir:
      1. Clique em ![Editar](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] e [!UICONTROL On Demand] inventário) Clique *[!UICONTROL *View by Source]** ou **[!UICONTROL View by Feed]** para alterar a forma como as origens são listadas.
      1. (Quando aplicável) Filtre o inventário conforme necessário.
      1. Especifique as fontes a serem incluídas e excluídas:
         * Para incluir uma fonte [!UICONTROL Public] ou [!UICONTROL On Demand], clique em **[!UICONTROL Include]** ao lado do nome da fonte.
         * Para incluir fontes [!UICONTROL Private]:
            * Para incluir todo o inventário em um negócio, clique em **[!UICONTROL Include all]** ao lado do nome do negócio.
            * Para incluir uma fonte de inventário individual, expanda o nome da transação e clique na caixa de seleção ao lado do nome da origem.
         * Para excluir uma fonte [!UICONTROL Public] ou [!UICONTROL On ], clique em **[!UICONTROL Exclude]** ao lado do nome da fonte.
   1. (Opcional) Para baixar um arquivo CSV com as informações de direcionamento para o local de Downloads do navegador, clique em **[!UICONTROL Save & Export]**.
   1. Clique em **[!UICONTROL Save]**.

>[!TIP]
>
>Se você se inscreveu no inventário [!UICONTROL On Demand], mas não consegue localizar os editores ou ofertas para o público-alvo, verifique o status das ofertas. Para obter mais informações sobre status, consulte [Sobre [!DNL On Demand] Inventário Premium](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (somente disposições de vídeo) exclui o tráfego externo.

Anúncios de fora normalmente aparecem sobre o conteúdo como um pop-up ou empilhados em conteúdo (na experiência nativa), em vez de como anúncios de vídeo comuns em um reprodutor de vídeo.

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** os tipos de tráfego para segmentar. As opções incluem **[!UICONTROL Websites]** e **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** (Disponível quando  **[!UICONTROL Paste list of targeted sites]** é  *[!UICONTROL Off]*) A qualidade dos sites a serem selecionados. As camadas 1 a 3 são seguras para a marca e foram verificadas e aprovadas pela equipe de mapeamento de DSP.

* *[!UICONTROL Tier 1]:* Sites Premium e aplicativos que são reconhecíveis nacionalmente.
* *[!UICONTROL Tier 2]:* direciona o nível 1, bem como sites de qualidade e aplicativos menos conhecidos do que o nível 1.
* *[!UICONTROL Tier 3]:* direciona as camadas 1 a 2, bem como sites e aplicativos legítimos e seguros para a marca que atendam a um público-alvo de nicho. Use a Camada 3 para obter alcance ou compras de direcionamento de dados.
* *[!UICONTROL All Sites]:* direciona as camadas 1 a 3 e o novo inventário que não foi filtrado ou categorizado, que pode ser usado para alcançar.

>[!NOTE]
>
>O inventário é específico para as unidades de publicidade na disposição.

>[!TIP]
>
>Para campanhas de desempenho, a prática recomendada é selecionar *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]:** (Opcional; disponível quando  **[!UICONTROL Paste list of targeted sites]** é  *[!UICONTROL Off]*) Categorias de site nos níveis de site selecionados para incluir ou excluir (mas não ambos) como alvos. Escolha nas listas de sites verticais que o Advertising Cloud mapeou com base no assunto do site:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique as categorias de site que serão incluídas ou excluídas:
   * Para incluir categorias de site:
      1. Clique em **[!UICONTROL Include categories]**.
      1. Marque a caixa de seleção ao lado de cada categoria a ser direcionada.
   * Para excluir categorias de site:
      1. Clique em **[!UICONTROL Exclude categories]**.
      1. Marque a caixa de seleção ao lado de cada categoria a ser excluída.
1. (Opcional) Para baixar um arquivo CSV com as informações de direcionamento para o local de Downloads do navegador, clique em **[!UICONTROL Export]**.
1. Clique em **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (Opcional; disponível quando  **[!UICONTROL Paste list of targeted sites]** é  *[!UICONTROL Off]*) Sites a serem excluídos. Você pode pesquisar e selecionar sites, ou inserir ou colar nomes de domínio:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique os sites:
   * Para procurar um site:
      1. Clique em **[!UICONTROL Search]**.
      1. Insira uma palavra-chave, selecione uma camada de site e/ou selecione uma categoria de site.
      1. Nos resultados da pesquisa, selecione os sites a serem excluídos:
         * Para excluir um site individual, marque a caixa de seleção ao lado dele.
         * (Quando mais de 50 resultados estiverem disponíveis) Para excluir os primeiros 50 resultados, clique em **[!UICONTROL Exclude these 50]**. Para excluir todos os resultados da pesquisa, clique em **[!UICONTROL Exclude these \<*NN *\>]**.
   * Para inserir nomes de domínio:
      1. Clique em **[!UICONTROL Paste]**.
      1. Insira um ou mais nomes de domínio em linhas separadas.
      1. Clique em **[!UICONTROL Exclude All]**.
1. Clique em **[!UICONTROL Done]** quando terminar.

>[!NOTE]
>
>* As listas de sites bloqueados no nível da conta e do anunciante também são aplicadas, além da lista de sites bloqueados global do Advertising Cloud DSP [que inclui sites considerados inseguros para anúncios.](/help/dsp/introduction/features/brand-safety-media-quality.md)
>* As listas de sites bloqueados sempre substituem as listas de sites direcionados. Se uma disposição excluir e incluir a mesma meta para um anúncio, a meta será excluída.


**[!UICONTROL Language]:** (opcional) um único idioma para direcionar.

**[!UICONTROL Site List Preview]:** (somente leitura) todos os sites direcionados e bloqueados para a disposição.

Como opção, você pode exportar a lista de sites direcionados e bloqueados como um arquivo CSV (valores separados por vírgula). Para exportar a lista, clique em **[!UICONTROL Export full site list]** e abra ou salve o arquivo de acordo com o procedimento normal do navegador.

<!-- **[!UICONTROL Allow unscreened sites]:** (XXX placements only) Allows you to XXXX.   Optional available for https://advertising.adobe.com/configurator/placement/edit/2432022 -->

**[!UICONTROL Paste list of targeted sites]:** permite direcionar somente sites específicos. Quando você habilita essa opção, as outras opções de direcionamento de site são desabilitadas.

**[!UICONTROL Sites]:** (Disponível quando  **[!UICONTROL Paste list of targeted sites]** é  *[!UICONTROL On]*) Sites para segmentação. Você pode pesquisar e selecionar sites, ou inserir ou colar nomes de domínio:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique os sites:
   * Para procurar um site:
      1. Clique em **[!UICONTROL Search]**.
      1. Insira uma palavra-chave, selecione uma camada de site e/ou selecione uma categoria de site.
      1. Nos resultados da pesquisa, selecione os sites que serão incluídos:
         * Para excluir um site individual, marque a caixa de seleção ao lado dele.
         * (Quando mais de 50 resultados estiverem disponíveis) Para incluir os primeiros 50 resultados, clique em **[!UICONTROL Include these 50]**. Para incluir todos os resultados da pesquisa, clique em **[!UICONTROL Include these \<*NN *\>]**.
   * Para inserir nomes de domínio:
      1. clique em **[!UICONTROL Paste]**.
      1. Insira um ou mais nomes de domínio em linhas separadas.
      1. Clique em **[!UICONTROL Include All]**.
1. Clique em **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Quaisquer segmentos de público-alvo da disposição, incluindo segmentos de  [terceiros, segmentos primários, segmentos de Adobe, segmentos personalizados e públicos salvos](/help/dsp/audiences/audience-settings.md). O tamanho total e ativo do público-alvo desduplicado em todos os segmentos selecionados e nos públicos salvos também é exibido. Você pode selecionar um público-alvo existente, criar um novo público-alvo que pode ser reutilizado posteriormente ou selecionar segmentos de público-alvo específicos:

* Para selecionar um público-alvo existente, clique em ![Select](/help/dsp/assets/chevron-down.png) ao lado de [!UICONTROL Included Audiences] e selecione-o.
* Para criar um novo público, clique em ![Select](/help/dsp/assets/chevron-down.png) ao lado de [!UICONTROL Included Audiences] e selecione **[!UICONTROL + Create Audience]**. Para obter instruções, consulte [Criar um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-create.md), a partir da Etapa 3.
* Para selecionar segmentos de público-alvo específicos, clique em **[!UICONTROL Select segments for this placement only]**. Selecione a lógica do segmento; para obter instruções, consulte a Etapa 6 em &quot;[Criar um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-create.md)&quot;. Quando terminar, clique em **Salvar**.

**[!UICONTROL Excluded Audiences]:** Quaisquer públicos-alvo a serem excluídos para a disposição, incluindo públicos-alvo com segmentos de  [terceiros, segmentos primários, segmentos de Adobe, segmentos personalizados e públicos](/help/dsp/audiences/audience-settings.md) salvos. O tamanho total e ativo do público-alvo desduplicado em todos os públicos excluídos também é exibido. Você pode selecionar um público-alvo existente ou criar um novo público-alvo que pode ser reutilizado posteriormente:

* Para selecionar um público-alvo existente, clique em ![Select](/help/dsp/assets/chevron-down.png) ao lado de [!UICONTROL Excluded Audiences] e selecione-o.
* Para criar um novo público, clique em ![Selecionar](/help/dsp/assets/chevron-down.png) ao lado de [!UICONTROL Excluded Audiences] e selecione **+ Criar público-alvo**. Para obter instruções, consulte [Criar um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-create.md), a partir da Etapa 3.

**[!UICONTROL Cross Device Targeting]:** (disponível ao selecionar pelo menos um segmento ou público-alvo e a  [campanha é configurada para direcionamento](/help/dsp/campaign-management/campaigns/campaign-settings.md) entre dispositivos com base em pessoas. Permite estender sua definição de metas em todos os dispositivos conhecidos de uma pessoa (de acordo com o gráfico de dispositivos especificado nas configurações da campanha), até mesmo em dispositivos que não estão nos segmentos especificados. As tarifas podem ser aplicadas dependendo do gráfico especificado para a campanha. Atualmente, os dados de gráficos de dispositivos só estão disponíveis na América do Norte.

**[!UICONTROL Placement Cap]:** (opcional) o número de vezes que um dispositivo ou uma pessoa exclusiva (dependendo do especificado  [!UICONTROL Cross Device Level]) será veiculada nos anúncios da disposição. As opções incluem *[!UICONTROL Unlimited]* ou uma quantidade específica por dia, semana ou mês.

>[!NOTE]
>
> Você pode definir limites de frequência nos níveis de campanha, pacote e disposição. DSP respeitará o limite de frequência mais restrito na hierarquia da campanha.

**[!UICONTROL Secondary Cap]:** (Opcional; disponível ao incluir um numérico  [!UICONTROL Placement Cap]) Uma limitação adicional dentro dos limites do limite de posicionamento principal. Selecione o número de impressões e o período (como 3 por 12 horas).

**[!UICONTROL Day Parting]:** (Opcional) Dias específicos da semana e hora do dia em que os anúncios podem ser veiculados. Para especificar intervalos de segmentação de dia:
1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Selecione o fuso horário aplicável.
1. Especifique os intervalos:
   * Para selecionar um intervalo predefinido, clique em um dos botões de intervalo. As opções incluem *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]* ou *[!UICONTROL Prime]* (primetime).
   * Para selecionar manualmente um intervalo, clique dentro de uma célula e, como opção, arraste para selecionar o intervalo.
1. Clique em **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Opcional; disponíveis para anunciantes configurados com  [!DNL Comscore] e  [!DNL Grapeshot] segmentos) Nomes ou IDs de segmentos específicos de  [!DNL Comscore] e  [!DNL Grapeshot] para incluir como alvos. Taxas adicionais podem ser aplicadas para este recurso. Para ativar esse recurso e configurar segmentos de tópicos, entre em contato com o gerente de conta do Adobe.

Para especificar o direcionamento do tópico:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique os segmentos a serem direcionados:
   1. Na coluna à esquerda, selecione o parceiro (*[!UICONTROL Comscore]* ou *[!UICONTROL Grapeshot]*).
   1. No campo de entrada, insira os nomes de segmento ou as IDs de segmento.
1. (Opcional) Para baixar um arquivo CSV com as informações do tópico para o local de Downloads do navegador, clique em **[!UICONTROL Export]**.
1. Clique em **[!UICONTROL Save]**.

>[!TIP]
>
>* A definição de metas de tópico limita o inventário no qual a disposição pode ser licitada, portanto, use a definição de metas de tópico somente para uma pequena porcentagem de sua compra geral.
>
>* Configure qualquer direcionamento negativo no segmento em [!DNL Comscore] ou [!DNL Grapeshot].


**[!UICONTROL Device Targeting]:** (Opcional) Informações específicas do dispositivo, incluindo tipos de dispositivo, fabricantes, sistemas operacionais, navegadores e tipos de conectividade, para incluir e excluir como alvos. Para especificar o direcionamento do dispositivo:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique os detalhes do dispositivo a serem incluídos e excluídos:
   1. Na coluna da esquerda, selecione a categoria .
   1. Especificar direcionamento:
      * Para incluir um valor, clique em **[!UICONTROL Include]** ao lado do nome do valor.
      * Para excluir um valor, clique em **[!UICONTROL Exclude]** ao lado do nome do valor.
1. (Opcional) Para baixar um arquivo CSV com as informações de direcionamento do dispositivo para o local de Downloads do navegador, clique em **[!UICONTROL Export]**.
1. Clique em **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Opcional) Provedores de serviços de Internet específicos (ISPs) para incluir ou excluir (mas não ambos) como alvos. Para especificar o direcionamento ISP:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique os ISPs a serem incluídos ou excluídos:
   * Para incluir ISPs:
      1. Clique em **[!UICONTROL Include ISPs]**.
      1. (Opcional) Filtre a lista por palavra-chave.
      1. Marque a caixa de seleção ao lado de cada ISP para segmentar.
   * Para excluir ISPs:
      1. Clique em **[!UICONTROL Exclude ISPs]**.
      1. (Opcional) Filtre a lista por palavra-chave.
      1. Marque a caixa de seleção ao lado de cada ISP a ser excluído.
1. (Opcional) Para baixar um arquivo CSV com as informações de direcionamento ISP para o local de Downloads do navegador, clique em **[!UICONTROL Export]**.
1. Clique em **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** Tipos de filtros  [!DNL Comscore],  [!DNL DoubleVerify],  [!DNL Integral Ad Science] e  [!DNL Peer39] contextuais a serem aplicados. Os padrões no nível do anunciante são selecionados para novas disposições, mas você pode alterar as configurações:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Opcional) Um ou mais tipos de contexto de inventário a serem bloqueados por padrão. Podem ser aplicadas taxas adicionais.

* [!UICONTROL Peer 39]:

   * **Sites alvo que são:**  (opcional) um ou mais tipos de atributos de inventário para direcionar por padrão. Podem ser aplicadas taxas adicionais.

* [!UICONTROL ComScore]:

   * **Bloquear sites que são:**  (Opcional) Um ou mais tipos de atributos de inventário a serem bloqueados por padrão. Podem ser aplicadas taxas adicionais.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Opcional) O grau de conteúdo adulto para o qual bloquear anúncios por padrão:  *[!UICONTROL Do Not Block]* (o padrão),  *[!UICONTROL Standard]* ou  *[!UICONTROL Strict]*. Podem ser aplicadas taxas adicionais.

   * **[!UICONTROL Alcohol Content]:** (Opcional) O grau de álcool para o qual bloquear anúncios por padrão:  *[!UICONTROL Do Not Block]* (o padrão),  *[!UICONTROL Standard]* ou  *[!UICONTROL Strict]*. Podem ser aplicadas taxas adicionais.

**[!UICONTROL Pre-bid fraud blocking]:** Tipos de sites a serem bloqueados com base em tráfego fraudulento e atividades suspeitas medidas por meio de  [!DNL DoubleVerify],  [!DNL Integral Ad Science]e  [!DNL Peer39]. Os padrões no nível do anunciante são selecionados para novas disposições, mas você pode alterar as configurações:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** por padrão, bloqueia todo o tráfego 100% inválido, incluindo o tráfego em dispositivos realçados, para novas disposições. Podem ser aplicadas taxas adicionais.

   * **[!UICONTROL Also block sites with]:** (Opcional) Um nível adicional de fraude e tráfego inválido que fará com que o DSP bloqueie anúncios por padrão:   *[!UICONTROL None]* (o padrão, que não bloqueia o tráfego adicional),  *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*,  *[!UICONTROL >4% Average Fraud/IVT levels]*,  *[!UICONTROL >6% Average Fraud/IVT levels]*,  *[!UICONTROL >10% Average Fraud/IVT levels]* ou  *[!UICONTROL >25% Average Fraud/IVT levels]*. Podem ser aplicadas taxas adicionais.

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** (Opcional) Um ou mais tipos de fraude que farão com que DSP bloqueiem anúncios por padrão:  *[!UICONTROL Fraud]* (que bloqueia todos os sites com fraude),  *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* e/ou  *[!UICONTROL Fraud: Zero Ads]*. Podem ser aplicadas taxas adicionais.

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** (Opcional) Um tipo de atividade suspeita de site ou aplicativo que fará com que o DSP bloqueie anúncios por padrão:  *[!UICONTROL None]* (o padrão, que não bloqueia anúncios com base em atividades suspeitas),  *[!UICONTROL Suspicious Activity - High Risk]* ou  *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Podem ser aplicadas taxas adicionais.

**[!UICONTROL Ads.txt filtering]:**

Qual nível de [Ads.txt](https://iabtechlab.com/ads-txt-about/) filtragem de pré-lance para usar aproveitando a lista de revendedores digitais autorizados de cada editor. O padrão de nível do anunciante é selecionado para novas disposições, mas você pode alterar as configurações:

* *[!UICONTROL Opt out of ads.txt (default)]*: Para comprar estoque de todos os vendedores.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Para priorizar o inventário de compras dos vendedores diretos e revendedores autorizados de um domínio.
* *[!UICONTROL Ads.txt sellers only]*: Comprar inventário apenas dos vendedores diretos e revendedores autorizados de um domínio.
* *[!UICONTROL Ads.txt sellers only]*: Comprar inventário apenas dos vendedores diretos autorizados de um domínio.

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (Anunciantes configurados com a  [!UICONTROL DoubleVerify Authentic Brand Safety] opção ) Ativa  [!DNL DoubleVerify Authentic Brand Safety], que bloqueia impressões pós-licitação usando as regras de segurança de marca personalizadas configuradas para a ID de segmento especificada. DSP fatura sua conta pelo uso da ID de segmento especificada nas configurações do anunciante.

## [!UICONTROL Tracking]

>[!NOTE]
>
>([!DNL Roku] disposições) Os fornecedores de rastreamento de terceiros aprovados por [!DNL Roku] incluem [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], &lt;a 13/>, [!DNL Placed], [!DNL Polk] e [!DNL Research Now].[!DNL Oracle]

**[!UICONTROL Event Pixels]:** (Opcional) pixels de rastreamento de eventos de terceiros que serão anexados por padrão a todos os novos anúncios na disposição. Para especificar pixels de evento:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Siga um destes procedimentos:
   * Para selecionar um pixel existente, marque a caixa de seleção na linha de pixels.
   * Para criar um novo pixel:
      1. Clique em **[!UICONTROL Create]**.
      1. Insira as seguintes informações:
         * **[!UICONTROL Pixel name]:** o nome do pixel; o comprimento máximo é de 500 caracteres. Use um nome que o ajudará a identificar o pixel com facilidade.
         * **[!UICONTROL Pixel event fires on]:** o evento que aciona o pixel para ser disparado. Os eventos disponíveis variam por tipo de anúncio.
         * **[!UICONTROL Pixel type]:** se o pixel é um  *[!UICONTROL IMG URL]* (arquivo de imagem de pixel 1x1),  *[!UICONTROL HTML]*, ou  *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** O URL da imagem de pixel.
      1. Clique em **[!UICONTROL Create and attach]**.
   1. Clique em **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (Opcional) Rastreamento de conversão que será anexado por padrão a todos os novos anúncios no posicionamento. Para especificar pixels de conversão:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Siga um destes procedimentos:
   * Para selecionar um pixel existente, marque a caixa de seleção na linha de pixels.
   * Para criar um novo pixel:
      1. Clique em **[!UICONTROL Create]**.
      1. Insira as seguintes informações:
         * **[!UICONTROL Conversion pixel name]:** o nome do pixel; o comprimento máximo é de 500 caracteres. Use um nome que o ajudará a identificar o pixel com facilidade.
         * **[!UICONTROL Conversion category]:** O tipo de conversão.
         * **[!UICONTROL Impression conversion window]:** o número de dias após uma impressão de anúncio em que a impressão pode ser atribuída a uma conversão. O padrão é 30 dias.
         * **[!UICONTROL Click conversion window]:** o número de dias após um clique em um anúncio no qual o clique pode ser atribuído a uma conversão. O padrão é 30 dias.
         * **[!UICONTROL Notes]:** (opcional) uma descrição ou outras informações sobre o pixel.
      1. Clique em **[!UICONTROL Create and attach]**.
      1. Implemente o pixel de conversão nas páginas da Web relevantes:
         1. No menu principal, vá para **[!UICONTROL Resources]>[!UICONTROL Conversion pixels]**.
         1. Na linha de pixel, clique em **[!UICONTROL edit]**.
         1. Copie os valores nos campos [!UICONTROL HTML Tag] e [!UICONTROL Flash Tag], conforme necessário, para fornecer ao anunciante ou ao contato do site.

            O departamento de TI do anunciante ou outro grupo pode precisar agendar ou ser informado sobre a implantação da tag.
   1. Clique em **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Opcional) Uma taxa de taxa estática de terceiros a ser rastreada como um custo não faturável por mil impressões. O padrão de nível de pacote é aplicado automaticamente para novas disposições, quando aplicável, a menos que você insira um valor diferente.

>[!NOTE]
>
>As tarifas faturáveis são refletidas na métrica [!UICONTROL Net CPM].

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de disposição](placement-about.md)
>* [Criar uma disposição](placement-create.md)
>* [Editar uma disposição](placement-edit.md)
>* [Atalhos de teclado](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Perguntas frequentes sobre o gerenciamento de campanhas](/help/dsp/campaign-management/campaign-management-faq.md)

