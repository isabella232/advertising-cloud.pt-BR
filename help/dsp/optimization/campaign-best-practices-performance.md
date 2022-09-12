---
title: Práticas recomendadas para configurar campanhas de desempenho
description: Conheça as práticas recomendadas para configurar campanhas focadas no desempenho, que incluem disposições otimizadas para o CPA mais baixo ou para o ROAS mais alto.
feature: DSP Optimization, DSP Best Practices
exl-id: fc64680d-9d1c-4f74-a8b9-2e9b670c00eb
source-git-commit: 1fd95b3193fba50ce7cd85b2ad6256a0ba346011
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Práticas recomendadas para configurar campanhas de desempenho

A Advertising Cloud pode otimizar suas campanhas focadas no desempenho para disposições com o menor custo por aquisição (CPA) ou o maior retorno sobre o gasto com anúncios (ROAS).

Veja as seguintes práticas recomendadas para campanhas de desempenho:

* Etapa 1 - Definir a meta
* Etapa 2 - Definir a estratégia
* Etapa 3 - Criar pacotes
* Etapa 4 - Criar estrutura de disposição
* Etapa 5 - Usar os ativos criativos certos

## Etapa 1 - Definir sua meta

É importante entender se o objetivo da campanha é alcançar o ROAS mais alto possível ou o CPA mais baixo possível. Para cada pacote na campanha, você especificará a meta do objetivo de acordo como *[!UICONTROL Highest ROAS - Custom Goal]* ou *[!UICONTROL Lowest CPA - Custom Goal]*.

![meta de otimização](/help/dsp/assets/optimization-goals.png)

Também é necessário determinar os eventos bem-sucedidos que levarão à meta geral e criar metas personalizadas adequadamente. Para cada pacote, você especificará uma meta personalizada a ser usada com a meta de otimização geral para relatórios e otimização algorítmica usando [!DNL Adobe Sensei]. Para obter mais informações sobre como criar metas personalizadas, consulte o [Práticas recomendadas para criar uma meta personalizada](custom-goal-best-practices.md).

![metas personalizadas](/help/dsp/assets/objective-goals.png)

## Etapa 2 - Definir a estratégia

### Estratégias de perspectivas

Os pacotes de funil superiores incluem disposições com direcionamento muito amplo para alcançar novos consumidores líquidos.

#### Estratégias de posicionamento recomendadas para perspectivas

* Encontre novos públicos-alvo que provavelmente serão convertidos usando as seguintes táticas:

   * Modelagem semelhante de uma plataforma de gerenciamento de dados (DMP), como o Adobe Audience Manager.
   * Direcionamento comportamental usando dados de terceiros.
   * Direcionamento contextual.
   * Definição de metas de site/categoria.

* Usar a execução de definição de metas da rede (RON): É importante incluir uma execução de inserção de rede sem direcionamento de público-alvo e com direcionamento de inventário abrangente. Isso permite que a variável [!DNL Adobe Sensei] para encontrar usuários valiosos que possam ter cookies mais recentes que ainda não foram categorizados em um público-alvo.

### Estratégias de redefinição de metas

Os pacotes de funil mais baixos incluem disposições que direcionam os usuários que já estiveram na página da Web do anunciante ou para os quais o anunciante tem dados de CRM.

#### Estratégias de posicionamento recomendadas para redirecionamento

* Se o anunciante for um cliente do Adobe Analytics ou Adobe Audience Manager, é possível criar segmentos primários (como visitantes de página inicial, páginas de produtos ou abandonadores de carrinho) e usá-los como alvos de posicionamento no Advertising Cloud.

* Evite atribuir muito orçamento a uma disposição direcionada ao público-alvo. Como regra geral, orçar US$ 30 por 1.000 usuários por mês.

## Etapa 3 - Criar pacotes

A prática recomendada é criar pacotes separados para prospecção de funil superior e para redirecionamento de funil inferior. A otimização ocorre no nível do pacote, de modo que os dados de desempenho de todas as disposições de um pacote sejam agrupados. Portanto, agrupe disposições em pacotes com desempenho esperado semelhante.

