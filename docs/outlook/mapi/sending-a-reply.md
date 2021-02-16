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
ms.openlocfilehash: f47741369b1091c0dd24358e063de8f4675000fa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437451"
---
# <a name="sending-a-reply"></a>Enviar una respuesta

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente normalmente admiten dos tipos de respuestas: una que se envía solo al remitente del mensaje original y otra que se envía a todos los demás destinatarios incluidos en la lista de destinatarios del mensaje original además del remitente. Este segundo tipo de respuesta se conoce comúnmente como un mensaje de respuesta a todos.
  
Para enviar una respuesta de cualquiera de los tipos, implemente algunas de las mismas tareas que al enviar un mensaje original. Por ejemplo, abra el almacén de mensajes predeterminado y la carpeta de mensajes salientes, normalmente la Bandeja de salida, y llame al método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la carpeta saliente para crear la respuesta. Además, abra la carpeta que contiene el mensaje original, normalmente la Bandeja de entrada. Para obtener información acerca de cómo abrir carpetas diferentes, vea [Abrir una carpeta del almacén de mensajes.](opening-a-message-store-folder.md)
  
La principal diferencia entre crear una respuesta y crear un mensaje original es que, con una respuesta, la mayoría de las propiedades se basan o se copian directamente de las propiedades del mensaje original. Los datos adjuntos , la **propiedad** PR_MESSAGE_ATTACHMENTS de un mensaje ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)), se excluyen específicamente. La lista de destinatarios para responder a todos los mensajes se crea a partir de la lista del mensaje original con el destinatario representado por la propiedad **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) y se quitan todos los destinatarios de copia carbón. La **PR_RECEIVED_BY_SEARCH_KEY** representa al usuario actual. 
  
### <a name="to-send-a-reply"></a>Para enviar una respuesta
  
1. Abra el almacén de mensajes predeterminado. Para obtener más información, vea [Abrir el almacén de mensajes predeterminado.](opening-the-default-message-store.md)
    
2. Abra la carpeta Bandeja de salida. Para obtener más información, vea [Abrir una carpeta del almacén de mensajes.](opening-a-message-store-folder.md)
    
3. Llame al método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la Bandeja de salida para crear la respuesta. 
    
4. Llame al método [IMAPIProp::CopyTo](imapiprop-copyto.md) del mensaje original para copiar las siguientes propiedades en el mensaje de respuesta: 
    
   - **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)) o **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), dependiendo de si se admite o no formato de texto enriquecido.
    
   - **PR \_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), si la respuesta irá a toda la lista de destinatarios.
    
   - **PR \_ NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
    
5. No incluya las siguientes propiedades en la llamada a **IMAPIProp::CopyTo:**
    
    |||
    |:-----|:-----|
    |**PR \_ CLIENT \_ SUBMIT \_ TIME** <br/> |**PR \_ MESSAGE \_ DELIVERY \_ TIME** <br/> |
    |**HORA DE \_ DESCARGA \_ DE MENSAJES \_ PR** <br/> |**MARCAS \_ DE MENSAJES \_ PR** <br/> |
    |**INFORME DE \_ ENTREGA PR \_ \_ ORIGINATOR\REQUESTED** <br/> |**PR \_ RCVD \_ REPRESENTING** properties  <br/> |
    |**PR \_ READ \_ RECEIPT \_ ENTRYID** <br/> |**CONFIRMACIÓN \_ DE LECTURA PR \_ \_ SOLICITADA** <br/> |
    |**PR \_ Propiedades RECEIVED \_ BY**  <br/> |**PR \_ Responder \_ propiedades DE DESTINATARIO**  <br/> |
    |**PR \_ REPORT \_ ENTRYID** <br/> |**PR \_ Propiedades del** remitente  <br/> |
    |**PR \_ Propiedades \_ SENT REPRESENTING**  <br/> |**PR \_ SENTMAIL \_ ENTRYID** <br/> |
    |**PREFIJO \_ PR SUBJECT \_** <br/> | <br/> |
   
