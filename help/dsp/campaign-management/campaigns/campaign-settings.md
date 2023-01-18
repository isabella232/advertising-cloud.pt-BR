---
title: Configurações da campanha
description: Consulte descrições das configurações disponíveis da campanha.
feature: DSP Campaigns
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---

# Configurações da campanha

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** O nome da campanha.

**[!UICONTROL Advertiser]:** (Somente leitura para campanhas existentes) O anunciante aplicável (marca). Selecione um anunciante existente ou crie um novo.

**[!UICONTROL Advertiser URL]:** A página oficial do anunciante. Esse campo acelera seu processo de aprovação de anúncios com parceiros de inventário.

**[!UICONTROL Timezone]:** (Somente leitura para campanhas existentes) O fuso horário para relatórios e lances.

**[!UICONTROL Customer PO]:** (Opcional) Uma ordem de compra do cliente para a ordem de inserção/compra.

**[Datas da campanha]:** As datas de início e término da campanha.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Se deseja gerenciar as margens da campanha: *[!UICONTROL Yes]* ou *[!UICONTROL No]* (padrão).

Ao escolher *[!UICONTROL Yes],* especifique o tipo e a quantia da margem:

* **[!UICONTROL Margin Type]:** O tipo de margem. Não é possível alterar o tipo de margem após habilitar o gerenciamento de margem e salvar a campanha.

   * *[!UICONTROL Fixed]:* (o padrão) Permite que o DSP calcule automaticamente e limite o gasto com base em uma porcentagem de margem fixa da variável [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Permite gerenciar margens até o nível de disposição especificando uma [!UICONTROL Budget Reserve %] e [!UICONTROL Gross Budget] para cada pacote e posicionamento na campanha. DSP otimiza com base na eficiência financeira de cada disposição, sem garantir uma margem específica. Use-o para ordens de inserção que consistem em vários itens de linha para os quais você concordou em fornecer uma quantidade fixa de unidades ou tipos de unidades a uma taxa fixa.

* **[!UICONTROL Fixed Margin %]:** (Campanhas com margens fixas apenas) A marcação padrão para cada ordem de inserção <!-- impression? -->, como uma porcentagem. Este montante é deduzido da [!UICONTROL Gross Budget] para definir o orçamento líquido da campanha.

* **[!UICONTROL Budget Reserve %]:** (Campanhas apenas com margens fixas; opcional) Reserva uma porcentagem específica da variável [!UICONTROL Gross Budget] como salvaguarda. Este montante é deduzido da [!UICONTROL Gross Budget] para definir o orçamento líquido da campanha.

**[!UICONTROL Gross Budget]:** (Campanhas com gestão de margem apenas) O orçamento bruto da campanha, antes da aplicação dos ajustamentos marginais especificados.

Opcionalmente, é possível adicionar um orçamento bruto adicional diário, semanal ou mensal:

1. Clique em **[!UICONTROL Add an additional Gross Budget]**.

1. Insira o **[!UICONTROL Gross Budget]** e selecione o intervalo do orçamento: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* ou *[!UICONTROL Monthly]*.

O orçamento líquido total, que é o limite de gastos da campanha, é calculado automaticamente com base nas configurações de margem e é indicado abaixo desse valor.

**[!UICONTROL Budget]:** (Campanhas sem gerenciamento de margem) O orçamento geral da campanha.

**[!UICONTROL Estimated Tax Withholding]:** Retém uma porcentagem do gasto total em despesas com anúncios, taxas de veiculação de anúncios e/ou taxas de dados no nível da conta para impostos locais ou por país. As taxas são estimativas para fins de orçamento e ritmo, portanto as taxas de imposto faturadas podem variar.

Para estimar impostos a serem retidos:

1. Clique em **[!UICONTROL Update rates here]**.

1. Especifique a **[!UICONTROL Estimated tax rate]**, como uma porcentagem.

1. Marque a caixa de seleção ao lado de cada tipo de taxa para a qual reter impostos. Os tipos de taxas incluem:

   * *[!UICONTROL Include estimated tax - ads fee]:* Aplica-se a todos os gastos com publicidade DSP mídia, incluindo impostos sobre taxas de gerenciamento de campanha.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* Aplica-se a todos os gastos em DSP de publicidade, exceto mídia e dados. Ela exclui impostos para taxas de gerenciamento de campanha

   * *[!UICONTROL Include estimated tax - data fee]:* Aplica-se a todos os dados gastos em DSP de publicidade.

1. Clique em **[!UICONTROL Submit]**.

>[!NOTE]
>
>* Nos EUA, os estados podem variar na inclusão de taxas de imposto em anúncios, veiculação de anúncios e dados. Para as organizações de outros países, inclua as três categorias de taxas de imposto a pagar pelo IVA.
>
>* Também é possível definir esses valores nas configurações de tarifas da conta.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]:** (Somente leitura para campanhas existentes criadas desde 22 de junho de 2020; não disponível para campanhas criadas antes de 22 de junho de 2020) O nível em que o DSP irá direcionar anúncios e aplicar limites de frequência: *Mesmo dispositivo* para direcionar um dispositivo ou *Pessoas* para direcionar uma pessoa em todos os seus dispositivos conhecidos.

