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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433181"
---
# <a name="forwarding-a-message"></a>Reenviar un mensaje

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El reenvío de un mensaje implica muchas de las mismas tareas que el envío de un mensaje original. En primer lugar, debe abrir el almacén de mensajes predeterminado y la carpeta designada para contener los mensajes salientes, normalmente la Bandeja de salida, y llamar al método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de esta carpeta para crear el mensaje que se reenviará. También debe abrir la carpeta que contiene el mensaje original, normalmente la Bandeja de entrada. Para obtener información acerca de cómo abrir carpetas diferentes, vea [Abrir una carpeta del almacén de mensajes.](opening-a-message-store-folder.md)
  
La principal diferencia entre crear un mensaje que se va a reenviar y crear el original es que, con un mensaje reenviado, la mayoría de las propiedades se basan o se copian directamente desde las propiedades del mensaje original. 
  
**Para reenviar un mensaje**
  
1. Abra el almacén de mensajes predeterminado. Para obtener más información, vea [Abrir el almacén de mensajes predeterminado.](opening-the-default-message-store.md)
    
2. Abra la carpeta Bandeja de salida. Para obtener más información, vea [Abrir una carpeta del almacén de mensajes.](opening-a-message-store-folder.md)
    
3. Llame al método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la Bandeja de salida para crear un nuevo mensaje reenviado. 
    
4. Llame al método [IMAPIProp::CopyTo](imapiprop-copyto.md) del mensaje original para copiar las siguientes propiedades en el mensaje reenviado: 
    
   - **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) o **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), dependiendo de si admite o no formato de texto enriquecido, texto sin formato o HTML.
    
   - **PR \_ NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. Copie los datos adjuntos del mensaje original llamando al método **IMAPIProp::CopyTo** del mensaje original para copiar la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) o invocando el siguiente procedimiento de tres pasos para cada dato adjunto que se va a copiar:
    
   1. Llame al método [IMessage::CreateAttach](imessage-createattach.md) del nuevo mensaje reenviado para crear un nuevo dato adjunto. 
      
   2. Llame al método [IMessage::OpenAttach](imessage-openattach.md) del mensaje original para abrir los datos adjuntos que se van a copiar. 
      
   3. Llame al método **IMAPIProp::CopyTo** del mensaje original para copiar todas las propiedades de datos adjuntos de los datos adjuntos antiguos a la nueva. 
    
6. No incluya las siguientes propiedades en la llamada a **IMAPIProp::CopyTo:** 
    
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> |**PR_RCVD_REPRESENTING** propiedades  <br/> |
|**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))  <br/> |**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))  <br/> |
|**PR_RECEIVED_BY** propiedades  <br/> |**PR_REPLY_RECIPIENT** propiedades  <br/> |
|**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |**PR_SENDER** propiedades  <br/> |
|**PR_SENT_REPRESENTING** propiedades  <br/> |**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))  <br/> |
|**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. Para dar formato al texto del mensaje, agregue sangría y un párrafo de encabezado que incluya el remitente original, la fecha de transmisión, el asunto y la lista de destinatarios. No incluya caracteres de prefijo de estilo Internet con el contenido.
    
2. Llame [a ScCreateConversationIndex](sccreateconversationindex.md), pasando el valor de la propiedad PR_CONVERSATION_INDEX **del** mensaje original ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)).
    
3. Establezca un prefijo para el mensaje reenviado. Si usa el estándar "FW:", concatene estos caracteres al principio de **PR_NORMALIZED_SUBJECT** y establezca **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) en esta nueva cadena. No establezca **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Si usa un prefijo no **estándar,** como una cadena de más de tres caracteres, guárdalo en PR_SUBJECT_PREFIX . 
    
4. Establezca las **PR_SENT_REPRESENTING** propiedades en los valores correspondientes de **las PR_RCVD_REPRESENTING** propiedades. 
    
5. Cree una lista de destinatarios. Para obtener más información, vea [Crear una lista de destinatarios.](creating-a-recipient-list.md)
    
6. Llame al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje reenviado para guardarlo o [a IMessage::SubmitMessage](imessage-submitmessage.md) para guardarlo y enviarlo. 
    
## <a name="see-also"></a>Consulte también

- [Propiedad canónica PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)

