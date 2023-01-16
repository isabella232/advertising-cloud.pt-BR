---
title: Fundamentos de [!DNL Marketing Channels]
description: Obter informações importantes sobre [!DNL Analytics Marketing Channels] that [!DNL Analytics for Advertising] Os usuários do devem entender o .
feature: Integration with Adobe Analytics
exl-id: 27b6fb07-0b63-4ff1-a316-20b9a2b60fe9
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# Fundamentos de [!DNL Analytics Marketing Channels]

*Anunciantes apenas com uma integração Adobe Advertising-Adobe Analytics*

Esta página explica as principais informações sobre [!DNL Analytics Marketing Channels] that [!DNL Analytics for Advertising] Os usuários do precisam entender.

Para obter a documentação completa em [!DNL Marketing Channels], consulte &quot;[Introdução ao [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html).&quot;

## Visão geral da [!DNL Marketing Channels]

[!DNL Marketing Channels] são um recurso principal do Adobe Analytics. [!DNL Marketing Channels] os relatórios mostram como os clientes chegam ao seu site pela janela de relatórios e como cada canal afeta a receita ou o comportamento no site.

Considere o exemplo a seguir de uma jornada entre visitas. Cada visita ao seu site é indicada pelo canal de marketing do qual o visitante entrou. A primeira visita, também conhecida como Canal de primeiro contato, é Email. Exibir na visita dois é um canal participante, e a Pesquisa natural é considerada o Canal de último contato. Se você usar [!UICONTROL Last Touch Attribution] within [!UICONTROL Attribution IQ], a Pesquisa natural receberia o crédito total pelo evento de conversão de $250. Usando o Serviço de Experience Cloud ID, é possível vincular essas visitas individuais para revelar uma jornada por um único visitante.

![Exemplo de jornada de conversão entre visitas em Canais de marketing](/help/integrations/assets/a4adc-mc-sample-journey.png)

Ao usar [!UICONTROL Marketing Channels] Regras de processamento, você pode criar conjuntos de lógicas para determinar os canais que geram tráfego e para rastrear cada canal conforme os usuários chegam ao seu site. Por exemplo, a variável [!UICONTROL Email] canal seria indicado por um código de rastreamento exclusivo gerado ao clicar que, quando registrado pelo Adobe Analytics, categorizaria a visita como originário de uma campanha de marketing por email.

## Regras de processamento e como os canais de marketing são definidos

Cada vez que um usuário acessa um site, ele faz isso por meio de um URL em que clicou ou digitou diretamente na barra de endereços. Quando o usuário entra no site, [!DNL Analytics] rastreia informações que podem ser usadas para determinar o canal que levou a visita.

Geralmente, os profissionais de marketing anexam códigos de rastreamento de parâmetro da sequência de consulta aos URLs do canal para ajudar a rastrear o impacto do canal em seu site. Você pode configurar [!DNL Marketing Channels] regras de processamento para acompanhar parâmetros e valores de rastreamento específicos para determinar o canal sem qualquer rastreamento adicional. Por exemplo, se todos os URLs de campanha de email seguirem o formato `www.adobe.com?cid=email…` (onde o URL contém o parâmetro e o valor da string de consulta `cid=email`), em seguida, é possível criar uma regra para acompanhar esse código de rastreamento e agrupar a visita no [!UICONTROL Email] canal.

Outros canais não têm caminhos de URL rastreáveis e precisam de mais lógica para identificação. Por exemplo, [!UICONTROL Earned Social], em que um usuário clica em um link que outro usuário compartilhou organicamente em uma rede social, é um canal importante para ser rastreado. No entanto, o comerciante não tem como anexar um código de rastreamento de parâmetro da string de consulta ao URL compartilhado. Nesse caso, é possível criar uma regra de processamento para acompanhar o domínio de referência das redes sociais de interesse e a ausência de códigos de rastreamento pago para determinar o canal. As visitas que atendem a esses requisitos seriam rastreadas como Social ganho no relatório Canais de marketing .

O Adobe recomenda trabalhar com a equipe de análise para criar um conjunto abrangente de [!DNL Marketing Channels] regras de processamento para rastrear todos os canais pertinentes à sua empresa. Isso permite criar poderosos relatórios de atribuição.

Para entender como a publicidade Adobe pode contribuir com os sinais necessários para criar canais de marketing personalizados, consulte &quot;[Usar IDs de publicidade para criar [!DNL Marketing Channels] Regras](mc-ids.md).&quot;

>[!MORELIKETHIS]
>
>* [Usar IDs de publicidade do Adobe para criar [!DNL Marketing Channels] Regras de processamento](mc-ids.md)
>* [Por que os dados de canal podem variar entre a publicidade Adobe e [!DNL Marketing Channels]](mc-data-variances.md)
>* [Usando [!DNL Analytics Marketing Channels] com dados de publicidade do Adobe](mc-ac-data.md)
>* [Vídeo: Usando [!DNL Marketing Channels] para relatórios de publicidade do Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Visão geral da [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

