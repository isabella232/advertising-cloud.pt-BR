---
title: Sobre o Gerenciamento de público-alvo no Advertising Cloud DSP
description: Saiba mais sobre os recursos de gerenciamento de público-alvo.
feature: DSP Audiences, DSP Segments
exl-id: 624d2211-59a2-4791-b8f1-a9a5cecd0b8e
source-git-commit: 578651a458ffd505573df0e9a61e26bd2176ad17
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 0%

---

# Sobre o Gerenciamento de público-alvo no Advertising Cloud DSP

No Advertising Cloud DSP, é possível criar e gerenciar segmentos de público-alvo e conjuntos de públicos-alvo, que você pode usar como alvos para suas disposições:

* Você pode coletar seus próprios dados de público-alvo primários criando e implementando segmentos. Posteriormente, é possível redirecionar os usuários no segmento com anúncios ou impedir que os usuários nele recebam anúncios. Você pode criar os seguintes tipos de segmentos:

   * [Segmentos personalizados para rastrear a) usuários expostos a anúncios de computadores, dispositivos móveis e dispositivos CTV e b) usuários que visitam páginas da Web específicas. ](/help/dsp/audiences/custom-segment-create.md) 

   * [Segmentos de cancelamento de venda do CCPA para rastrear as IDs de usuários das solicitações de cancelamento de venda do consumidor no seu site, de acordo com a California Consumer Privacy Act (CCPA). ](/help/dsp/audiences/ccpa-opt-out-segment-create.md) É possível recuperar relatórios mensais das IDs de usuário a partir de solicitações de recusa de venda.

      Para obter mais informações sobre o suporte do Advertising Cloud para solicitações de cancelamento de venda da CCPA, consulte [Adobe Advertising Cloud Support for the California Consumer Privacy Act: Suporte para cancelamento do consumidor](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html).

* Você pode criar uma biblioteca de público-alvo de [públicos-alvo reutilizáveis](/help/dsp/audiences/reusable-audience-create.md). Os públicos salvos são compostos de qualquer um dos segmentos de público-alvo disponíveis e de qualquer um dos outros públicos salvos. Todas as alterações feitas em um público-alvo salvo são aplicadas automaticamente a todas as disposições que direcionam ou excluem o público-alvo e a todos os outros públicos-alvo que incluem o público-alvo salvo.

   Públicos salvos permitem que os planejadores de mídia agruparem públicos conforme necessário, incluindo e excluindo vários segmentos usando uma lógica booleana complexa. O tamanho de cada segmento individual e o tamanho total do público-alvo são indicados durante a criação de um público-alvo. Os executores de campanha podem simplesmente selecionar um ou mais públicos salvos como alvos de disposição, em vez de configurar manualmente os públicos-alvo para cada disposição.

Tipos adicionais de público-alvo também estão disponíveis para direcionamento por posicionamento.

## Importação de segmentos de dados primários e de terceiros

A Advertising Cloud DSP pode importar seus próprios segmentos de dados primários da sua plataforma de gerenciamento de dados (DMP) e fornecê-los a qualquer conjunto de anunciantes, conforme necessário.

O Advertising Cloud DSP também pode importar segmentos personalizados de terceiros, incluindo combinações complexas de segmentos de terceiros. Você pode fornecer os segmentos a qualquer conjunto de anunciantes, conforme necessário.

Entre em contato com o Gerente de conta para obter mais informações.

## Públicos-alvo disponíveis como metas de posicionamento

Você pode direcionar suas disposições para todos os tipos de público-alvo a seguir.

* Todos os conjuntos de públicos-alvo criados pelo usuário que foram salvos no Advertising Cloud DSP.

* Todos os segmentos de público-alvo criados pelo usuário que foram criados no Advertising Cloud DSP:

   * Segmentos personalizados para usuários que visitaram páginas da Web específicas e usuários expostos a impressões de anúncios específicos.

   * Segmentos de público-alvo de não participação na venda do CCPA para usuários que enviaram solicitações de não participação na venda em seu site, de acordo com a California Consumer Privacy Act (CCPA).

* Todos os segmentos de dados primários importados.

* Todos os segmentos de dados personalizados de terceiros importados.