**[!UICONTROL Device Graph]:** (Somente leitura para campanhas existentes; campanhas com direcionamento entre dispositivos com base em pessoas somente) O gráfico de dispositivos a ser usado para direcionamento entre dispositivos e gerenciamento de frequência:

* *[!UICONTROL LiveRamp - U.S. only]:* Disponível para todos os anunciantes para direcionamento entre dispositivos em US$ 0,35 CPM para impressões que são entregues usando o [!DNL LiveRamp] gráfico de dispositivos (ou seja, para dispositivos não encontrados nos segmentos de público-alvo direcionados). Você pode configurar o direcionamento entre dispositivos no nível da disposição.

   Essa opção também está disponível para todos os anunciantes, sem taxas, para gerenciamento de frequência e medição de atribuição.

**[!UICONTROL Frequency Cap]:** (Opcional) O número de vezes que um dispositivo ou pessoa exclusiva (dependendo do [!UICONTROL Cross Device Level]) serão veiculados anúncios da campanha. As opções incluem *[!UICONTROL Unlimited]* ou um valor específico por dia, semana ou mês.

>[!NOTE]
>
> Você pode definir limites de frequência nos níveis de campanha, pacote e disposição. DSP respeitará o limite de frequência mais restrito na hierarquia da campanha.

**[!UICONTROL Packages]:** O [pacotes](/help/dsp/campaign-management/packages/package-about.md) para incluir na campanha. Selecione pacotes existentes e/ou crie pacotes para incluir. Se você criar pacotes, consulte as descrições sobre o [configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md) para obter mais informações.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>As configurações a seguir ativam apenas os recursos de medição e relatório. A otimização de desempenho é executada somente no nível do pacote e do posicionamento.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Opcional) Habilita [!DNL IAS] medição e emissão de relatórios sobre a possibilidade de visualização, fraude, segurança da marca e verificação de público-alvo, usando as configurações especificadas. Taxas adicionais se aplicam.

* **[!UICONTROL Measure On]:** O inventário sobre o qual se deve medir: *[!UICONTROL Display and VPAID video inventory]* (padrão) ou *[!UICONTROL Display, VPAID & VAST video inventory]*.

   >[!NOTE]
   >
   >A visualização de vídeo pode ser medida somente no inventário VPAID.

* **[!UICONTROL IAS Account ID (AnID)]:** (Anunciantes com seus próprios [!DNL IAS] Contas; opcional) O relatório da organização [!DNL IAS] ID da conta, que [!DNL IAS] cobrará diretamente pelo uso.

* **[!UICONTROL IAS Team ID]:** (Anunciantes com seus próprios [!DNL IAS] Contas; opcional) a ID da equipe do [!DNL IAS] conta, que [!DNL IAS] cobrará diretamente pelo uso. <!-- verify -->

**[!UICONTROL MOAT]:** (Opcional) Habilita [!DNL MOAT] medição e emissão de relatórios sobre visualizabilidade, fraude, segurança da marca e verificação de público-alvo. Taxas adicionais se aplicam.

#### Verificação de público-alvo

**[!UICONTROL Nielsen]:** (Opcional) Habilita [!DNL Nielsen] medição e relatório da verificação de público-alvo, usando as configurações especificadas. Taxas adicionais se aplicam.

* **[!UICONTROL Target Gender]:** O gênero a ser direcionado: *[!UICONTROL Both]* (o padrão), *[!UICONTROL Male]* ou *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** A faixa etária a ser definida como meta. Use os controles deslizantes esquerdo e direito para reduzir o intervalo, conforme necessário.

* **[!UICONTROL Target Country]:** (Opcional) Um país como meta. [!DNL Nielsen] mede impressões servidas somente em países compatíveis.

**[!UICONTROL comScore vCE]:** (Opcional) Habilita [!DNL Comscore validated Campaign Essentials (vCE)] medição e relatório da verificação de público-alvo, usando as configurações especificadas. Taxas adicionais se aplicam.

* **[!UICONTROL Target Gender]:** O gênero a ser direcionado: *[!UICONTROL Both]* (o padrão), *[!UICONTROL Male]* ou *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** A faixa etária a ser definida como meta. Use os controles deslizantes esquerdo e direito para reduzir o intervalo, conforme necessário.

* **[!UICONTROL Target Country]:** (Opcional) Um país como meta. [!DNL Comscore] mede impressões servidas somente em países compatíveis.

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Permite a avaliação e o relatório primários da visualização usando o [!DNL IAB Open Video Viewability (OpenVV)] tecnologia, com base no nível de sensibilidade especificado:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Sobre o Campaign Management](campaign-about.md)
>* [Criar uma campanha](campaign-create.md)
>* [Editar uma campanha](campaign-edit.md)

