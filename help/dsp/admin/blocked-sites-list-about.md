---
type: Documentation
cloud: Experience Cloud
solution: Advertising Cloud
product: advertising cloud
title: Sobre as listas de sites bloqueados no nível da conta e no nível do anunciante
description: Sobre as listas de sites bloqueados no nível da conta e no nível do anunciante
source-git-commit: ac35677ef4832177b7a7e735bbbbf24454371496
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Sobre as listas de sites bloqueados no nível da conta e no nível do anunciante

<!-- Can you just add domains for your acct profile or advertiser to which you have access? It doesn't look like you can remove or edit any existing domains. Or can you with a specific syntax? -->

<!-- For domains, sub-domains,...? Specify what is valid. -->
Você pode editar a lista de sites bloqueados usada para toda a conta do Advertising Cloud e listas adicionais para anunciantes individuais na conta.

Os sites bloqueados listam os conjuntos de metas a serem excluídos para suas disposições. Cada lista pode consistir em domínios de sites de nível superior e qualquer nível <!--- verify --> de subdomínios (como example.com, my.example.com ou my.new.example.com) e nomes de aplicativos móveis (como ???)<!-- package names/app IDs, the full URL in Google Play/iTunes? Specify what is valid. -->.

As listas no nível do anunciante substituem as listas no nível da conta.

>[!NOTE]
>
>* As listas de sites bloqueados no nível da conta e do anunciante são aplicadas além da Advertising Cloud DSP [lista de sites bloqueados globalmente](/help/dsp/introduction/features/brand-safety-media-quality.md), que incluem sites considerados inseguros para anúncios.
>* Os usuários também podem adicionar sites direcionados a qualquer disposição.
>* As listas de sites bloqueados sempre substituem as listas de sites direcionados. Se uma disposição excluir e incluir a mesma meta para um anúncio, a meta será excluída. <!-- Verify -->


>[!MORELIKETHIS]
<!--
>* [Edit an Account-level or Advertiser-level Blocked Site List](/help/dsp/admin/blocked-sites-list-edit.md)
[Brand Safety and Media Quality](/help/dsp/introduction/features/brand-safety-media-quality.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
-->