![exemplo de pacotes separados para prospecção e redefinição de metas](/help/dsp/assets/p-r.png)

Além disso, use as seguintes configurações.

### Metas e orçamento

* **Embalagem e limitação:** Para selecionar uma meta de otimização de CPA ou ROAS, o pacote deve usar o ritmo de nível de pacote. Isso garante que todas as disposições do pacote sejam otimizadas para distribuir gastos com base no desempenho e dimensionar para as metas selecionadas.

* **Datas de voo:** (Pacotes de prospecção) Quando a campanha for executada por mais de 25 dias, use a variável [!UICONTROL Activate Custom Flighting] recurso. Primeiro, defina um voo personalizado para os primeiros 10 dias em aproximadamente 75% do orçamento diário necessário para reduzir os gastos durante o *fase de aprendizagem*. Em seguida, defina um segundo voo personalizado para o restante do orçamento.

   Por exemplo, se você tiver $100.000 para gastar em 30 dias, defina o orçamento para o voo 1 (Dias 1-10) para $25.000 (75% x $100.000/30 dias = $2.500 por dia). Use o orçamento restante de US$ 75.000 para o voo 2 (Dias 11-30).

* **Orçamento:** DSP sempre tentará alocar 100% do orçamento do pacote uniformemente entre todas as disposições em um pacote. Se uma disposição tiver baixo gasto ou nenhum gasto, recomendamos que o orçamento limite a disposição para permitir que mais do orçamento seja alocado em disposições com escala. Aguarde de 24 a 48 horas para que as alterações no orçamento sejam calibradas.

* **Metas de otimização:** Use uma das duas metas de otimização de desempenho, *[!UICONTROL Highest ROAS]* ou *[!UICONTROL Lowest CPA]*, dependendo da meta do pacote. Essas metas otimizam automaticamente o pacote em direção às posições de ROAS mais alto ou CPA mais baixo, respectivamente.

* **Metas personalizadas:**
   * Se um novo pacote tiver a mesma meta de um pacote existente, você poderá, opcionalmente, vincular o pacote existente para que o algoritmo possa usar os dados de aprendizado de máquina existentes.
   * Insira o [!UICONTROL Target CPA] ou [!UICONTROL Target ROAS].

* **Embalagem de voo e embalagem intradiária:** Para ambos os tipos de ritmo, selecione *[!UICONTROL Even]* para maximizar seus objetivos de desempenho, seguindo uniformemente todos os dias e durante todo o voo.

   >[!CAUTION]
   >
   >Use *[!UICONTROL FrontLoad]* e *[!UICONTROL Aggressive Front Load]* para a navegação de voo e *[!UICONTROL ASAP]* ritmo para o ritmo intradiário somente quando você prioriza totalmente a entrega e gasta em relação à otimização de desempenho, pois essas estratégias podem afetar negativamente seus KPIs de desempenho desejados.

## Etapa 4 - Criar estrutura de disposição

Menos é mais. Se você puder configurar menos de seis disposições por pacote, o orçamento disponível poderá mudar dinamicamente para as disposições com melhor desempenho mais facilmente.

Além disso, adicione cada disposição a um pacote com um tipo de meta de pacote de *[!UICONTROL Prospecting]* ou *[!UICONTROL Retargeting]*, conforme adequado.

Veja a seguir as configurações de posicionamento recomendadas para campanhas de desempenho.

### Metas

Você definirá a otimização de CPA ou ROAS no nível do pacote (consulte Etapa 3 - Criar pacotes), mas poderá adicionar outras configurações no nível de posicionamento.

* **Lance máximo:**
   * Para disposições de prospecção, use um lance máximo baixo ($5).
   * Para disposições de redirecionamento, use um lance máximo alto ($12).

* **Filtros pré-lances:** Minimize, ou idealmente evite, a configuração de filtros pré-lances agressivos, que impedem que a disposição alcance a escala. As práticas recomendadas incluem:

   * Use um (1) filtro de pré-oferta por disposição. Vários filtros pré-lances exigirão que ambos sejam atendidos, o que reduz a escala.

   * Considere a configuração de filtros pré-lances menos estritos em casos em que o direcionamento adicional (como público-alvo, geografia e direcionamento de site) é aplicado.

