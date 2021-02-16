---
title: IMessage IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage
api_type:
- COM
ms.assetid: 7e244d40-595e-432c-aa8c-f9f62ca3c138
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 217411dc8bae12a3d7544a4cfd189c4c8f863195
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432502"
---
# <a name="imessage--imapiprop"></a>IMessage : IMAPIProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Administra mensajes, datos adjuntos y destinatarios.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuesto por:  <br/> |Objeto Message  <br/> |
|Implementado por:  <br/> |Proveedores de al almacenamiento de mensajes  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMessage  <br/> |
|Tipo de puntero:  <br/> |LPMESSAGE  <br/> |
|Modelo de transacción:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
|[GetAttachmentTable](imessage-getattachmenttable.md) <br/> |Devuelve la tabla de datos adjuntos del mensaje.  <br/> |
|[OpenAttach](imessage-openattach.md) <br/> |Abre un archivo adjunto.  <br/> |
|[CreateAttach](imessage-createattach.md) <br/> |Crea un nuevo archivo adjunto.  <br/> |
|[DeleteAttach](imessage-deleteattach.md) <br/> |Elimina datos adjuntos.  <br/> |
|[GetRecipientTable](imessage-getrecipienttable.md) <br/> |Devuelve la tabla de destinatarios del mensaje.  <br/> |
|[ModifyRecipients](imessage-modifyrecipients.md) <br/> |Agrega, elimina o modifica a los destinatarios del mensaje.  <br/> |
|[SubmitMessage](imessage-submitmessage.md) <br/> |Guarda todos los cambios en el mensaje y lo marca como listo para el envío.  <br/> |
|[SetReadFlag](imessage-setreadflag.md) <br/> |Establece o borra la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje y administra el envío de informes de lectura.  <br/> |
   
Las siguientes propiedades son necesarias en los mensajes en algún momento durante su ciclo de vida. La mayoría de las propiedades de solo lectura las establece el proveedor del almacén de mensajes cuando un cliente llama al método [IMAPIProp::SaveChanges de](imapiprop-savechanges.md) un mensaje. El proveedor de transporte establece otras propiedades de solo lectura. 
  
|**Propiedades necesarias para los mensajes de todas las clases**|**Access**|
|:-----|:-----|
|**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Lectura/escritura  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Lectura/escritura  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_ORIGINATOR** propiedades  <br/> |Solo lectura  <br/> |
|**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RECEIVED_BY** propiedades  <br/> |Solo lectura  <br/> |
|**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_SENDER** propiedades  <br/> |Solo lectura  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
Las propiedades siguientes son de solo lectura para los clientes, con la excepción de **PR_BODY**. Los clientes construyen esta propiedad cuando procesan un informe.
  
|**Propiedades de los mensajes de informe**|
|:-----|
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |
|**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))  <br/> |
|**PR_MESSAGE_CLASS** <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DISPLAY_BCC** ([PidTagOriginalDisplayBcc](pidtagoriginaldisplaybcc-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DISPLAY_CC** ([PidTagOriginalDisplayCc](pidtagoriginaldisplaycc-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DISPLAY_TO** ([PidTagOriginalDisplayTo](pidtagoriginaldisplayto-canonical-property.md))  <br/> |
|**PR_ORIGINAL_SUBJECT** ([PidTagOriginalSubject](pidtagoriginalsubject-canonical-property.md))  <br/> |
|**PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md))  <br/> |
|**PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md))  <br/> |
|**PR_REPORT_TEXT** ([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |
|**PR_REPORT_TIME** ([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |
|**PR_SEARCH_KEY** <br/> |
|**PR_SENDER** propiedades  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
|**Propiedades de destinatarios de mensajes**|**Access**|**Obligatorio u opcional**|
|:-----|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Solo lectura  <br/> |Obligatorio  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lectura/escritura  <br/> |Obligatorio  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Lectura/escritura  <br/> |Obligatorio  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Solo lectura  <br/> |Opcional  <br/> |
|**PR_ENTRYID** <br/> |Solo lectura  <br/> |Obligatorio  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Solo lectura  <br/> |Obligatorio  <br/> |
|**PR_SEARCH_KEY** <br/> |Solo lectura  <br/> |Opcional  <br/> |
   