6. Agregue texto separador a cualquier propiedad del cuerpo del mensaje que admita **PR_BODY,** **PR_HTM** L o **PR_RTF_COMPRESSED**.
    
7. Llame [a ScCreateConversationIndex](sccreateconversationindex.md), pasando el valor de la propiedad PR_CONVERSATION_INDEX **del** mensaje original ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)).
    
8. Establezca un prefijo para la respuesta. Si usa el estándar "RE:", concatene estos caracteres al principio de **PR_NORMALIZED_SUBJECT** y establezca **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) en esta nueva cadena. No establezca **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Si usa un prefijo no **estándar,** como una cadena de más de tres caracteres, guárdalo en PR_SUBJECT_PREFIX . 
    
9. Establezca las **PR_SENT_REPRESENTING** propiedades en los valores correspondientes de **las PR_RCVD_REPRESENTING** propiedades. 
    
10. Establezca cada una de las entradas de **PR \_ REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) y **PR_REPLY \_ RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) en el identificador de entrada y el nombre para mostrar de un destinatario principal, un destinatario cuyo tipo es MAPI_TO. Mantenga estas propiedades sincronizadas. Es decir, **PR_REPLY_RECIPIENT \_ ENTRIES** y **PR_REPLY_RECIPIENT_NAMES** deben contener el mismo número de entradas, y una entrada en una posición determinada de una de las propiedades debe corresponder a una entrada en la misma posición de la otra propiedad. 
    
11. Si la respuesta se envía solo al remitente del mensaje original, cree una lista de destinatarios de entrada única con el destinatario representado por la propiedad PR_SENT_REPRESENTING original **del** mensaje. Para obtener más información acerca de la creación de una lista de destinatarios, vea [Crear una lista de destinatarios.](creating-a-recipient-list.md)
    
12. Si la respuesta es una respuesta a todos, cree una lista de destinatarios de la siguiente manera:
    
    1. Llame al método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) del mensaje original para obtener acceso a su tabla de destinatarios. 
        
    2. Llame [a HrQueryAllRows](hrqueryallrows.md) para recuperar todas las filas de la tabla. Determine si cada fila representa un destinatario de copia principal o carboníceo y debe permanecer en la lista o si representa a un destinatario de copia carbón o al usuario y debe quitarse de la lista. 
        
    3. Para diferenciar entre tipos de destinatarios, consulte **la PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Esta columna se establecerá en MAPI_TO destinatarios principales, MAPI_CC destinatarios con copia carbón y MAPI_BCC destinatarios con copia carbón a la vista. 
        
    4. Compare la **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) con la propiedad **PR_RECEIVED_BY_SEARCH_KEY** del mensaje original para determinar si la fila representa al usuario. 
        
    5. Quite filas no deseadas de la lista de destinatarios llamando a [MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria asociada a las entradas correspondientes en la estructura [SRowSet](srowset.md) de la tabla de destinatarios. Establezca todos los valores de la matriz de valores de propiedad en cero, todos los miembros **cValues** en cero y todos los miembros **lpProps** de cada estructura [SRow](srow.md) del **SRowSet** en NULL. 
        
    6. Agregue el remitente a la lista de destinatarios, tal como se representa mediante las propiedades **PR \_ SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) y **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) del mensaje original. Compruebe que el remitente no está duplicado en la lista.
        
    7. Llame al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) del mensaje de respuesta, estableciendo el parámetro  _ulFlags_ en cero, para crear una nueva lista de destinatarios para el mensaje de respuesta o reenviado en función de la lista del mensaje original. 
    
13. Llame al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la respuesta para guardar el mensaje o [IMessage::SubmitMessage](imessage-submitmessage.md) para guardarlo y enviarlo. 
    
> [!NOTE]
> Antes de **llamar a IMessage::ModifyRecipients** para almacenar los cambios en la lista de destinatarios, puede permitir que los usuarios realicen modificaciones a través del formulario de mensaje. Los usuarios pueden agregar a la lista o quitar miembros concretos. Permitir a los usuarios realizar cambios en una lista de destinatarios es una característica de cliente opcional. 
  

