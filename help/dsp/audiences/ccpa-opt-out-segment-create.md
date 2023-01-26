---
title: Criar e implementar um segmento de recusa de venda da CCPA
description: Saiba como criar e implementar um segmento para rastrear as IDs de usuários das solicitações de cancelamento da venda do consumidor.
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
source-git-commit: 1b5f5a56045616a2d67d9bfc5840bb1f06436fbb
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Criar e implementar um segmento de recusa de venda da CCPA

Você pode criar um segmento para rastrear IDs de usuários a partir de solicitações de cancelamento da venda do consumidor no seu site, de acordo com a California Consumer Privacy Act (CCPA). Os usuários permanecem indefinidamente em segmentos de opção de não participação na CCPA.

Quando a tag pixel do segmento for implementada, a Adobe Advertising começará a coletar um pool de IDs em nome do anunciante.

>[!NOTE]
>
>* Para obter informações sobre como comunicar solicitações de cancelamento de venda do CCPA à Adobe Advertising usando a API do Adobe Experience Platform Privacy Service, consulte [https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ccpa/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ccpa/ccpa-opt-out-of-sale.html).
>* Para rastrear usuários que visitam páginas da Web para fins não relacionados ao rastreamento de eventos de não participação na venda do CCPA, bem como usuários expostos a anúncios de computadores, dispositivos móveis e dispositivos CTV, crie uma [segmento personalizado](/help/dsp/audiences/custom-segment-create.md).


1. Crie o segmento:

   1. No menu principal, clique em **Públicos-alvo > Segmentos**.

   1. Acima da tabela de dados, clique em **[!UICONTROL Create]**.

   1. Insira um **[!UICONTROL Segment Name]**.

      Nome de segmento recomendado: &quot;&lt;*Seu nome do anunciante*> - Não participação na venda do CCPA&quot; (como &quot;Acme - CCPA Opt out of Sale&quot;)

   1. Para o [!UICONTROL Segment Type], selecione **[!UICONTROL CCPA Opt-out of sale]**.

   1. Clique em **[!UICONTROL Save]**.

1. Copie e implemente uma tag de pixel para rastrear o segmento:

   1. Retornar para **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. Na linha do segmento, mantenha o cursor sobre o novo segmento e clique em **[!UICONTROL Get pixel]**.

   1. Copie o pixel da imagem (começando com `<img src="https://rtd-tm.everesttech.net"`) para coletar IDs de usuário de visitantes móveis e de desktop em uma página da Web.

   1. Forneça a tag para o anunciante ou contato do site para implantação usando o mecanismo usado pela empresa para rastrear solicitações de recusa de venda da CCPA (como o uso de uma Plataforma de gerenciamento de consentimento).

      O departamento de TI do anunciante ou outro grupo pode precisar agendar ou ser informado sobre a implantação da tag.

      Quando o pixel for implementado, a Adobe Advertising começará a coletar um pool de IDs em nome do anunciante.

      Embora a opção e a lógica de implementação sejam da responsabilidade do anunciante, este é um exemplo de como um anunciante pode acionar o pixel:

      1. Um consumidor chega à página inicial do anunciante.
      1. O consumidor encontra e clica no botão &quot;Recusa de venda da CCPA&quot; do anunciante.
      1. O consumidor é apresentado com uma lista de provedores de serviços com os quais o anunciante trabalha.
      1. O consumidor marca a caixa para recusar a venda de dados para Adobe Advertising.

         Essa ação aciona o pixel para ser acionado e coletar a ID de cookie do consumidor dentro do &quot;[!UICONTROL CCPA Opt-out of sale]&quot;.

>[!MORELIKETHIS]
>
>* [Suporte de publicidade Adobe para a Lei de Privacidade do Consumidor da Califórnia: Suporte ao cancelamento da adesão do consumidor](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Sobre [!UICONTROL CCPA Opt-out-of-Sale] Segmentos e relatórios](ccpa-opt-out-about.md)
>* [Recuperar relatórios de cancelamento da venda do consumidor](ccpa-opt-out-segment-report-retrieve.md)
>* [Criar e implementar um segmento personalizado](custom-segment-create.md)
>* [Sobre o Gerenciamento de público-alvo](audience-about.md)

