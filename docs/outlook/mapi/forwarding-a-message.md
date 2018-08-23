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
ms.openlocfilehash: 18113fd48f33eaf067942116f168a54e8b91c55c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579238"
---
# <a name="forwarding-a-message"></a>Reenviar un mensaje

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Reenviar un mensaje implica muchas de las mismas tareas como enviar un mensaje original. En primer lugar, debe abrir el almacén de mensajes de forma predeterminada y la carpeta que se designa para contener los mensajes salientes, normalmente la Bandeja de salida, y llamar al método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la carpeta para crear el mensaje que se debe reenviar. También debe abrir la carpeta que contiene el mensaje original, normalmente en la Bandeja de entrada. Para obtener información acerca de cómo abrir diferentes carpetas, vea [Abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md).
  
La principal diferencia entre crear un mensaje que se debe reenviar y crear el original es que con un mensaje reenviado, la mayoría de las propiedades es según o copió directamente desde las propiedades del mensaje original. 
  
**Para reenviar un mensaje**
  
1. Abra el almacén de mensajes predeterminado. Para obtener más información, vea [Abrir el almacén de mensajes predeterminado](opening-the-default-message-store.md).
    
2. Abra la carpeta Bandeja de salida. Para obtener más información, vea [Abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md).
    
3. Llamar al método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la Bandeja de salida para crear un nuevo mensaje reenviado. 
    
4. Llamar al método [IMAPIProp::CopyTo](imapiprop-copyto.md) del mensaje original para copiar las propiedades siguientes en el mensaje reenviado: 
    
   - **Precio:\_cuerpo** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), o **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), dependiendo de si o no admite formato de texto enriquecido, texto sin formato o HTML.
    
   - **Precio:\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. Copiar los datos adjuntos de mensajes del mensaje original llamando al método **IMAPIProp::CopyTo** del mensaje original para copiar la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) o invocando el siguiente procedimiento de tres pasos para cada objeto attachment que se va a copiar:
    
   1. Llame a la nueva reenviado (método [IMessage::CreateAttach](imessage-createattach.md) ) del mensaje para crear un nuevo dato adjunto. 
      
   2. Llamar al método [IMessage::OpenAttach](imessage-openattach.md) del mensaje original para abrir los datos adjuntos que se va a copiar. 
      
   3. Llamar al método **IMAPIProp::CopyTo** del mensaje original para copiar todas las propiedades de los datos adjuntos de los datos adjuntos antiguo a la nueva. 
    
6. No se incluyen las siguientes propiedades en la llamada a **IMAPIProp::CopyTo**: 
    
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> |Propiedades **PR_RCVD_REPRESENTING**  <br/> |
|**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))  <br/> |**PR_READ_RECEIPT_REQUESTED de MAPI** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))  <br/> |
|Propiedades **PR_RECEIVED_BY**  <br/> |Propiedades **PR_REPLY_RECIPIENT**  <br/> |
|**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |Propiedades **PR_SENDER**  <br/> |
|Propiedades **PR_SENT_REPRESENTING**  <br/> |**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))  <br/> |
|**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. Dar formato al texto de mensaje mediante la adición de sangría y un párrafo de encabezado que incluye al remitente original, fecha de transmisión, el asunto y la lista de destinatarios. No incluya caracteres de prefijo de estilo de Internet con el contenido.
    
2. Llame a [ScCreateConversationIndex](sccreateconversationindex.md), pasando el valor de propiedad de **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) del mensaje original.
    
3. Establecer un prefijo para el mensaje reenviado. Si está utilizando el estándar "Rv:", concatene estos caracteres hasta el principio del **PR_NORMALIZED_SUBJECT** y establecer **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) a esta nueva cadena. No establezca **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Si está utilizando un prefijo no estándar, como una cadena de más de tres caracteres, almacenar en **PR_SUBJECT_PREFIX**. 
    
4. Establecer las propiedades **PR_SENT_REPRESENTING** a los valores correspondientes en las propiedades **PR_RCVD_REPRESENTING** . 
    
5. Crear una lista de destinatarios. Para obtener más información, vea [crear una lista de destinatarios](creating-a-recipient-list.md).
    
6. Llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje reenviado para guardar este archivo o [IMessage::SubmitMessage](imessage-submitmessage.md) para guardar y enviarla. 
    
## <a name="see-also"></a>Recursos adicionales

- [Propiedad canónica PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)

