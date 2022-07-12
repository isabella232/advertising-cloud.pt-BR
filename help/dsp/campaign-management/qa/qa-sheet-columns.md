---
title: Colunas em planilhas baixadas/carregadas
description: Faça referência às colunas em planilhas de controle de qualidade do Excel baixadas e carregadas.
feature: DSP Placements
exl-id: 8a8dceed-f77d-4b6b-a842-f57528125c92
source-git-commit: 0c3984d755131ad98b7ddecfd9567ff4be54b64e
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%

---

# Colunas em planilhas baixadas/carregadas

<!-- rename -- not specific enough - I think you can download Excel files of other things too -->

<!-- see notes within the table about descriptions that need to be edited -->

>[!TIP]
>
> Em uma planilha baixada, todas as colunas editáveis são destacadas em azul.

| Seção | Coluna | Descrição | Editável? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | A ID numérica da disposição. | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | O nome da disposição. | Sim |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Quaisquer rótulos aplicados, para relatórios. | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | Um link para abrir a disposição no modo de Edição. | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | O status da disposição: *[!UICONTROL active]* ou *[!UICONTROL inactive]*. | Sim |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | O tipo de disposição. | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | O nome do pacote pai, quando aplicável. | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | A data de início da disposição. | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | A data de término da disposição. | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Se a segmentação de dia é *[!UICONTROL ON]* ou *[!UICONTROL OFF]*.<br><b>Observação:</b> Para verificar a programação de dayparting real, abra as configurações de posicionamento em [!DNL DSP]. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | O orçamento de colocação, se houver. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | O intervalo de orçamento: &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* ou *[!UICONTROL All Time]*.[!UICONTROL >Daily] | Sim |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | O objetivo do pacote. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | O valor da meta da meta. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Se a disposição está avançando na direção da variável *[!UICONTROL Budget]* ou *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | O lance máximo da disposição. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Pacing Fill Strategy] | A estratégia de preenchimento de ritmo para a disposição: *[!UICONTROL evenly]*, *[!UICONTROL frontload]* ou *[!UICONTROL aggressive frontload]*. | Sim |
| [!UICONTROL Goals] | [!UICONTROL  Pre-Bid Filters] | Qualquer critério de filtro pré-lance a ser aplicado. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Se as regras de licitação (obsoleto) são *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | O limite de frequência principal para a colocação durante o período especificado [!UICONTROL Frequency Cap Interval]. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Intervalo para o limite de frequência primária: *[!UICONTROL Day]*, *[!UICONTROL Week]* ou *[!UICONTROL Month]*. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | O limite de frequência secundária para a colocação durante o período especificado [!UICONTROL Secondary Frequency Cap Interval] | Sim |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | O tipo de intervalo para o limite de frequência secundária: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* ou *[!UICONTROL Minute]*. O número aplicável de semanas, dias, horas ou minutos é indicado pela variável [!UICONTROL Secondary Frequency Cap Interval Value]. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | O número de semanas, dias, horas ou minutos para os quais a variável [!UICONTROL Secondary Frequency Cap] se aplica. Por exemplo, se o limite secundário for três impressões por seis horas, o valor aqui será <b>6&lt;/>. | Sim |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | O número de localizações geográficas específicas, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | As localizações geográficas-alvo, separadas por ponto-e-vírgula, ou *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | O número de localizações geográficas excluídas ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | As localizações geográficas excluídas, separadas por ponto e vírgula, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | O número de ofertas de inventário público, se for caso disso, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | O número de ofertas de inventário público excluídas, se for caso disso, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | O número de transações de inventário privado direcionadas, se houver, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | O número de transações de inventário privado excluídas, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | O número de target [!UICONTROL On-Demand Inventory] ofertas, se houver algum especificado, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | O número de ofertas de Inventário sob demanda excluídas, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | O tipo de tráfego direcionado: *[!UICONTROL Website]* e/ou *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Se a opção Direcionamento de inventário para excluir o tráfego externo é &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />* ou *[!UICONTROL OFF]*.[!UICONTROL >ON]<br>Anúncios de fora normalmente aparecem sobre o conteúdo como um pop-up ou empilhados em conteúdo (na experiência nativa), em vez de como anúncios de vídeo comuns em um reprodutor de vídeo. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | A qualidade dos sítios a atingir: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]* ou *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | O número de categorias de site alvo, se houver, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | O número de categorias de site excluídas, se houver, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | Os sites excluídos, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Os idiomas do site de destino. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Somente disposições de exibição padrão) Permitir ou não a entrega de anúncios em sites não auditados: *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. Quando a disposição é direcionada ao inventário privado, essa opção pode fornecer anúncios em sites bloqueados. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | O número de sites direcionados, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | Os públicos-alvo direcionados, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | Os públicos-alvo excluídos, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Se ou não [!DNL Comscore] os segmentos demográficos são habilitados para a disposição (e outras disposições na campanha): *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. Esse recurso pode ser ativado apenas para campanhas para as quais a variável [!DNL Audience Verification] está habilitado para [!DNL Nielsen] e/ou [!DNL Comscore].  Incorre em taxas adicionais. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Estender ou não o direcionamento de anúncios em dispositivos: *[!UICONTROL ON]* ou *[!UICONTROL OFF]*.<!-- Whether or not the Cross Device Targeting setting is enabled for the placement : *ON* or *OFF*. Cross-device targeting extends your targeting across all of a person's known device, per the device graph specified in the campaign settings.--> | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Incluído # | O número de códigos de tópico direcionado, se houver, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | O número de códigos de tópico excluídos, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | O número de alvos de dispositivo, se houver, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | O número de alvos de dispositivos excluídos, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | O número de provedores ISP direcionados, se houver, ou *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | O número de provedores ISP excluídos, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | O número de filtros de segurança da marca aplicados, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | O número de filtros de bloqueio de fraude de pré-oferta aplicados, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | O número de filtros de visualização de pré-oferta aplicados, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Se o Bloco de Segurança do Site está ativado ou não: *[!UICONTROL ON]* ou *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | O número de pixels de rastreamento de eventos de terceiros anexados à disposição, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | O número de pixels de rastreamento de conversão anexados à disposição ou *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Uma taxa de taxa estática de terceiros a ser rastreada como um custo não faturável por 1000 impressões, se aplicável. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | O número de anúncios anexados à disposição, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | Os nomes dos anúncios anexados ao posicionamento, se houver algum, ou *[!UICONTROL None]*. | — |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Sobre a correção das configurações de disposição de uma campanha usando planilhas](qa-about.md)
>* [Baixar configurações de posicionamento para uma campanha](qa-sheet-download.md)
>* [Fazer upload de configurações de disposição para uma campanha](qa-sheet-upload.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)

