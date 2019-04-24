---
title: Reenviar un mensaje
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d1df84c37cc2a24806c35ae0c90e4bf2a5e438d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328066"
---
# <a name="forwarding-a-message"></a>Reenviar un mensaje

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El reEnvío de un mensaje implica muchas de las tareas que se envían a un mensaje original. En primer lugar, debe abrir el almacén de mensajes predeterminado y la carpeta designada para contener los mensajes salientes, normalmente la bandeja de salida, y llamar al método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) de esta carpeta para crear el mensaje que se va a reenviar. También debe abrir la carpeta que contiene el mensaje original, que suele ser la bandeja de entrada. Para obtener información acerca de cómo abrir carpetas diferentes, consulte [abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md).
  
La principal diferencia entre crear un mensaje que se va a reenviar y crear el original es que con un mensaje reenviado, la mayoría de las propiedades se basan o copian directamente de las propiedades del mensaje original. 
  
**Para reenviar un mensaje**
  
1. Abra el almacén de mensajes predeterminado. Para obtener más información, consulte [abrir el almacén de mensajes predeterminado](opening-the-default-message-store.md).
    
2. Abra la carpeta Bandeja de salida. Para obtener más información, consulte [abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md).
    
3. Llame al método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) de la bandeja de salida para crear un nuevo mensaje reenviado. 
    
4. Llame al método [IMAPIProp:: CopyTo](imapiprop-copyto.md) del mensaje original para copiar las siguientes propiedades en el mensaje reenviado: 
    
   - **El\_cuerpo de PR** ([PidTagBody](pidtagbody-canonical-property.md)), el **HTML de PR\_** ([PidTagHtml](pidtaghtml-canonical-property.md)) o **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), en función de si admite o no el formato de texto enriquecido, el texto sin formato o HTML.
    
   - **PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. Copie los datos adjuntos del mensaje original mediante una llamada al método **IMAPIProp:: CopyTo** del mensaje original para copiar la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) o invocando el siguiente procedimiento de tres pasos para cada dato adjunto que se va a copiar:
    
   1. Llame al nuevo método [IMessage:: CreateAttach](imessage-createattach.md) del nuevo mensaje reenviado para crear un nuevo archivo de datos adjuntos. 
      
   2. Llame al método [IMessage:: OpenAttach](imessage-openattach.md) del mensaje original para abrir los datos adjuntos que se van a copiar. 
      
   3. Llame al método **IMAPIProp:: CopyTo** del mensaje original para copiar todas las propiedades de datos adjuntos de los datos adjuntos antiguos en el nuevo. 
    
6. No incluya las siguientes propiedades en la llamada a **IMAPIProp:: CopyTo**: 
    
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> |Propiedades de **PR_RCVD_REPRESENTING**  <br/> |
|**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))  <br/> |**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))  <br/> |
|Propiedades de **PR_RECEIVED_BY**  <br/> |Propiedades de **PR_REPLY_RECIPIENT**  <br/> |
|**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |Propiedades de **PR_SENDER**  <br/> |
|Propiedades de **PR_SENT_REPRESENTING**  <br/> |**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))  <br/> |
|**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. Aplique formato al texto del mensaje agregando sangría y un párrafo de encabezado que incluya el remitente original, la fecha de transmisión, el asunto y la lista de destinatarios. No incluya caracteres de prefijo de estilo Internet con el contenido.
    
2. Llamar a [ScCreateConversationIndex](sccreateconversationindex.md), pasando el valor de la propiedad **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) del mensaje original.
    
3. Establezca un prefijo para el mensaje reenviado. Si usa el "FW:" estándar, concatene estos caracteres al principio de **PR_NORMALIZED_SUBJECT** y establezca **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) en esta nueva cadena. No establezca **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Si usa un prefijo no estándar, como una cadena de más de tres caracteres, almacénelo en **PR_SUBJECT_PREFIX**. 
    
4. Establezca las propiedades **PR_SENT_REPRESENTING** en los valores correspondientes de las propiedades de **PR_RCVD_REPRESENTING** . 
    
5. Crear una lista de destinatarios. Para obtener más información, vea [crear una lista de destinatarios](creating-a-recipient-list.md).
    
6. Llame al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del mensaje reenviado para guardarlo o [IMessage:: SubmitMessage](imessage-submitmessage.md) para guardarlo y enviarlo. 
    
## <a name="see-also"></a>Vea también

- [Propiedad canónica PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)

