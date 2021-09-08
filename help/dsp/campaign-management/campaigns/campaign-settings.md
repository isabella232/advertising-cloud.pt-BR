---
title: Configurações da campanha
description: Consulte descrições das configurações disponíveis da campanha.
feature: Campaigns
exl-id: ff2e22ff-8073-4532-884b-36e0c1f22641
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Configurações da campanha

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** O nome da campanha.

**[!UICONTROL Advertiser]:**  (somente leitura para campanhas existentes) O anunciante aplicável (marca). Selecione um anunciante existente ou crie um novo.

**[!UICONTROL Advertiser URL]:** A página oficial do anunciante. Esse campo acelera seu processo de aprovação de anúncios com parceiros de inventário.

**[!UICONTROL Timezone]:**  (somente leitura para campanhas existentes) O fuso horário para relatórios e lances.

**[!UICONTROL Customer PO]:** (Opcional) Uma ordem de compra do cliente para a ordem de inserção/ordem de compra.

**[Datas da campanha]:** as datas de início e término da campanha.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Se deseja gerenciar as margens da campanha:  *[!UICONTROL Yes]* ou  *[!UICONTROL No]* (o padrão).

Ao escolher *[!UICONTROL Yes],* especifique o tipo e a quantia da margem:

* **[!UICONTROL Margin Type]:** o tipo de margem. Não é possível alterar o tipo de margem após habilitar o gerenciamento de margem e salvar a campanha.

   * *[!UICONTROL Fixed]:* (o padrão) permite que o Advertising Cloud DSP calcule e limite o gasto automaticamente com base em uma porcentagem de margem fixa do  [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* permite gerenciar as margens até o nível de posicionamento, especificando um  [!UICONTROL Budget Reserve %] e  [!UICONTROL Gross Budget] para cada pacote e posicionamento na campanha. O Advertising Cloud DSP otimiza com base na eficiência financeira de cada disposição, sem garantir uma margem específica. Use-o para ordens de inserção que consistem em vários itens de linha para os quais você concordou em fornecer uma quantidade fixa de unidades ou tipos de unidades a uma taxa fixa.

* **[!UICONTROL Fixed Margin %]:** (Campanhas com margens fixas apenas) A marcação padrão para cada ordem de inserção,  <!-- impression? -->como uma porcentagem. Esse valor é deduzido do [!UICONTROL Gross Budget] para definir o orçamento líquido da campanha.

* **[!UICONTROL Budget Reserve %]:** (Campanhas apenas com margens fixas; opcional) Reserva uma percentagem específica do  [!UICONTROL Gross Budget] como salvaguarda. Esse valor é deduzido do [!UICONTROL Gross Budget] para definir o orçamento líquido da campanha.

**[!UICONTROL Gross Budget]:** (Campanhas com gerenciamento de margem somente) O orçamento bruto da campanha, antes da aplicação dos ajustes marginais especificados.

Opcionalmente, é possível adicionar um orçamento bruto adicional diário, semanal ou mensal:

1. Clique em **[!UICONTROL Add an additional Gross Budget]**.

1. Insira o **[!UICONTROL Gross Budget]** e selecione o intervalo do orçamento: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* ou *[!UICONTROL Monthly]*.

O orçamento líquido total, que é o limite de gastos da campanha, é calculado automaticamente com base nas configurações de margem e é indicado abaixo desse valor.

**[!UICONTROL Budget]:**  (Campanhas sem gerenciamento de margem) O orçamento geral da campanha.

**[!UICONTROL Estimated Tax Withholding]:** Retorna uma porcentagem do gasto total em taxas de publicidade, taxas de veiculação de anúncios e/ou taxas de dados no nível da conta para impostos locais ou por país. As taxas são estimativas para fins de orçamento e ritmo, portanto as taxas de imposto faturadas podem variar.

Para estimar impostos a serem retidos:

1. Clique em **[!UICONTROL Update rates here]**.

1. Especifique o **[!UICONTROL Estimated tax rate]**, como uma porcentagem.

1. Marque a caixa de seleção ao lado de cada tipo de taxa para a qual reter impostos. Os tipos de taxas incluem:

   * *[!UICONTROL Include estimated tax - ads fee]:* aplica-se a todos os gastos com mídia do Advertising Cloud DSP, incluindo impostos sobre taxas de gerenciamento de campanha.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* aplica-se a todos os gastos no Advertising Cloud DSP, exceto mídia e dados. Ela exclui impostos para taxas de gerenciamento de campanha

   * *[!UICONTROL Include estimated tax - data fee]:* aplica-se a todos os dados gastos no Advertising Cloud DSP.

1. Clique em **[!UICONTROL Submit]**.

>[!NOTE]
>
>* Nos EUA, os estados podem variar na inclusão de taxas de imposto em anúncios, veiculação de anúncios e dados. Para as organizações de outros países, inclua as três categorias de taxas de imposto a pagar pelo IVA.
>
>* Você também pode configurar esses valores nas configurações de tarifas da conta.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]:** (somente leitura para campanhas existentes criadas desde 22 de junho de 2020; não disponível para campanhas criadas antes de 22 de junho de 2020) O nível no qual o Advertising Cloud irá direcionar anúncios e aplicar limites de frequência:  *Mesmo* dispositivo para direcionar um dispositivo ou  ** pessoas a uma pessoa em todos os dispositivos conhecidos.

