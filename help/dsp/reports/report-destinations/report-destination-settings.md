---
title: Configurações de destino do relatório
description: Consulte os detalhes necessários para os destinos do seu relatório, por tipo de destino.
feature: DSP Custom Reports
exl-id: 584c9c69-7b94-4e5c-bcc1-277ac2689d8e
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Configurações de destino do relatório

Os detalhes necessários para destinos de relatórios que não são de email variam de acordo com o tipo de destino.

>[!NOTE]
>
> Você também pode enviar seus relatórios personalizados para destinatários de email, que não exigem um destino de relatório salvo. Você pode especificar destinatários de email, em vez de destinos salvos, nas configurações do relatório.

## [!UICONTROL S3]

**[!UICONTROL Name]:** Um nome para ajudar a identificar o destino.

**[!UICONTROL S3 Bucket URL]:** O caminho completo para a pasta no [!DNL Amazon Simple Storage Service] (S3) para o qual o relatório será carregado. Exemplo: `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]:** A ID da chave de acesso para o ([!DNL Amazon S3]) bucket (fornecido por [!DNL Amazon]).

**[!UICONTROL Secret Access Key]:** A chave de acesso secreta para o ([!DNL Amazon S3]) bucket (fornecido por [!DNL Amazon]).

## [!UICONTROL FTP]

**[!UICONTROL Name]:** Um nome para ajudar a identificar o destino.

**[!UICONTROL Server]:** O nome do host do servidor.

**[!UICONTROL Port]:** O número da porta a ser usado no servidor. O padrão é *[!UICONTROL 21]*.

**[!UICONTROL Username]:** O nome de usuário para fazer logon no servidor.

**[!UICONTROL Password]:** A senha para fazer logon no servidor.

**[!UICONTROL Path (Optional)]:** O caminho do servidor para o qual os arquivos serão carregados.

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** Um nome para ajudar a identificar o destino.

**[!UICONTROL Server]:** O nome do host do servidor.

**[!UICONTROL Port]:** O número da porta a ser usado no servidor. O padrão é *[!UICONTROL 21]*.

**[!UICONTROL Username]:** O nome de usuário para fazer logon no servidor.

**[!UICONTROL Password]:** A senha para fazer logon no servidor.

**[!UICONTROL Path (Optional)]:** O caminho do servidor para o qual os arquivos serão carregados.

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** Um nome para ajudar a identificar o destino.

**[!UICONTROL Server]:** O nome do host do servidor.

**[!UICONTROL Port]:** O número da porta a ser usado no servidor. O padrão é *[!UICONTROL 21]*.

**[!UICONTROL Username]:** O nome de usuário para fazer logon no servidor.

**[!UICONTROL Password]:** A senha para fazer logon no servidor.

**[!UICONTROL Path (Optional)]:** O caminho do servidor para o qual os arquivos serão carregados.

>[!MORELIKETHIS]
>
>* [Sobre [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Crie um [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [Edite um [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [Excluir um [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)

