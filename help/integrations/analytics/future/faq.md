---
title: Perguntas frequentes
description: xxx
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Perguntas frequentes xxx

## título

https://adobeadcloud.zendesk.com/agent/tickets/14214 Por padrão, o Adobe Analytics relata todos os eventos capturados em cada relatório. &quot;[!UICONTROL Unspecified]&quot; representam eventos de preenchimento de formulário que não foram conectados à Adobe Advertising. Por exemplo, no relatório Plataforma de publicidade , as conversões orgânicas ou as conversões orientadas por uma campanha de email se encaixavam em &quot;não especificado&quot;.

Você pode usar o filtro para remover eventos não especificados dos relatórios, removendo a marca de seleção pela opção &quot;Incluir não especificado (nenhum)&quot;. <!-- Not sure if this is in DSP or in Analytics Workspace -->

## título

https://adobeadcloud.zendesk.com/agent/tickets/24323 Coloque as tags de evento do Analytics nos mesmos pontos que os pixels do Ad Cloud para garantir a correspondência de XXX.

## título

https://adobeadcloud.zendesk.com/agent/tickets/24323

P: Durante nossa auditoria de segurança interna, alguns recursos foram sinalizados como preocupações de segurança que ativamos quando integramos o Ad Cloud em nossa instalação existente do Adobe Analytics.

A integração em questão é entre a AdCloud e a Adobe Audience Manager. Esse recurso aumenta a taxa de correspondência da ID de visitante entre a AdCloud e a Adobe Audience Manager. Ele faz isso enviando solicitações de rede para pagead.l.doubleclick.net, star-mini.c10r.facebook.com e pug88000nf.pubmatic.com para determinar se esses serviços têm uma ID existente para o visitante que pode ser aproveitada. Essas são as solicitações de rede que foram sinalizadas como um risco de segurança e estão ocorrendo para todos os visitantes do site.

Nosso auditor está nos pedindo para desativar esse recurso. O que acontece se bloquearmos essas solicitações de rede?

A: Verificamos com nosso produto e eles mencionaram que os pixels em questão são para a finalidade de aumentar as taxas de correspondência de cookies entre o Ad Cloud, inventário específico/parceiros SSP (em relação ao DSP) e AAM.  Se forem removidos, o cliente poderá ver algum nível de taxa de correspondência diminuída entre o AAC/AAM e os parceiros de inventário para os respectivos pixels, mas eles não esperarão que seja substancial.

Para o Ad Cloud Search, vemos que a ID de organização do Experience Cloud do anunciante está configurada para Mathworks, mas nossa equipe de produtos não vê a configuração do Mathworks para ativar públicos no Ad Cloud. Você está usando o Adobe Audience Manager para enviar públicos para o Ad Cloud Search? Caso contrário, removê-los não terá impacto no fluxo de trabalho atual. AAM Atendimento ao cliente pode ajudar na remoção desses pixels se você não quiser que eles sejam acionados.