**[!UICONTROL Device Graph]:**  (somente leitura para campanhas existentes; campanhas com direcionamento entre dispositivos com base em pessoas somente) O gráfico de dispositivos a ser usado para direcionamento entre dispositivos e gerenciamento de frequência:

* *[!UICONTROL LiveRamp - U.S. only]:* disponível para todos os anunciantes para direcionamento entre dispositivos em US$ 0,35 CPM para impressões que são entregues usando o gráfico de  [!DNL LiveRamp] dispositivos (ou seja, para dispositivos não encontrados nos segmentos de público-alvo direcionados). Você pode configurar o direcionamento entre dispositivos no nível da disposição.

   Essa opção também está disponível para todos os anunciantes, sem taxas, para gerenciamento de frequência e medição de atribuição.

* *[!UICONTROL Adobe Co-op U.S. and Canada only]:* Disponível somente para  [!DNL Device Co-op] participantes do Adobe Experience Cloud sem taxas adicionais.

>[!TIP]
>
>Se o anunciante também usar atribuição entre dispositivos, a prática recomendada é usar as mesmas configurações de gráficos de dispositivos para direcionamento e gerenciamento de frequência que as especificadas nas configurações de atribuição entre dispositivos do anunciante. Se você selecionar um gráfico de dispositivos diferente para essa campanha, podem ocorrer discrepâncias de relatórios.

**[!UICONTROL Frequency Cap]:** (opcional) o número de vezes que um dispositivo ou uma pessoa exclusiva (dependendo do especificado  [!UICONTROL Cross Device Level]) será veiculada nos anúncios da campanha. As opções incluem *[!UICONTROL Unlimited]* ou uma quantidade específica por dia, semana ou mês.

>[!NOTE]
>
> Você pode definir limites de frequência nos níveis de campanha, pacote e disposição. DSP respeitará o limite de frequência mais restrito na hierarquia da campanha.

**[!UICONTROL Packages]:** Os  [](/help/dsp/campaign-management/packages/package-about.md) pacotes a serem incluídos na campanha. Selecione pacotes existentes e/ou crie pacotes para incluir. Se você criar pacotes, consulte descrições sobre as [configurações de pacote](/help/dsp/campaign-management/packages/package-settings.md) para obter mais informações.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>As configurações a seguir ativam apenas os recursos de medição e relatório. A otimização de desempenho é executada somente no nível do pacote e do posicionamento.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (opcional) permite a  [!DNL IAS] medição e a emissão de relatórios sobre visibilidade, fraude, segurança da marca e verificação de público-alvo, usando as configurações especificadas. Taxas adicionais se aplicam.

* **[!UICONTROL Measure On]:** O inventário em que deve ser medida:  *[!UICONTROL Display and VPAID video inventory]* (o padrão) ou  *[!UICONTROL Display, VPAID & VAST video inventory]*.

   >[!NOTE]
   >
   >A visualização de vídeo pode ser medida somente no inventário VPAID.

* **[!UICONTROL IAS Account ID (AnID)]:** (Anunciantes com  [!DNL IAS] contas próprias; opcional) a ID da  [!DNL IAS] conta da organização, que  [!DNL IAS] cobrará diretamente pelo uso.

* **[!UICONTROL IAS Team ID]:** (Anunciantes com  [!DNL IAS] contas próprias; (opcional) A ID da equipe da  [!DNL IAS] conta da organização, que  [!DNL IAS] cobrará diretamente pelo uso.  <!-- verify -->

**[!UICONTROL MOAT]:** (opcional) permite a  [!DNL MOAT] medição e a emissão de relatórios sobre visualizabilidade, fraude, segurança da marca e verificação de público-alvo. Taxas adicionais se aplicam.

#### Verificação de público-alvo

**[!UICONTROL Nielsen]:** (opcional) permite a  [!DNL Nielsen] medição e o relatório da verificação de público-alvo, usando as configurações especificadas. Taxas adicionais se aplicam.

* **[!UICONTROL Target Gender]:** O gênero a ser direcionado:  *[!UICONTROL Both]* (o padrão),  *[!UICONTROL Male]* ou  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** a faixa etária a ser definida. Use os controles deslizantes esquerdo e direito para reduzir o intervalo, conforme necessário.

* **[!UICONTROL Target Country]:** (Opcional) Um país para definir como meta. [!DNL Nielsen] mede impressões servidas somente em países compatíveis.

**[!UICONTROL comScore vCE]:** (opcional) permite a  [!DNL Comscore validated Campaign Essentials (vCE)] medição e o relatório da verificação de público-alvo, usando as configurações especificadas. Taxas adicionais se aplicam.

* **[!UICONTROL Target Gender]:** O gênero a ser direcionado:  *[!UICONTROL Both]* (o padrão),  *[!UICONTROL Male]* ou  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** a faixa etária a ser definida. Use os controles deslizantes esquerdo e direito para reduzir o intervalo, conforme necessário.

* **[!UICONTROL Target Country]:** (Opcional) Um país para definir como meta. [!DNL Comscore] mede impressões servidas somente em países compatíveis.

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** permite a medição e o relatório primários da possibilidade de visualização usando a  [!DNL IAB Open Video Viewability (OpenVV)] tecnologia, com base no nível de sensibilidade especificado:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de campanhas](campaign-about.md)
>* [Criar uma campanha](campaign-create.md)
>* [Editar uma campanha](campaign-edit.md)

