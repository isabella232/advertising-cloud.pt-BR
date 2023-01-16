---
title: Publicidade DSP macros
description: Consulte as macros disponíveis para rastreamento geral e rastrear cliques em anúncios de terceiros.
feature: DSP Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---

# Publicidade DSP macros

Uma macro é um comando curto ou abreviação de uma instrução e geralmente segue o formato `${MACRO_NAME}`. As macros incluídas no código criativo ou URLs de click-through são expandidas em uma sequência de código mais longa que o servidor de anúncios pode entender. O servidor de publicidade DSP executa macros quando o anúncio é veiculado ou clicado.

As macros de servidor de anúncios são úteis para transmitir informações importantes para DSP ou servidores de anúncios de terceiros. As macros são usadas mais frequentemente durante o tráfico de código criativo ou metadados de terceiros e personalizados (como pixels de terceiros).

Você pode inserir manualmente uma macro em qualquer lugar, como em uma tag VAST, em qualquer URL, ou em um pixel de evento DSP ou de terceiros. No entanto, cada cliente e parceiro DSP tem um formato de tag de anúncio diferente, e as macros devem ser inseridas em pontos diferentes na tag de acordo. Sempre que você trabalhar com um novo cliente ou parceiro, peça documentação sobre onde inserir as macros nas tags de publicidade que DSP tráfego.

## Macros de rastreamento geral

Use macros de rastreamento geral em todos os tipos de anúncios e tags para retornar dados específicos, conforme necessário.

| Macro | Descrição da substituição | Tipo |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | A ID da conta. | integer |
| `${TM_AD_ID}` | A chave do anúncio (adKey). | string |
| `${TM_AD_ID_NUM}` | A ID do anúncio. | integer |
| `${TM_ADVERTISER_ID}` | A ID do anunciante. | integer |
| `${TM_CAMPAIGN_ID}` | A chave da campanha. | string |
| `${TM_CAMPAIGN_ID_NUM}` | A ID da campanha. | integer |
| ` ${TM_CLICK_URL}` | O URL de redirecionamento, que permite aos servidores de publicidade rastrear e contar cliques de anúncios. Quando a publicidade é veiculada, se o usuário clica nela, a macro é ativada e o clique é registrado e contado para fins de relatório. | string |
| ` ${TM_CLICK_URL_URLENC}` | O URL de redirecionamento codificado, que permite aos servidores de publicidade rastrear e contar cliques de anúncios. Quando a publicidade é veiculada, se o usuário clica nela, a macro é ativada e o clique é registrado e contado para fins de relatório. Não use essa macro a menos que você esteja criando anúncios de terceiros e seu fornecedor exija codificação de URL. | string |
| `${TM_FEED_ID}` | A chave para o posicionamento da mídia (feedKey). | string |
| `${TM_FEED_ID_NUM}` | A ID do posicionamento da mídia. | integer |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | A chave do site para a disposição. Obrigatório para [!DNL AppsFlyer] clique em rastreadores para anúncios de instalação de aplicativos móveis.<!-- should map to placement_site_key column of placement_site table --> | string |
| `${TM_PLACEMENT_ID}` | A chave de posicionamento (cpKey). | string |
| `${TM_PLACEMENT_ID_NUM}` | A ID de posicionamento. | integer |
| `${TM_RANDOM}` | Cachebuster: um número aleatório entre 1 e 1000000. | long |
| `${TM_SESSION_ID}` | A ID da sessão, que corresponde a uma única recuperação da tag do anúncio. | string |
| `${TM_SITE_DOMAIN_URLENC}` | O subdomínio de página analisado a partir do URL na solicitação de licitação; Codificado por URL. Não compatível com anúncios em banners, de cliques para reprodução. | string |
| ` ${TM_SITE_NAME}` | O nome do site para a disposição. | string |
| `${TM_SITE_URL_URLENC}` | O URL transmitido na solicitação de licitação; Codificado por URL. Não compatível com anúncios em banners, de cliques para reprodução. | string |
| `${TM_SITE_ID_NUM}` | A ID do site para a disposição. | integer |
| `${TM_TIMESTAMP}` | O carimbo de data e hora Unix indica o número de segundos decorridos desde a meia-noite (00:00 UTC) em 1 de Janeiro de 1970. | long |
| ` ${TM_VIDEO_DURATION}` | A duração do vídeo do anúncio em segundos. | integer |

