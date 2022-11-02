---
title: Uso de Advertising Cloud IDs para criar [!DNL Marketing Channels] Regras
description: Saiba como usar as Advertising Cloud IDs para criar regras de processamento para [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 4fcdd586-e9c5-4405-a6dc-7799d2bac93e
source-git-commit: d136b1fe6f6fd3861d0850e07efe7c320da4a7cc
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Uso de Advertising Cloud IDs para criar [!DNL Marketing Channels] Regras de processamento

*Anunciantes somente com uma integração Advertising Cloud-Adobe Analytics*

Você pode usar Advertising Cloud IDs ([ID AMO e ID EF](../ids.md)) para configurar [!DNL Marketing Channels] regras de processamento no Adobe Analytics. Use as Advertising Cloud IDs para regras específicas de suas campanhas do Advertising Cloud.

## A ID do AMO nas Regras de processamento

A ID do AMO é o código de rastreamento principal usado para relatar dados do Advertising Cloud no [!DNL Analytics]. A ID do AMO é uma concatenação de valores dinâmicos gerenciados pelo Adobe para fornecer relatórios granulares no [!DNL Analytics]. Está armazenado em um [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou da dimensão rVar (ID do AMO). A ID do AMO pode ser definida em [!DNL Analytics] de duas formas:

* Rastreamento de click-through: A Advertising Cloud define a variável `s_kwcid` parâmetro da string de consulta em um link e [!DNL Analytics] O seleciona o parâmetro do URL da página inicial quando ocorre um click-through.
* Rastreamento de view-through ([!DNL DSP] Somente): O Serviço de último evento detecta um view-through no lado do servidor e envia a ID do AMO para o [!DNL Analytics]. Nesse caso, o URL não contém um `s_kwcid` parâmetro.

Os valores dinâmicos nas IDs do AMO indicam o canal de marketing que foi rastreado:

* O prefixo na ID do AMO pode ser usado para identificar o canal de nível superior no [!DNL Marketing Channels].

* Frases de caracteres no corpo da ID do AMO indicam um tipo de campanha mais específico.

* O sufixo &quot;vt&quot; está presente para [!DNL DSP] tráfego view-through e pode ser usado para criar click-through e view-through separados [!DNL DSP] canais.

O restante da ID do AMO pode ser ignorado.

| ID do AMO | Canal | Lógica da regra |
|--------|---------|--------------------|
| AL! (prefixo) | [!UICONTROL Paid Search] | Começa com |
| AC! (prefixo) | [!UICONTROL DSP] | Começa com |
| !g! (corpo) | [!UICONTROL Google Search] | Contém |
| !s! (corpo) | [!UICONTROL Search Partner] | Contém |
| !d! (corpo) | [!UICONTROL Display Network] | Contém |
| !u! (corpo) | [!UICONTROL Smart Shopping Campaign] | Contém |
| !ytv! (corpo) | [!UICONTROL YouTube Video Ad] | Contém |
| !yts! (corpo) | [!UICONTROL YouTube Search Ad] | Contém |
| !vp! (corpo) | [!UICONTROL Google Video Partners] | Contém |
| !vt (sufixo) | [!UICONTROL DSP View-through] | Termina com |

### Exemplos de regras de processamento que usam a ID do AMO

O [!DNL Marketing Channels] regra de processamento para a [!UICONTROL Paid Search] canal pode ter esta aparência:

![Exemplo de um [!UICONTROL Paid Search] regra](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

O [!DNL Marketing Channels] regra de processamento para a [!UICONTROL YouTube Video Ads] canal pode ter esta aparência:

![Exemplo de um [!UICONTROL YouTube Video Ads] regra](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Certifique-se de executar suas regras em ordem de especificidade. Se as duas regras acima foram executadas em ordem, a variável [!DNL YouTube] o tráfego de anúncios de vídeo se encaixaria no [!UICONTROL Paid Search] , pois a ID do AMO começaria com &quot;AL!&quot; e contém &quot;!ytv!&quot;.

## A ID EF nas regras de processamento

A AMO EF ID (EF ID) é o segundo código de rastreamento utilizado na variável [!DNL Analytics for Advertising Cloud] integração. Seu objetivo principal é rastrear e passar [!DNL Analytics] dados do evento no Advertising Cloud. Toda vez que um click-through ou view-through ocorre, uma ID EF exclusiva é gerada, mesmo se for exatamente a mesma publicidade para o mesmo visitante. A ID EF não é utilizada na variável [!DNL Analytics] interface de usuário do relatório porque normalmente excede os valores únicos de 500k por limite de variável em [!DNL Analytics], tornando-o inutilizável para relatórios. As métricas e os metadados Advertising Cloud não são aplicados ao EF ID; elas são aplicadas somente à ID do AMO. A granularidade adicionada do rastreamento é necessária para a otimização da campanha no Advertising Cloud, portanto, ambas as IDs são necessárias.

Embora a dimensão EF ID não seja usada diretamente em [!DNL Analytics] no relatório, a EF ID pode ser útil na criação de canais de marketing. O sufixo EF ID indica o canal (exibição ou pesquisa) e se a visita foi guiada por um click-through ou view-through. O delimitador na ID EF é um ponto e vírgula, em vez do ponto de exclamação na ID do AMO.

| Sufixo de ID EF | Canal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Exemplos de regras de processamento que usam EF ID

#### Exibir regra de click-through

Crie um canal de marketing Display click-through capturando apenas click-throughs. Como a ID do AMO é a mesma para click-throughs e view-throughs, essa regra usa a variável EF ID e a variável `ef_id` parâmetro da string de consulta.

Às vezes, os click-throughs são rastreados pelo URL (o padrão). Em outros casos, os click-throughs são rastreados pelo Serviço de último evento no lado do servidor e, portanto, o URL não contém a variável `ef_id` parâmetro. Por conseguinte, a regra verifica as condições em que a variável EF ID ou a variável EF ID `ef_id` o parâmetro da string de consulta termina com &quot;:d&quot;. Use o &quot;`Any`&quot; porque você deseja que essa regra seja acionada para qualquer condição.

![Exemplo de uma regra de click-through de exibição](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Exibir regra de view-through

Para criar um canal de view-through de exibição, crie uma regra na qual a ID EF termine com &quot;:i&quot;. Como o visitante não clicou no anúncio, o rastreamento de view-through não inclui a variável `ef_id` ou `s_kwcid` no URL, portanto, a regra requer apenas uma condição.

![Exemplo de uma regra de view-through de exibição](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Fundamentos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Por que os dados de canal podem variar entre a Advertising Cloud e a [!DNL Marketing Channels]](mc-data-variances.md)
>* [Usando [!DNL Analytics Marketing Channels] com dados do Advertising Cloud](mc-ac-data.md)
>* [Vídeo: Relatórios com o Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Advertising Cloud IDs usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md)

