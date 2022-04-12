---
title: Especificações do anúncio
description: Consulte as especificações gerais e específicas do editor.
feature: DSP Ads
source-git-commit: 2110a30cf41a5cc091ec6224a7cbaf9b170ef1db
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 0%

---

# Especificações para tipos de anúncios suportados

## Anúncios de vídeo (pré-rolagem e CTV)

### Telas suportadas

Os anúncios são fornecidos por padrão em dispositivos de desktop, móveis e TV conectados. O direcionamento de dispositivo está disponível para ajustar o delivery.

### Servidores de anúncios de terceiros suportados

Você pode usar folhas de tags de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]e [!DNL Sizmek]. Para obter uma lista completa dos fornecedores suportados, consulte &quot;[Parceiros de veiculação de anúncios certificados](certified-ad-servers.md).&quot;

### Requisitos para ativos de vídeo de alta definição (obrigatório)

**Tipo de tag de vídeo:** JavaScript VPAID 2.0 ou VAST (CTV). Todas as unidades de anúncio VPAID devem seguir o [Especificação VPAID 2.0](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) conforme definido pelo Interative Advertising Bureau (IAB).

**Codec de vídeo:** MP4/H.264

**Resolução:** 1280x720 para 720p, 1920x1080 para 1080p

**Taxa de bits:** 1500-2500 kbps para 720p, 2500-3500 kbps para 1080p

**Perfil/nível H.264:** Alto perfil, nível 3.1 para 720p; Alto perfil, nível 4.0 para 1080p

**Taxa de quadros do vídeo:** 29,970 fps (comumente chamados de 30 fps) para países NTSC, 25 fps para países PAL, 23,976 fps (comumente chamados de 24 fps) para conteúdo de exibição de filme

**Espaço de cor do vídeo:** 4:2:0 YUV Chroma subsampling

**Vídeo entrelaçado:** Varredura progressiva, ou seja, não entrelaçada. Nenhum movimento de campo interno (quadros de mesclagem) ou entrelaçamento.

**Líderes (Tabuleiro):** Não permitido

**Codec de áudio:** AAC-LC ou HE-AACv1

**Taxa de bits de áudio:** 128-192 kbps para AAC-LC, 64-128 kbps para HE-AACv1

**Canal de áudio:** Mistura estéreo de 2 canais

**Taxa de amostra de áudio:** 44,1 kHz ou 48 kHz, por material de origem

**Níveis de áudio:** 24 LKFS (+/- 2.0 dB) nos EUA de acordo com o ATSC A/85; 23 LUFS (+/- 1.0) na UE de acordo com o EBU R128

#### Requisitos adicionais do editor para anúncios de TV conectados

* **Hulu:** Veja Hulu&#39;s [especificações de anúncios](https://advertising.hulu.com/ad-products/video-commercial/).

* **Disney:**

   * Transmissão em Livestreaming ESPN:

      **Taxa de bits:** > 14000kbps
      **Formato:** .mp4
      **Tipo de tag:** VAST 2.0
      **Tamanho criativo:** 1280x720 ou 1920x1080

   * Programação de episódio completo (FEP): ESPN, ABC, Forma livre, Nat Geo e FX

      * **Taxa de bits:** > 14000 kbps:

         **Formato:** .mp4

         **Tipo de tag:** VAST 2.0

         **Tamanho criativo:** 1280x720 ou 1920x1080

      * **Taxa de bits:** > 1000 kbps (baixa resolução) ou 15000 kbps (alta resolução):

         **Formato:** .mp4

         **Tipo de tag:** VAST 2.0 (VPAID 1.0 somente no desktop)

         **Tamanho criativo:** 1280x720 ou 1920x1080

## Exibir anúncios

### Telas suportadas

Os anúncios são fornecidos por padrão em dispositivos móveis e de desktop. O direcionamento de dispositivo está disponível para ajustar o delivery.

### Tipos de arquivo suportados

**Imagem:** GIF, JPG/JPEG, PNG

**HTML5:** Tipos de arquivo de imagem: GIF, JPG/JPEG, PNG, SVG

### Requisitos para ativos de imagem (obrigatório)

O Universal Display é compatível.

**Tamanhos de anúncio recomendados:** 120x60, 160x600, 180x150, 300x50, 300x100, 300x1050, 300x250, 300x60 0, 320x50, 320x480, 480x60, 640x480, 88x31, 728x90, 970x250, 970x90

**Servidores de anúncios de terceiros suportados:** Você pode usar folhas de tags de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]e [!DNL Sizmek]. Para obter uma lista completa dos fornecedores suportados, consulte &quot;[Parceiros de veiculação de anúncios certificados](certified-ad-servers.md).&quot;

## Anúncios de áudio

### Telas suportadas

Desktop, celular, tablet, alto-falantes inteligentes e TV conectada

### Servidores de anúncios de terceiros suportados

Para obter uma lista completa dos fornecedores suportados, consulte &quot;[Parceiros de veiculação de anúncios certificados](certified-ad-servers.md).&quot;

### Requisitos para ativos de áudio (obrigatório)

**Tipo de arquivo:** MP3, OGG, AAC

**Líderes (tabuleiro):**  Não permitido

