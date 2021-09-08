---
title: Segurança da marca e qualidade da mídia
description: Saiba mais sobre a segurança da marca e os recursos de qualidade de mídia.
feature: Introduction
exl-id: df5be5d4-490e-479f-b76d-4fda4acd4201
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Segurança da marca e qualidade da mídia

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

O Advertising Cloud DSP fornece um conjunto de recursos de proteção da marca para garantir que cada uma de suas campanhas atinja os usuários reais em um ambiente seguro para a marca.

Nossa equipe de Vigilância de Fraude trabalha em estreita colaboração com parceiros líderes do setor, como [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)] e [!DNL WhiteOps], para preparar cuidadosamente o inventário em nossa plataforma. Por meio do gerenciamento pró-ativo de nosso suprimento, o DSP garante que todos os anunciantes em toda a plataforma estejam protegidos do tráfego não humano (bots, crawlers, tráfego do data center e fraude) e sejam fornecidos apenas em contextos seguros para a marca.

Além de fornecer gerenciamento de qualidade central, acreditamos em capacitar os anunciantes a projetar os controles que se alinham à marca. A Adobe Advertising Cloud oferece integrações com [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud] e [!DNL Peer39], garantindo que cada anunciante possa escolher o nível desejado de proteção contra fraudes, filtragem contextual e definição de metas de palavras-chave.

## Iniciativas de qualidade do Advertising Cloud DSP

### Verificação de inventário com suporte a [!DNL Ads.txt]

