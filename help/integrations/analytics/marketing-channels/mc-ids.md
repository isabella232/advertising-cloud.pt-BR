---
title: Usar Advertising Cloud IDs para criar [!DNL Marketing Channels] regras
description: Saiba como usar Advertising Cloud IDs para criar regras de processamento para [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 5224d891d665b901d076ff6a203e9ff3bab80f85
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Usar Advertising Cloud IDs para criar [!DNL Marketing Channels] regras de processamento

*Anunciantes somente com uma integração Advertising Cloud-Adobe Analytics*

Você pode usar Advertising Cloud IDs ([AMO ID e EF ID](../ids.md)) para configurar [!DNL Marketing Channels] regras de processamento no Adobe Analytics. Use as Advertising Cloud IDs para regras específicas de suas campanhas do Advertising Cloud.

## A ID do AMO nas Regras de processamento

A ID do AMO é o código de rastreamento principal usado para relatar dados do Advertising Cloud em [!DNL Analytics]. A ID do AMO é uma concatenação de valores dinâmicos gerenciados pelo Adobe para fornecer relatórios granulares em [!DNL Analytics]. Ele é armazenado em uma dimensão [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou rVar (ID do AMO). A ID do AMO pode ser definida em [!DNL Analytics] de duas maneiras:

* Rastreamento de click-through: O Advertising Cloud define o parâmetro da sequência de consulta `s_kwcid` em um link e [!DNL Analytics] seleciona o parâmetro do URL da página inicial quando ocorre um click-through.
* Rastreamento de view-through ([!DNL DSP] Somente): O Serviço de último evento detecta um view-through no lado do servidor e envia a ID do AMO para [!DNL Analytics]. Nesse caso, o URL não contém um parâmetro `s_kwcid`.

Os valores dinâmicos nas IDs do AMO indicam o canal de marketing que foi rastreado:

* O prefixo na ID do AMO pode ser usado para identificar o canal de nível superior dentro de [!DNL Marketing Channels].

* Frases de caracteres no corpo da ID do AMO indicam um tipo de campanha mais específico.

* O sufixo &quot;vt&quot; está presente para o tráfego de view-through [!DNL DSP] e pode ser usado para criar canais de click-through e view-through separados [!DNL DSP].

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

A regra de processamento [!DNL Marketing Channels] do canal [!UICONTROL Paid Search] pode ser semelhante a:

![Exemplo de uma  [!UICONTROL Paid Search] regra](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

A regra de processamento [!DNL Marketing Channels] do canal [!UICONTROL YouTube Video Ads] pode ser semelhante a:

![Exemplo de uma  [!UICONTROL YouTube Video Ads] regra](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Certifique-se de executar suas regras em ordem de especificidade. Se as duas regras acima fossem executadas em ordem, o tráfego de anúncio de vídeo [!DNL YouTube] ficaria no canal [!UICONTROL Paid Search] porque a ID do AMO começaria com &quot;AL!&quot; e contém &quot;!ytv!&quot;.

## A ID EF nas regras de processamento

A AMO EF ID (EF ID) é o segundo código de rastreamento usado na integração [!DNL Analytics for Advertising Cloud]. Seu objetivo principal é rastrear e transmitir os dados do evento [!DNL Analytics] para o Advertising Cloud. Toda vez que um click-through ou view-through ocorre, uma ID EF exclusiva é gerada, mesmo se for exatamente a mesma publicidade para o mesmo visitante. A ID EF não é usada na interface do usuário de relatórios [!DNL Analytics] porque normalmente excede os valores exclusivos de 500k por limite de variável em [!DNL Analytics], tornando-a inutilizável para relatórios. As métricas e os metadados Advertising Cloud não são aplicados ao EF ID; elas são aplicadas somente à ID do AMO. A granularidade adicionada do rastreamento é necessária para a otimização da campanha no Advertising Cloud, portanto, ambas as IDs são necessárias.

Embora a dimensão EF ID não seja usada diretamente nos relatórios [!DNL Analytics], a EF ID pode ser útil na criação de canais de marketing. O sufixo EF ID indica o canal (exibição ou pesquisa) e se a visita foi guiada por um click-through ou view-through. O delimitador na ID EF é um ponto e vírgula, em vez do ponto de exclamação na ID do AMO.

| Sufixo de ID EF | Canal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Exemplos de regras de processamento que usam EF ID

#### Exibir regra de click-through

Crie um canal de marketing Display click-through capturando apenas click-throughs. Como a ID do AMO é a mesma para click-throughs e view-throughs, essa regra usa a variável EF ID e o parâmetro da sequência de consulta `ef_id`.

Às vezes, os click-throughs são rastreados pelo URL (o padrão). Em outros casos, os click-throughs são rastreados pelo Serviço de último evento no lado do servidor e, portanto, o URL não contém o parâmetro `ef_id`. A regra, portanto, verifica as condições em que a variável EF ID ou o parâmetro da sequência de consulta `ef_id` termina com &quot;:d&quot;. Use o operador &quot;`Any`&quot; porque deseja que essa regra seja acionada para qualquer condição.

![Exemplo de uma regra de click-through de exibição](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Exibir regra de view-through

Para criar um canal de view-through de exibição, crie uma regra na qual a ID EF termine com &quot;:i&quot;. Como o visitante não clicou no anúncio, o rastreamento de view-through não inclui o `ef_id` ou `s_kwcid` no URL. Portanto, apenas uma condição é necessária.

![Exemplo de uma regra de view-through de exibição](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Fundamentos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Por que os dados de canal podem variar entre a Advertising Cloud e a [!DNL Marketing Channels]](mc-data-variances.md)
>* [ [!DNL Analytics Marketing Channels] Usar com dados do Advertising Cloud](mc-ac-data.md)
>* [Vídeo: Relatórios com o Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Advertising Cloud IDs usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md)