{style=&quot;table-layout:auto&quot;}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## Macros específicas para dispositivos móveis

| Macro | Descrição da substituição | Tipo |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore]) A ID da plataforma, que corresponde ao sistema operacional do dispositivo:<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` quando a plataforma não estiver em nenhuma das opções acima</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore]) O nome do modelo do dispositivo, codificado por URL. | string |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore]) O ambiente em que o anúncio foi veiculado:<ul><li>`a` = aplicativo móvel</li><li>`b` = site móvel</li></ul> | string (`a` ou `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen]) A ID da plataforma, que corresponde ao sistema operacional do dispositivo:<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` quando a plataforma não estiver em nenhuma das opções acima</li></ul> | string |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen]) O tipo de dispositivo no qual o anúncio foi visualizado:<ul><li>`TAB` = tablet</li><li>`PHN` = móvel</li><li>`computer` = computador</li></ul> | string |
| `${UOO}` | ([!DNL Nielsen]) Se o usuário recusou ou o rastreamento de anúncios:<ul><li>`1` (Sinalizador DNT = 1) = o usuário recusou o rastreamento de anúncios</li><li>`0` (Sinalizador DNT = 0) = o usuário aceitou o rastreamento de anúncios</li></ul> | integer (`0` ou `1`) |
| `${TM_BUNDLE}` | O [!DNL iOS] ou [!DNL Android] ID do pacote da loja de aplicativos. Exemplos: com.zynga.wf2.free ou id804379658 | string |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` indica se o licitante determina que a solicitação de oferta vem da origem da União Europeia e requer a aplicação do GDPR:<ul><li>`1` = O GDPR deve ser aplicado</li><li>`0` = O GDPR não deve ser aplicado</li></ul>`gdpr_consent=${GDPR_CONSENT}` é o valor de consentimento passado pelo parceiro de suprimento na solicitação de lance de entrada:<ul><li>Na maioria dos casos, essa é uma cadeia de consentimento codificada em base64url ou um daisybit (exemplo: BN5lERiOMYEdiAKAWEND1HoSBE6CAFAApAMBkIDIgM0AgJOxAnQA)</li><li>`0` = sem consentimento</li><li>`1` = consentimento</li></ul> | daisybit ou integer |

{style=&quot;table-layout:auto&quot;}

## Clique em Macros para anúncios de exibição de terceiros

Para rastrear com precisão os cliques de anúncios usando tags de exibição de terceiros, DSP requer uma macro de clique de exibição. É necessária apenas uma versão da macro; a macro relevante depende do tipo de tag.

| Macro | Descrição da substituição | Tipo |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | O URL de redirecionamento que permite aos servidores de publicidade rastrear e contar cliques de anúncios na plataforma. | string |
| `${TM_CLICK_URL_URLENC}` | O URL de redirecionamento que permite aos servidores de publicidade que exigem codificação de URL rastrear e contar cliques e cliques na plataforma. | string |

{style=&quot;table-layout:auto&quot;}

DSP insere automaticamente macros de clique de exibição em uma tag de exibição de terceiros quando você:

* Exportar tags de publicidade de um parceiro de servidor de publicidade <!-- [Needs PM confirmation.] -->
* Upload em massa [!DNL Flashtalking] ou [!DNL Google DoubleClick for Advertisers] tags de publicidade diretamente no DSP

Se uma macro de clique estiver ausente durante a criação de um anúncio de exibição, o DSP exibe uma mensagem de aviso, que solicita a inserção manual da macro de clique de exibição apropriada na área correta da tag.

## Solução de problemas de erros de macro

Ao adicionar macros ao seu código, certifique-se de usar a sintaxe exata da macro. Ao validar as macros, o DSP verifica se a macro corresponde exatamente a uma das macros válidas.

Erros são gerados se os caracteres estiverem ausentes no início ou no fim do nome da macro. Por exemplo, você verá uma mensagem de erro se:

* Você esqueceu um ou mais caracteres no início do nome da macro, como `${`. Se não incluir a sintaxe completa, a entrada não será reconhecida como uma macro válida.
* A macro não termina com um conjunto válido de caracteres, como `}`.

>[!MORELIKETHIS]
>
>* [Configurações de anúncio de áudio](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Configurações do anúncio de TV conectado](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Exibir configurações do anúncio](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Configurações de anúncio móvel](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Configurações de anúncio nativo](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Configurações de anúncio precedente](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [Configurações universais de anúncio de vídeo](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)