[[!DNL Ads.txt], which stands for [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) é uma iniciativa lançada pelo  [!DNL Interactive Advertising Bureau] ([!DNL IAB]) em junho de 2017 para facilitar a representação adequada do inventário no mercado aberto, combatendo assim fontes ilegítimas de tráfego e falsificação de domínios. Os editores e distribuidores participantes declaram publicamente as empresas autorizadas a vender o seu inventário digital e a natureza dessas relações, mantendo uma página `ads.txt` no nível superior do domínio (como `example.com/ads.txt`).

DSP suporta [!DNL ads.txt] lendo o arquivo `ads.txt` de cada editor e dando a você a opção de comprar somente de [!DNL ads.txt] vendedores verificados. Por exemplo, ao combinar os vendedores que vemos acessando `nytimes.com` ao arquivo `ads.txt` do New York Times, podemos identificar quais são legítimos e quais não são, e vamos bloquear os infratores se a disposição estiver configurada para comprar apenas de vendedores verificados. <!-- can we actually mention NY Times? -->

Você pode definir os controles padrão [!DNL ads.txt] para cada anunciante<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> e, opcionalmente, [personalizar as configurações de cada disposição](/help/dsp/campaign-management/placements/placement-settings.md) para:

* comprar inventário apenas de vendedores diretos autorizados de um domínio

* comprar inventário apenas de vendedores diretos e revendedores autorizados de um domínio

* priorizar o inventário de compras dos vendedores diretos e revendedores autorizados de um domínio

* comprar inventário de todos os vendedores

### Supervisão de fraude de plataforma

A DSP criou ferramentas e sistemas internos fortes para gerenciar fraudes em nossa plataforma, em parceria com fornecedores líderes do setor, como [!DNL Whiteops] e [!DNL Integral Ad Science].

Além disso, o Adobe trabalha em conjunto com [!DNL IAB] e [!DNL TAG] para garantir um bloqueio de fraude robusto e padrão do setor para proteger nossos anunciantes, aproveitando ferramentas como [!DNL ads.txt] (consulte a seção anterior), a lista de bots e spiders [!DNL IAB] e a lista de IP do datacenter.[!DNL TAG]

Por meio de nossa abordagem multidimensional à qualidade, nossa equipe monitora anomalias e padrões de tráfego inválidos, garantindo menos de 3% de tráfego inválido no inventário protegido. Qualquer inventário suspeito — incluindo o inventário de domínios específicos ou de editores ou vendedores específicos — é imediatamente bloqueado em toda a plataforma.

### Mapeamento de inventário, hierarquização e categorização

O mapeamento de inventário é o processo detalhado de revisão e integração necessário para todo o novo inventário antes de ele ser adicionado à nossa plataforma. Este processo destina-se a garantir a segurança e a qualidade de todo o inventário DSP.

* **Mapeamento:** nossa equipe de inventário analisa cada domínio cuidadosamente, avaliando aspectos como:

   * Segurança da marca

   * Verificação do tipo de anúncio

   * Conteúdo genérico, domínios duplicados e fornecimento falso de anúncios

* **Classificação por níveis:** examinamos holisticamente a presença da marca no ecossistema geral para classificar o inventário em diferentes níveis. Você pode [direcionar suas disposições](/help/dsp/campaign-management/placements/placement-settings.md) para esses níveis para o nível de alcance desejado:

   * **[!UICONTROL T1]** - Nome da marca, sítios internacionalmente reconhecíveis

   * **[!UICONTROL T2]** - Sites bonitos, atuais, atualizados, sem conteúdo gerado pelo usuário e geralmente sem reconhecimento global

   * **[!UICONTROL T3]** - Conteúdo gerado pelo usuário e conteúdo de nicho

* **Categorização do site:** para garantir o direcionamento e o bloqueio fáceis do conteúdo, marcamos cada propriedade com uma categoria de site definida pela Advertising Cloud com base no conteúdo da propriedade. Você pode [direcionar ou excluir essas categorias de site para cada disposição](/help/dsp/campaign-management/placements/placement-settings.md) com base nas metas de posicionamento.

### Suporte abrangente para bloqueio de site

O Advertising Cloud DSP fornece uma lista de sites bloqueados globalmente e a opção para criar listas de sites bloqueados personalizados para anunciantes e contas.

#### Lista de sites bloqueados globalmente do Advertising Cloud DSP

A Advertising Cloud DSP mantém uma lista de sites bloqueados globalmente de sites considerados inseguros para executar anúncios. Esta lista contém sites com conteúdo duvidoso (como ódio ou terror) e sites infectados por bots, falsos antes da exibição, domínios incompatíveis e outras atividades fraudulentas.

Como parte da nossa iniciativa Segurança da marca para eliminar atividades que defraudam anunciantes, todos os sites são rastreados usando as medidas na lista de sites bloqueados do gráfico. Todos os sites que não passam pelas verificações de segurança da marca são adicionados à lista de sites bloqueados globalmente. Como o Advertising Cloud DSP gerencia essa lista dinamicamente, os sites podem continuar ou sair da lista a qualquer momento, com base na análise de segurança da marca mais recente.

Quando você inclui um site na lista de sites bloqueados globalmente como meta de posicionamento, o site é sinalizado com um ponto de exclamação vermelho (!). Isso indica que os anúncios não serão executados no site sinalizado.

#### Listas de sites bloqueados no nível da conta e no nível do anunciante

Os usuários também podem manter listas bloqueadas de sites no nível da conta e do anunciante<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, que são usadas automaticamente para todas as disposições. Lista de sites bloqueados de nível inferior é aplicada além da lista de sites bloqueados globalmente.

## Integrações de terceiros

### Filtragem contextual

A filtragem contextual permite direcionar ou bloquear oportunidades de publicidade com base no contexto da página que o anúncio veicularia. O Adobe oferece filtragem contextual por meio de integrações com os principais fornecedores do setor: [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] e [!DNL Peer39]. Os exemplos de filtros atuais incluem [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics] e [!UICONTROL G-rated Sites].

Você pode definir controles de filtro contextual padrão para cada anunciante<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> e, opcionalmente, [personalizar as configurações para cada disposição](/help/dsp/campaign-management/placements/placement-settings.md). Taxas adicionais podem ser aplicadas quando você usa esse recurso.

![Logotipo da Comscore ](/help/dsp/assets/comscore-logo.png) ![DoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![logoLogotipo Integral da Ciência da Publicidade ](/help/dsp/assets/ias-logo.png) ![logoPeer39](/help/dsp/assets/peer39-logo.png)

### Bloqueio de fraude de pré-lance

Aproveite as integrações de terceiros com [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] e [!DNL Peer39] para bloquear o tráfego não humano de suas campanhas. Essas integrações fornecem recursos líderes do setor de bloqueio pré-lance para minimizar o tráfego inválido geral e sofisticado (GIVT e SIVT) em suas campanhas.

Você pode definir controles de bloqueio de fraude de pré-oferta padrão para cada anunciante<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> e, opcionalmente, [personalizar as configurações para cada disposição](/help/dsp/campaign-management/placements/placement-settings.md). Taxas adicionais podem ser aplicadas quando você usa esse recurso.

Para obter mais informações sobre funcionalidade, entre em contato diretamente com seu fornecedor preferencial ou entre em contato com seu gerente de conta do Adobe.

![Logotipo da Comscore ](/help/dsp/assets/comscore-logo.png) ![DoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![logoLogotipo Integral da Ciência da Publicidade ](/help/dsp/assets/ias-logo.png) ![logoPeer39](/help/dsp/assets/peer39-logo.png)

### Visualização de pré-lance {#pre-bid-viewability}

Filtros de visualização pré-lances fornecidos por nossos parceiros líderes do setor [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]) e [!DNL Integral Ad Science] permitem que os anunciantes garantam que suas campanhas atendam às metas de desempenho de visualização desejadas no inventário de vídeo e exibição.

Você pode definir filtros de visualização padrão para cada anunciante<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) --> e, opcionalmente, [personalizar as configurações de cada disposição](/help/dsp/campaign-management/placements/placement-settings.md). Taxas adicionais podem ser aplicadas quando você usa esse recurso.

![Logotipo do DoubleVerifyLogotipo do ](/help/dsp/assets/doubleverify-logo.png) ![Oracle Advertising ](/help/dsp/assets/oracle-advertising-logo.png) ![Logotipo Integral da Ad Science](/help/dsp/assets/ias-logo.png)

### Direcionamento de tópico

DSP direcionamento de tópico permite direcionar ou bloquear listas de palavras-chave aproveitando nossos parceiros contextuais líderes do setor [!DNL Comscore] e [!DNL Oracle Data Cloud] ([!DNL Grapeshot]).

A definição de metas por tópico ajuda você a garantir que seus anúncios sejam sempre veiculados em um ambiente alinhado à sua marca, seja isso o que inclui o bloqueio de conteúdo prejudicial ou a garantia de gastos em um contexto que garanta um resultado maior.

O direcionamento de tópico requer a criação de segmentos de tópico diretamente com [!DNL Comscore] ou [!DNL Grapeshot] (usando [!DNL Oracle Data Cloud]). Depois que eles forem criados na plataforma do parceiro, você poderá [direcionar ou excluir uma ID de segmento na seção[!UICONTROL  Audience Targeting] para cada disposição](/help/dsp/campaign-management/placements/placement-settings.md). Taxas adicionais podem ser aplicadas para este recurso.

Para começar, entre em contato com seu fornecedor preferencial ou com o gerente de conta do Adobe.

![Logotipo ](/help/dsp/assets/comscore-logo.png) ![da ComscoreGrapeshot](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP fez parceria com [!DNL DoubleVerify] para oferecer sua [!DNL Authentic Brand Safety] solução de direcionamento, que permite criar um conjunto centralizado de requisitos de segurança da marca para direcionar a todas as plataformas de compra para fins de consistência.

Depois de criar um segmento de segurança da marca [!DNL DoubleVerify] com o direcionamento necessário, você pode usá-lo em DSP para replicar suas regras de bloco pós-oferta com pré-licitação em ambientes da Web.

Você pode especificar uma ID de segmento [!DNL DoubleVerify] para cada anunciante<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) --> e, opcionalmente, [ativar ou desativar [!UICONTROL Authentic Brand Safety] para cada disposição](/help/dsp/campaign-management/placements/placement-settings.md). DSP conta para uso da ID de segmento.

Para obter mais informações sobre a funcionalidade, entre em contato diretamente com [!DNL DoubleVerify] ou entre em contato com o gerente de conta do Adobe.

![Logotipo do DoubleVerify](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
