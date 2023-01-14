---
title: Sobre o Gerenciamento de público-alvo em DSP de publicidade
description: Saiba mais sobre os recursos de gerenciamento de público-alvo.
feature: DSP Audiences, DSP Segments
exl-id: 624d2211-59a2-4791-b8f1-a9a5cecd0b8e
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '1036'
ht-degree: 0%

---

# Sobre o Gerenciamento de público-alvo em DSP de publicidade

No DSP, é possível criar e gerenciar segmentos de público-alvo e conjuntos de públicos-alvo, que você pode usar como alvos para suas disposições:

* Você pode coletar seus próprios dados de público-alvo primários criando e implementando segmentos. Posteriormente, é possível redirecionar os usuários no segmento com anúncios ou impedir que os usuários nele recebam anúncios. Você pode criar os seguintes tipos de segmentos:

   * [Segmentos personalizados](/help/dsp/audiences/custom-segment-create.md) para rastrear a) usuários expostos a anúncios de dispositivos de desktop, móveis e CTV e b) usuários que visitam páginas da Web específicas.

   * [Segmentos de cancelamento de venda do CCPA](/help/dsp/audiences/ccpa-opt-out-segment-create.md) para rastrear as IDs de usuários das solicitações de cancelamento da venda do consumidor no seu site, de acordo com a California Consumer Privacy Act (CCPA). É possível recuperar relatórios mensais das IDs de usuário a partir de solicitações de recusa de venda.

      Para obter mais informações sobre o suporte de publicidade Adobe para solicitações de cancelamento de venda do CCPA, consulte [Suporte de publicidade Adobe para a Lei de Privacidade do Consumidor da Califórnia: Suporte ao cancelamento da adesão do consumidor](/help/privacy/ccpa-opt-out-of-sale.md).

* Você pode criar uma biblioteca de público-alvo de [públicos-alvo reutilizáveis](/help/dsp/audiences/reusable-audience-create.md). Os públicos salvos são compostos de qualquer um dos segmentos de público-alvo disponíveis e de qualquer um dos outros públicos salvos. Todas as alterações feitas em um público-alvo salvo são aplicadas automaticamente a todas as disposições que direcionam ou excluem o público-alvo e a todos os outros públicos-alvo que incluem o público-alvo salvo.

   Públicos salvos permitem que os planejadores de mídia agruparem públicos conforme necessário, incluindo e excluindo vários segmentos usando uma lógica booleana complexa. O tamanho de cada segmento individual e o tamanho total do público-alvo são indicados durante a criação de um público-alvo. Os executores de campanha podem simplesmente selecionar um ou mais públicos salvos como alvos de disposição, em vez de configurar manualmente os públicos-alvo para cada disposição.

Tipos adicionais de público-alvo também estão disponíveis para direcionamento por posicionamento.

## Importação de segmentos de dados primários e de terceiros

DSP pode importar seus próprios segmentos de dados primários da sua plataforma de gerenciamento de dados (DMP) e fornecê-los a qualquer conjunto de anunciantes, conforme necessário.

