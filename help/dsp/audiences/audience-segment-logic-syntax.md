---
title: Sintaxe para lógica de segmento do público-alvo
description: Referencie a sintaxe que pode ser usada para definir a lógica dos segmentos de público-alvo.
feature: DSP Audiences
exl-id: 3a51b1b5-1eef-453b-9be5-0694e27491a8
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Sintaxe para lógica de segmento do público-alvo

Ao criar públicos reutilizáveis, é possível definir manualmente a lógica do segmento usando IDs de segmento alfanumérico e a sintaxe a seguir:

* (b) para indicar um grupo
* `||` para  [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp;&amp; para [!DNL AND]
* ! para [!DNL NOT] (excluir)

>[!NOTE]
>
>* Todos os grupos de segmentos especificados são incluídos, a menos que sejam precedidos por ! (o que os exclui).


Por exemplo, a seguinte lógica:

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

significa (em inglês simples)

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>Nas configurações de posicionamento, você pode usar públicos salvos como públicos-alvo para direcionar explicitamente ou como públicos-alvo separados para excluir do direcionamento. Certifique-se de que a lógica do segmento reflete a finalidade para a qual você usará o público-alvo.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de público-alvo](audience-about.md)
>* [Criar um público-alvo reutilizável](reusable-audience-create.md)
>* [Configurações de público-alvo](audience-settings.md)
>* [Fornecedores de dados de terceiros disponíveis](third-party-data-providers.md)

