---
title: Sobre [!UICONTROL CCPA Opt-out-of-Sale] Segmentos e relatórios
description: Saiba mais sobre como criar segmentos para rastrear IDs de solicitações de não participação na venda do CCPA e como recuperar relatórios das IDs.
feature: CCPA, DSP Segments
exl-id: 9256d34e-d0dd-4abf-bc96-2b599caf2a8e
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# Sobre [!UICONTROL CCPA Opt-out-of-Sale] Segmentos e relatórios

Você pode rastrear as IDs de usuários das solicitações de recusa de venda do consumidor no seu site, de acordo com a California Consumer Privacy Act (CCPA), ao [criar e implementar um segmento de recusa de venda da CCPA](ccpa-opt-out-segment-create.md). Os usuários permanecem indefinidamente em segmentos de opção de não participação na CCPA.

Quando a tag de pixel do segmento for implementada, a Advertising Cloud começará a coletar um pool de IDs em nome do anunciante.

## Relatórios de cancelamento de venda do consumidor

O Advertising Cloud gera relatórios mensais de IDs que os clientes enviaram para solicitações de não participação na venda da conta. Os dados consolidam solicitações capturadas por meio de segmentos de não participação na venda do CCPA criados no Advertising Cloud DSP e quaisquer envios feitos por meio da API do Privacy Service.  Os relatórios são gerados no primeiro de cada mês do mês anterior. Por exemplo, a lista mensal de usuários para junho está disponível em 1 de julho.

Cada relatório está disponível como um arquivo de texto separado por tabulações compactado no formato GZIP. As IDs de usuário capturadas nos segmentos de não participação na venda do CCPA são identificadas por segmento e pelo anunciante.

Você pode [recuperar links para os relatórios mensais](ccpa-opt-out-segment-report-retrieve.md) que foram criados nos três meses anteriores, dentro do Advertising Cloud DSP ou usando o Advertising Cloud [!DNL Trafficking API]. Cada link é válido por sete dias, mas é atualizado sempre que um cliente tenta recuperar um.

>[!MORELIKETHIS]
>
>* [Suporte da Adobe Advertising Cloud para a Lei de Privacidade do Consumidor da Califórnia: Suporte ao cancelamento da adesão do consumidor](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)
>* [Criar e implementar um  [!UICONTROL CCPA Opt-Out-of-Sale] segmento](ccpa-opt-out-segment-create.md)
>* [Recuperar relatórios de cancelamento da venda do consumidor](ccpa-opt-out-segment-report-retrieve.md)
>* [Sobre o Gerenciamento de público-alvo](audience-about.md)