* (Disposições direcionadas somente para os EUA) [Todos os segmentos de dados de terceiros disponíveis para clientes do Advertising Cloud DSP de mais de 30 provedores](/help/dsp/audiences/third-party-data-providers.md), incluindo [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast] e muito mais.

   Você pode direcionar segmentos específicos, que direcionam usuários com base em dados de público-alvo (por exemplo, usuários com dados demográficos, interesses ou intenções específicos e/ou perfis comportamentais). Você pode navegar por provedor de dados e categoria, pesquisar segmentos por nome ou ID de segmento, ou filtrar os resultados por provedor de dados, tamanho total do segmento, contagem de navegador da Web ou contagem de dispositivos.

   Segmentos de terceiros incorrem em tarifas adicionais, que são indicadas ao lado de cada nome de segmento.

* (Anunciantes com Adobe Experience Cloud, Adobe Audience Manager ou Adobe Analytics que usam somente tags de conversão JavaScript do Advertising Cloud) Todos os seus segmentos de público-alvo disponíveis, primários, secundários ou de terceiros, criados no Adobe Experience Cloud, criados no Audience Manager ou publicados no Adobe Experience Cloud a partir do Audience Manager ou [!DNL Analytics].

   A precificação para o uso dos segmentos é pré-negociada e não é visível no Advertising Cloud.  <!-- Verify -->

   Os segmentos do Adobe Experience Cloud estão disponíveis cerca de uma hora depois que você os cria ou publica no Adobe Experience Cloud. Os segmentos provenientes diretamente do Audience Manager estão disponíveis cerca de 24 horas após sua criação. <!-- Verify all -->

   >[!NOTE]
   >
   >Consulte a documentação para [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html) e [Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) para obter informações sobre como configurar e coletar dados para segmentos nessas soluções.

## Dados de tamanho de público-alvo

Nas configurações salvas do público-alvo e das configurações de posicionamento, é possível visualizar dados detalhados do tamanho do público-alvo:

* O tamanho total e ativo do público-alvo desduplicado em todos os segmentos selecionados e os públicos salvos é exibido, e você pode exibir detalhes por tipo de dispositivo (navegador, celular ou TV conectada).

   ![o tamanho do público-alvo combinado](/help/dsp/assets/audience-size.png)

* Para segmentos individuais e públicos salvos, o tamanho total do público-alvo e o CPM (quando aplicável) são exibidos ao lado do nome do segmento. Você pode visualizar mais detalhes sobre o segmento, incluindo o tamanho por tipo de dispositivo (navegador, celular ou TV conectada). Para públicos salvos, o tamanho total é o total desduplicado.

   ![o tamanho individual do segmento](/help/dsp/assets/audience-size-segment.png)

## As exibições de públicos-alvo

### A exibição Todos os públicos

Na visualização [!UICONTROL All Audiences] ou na Biblioteca de público-alvo, é possível salvar e gerenciar públicos reutilizáveis, que incluem grupos de segmentos de público-alvo e até outros públicos salvos. Você pode usar públicos-alvo como alvos para várias disposições. O número de disposições em que cada público-alvo é usado é indicado ao lado do nome da disposição.

Você pode editar, clonar, excluir, exportar ou compartilhar qualquer público-alvo.

### A visualização Segmentos

Na visualização [!UICONTROL Segments], todos os usuários podem criar segmentos personalizados adicionais.

A visualização [!UICONTROL Segments] também lista os seguintes tipos de segmento:

* Todos os segmentos personalizados criados pelo usuário estão disponíveis para o usuário.

   Você pode exibir tags de rastreamento para qualquer um dos segmentos personalizados criados e compartilhá-los com outros usuários. Também é possível editar ou excluir os segmentos personalizados criados.

   Você não pode editar ou compartilhar segmentos personalizados que outros usuários compartilharam com você.

* Todos os segmentos primários importados disponíveis para o usuário.

   Não é possível editar ou compartilhar segmentos primários que foram compartilhados com você. Entre em contato com o Gerente de conta se precisar compartilhar segmentos primários com usuários adicionais.

* Todos os segmentos personalizados de terceiros disponíveis para o usuário.

   Não é possível editar ou compartilhar segmentos de terceiros que foram compartilhados com você. Entre em contato com o Gerente de conta se precisar compartilhar segmentos de terceiros com usuários adicionais.

>[!MORELIKETHIS]
>
>* [Criar um público-alvo reutilizável](reusable-audience-create.md)
>* [Configurações de público-alvo](audience-settings.md)
>* [Sintaxe para lógica de segmento do público-alvo](audience-segment-logic-syntax.md)
>* [Criar e implementar um segmento personalizado](custom-segment-create.md)
>* [Criar e implementar um  [!UICONTROL CCPA Opt-Out-of-Sale] segmento](ccpa-opt-out-segment-create.md)
>* [Fornecedores de dados de terceiros disponíveis](third-party-data-providers.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)

