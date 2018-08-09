---
title: Enviar una respuesta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 90dafeae-6b61-40e3-8341-d6a11799d0f2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d83fce761afb4673b71df9d620ac3fd794d6009f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820597"
---
# <a name="sending-a-reply"></a>Enviar una respuesta

**Hace referencia a**: Outlook 
  
Normalmente, las aplicaciones cliente admiten dos tipos de respuestas: uno que se envía sólo al remitente del mensaje original y uno que se envía a todos los otros destinatarios incluidos en la lista de destinatarios del mensaje original además el remitente. En este segundo tipo de respuesta con frecuencia se conoce como una respuesta de que todos los mensajes.
  
Para enviar una respuesta de cualquier tipo, implementar algunas de las mismas tareas que al enviar un mensaje original. Por ejemplo, abra el almacén de mensajes de forma predeterminada y la carpeta de mensaje saliente, normalmente la Bandeja de salida y llamar al método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la carpeta de salida para crear la respuesta. Además, abra la carpeta que contiene el mensaje original, normalmente en la Bandeja de entrada. Para obtener información acerca de cómo abrir diferentes carpetas, vea [Abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md).
  
La diferencia principal entre la creación de una respuesta y la creación de un mensaje original es que con una respuesta, la mayoría de las propiedades es según o copió directamente desde las propiedades del mensaje original. Los datos adjuntos: propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) de un mensaje, se excluyen específicamente. La lista de destinatarios para una respuesta de todos los mensajes se crean a partir de lista del mensaje original con el destinatario representada por la propiedad **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) y todos los destinatarios de copia carbón quitados. La propiedad **PR_RECEIVED_BY_SEARCH_KEY** representa al usuario actual. 
  
### <a name="to-send-a-reply"></a>Para enviar una respuesta
  
1. Abra el almacén de mensajes predeterminado. Para obtener más información, vea [Abrir el almacén de mensajes predeterminado](opening-the-default-message-store.md).
    
2. Abra la carpeta Bandeja de salida. Para obtener más información, vea [Abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md).
    
3. Llamar al método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la Bandeja de salida para crear la respuesta. 
    
4. Llamar al método [IMAPIProp::CopyTo](imapiprop-copyto.md) del mensaje original para copiar las propiedades siguientes en el mensaje de respuesta: 
    
   - **Precio:\_cuerpo** ([PidTagBody](pidtagbody-canonical-property.md)) o **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), dependiendo de si admite formato de texto enriquecido.
    
   - **Precio:\_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), si la respuesta se realizarán a toda la lista de destinatarios.
    
   - **Precio:\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
    
5. No se incluyen las siguientes propiedades en la llamada a **IMAPIProp::CopyTo**:
    
    |||
    |:-----|:-----|
    |**Precio:\_cliente\_envío\_tiempo** <br/> |**Precio:\_mensaje\_entrega\_tiempo** <br/> |
    |**Precio:\_mensaje\_descargar\_tiempo** <br/> |**Precio:\_mensaje\_marcas** <br/> |
    |**Precio:\_ORIGINADOR\_entrega\_ REPORT\REQUESTED** <br/> |**PR\_recibidos\_que representa** propiedades  <br/> |
    |**Precio:\_leer\_confirmación\_ENTRYID** <br/> |**Precio:\_leer\_confirmación\_solicitado** <br/> |
    |**PR\_RECEIVED\_BY** propiedades  <br/> |**PR\_respuesta\_destinatario** propiedades  <br/> |
    |**Precio:\_informe\_ENTRYID** <br/> |**PR\_remitente** propiedades  <br/> |
    |**PR\_SENT\_que representa** propiedades  <br/> |**Precio:\_correo enviado\_ENTRYID** <br/> |
    |**Precio:\_asunto\_PREFIJO** <br/> | <br/> |
   
6. Agregar texto de separador a sea cual sea el cuerpo de mensaje (propiedad) admiten: **PR_BODY**, **PR_HTM**L o **PR_RTF_COMPRESSED**.
    
