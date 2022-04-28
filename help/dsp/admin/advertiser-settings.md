---
title: Configurações da conta do anunciante
description: Consulte as descrições das configurações disponíveis do anunciante.
source-git-commit: 2e0395dc1e5aa52adc83c1aaea49793fd5555390
workflow-type: tm+mt
source-wordcount: '975'
ht-degree: 0%

---

# Configurações da conta do anunciante

*Não disponível para usuários somente leitura*

## [!UICONTROL General] Configurações

**[!UICONTROL Advertiser Name]:** O nome do anunciante.

**[!UICONTROL Category]:** A categoria em que a empresa do anunciante opera. A categoria é comunicada aos editores quando você faz lances no inventário. Escolha uma categoria que se alinha a seus anúncios ou os editores possam rejeitar seus anúncios.

>[!NOTE]
>
>Se você selecionar *[!UICONTROL Other]*, o anunciante não poderá acessar DSP [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** A página inicial do anunciante ou o URL do site principal (começando com `http://` ou `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (Somente novas contas de anunciante) Disponibiliza ao anunciante todos os feeds de troca privados configurados para a conta de DSP da organização.

### [!UICONTROL Adobe IMS IDs]

Os anunciantes com produtos adicionais da Adobe Experience Cloud podem compartilhar dados em alguns produtos usando a ID exclusiva da organização para o Experience Cloud. Você pode configurar integrações específicas de produtos no [!UICONTROL Integrations] seção.

**[!UICONTROL Account IMS org and ID]:** (Anunciantes com produtos Experience Cloud adicionais licenciados por meio de uma conta Experience Cloud com vários anunciantes; opcional) a ID de organização do Experience Cloud do anunciante.

**[!UICONTROL Advertiser IMS org and ID]:** [Anunciantes com licenças diretas para produtos Experience Cloud adicionais; opcional) a ID de organização do Experience Cloud do anunciante.

### [!UICONTROL Integrations]

(Opcional) Produtos de Experience Cloud adicionais vinculados à conta de DSP. Os produtos devem ser associados à mesma ID de organização do Experience Cloud fornecida no [!UICONTROL Adobe IMS IDs] seção.

**[!UICONTROL Adobe Media Optimizer]:** (Anunciantes com Advertising Cloud Search ou que usam pixels de conversão Advertising Cloud) A [!DNL Search] conta com a qual DSP irá trocar dados de atribuição.

**[!UICONTROL Adobe Device Co-op or 3rd Party Graph]:** (Anunciantes que usam pixels de conversão do Advertising Cloud; (opcional) Você pode usar um gráfico de dispositivos para medição de atribuição baseada em pessoa das configurações de conta do anunciante no Advertising Cloud Search.

>[!NOTE]
>
> * A atribuição de dispositivo está disponível somente para conversões rastreadas usando o serviço de rastreamento de conversão do Advertising Cloud, não para conversões rastreadas pelo Adobe Analytics.
> * Você também pode selecionar um gráfico de dispositivos com base em pessoas para o direcionamento entre dispositivos e o gerenciamento de frequência no [nível de campanha](/help/dsp/campaign-management/campaigns/campaign-settings.md). Em seguida, você pode configurar o direcionamento entre dispositivos na [nível de inserção](/help/dsp/campaign-management/placements/placement-settings.md) e limites de frequência adicionais na [nível de pacote](/help/dsp/campaign-management/packages/package-settings.md) e [nível de inserção](/help/dsp/campaign-management/placements/placement-settings.md). O direcionamento entre dispositivos e o gerenciamento de frequência não exigem medição de atribuição no nível do anunciante; em vez disso, eles trabalham com o gráfico de dispositivos especificado nas configurações da campanha.


**[!UICONTROL Adobe Analytics]:** (Anunciantes com a Adobe Analytics; facultativo; aplicável somente aos dados coletados usando tags de rastreamento de conversão do Advertising Cloud que incluem um [!DNL EF Redirect] e somente token) um ou mais [!DNL Analytics] conjuntos de relatórios para os quais o DSP enviará dados coletados de editores e parceiros do lado do suprimento. O Analytics também enviará os dados coletados do site do cliente para o DSP.

Para que os dados apareçam nos conjuntos de relatórios, a variável [!DNL Search] configuração no nível do anunciante como &quot;[!UICONTROL Enable tracking for SAINT feeds]&quot; deve estar ativado. Além disso, o [!DNL Analytics] deve ser configurada para receber dados do Advertising Cloud. <!-- from Advertising Cloud or DSP in particular? Add cross-reference to file in Integrations section. -->

>[!WARNING]
>
>Se você remover um conjunto de relatórios vinculado anteriormente, o DSP não trocará mais dados com esse conjunto. Espera-se ver as flutuações de dados. <!-- Fluctuations where? Clarify -->

**[!UICONTROL Adobe Analytics Cloud]:** (Anunciantes com Adobe Audience Manager ou Adobe Analytics; opcional) um Audience Manager ou [!DNL Analytics] conta da qual DSP obterá metadados de segmento, dados de hierarquia e dados de público-alvo exclusivos para todos os públicos-alvo do Adobe do anunciante. Isso inclui dados para:

* Segmentos Audience Manager
* [!DNL Analytics] segmentos publicados na Adobe Experience Cloud
* Segmentos criados no Adobe Experience Cloud usando o [!DNL People core service]
* Segmentos criados no Adobe Experience Platform e enviados para o Advertising Cloud via Audience Manager

A sincronização inicial leva cerca de 24 horas. Depois disso, os dados são sincronizados em tempo real, com um atraso de um a dois segundos.
<!-- I don't think this is true anymore:
Segment membership data is sent to Advertising Cloud only after one of the following:

* The segment is targeted in an Advertising Cloud placement or audience library
* The segment is added to the Advertising Cloud batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] Configurações

Opcionalmente, você pode configurar metas padrão para as novas disposições do anunciante. Os usuários podem substituir os destinos padrão de qualquer nova disposição.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** O país padrão para cada geolocalização de posicionamento. Os usuários podem alterar o país e configurar o geolocalização mais específico para cada disposição.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** Qualquer público-alvo ou segmento a ser suprimido por padrão. Os usuários podem alterar as exclusões de cada disposição.

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

Tipos de [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]e [!DNL Peer39] filtros contextuais a serem aplicados. Você pode substituir as configurações no nível do anunciante na [nível de inserção](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (Opcional) Um ou mais tipos de contexto de inventário a serem bloqueados por padrão. Podem ser aplicadas taxas adicionais.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (Opcional) Um ou mais tipos de atributos de inventário para definição de metas por padrão. Podem ser aplicadas taxas adicionais.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (Opcional) Um ou mais tipos de atributos de inventário a serem bloqueados por padrão. Podem ser aplicadas taxas adicionais.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Opcional) O grau de conteúdo adulto para o qual bloquear anúncios por padrão: *[!UICONTROL Do Not Block]* (o padrão), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Podem ser aplicadas taxas adicionais.

**[!UICONTROL Alcohol Content]:** (Opcional) O grau de álcool para o qual bloquear anúncios por padrão: *[!UICONTROL Do Not Block]* (o padrão), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Podem ser aplicadas taxas adicionais.

#### [!UICONTROL Pre-Bid Fraud Blocking]

Tipos de sites a bloquear com base em tráfego fraudulento e atividades suspeitas medidas através de [!DNL DoubleVerify], [!DNL Integral Ad Science]e [!DNL Peer39]. Você pode substituir as configurações no nível do anunciante na [nível de inserção](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Por padrão, o bloqueia todo o tráfego 100% inválido, incluindo o tráfego em dispositivos sequenciados, para novas disposições. Podem ser aplicadas taxas adicionais.

**[!UICONTROL Also block sites with]:** (Opcional) Um nível adicional de fraude e tráfego inválido que fará com que o DSP bloqueie anúncios por padrão:  *[!UICONTROL None]* (o padrão, que não bloqueia o tráfego adicional), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* ou *[!UICONTROL >25% Average Fraud/IVT levels]*. Podem ser aplicadas taxas adicionais.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (Opcional) Um ou mais tipos de fraude que farão com que o DSP bloqueie anúncios por padrão: *[!UICONTROL Fraud]* (que bloqueia todos os sítios com fraude), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* e/ou *[!UICONTROL Fraud: Zero Ads]*. Podem ser aplicadas taxas adicionais.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (Opcional) Um tipo de atividade suspeita de site ou aplicativo que fará com que DSP bloqueie anúncios por padrão: *[!UICONTROL None]* (o padrão, que não bloqueia anúncios com base em atividades suspeitas), *[!UICONTROL Suspicious Activity - High Risk]* ou *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Podem ser aplicadas taxas adicionais.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** Por padrão, qual nível de [[!DNL Ads.txt] filtragem pré-lance](https://iabtechlab.com/ads-txt-about/) para usar aproveitando cada editor [!DNL Authorized Digital Sellers] lista:
* *[!UICONTROL Opt out of ads.txt (default)]*: Para comprar estoque de todos os vendedores.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Para priorizar o inventário de compras dos vendedores diretos e revendedores autorizados de um domínio.
* *[!UICONTROL Ads.txt sellers only]*: Comprar inventário apenas dos vendedores diretos e revendedores autorizados de um domínio.
* *[!UICONTROL Ads.txt sellers only]*: Comprar inventário apenas dos vendedores diretos autorizados de um domínio.

Você pode substituir a configuração no nível do anunciante na [nível de inserção](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** Por padrão, o ativa um filtro pós-lance em tempo real para garantir que os anúncios vejam os sites que o anunciante está direcionando. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Safety]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] Apenas clientes; opcional) a ID do segmento de segurança da marca associada ao relatório de [!DNL DoubleVerify] conta.

**[!UICONTROL Enable Authentic Brand Safety]:** (Opcional) Por padrão, habilita [!DNL DoubleVerify] Segurança de marca autêntica, que bloqueia impressões pós-licitação usando as regras de segurança de marca personalizadas configuradas para a ID de segmento especificada. DSP conta para uso da ID de segmento.

Você pode substituir a configuração no nível do anunciante no nível de posicionamento.

>[!MORELIKETHIS]
>
>* [Criar uma conta de anunciante](/help/dsp/admin/advertiser-create.md)


<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
