---
title: Códigos de erro para [!DNL FreeWheel] Envios de anúncio
description: Referencie os códigos de erro que são retornados para envios de anúncios para [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 2%

---

# Códigos de erro para [!DNL FreeWheel] envios de anúncios

As mensagens de erro para envios de anúncios com falha podem vir do Advertising Cloud DSP ou de [!DNL FreeWheel]. As mensagens de erro são mostradas na coluna [!UICONTROL API Response] na caixa de diálogo [[!UICONTROL Freewheel Status]](freewheel-check-status.md).

## Erros internos do Advertising Cloud DSP

| Mensagem de erro | Descrição | Próximas etapas |
|--- |--- |--- |
| [!DNL Aguardando resposta de status de [!DNL FreeWheel]] | [!DNL FreeWheel] ainda não respondeu que o envio foi bem-sucedido ou falhou. | Verifique o status novamente em 10 minutos. |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] não aceita anúncios do Reino Unido sem números de relógio atribuídos. | Atribua um número de relógio ao anúncio e, em seguida, envie-o novamente. |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | O transcodificador não tinha terminado de transcodificar o anúncio quando você tentou enviar o anúncio. | Aguarde dez minutos e envie o anúncio novamente. |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | O acordo apresentado não é estabelecido como um acordo programático garantido. [!DNL FreeWheel] aceita apenas acordos garantidos. | Configure a ID de negócio como um acordo programático garantido. O anúncio é enviado automaticamente para [!DNL FreeWheel] quando você salva a disposição padrão programática garantida no final do fluxo de trabalho da ID de negócios. |
| [!DNL Invalid external_deal_id:] \&lt;deal_id> | A ID de negócios enviada não existe ou não está ativa no Adobe. | Certifique-se de que o negócio está ativo e envie o anúncio novamente. |
| [!DNL \[public_id=]\&lt;deal>] não existe | A id de negócios enviada não existe no fim [!DNL FreeWheel]. | Entre em contato com seu representante [!DNL FreeWheel] para confirmar a ID do contrato. |
| [!DNL Ad with identifier] \&lt;>nome da publicidade *\>  [!DNL was not found.]* | A chave de anúncio enviada não existe ou não está ativa no Adobe. | Encontre a chave de anúncio correta e, em seguida, envie o anúncio novamente. |
| [!DNL Pending Submission] | O envio ainda está pendente. | Atualize a página. |

{style=&quot;table-layout:auto&quot;}

## Erros da API FreeWheel

| Código | Significado | Descrição | Próximas etapas |
|--- |--- |--- |--- |
| 401° | Não autorizado | Credenciais de acesso incorretas, ausentes ou inválidas. | Entre em contato com o gerente de conta do Adobe. |
| 403 | Proibido | O servidor entendeu a solicitação, mas recusa autorizá-la. | Entre em contato com o gerente de conta do Adobe. |
| 404 | Não encontrado | O recurso solicitado não está disponível. Se a ID de criação não for encontrada na operação PUT, um 404 será retornado. | Entre em contato com o gerente de conta do Adobe. |
| 405 | Método Não Permitido | Uma solicitação foi feita de um recurso usando um método de solicitação não suportado por esse recurso (por exemplo, usando o GET em um método que requer que os dados sejam enviados pelo POST ou usando o PUT em um recurso somente leitura). | Entre em contato com o gerente de conta do Adobe. |
| 408 | Tempo limite da solicitação | Ocorreu um tempo limite durante o processamento desta solicitação. Normalmente, os tempos limite são causados por solicitações simultâneas de acesso exclusivo a determinados recursos. | Envie novamente a solicitação ao receber esse status. Se o problema persistir, entre em contato com o gerente de conta do Adobe. |
| 422 | Entidade não processável | Recurso inválido. Esse erro ocorre quando o corpo da solicitação é inválido ou o recurso criado/atualizado é inválido (por exemplo, se a ID do contrato não foi encontrada). Consulte [API FreeWheel 422 Errors](#freewheel-422-errors) para obter mais informações. | Entre em contato com o gerente de conta do Adobe. |
| 500 | Erro interno do servidor | Erro de sistema de API. | Entre em contato com o gerente de conta do Adobe. |

{style=&quot;table-layout:auto&quot;}

## Erros da API FreeWheel 422 {#freewheel-422-errors}

| Código | Código HTTP | Descrição |
|--- |--- |--- |
| DATA_UNMAREY_FAILURE | 422 | Os dados da solicitação são um formato json inválido. Verifique a mensagem de erro para obter detalhes. |
| DATA_VALIDATION_FAILURE | 422 | Os dados da solicitação não têm campos obrigatórios ou têm um tipo de dados inválido. Verifique a mensagem de erro para obter detalhes. |
| DATA_DEAL_INVALID | 422 | O negócio está configurado incorretamente ou não existe. Verifique a mensagem de erro para obter detalhes. |
| DATA_DEAL_GET_FAILURE | 422 | O negócio não foi encontrado ou sua configuração tem um problema. Verifique a mensagem de erro para obter detalhes. |
| DATA_CREATIVE_INGEST_FAILURE | 422 | O URL de criação é inválido. Verifique a mensagem de erro para obter detalhes. |
| DATA_CREATIVE_LINK_FAILURE | 422 | O anúncio não estava vinculado aos nós da unidade de anúncio do negócio. Verifique a mensagem de erro para obter detalhes. |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | O anúncio não foi atualizado. Verifique a mensagem de erro para obter detalhes. |
| DATA_DSP_GET_FAILURE | 422 | O DSP não existe no sistema. |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | O anúncio não foi desvinculado das unidades de anúncios. |
| DATA_CREATIVE_DELETE_FAILURE | 422 | O anúncio não foi excluído. |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | O URL não foi detectado. |
| DATA_ENTITY_NOT_FOUND | 422 | O anúncio não existe. |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Visão Geral da Configuração de Contratos Programáticos Garantidos em FreeWheel](/help/dsp/inventory/freewheel-overview.md)
>* [Aceitar um contrato na Caixa de entrada da ID do contrato](deal-id-inbox-accept.md)
>* [Envie um anúncio para um acordo programático garantido para FreeWheel](/help/dsp/inventory/freewheel-submit.md)
>* [Verifique o status dos anúncios  [!DNL FreeWheel] para ver os contratos programáticos garantidos](/help/dsp/inventory/freewheel-check-status.md)