7. Llame a [ScCreateConversationIndex](sccreateconversationindex.md), pasando el valor de propiedad de **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) del mensaje original.
    
8. Establecer un prefijo de la respuesta. Si está utilizando el estándar "RE:", concatene estos caracteres hasta el principio del **PR_NORMALIZED_SUBJECT** y establecer **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) a esta nueva cadena. No establezca **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Si está utilizando un prefijo no estándar, como una cadena de más de tres caracteres, almacenar en **PR_SUBJECT_PREFIX**. 
    
9. Establecer las propiedades **PR_SENT_REPRESENTING** a los valores correspondientes en las propiedades **PR_RCVD_REPRESENTING** . 
    
10. Establecer cada una de las entradas de **PR\_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) y **PR_REPLY\_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) en el nombre de identificador y presentación de entrada de un destinatario principal: un destinatario cuyo tipo es MAPI_TO. Mantener estas propiedades sincronizadas. Es decir, **PR_REPLY_RECIPIENT\_entradas** y **PR_REPLY_RECIPIENT_NAMES** debe contener el mismo número de entradas y una entrada en una posición determinada en una de las propiedades debe corresponder a una entrada en la misma posición en el otro propiedad. 
    
11. Si la respuesta se envía sólo al remitente del mensaje original, cree una lista de destinatarios de entrada único con el destinatario representado por la propiedad **PR_SENT_REPRESENTING** del mensaje original. Para obtener más información acerca de cómo crear una lista de destinatarios, vea [crear una lista de destinatarios](creating-a-recipient-list.md).
    
12. Si la respuesta es una respuesta todas, cree una lista de destinatarios de la siguiente manera:
    
    1. Llamar al método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) del mensaje original para obtener acceso a su tabla de destinatarios. 
        
    2. Llame a [HrQueryAllRows](hrqueryallrows.md) para recuperar todas las filas en la tabla. Determinar si cada fila representa a un destinatario principal o con copia oculta y debe permanecer en la lista o si se representa un destinatario de copia carbón oculta o el usuario y debe quitarse de la lista. 
        
    3. Diferenciar entre tipos de destinatarios mirando en la columna **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Esta columna se establecerá en MAPI_TO para destinatarios principales, MAPI_CC para destinatarios de copia carbón y MAPI_BCC para destinatarios de copia carbón. 
        
    4. Compare la columna **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) con la propiedad **PR_RECEIVED_BY_SEARCH_KEY** del mensaje original para determinar si la fila representa al usuario. 
        
    5. Quitar filas no deseadas de la lista de destinatarios llamando [MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria asociada con las entradas correspondientes en la estructura de [SRowSet](srowset.md) de la tabla de destinatarios. Establecer todos los valores en la matriz de valores de propiedad en cero, todos los miembros de **cValues** en cero y todos los miembros de **lpProps** en cada estructura [SRow](srow.md) en el **SRowSet** en NULL. 
        
    6. Agregar el remitente a la lista de destinatarios, tal como está representado por el mensaje original **PR\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) y **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) Propiedades. Compruebe que el remitente no está duplicado en la lista.
        
    7. Llamar al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) del mensaje de respuesta, al establecer el parámetro _ulFlags_ en cero, para crear una nueva lista de destinatarios de la respuesta o reenviar el mensaje en función de la lista desde el mensaje original. 
    
13. Llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la respuesta para guardar el mensaje o [IMessage::SubmitMessage](imessage-submitmessage.md) para guardar y enviarla. 
    
> [!NOTE]
> Antes de llamar a **IMessage::ModifyRecipients** para almacenar los cambios en la lista de destinatarios, puede permitir a los usuarios realizar modificaciones a través del formulario de mensaje. Los usuarios puedan agregar a la lista o quitar a miembros determinados. Permitir a los usuarios realizar cambios en una lista de destinatarios es una característica de cliente opcional. 
  