Veja descrições de quando usar cada filtro pré-lance em [Filtros de pré-lance em nível de posicionamento e como usá-los](/help/dsp/optimization/optimization-pre-bid-filters.md).

### Inventário

Para maximizar a escala, use [!UICONTROL Public] (Open Exchange) e [!UICONTROL On Demand] inventário.

### Direcionamento de site

* **[!UICONTROL Traffic Type]**: [!UICONTROL Websites] only
* **[!UICONTROL Site Tier]**: [!UICONTROL All sites]

### Direcionamento de público-alvo

* **[!UICONTROL Included Audiences]:**
   * Para disposições de prospecção, agrupe categorias de público-alvo semelhantes e tamanhos de público-alvo semelhantes em uma única disposição. Em seguida, com base no desempenho, execute um dos seguintes procedimentos:
      * Remova públicos-alvo com baixo desempenho de disposições existentes.
      * Mova públicos-alvo com melhor desempenho em uma disposição separada para controlar melhor os orçamentos.
   * Para disposições de redirecionamento, você deve, idealmente, incluir um segmento de público-alvo por disposição para controlar facilmente as ofertas e o orçamento.

>[!NOTE]
>
>Seus anúncios terão melhor desempenho se um usuário puder ser acessado por apenas uma disposição. A sobreposição significativa entre usuários em disposições pode causar concorrência, o que gera um ciclo de lances continuamente crescentes, aumentando o custo por usuário. Portanto, se você incluir vários públicos, verifique se eles não consistem em usuários sobrepostos/membros do público-alvo.
>
> Você pode evitar a sobreposição de públicos-alvo criando seus públicos-alvo em camadas para suprimir os níveis mais altos e mais inclusivos de disposições, conforme necessário.

* **[!UICONTROL Frequency Capping]:**
   * Para disposições de prospecção, use limites de frequência apertados (uma impressão por dia).
   * Para posicionamentos de redirecionamento, defina o limite de posicionamento principal como 6 a 10 impressões por dia e o limite secundário como uma impressão por hora.

* **[!UICONTROL Device Targeting]**:
   * Incluir [!UICONTROL Computer], [!UICONTROL Mobile]e [!UICONTROL Tablet].
   * Não direcionar [!UICONTROL Firefox] e [!UICONTROL Safari] devido às limitações de direcionamento e medição. Entre em contato com seu [!DNL Adobe] equipe da conta para obter mais detalhes sobre [!DNL Adobe] suporte para [!DNL Safari ITP].
   * Se você direcionar o tráfego da Web móvel, desative todos os navegadores móveis exceto [!UICONTROL Chrome] e [!UICONTROL Edge].

### Segurança da marca e qualidade da mídia

Usar filtragem contextual, bloqueio de fraude pré-lance e/ou [!UICONTROL Ads.txt] a filtragem limitará a escala de suas disposições, mas as usará, se necessário.

## Etapa 5 - Usar os ativos criativos certos

* A prática recomendada é incluir o maior número possível de tamanhos de anúncio exclusivos para maximizar o alcance. O modelo de exibição universal permite carregar qualquer tamanho de anúncio de exibição padrão.
* Verifique se todas as disposições contêm *pelo menos* todos os tamanhos de anúncio de exibição principais (300x250, 728x90, 160x600, 300x600, 320x50 e 300x50).
* Atualize os criativos frequentemente para evitar a fadiga criativa.

>[!MORELIKETHIS]
>
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
> * [Como o DSP otimiza suas campanhas](optimization-how-dsp-optimizes-campaigns.md)
>* [Metas de otimização e como usá-las](optimization-goals.md)
>* [Filtros de pré-lance em nível de posicionamento e como usá-los](optimization-pre-bid-filters.md)
>* [Lista de verificação do lançamento da campanha](/help/dsp/campaign-management/campaign-launch-checklist.md)