DSP é um destino integrado para [o [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), permitindo compartilhar segmentos originais autenticados com anunciantes e usuários aprovados para ativação da campanha. Para saber mais sobre a integração do Real-Time CDP, consulte o [Seção Fontes](/help/dsp/audiences/sources/source-about.md).

DSP também pode importar segmentos personalizados de terceiros, incluindo combinações complexas de segmentos de terceiros. Você pode fornecer os segmentos a qualquer conjunto de anunciantes, conforme necessário.

Entre em contato com seu [!DNL Adobe] para obter mais informações.

## Públicos-alvo disponíveis como metas de posicionamento

Você pode direcionar suas disposições para todos os tipos de público-alvo a seguir.

* Todos os conjuntos de públicos-alvo criados pelo usuário que foram salvos em DSP.

* Todos os segmentos de público-alvo criados pelo usuário que foram criados no DSP:

   * Segmentos personalizados para usuários que visitaram páginas da Web específicas e usuários expostos a impressões de anúncios específicos.

   * Segmentos de público-alvo de não participação na venda do CCPA para usuários que enviaram solicitações de não participação na venda em seu site, de acordo com a California Consumer Privacy Act (CCPA).

* Todos os segmentos de dados primários importados.

* Todos os segmentos de dados personalizados de terceiros importados.

* (Disposições direcionadas somente para os EUA) [Todos os segmentos de dados de terceiros disponíveis para DSP clientes de mais de 30 provedores](/help/dsp/audiences/third-party-data-providers.md), incluindo [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast]e muito mais.

   Você pode direcionar segmentos específicos, que direcionam usuários com base em dados de público-alvo (por exemplo, usuários com dados demográficos, interesses ou intenções específicos e/ou perfis comportamentais). Você pode navegar por provedor de dados e categoria, pesquisar segmentos por nome ou ID de segmento, ou filtrar os resultados por provedor de dados, tamanho total do segmento, contagem de navegador da Web ou contagem de dispositivos.

   Segmentos de terceiros incorrem em tarifas adicionais, que são indicadas ao lado de cada nome de segmento.

* (Anunciantes com a Adobe Experience Platform e [!DNL Real-Time CDP], Adobe Audience Manager ou Adobe Analytics que usam somente as tags de conversão JavaScript de Adobe Advertising) Todos os segmentos de público-alvo de primeiro, segundo ou terceiro disponíveis criados no [!DNL Real-Time CDP], criado no Audience Manager ou publicado no Adobe Experience Cloud a partir do Audience Manager ou [!DNL Analytics].

   A precificação para o uso dos segmentos é pré-negociada e não é visível no DSP.

   Segmentos de [!DNL Analytics] estão disponíveis cerca de uma hora depois de criá-los ou publicá-los como Experience Cloud audiences. Segmentos provenientes diretamente do Audience Manager ou [!DNL Real-Time CDP] estão disponíveis dentro de 24 horas após compartilhá-los.

   >[!NOTE]
   >
   >Consulte a documentação para [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html)e [o [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) para obter informações sobre como configurar e coletar dados para segmentos nessas soluções.

## Dados de tamanho de público-alvo

Nas configurações salvas do público-alvo e das configurações de posicionamento, é possível visualizar dados detalhados do tamanho do público-alvo:

* O tamanho total e ativo do público-alvo desduplicado em todos os segmentos selecionados e os públicos salvos é exibido, e você pode exibir detalhes por tipo de dispositivo (navegador, celular ou TV conectada).

   ![o tamanho do público-alvo combinado](/help/dsp/assets/audience-size.png)

* Para segmentos individuais e públicos salvos, o tamanho total do público-alvo e o CPM (quando aplicável) são exibidos ao lado do nome do segmento. Você pode visualizar mais detalhes sobre o segmento, incluindo o tamanho por tipo de dispositivo (navegador, celular ou TV conectada). Para públicos salvos, o tamanho total é o total desduplicado.

   ![o tamanho individual do segmento](/help/dsp/assets/audience-size-segment.png)

## As exibições de públicos-alvo

### A exibição Todos os públicos

No [!UICONTROL All Audiences] Para visualizar a Biblioteca de público-alvo, é possível salvar e gerenciar públicos reutilizáveis, que incluem grupos de segmentos de público-alvo e até outros públicos salvos. Você pode usar públicos-alvo como alvos para várias disposições. O número de disposições em que cada público-alvo é usado é indicado ao lado do nome da disposição.

Você pode editar, clonar, excluir, exportar ou compartilhar qualquer público-alvo.

### A visualização Segmentos

No [!UICONTROL Segments] , todos os usuários podem criar segmentos personalizados adicionais.

O [!UICONTROL Segments] também lista os seguintes tipos de segmento:

* Todos os segmentos personalizados criados pelo usuário estão disponíveis para o usuário.

   Você pode exibir tags de rastreamento para qualquer um dos segmentos personalizados criados e compartilhá-los com outros usuários. Também é possível editar ou excluir os segmentos personalizados criados.

   Você não pode editar ou compartilhar segmentos personalizados que outros usuários compartilharam com você.

* Todos os segmentos primários importados disponíveis para o usuário.

   Não é possível editar ou compartilhar segmentos primários que foram compartilhados com você. Entre em contato com seu [!DNL Adobe] equipe de contas caso precise compartilhar segmentos primários com usuários adicionais.

* Todos os segmentos personalizados de terceiros disponíveis para o usuário.

   Não é possível editar ou compartilhar segmentos de terceiros que foram compartilhados com você. Entre em contato com seu [!DNL Adobe] equipe de contas caso precise compartilhar segmentos de terceiros com usuários adicionais.

>[!MORELIKETHIS]
>
>* [Criar um público-alvo reutilizável](reusable-audience-create.md)
>* [Configurações de público-alvo](audience-settings.md)
>* [Sintaxe para lógica de segmento do público-alvo](audience-segment-logic-syntax.md)
>* [Criar e implementar um segmento personalizado](custom-segment-create.md)
>* [Criar e implementar um [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Fornecedores de dados de terceiros disponíveis](third-party-data-providers.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)

