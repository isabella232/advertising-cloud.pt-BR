---
title: Duplicar um pacote
description: Saiba como duplicar um pacote.
feature: Packages
exl-id: 4c37883f-5feb-4513-9573-ed4e32606132
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Duplicar um pacote

Duplique um pacote para criar um pacote com configurações semelhantes. É possível:

* Duplique o pacote no anunciante e na campanha originais ou em campanhas diferentes
* Opcionalmente, duplique as disposições dentro do pacote
* (Para pacotes duplicados nas campanhas originais) Duplique opcionalmente os anúncios originais e os pixels de evento de nível de posicionamento
* Modificar as datas de voo do novo pacote

Consulte &quot;[O que não é duplicado](#package-not-duplicated)&quot; para obter uma lista de configurações de posicionamento que não são duplicadas.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.
1. Clique no nome da campanha para abrir a visualização [!UICONTROL Packages].
1. Ao lado do nome do pacote, clique em **[!UICONTROL ...]>[!UICONTROL Duplicate]**.
1. Especifique as novas configurações de pacote:
   1. Insira o novo nome do pacote.
   1. (Opcional) Altere as configurações padrão.

      Por padrão:

      * O novo pacote é atribuído ao anunciante e à campanha originais.
      * O novo pacote torna-se ativo no dia atual.<!-- and the flight continues for NN  days. -->
      * As disposições contidas na embalagem original são copiadas para a nova embalagem.
      * Os anúncios e os pixels de evento de nível de posicionamento não são copiados para o novo pacote.
1. Clique em **[!UICONTROL Submit]**.

## O que não é duplicado {#package-not-duplicated}

Todas as configurações das disposições originais são duplicadas, exceto:

* Configurações do experimento
* (Se você alterar as datas de voo) Programação de anúncio personalizada
* (Se você não anexar anúncios) Peso de anúncio personalizado e agendamento
* Disposições padrão para ofertas programáticas garantidas (PG) e disposições para [!UICONTROL Simple Ad Serving] ofertas
* (Se você copiar disposições para uma campanha diferente):
   * Meta geográfica
   * pixels do evento
   * Anúncios
   * Segmentos [!DNL DoubleVerify Authentic Brand Safety] no nível da disposição (que substituem os segmentos no nível do anunciante)

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de pacotes](package-about.md)
>* [Criar um pacote](package-create.md)
>* [Editar um pacote](package-edit.md)
>* [Configurações do pacote](package-settings.md)