**Tamanho máximo do arquivo:** 2 MB

**Taxa de bits:** 128

**Comprimento do arquivo:** 0-60s

#### Requisitos adicionais do editor

* **[!DNL Spotify]**
   * Comprimento: Até 30 segundos
   * Tipo de arquivo: OGG
   * Tamanho máximo do arquivo: 500 MB
   * Volume: RMS normalizado para -14; Pico dBFS normalizado para -0,2 dBFS

* **[!DNL SoundCloud]**
   * Comprimento: 6, 15 ou 30 segundos
   * Tipo de arquivo: MP3
   * Tamanho máximo do arquivo: 5 MB

* **[!DNL Pandora]**
   * Comprimento: 15 ou 30 segundos
   * Tipo de arquivo: MP4 (no aplicativo), MP3 (desktop)
   * Tamanho máximo do arquivo: 2,2 MB

* **[!DNL TuneIn]**
   * Comprimento: 10, 15 ou 30 segundos
   * Tipo de arquivo: MP3, OGG
   * Volume: 44,1 kHz

* **[!DNL iHeartRadio]**
   * Comprimento: 5, 15, 30 ou 60 segundos
   * Tipo de arquivo: MP3
   * Tamanho máximo do arquivo: 320 kbps
   * Volume: 44,1 kHz

* **[!DNL TargetSpot]**
   * Comprimento: 15, 30 ou 60 segundos
   * Tipo de arquivo: MP3

### Requisitos para anúncios de banner complementares (opcional)

**Tamanhos compatíveis:** 300x250, 500x500, 640x640, 1024x1024

#### Requisitos adicionais do editor

* **[!DNL Spotify]:**
   * Tipo de arquivo: JPG estático, PNG
   * Tamanho máximo do arquivo: 200 KB
   * Dimension: 300x250

* **[!DNL SoundCloud]:**
   * Tipo de arquivo: JPG estático, PNG
   * Tamanho máximo do arquivo: Menos de 400 KB
   * Dimension: 1024x1024

* **[!DNL Pandora]:**
   * Tipo de arquivo: JPEG, GIF
   * Tamanho máximo do arquivo: Tamanho: 100 KB
   * Dimension: 300x250 (móvel ou desktop) ou 500x500 (desktop)

* **[!DNL TuneIn]:**
   * Tipo de arquivo: JPEG, JPG, PNG, GIF, HTML
   * Tamanho máximo do arquivo: 2 MB
   * Dimension: 300x250

* **[!DNL iHeartRadio]:**
   * Tipo de arquivo: JPEG, JPG, PNG, GIF, SWF, HTML
   * Tamanho máximo do arquivo: 2,2 MB
   * Dimension: 300x250
 

## Anúncios de exibição nativos

Cada anúncio pode incluir uma imagem estática ou um GIF em movimento (cinemparágrafo).

### Telas suportadas

Os anúncios são fornecidos por padrão em dispositivos móveis e de desktop. O direcionamento de dispositivo está disponível para ajustar o delivery.

### Ativos necessários para todos os formatos nativos no feed

#### Ativo de imagem

**Resolução:** Mínimo de 600x600px; Mínimo recomendado de 1200x627px

**Tipo de arquivo:** JPEG (imagem de anúncio de vídeo ou imagem de capa de anúncio de vídeo), GIF (cinemógrafo)

**Tamanho do arquivo:** Menos de 1 MB (a imagem deve ficar sem texto.)

#### Logotipo do anunciante

**Resolução:** Mínimo de 80x80px; Mínimo recomendado de 300x300px

**Tipo de arquivo:** JPEG ou PNG.

**Proporção:**  Proporção de 1x1

>[!NOTE]
>
>Dependendo da imagem sobre a qual será sobreposta, escolha entre os ativos de logotipo claro ou escuro.

#### Texto/Cópia

**Título:** Máximo de 200 caracteres; 25 caracteres recomendados

**Legenda:** Máximo de 200 caracteres; 100 caracteres recomendados

**Patrocinado por:** Máximo de 200 caracteres; 30 caracteres recomendados

**Chamada para ação (somente MoPub):** Máximo de 15 caracteres

>[!NOTE]
>
>O layout final é definido pelo editor no tempo de execução. Se um anúncio exceder a contagem de caracteres recomendada, alguns provedores de inventário podem não fornecer o anúncio, ou o editor ou SSP pode truncar o texto.

#### URL da página de aterrissagem

O URL de clickthrough com rastreadores de cliques opcionais.

Requisitos para rastreadores de cliques:

* Pixels de rastreamento de impressão de terceiros: Formato de URL de imagem 1x1 somente

* Rastreadores de JavaScript de visualização: Suportado apenas para IAS; Imagens 1x1 somente no formato JS.append

* Pixels de rastreamento de cliques de terceiros: Deve redirecionar para a landing page incorporada no URL (redirecionamento HTTP 302)

* Rastreadores de cliques da plataforma de gerenciamento de dados (DMP) com 200 ou mais respostas não são compatíveis.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de anúncios](ad-about.md)
>* [Criar um único anúncio](ad-create.md)
>* [Criar vários anúncios de terceiros](ad-create-multiple.md)
>* [Editar uma publicidade](ad-edit.md)

