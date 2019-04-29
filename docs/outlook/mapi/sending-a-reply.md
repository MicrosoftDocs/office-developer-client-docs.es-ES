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
  
Normalmente, las aplicaciones cliente admiten dos tipos de respuesta: una que se envía solo al remitente del mensaje original y otra que se envía a todos los demás destinatarios incluidos en la lista de destinatarios del mensaje original, además del remitente. Este segundo tipo de respuesta se conoce comúnmente como mensaje responder a todos.
  
Para enviar una respuesta de cualquier tipo, se implementan algunas de las tareas que se deben realizar al enviar un mensaje original. Por ejemplo, se abre el almacén de mensajes predeterminado y la carpeta de mensajes salientes, normalmente la bandeja de salida, y se llama al método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) de la carpeta de salida para crear la respuesta. Además, se abre la carpeta que contiene el mensaje original, que suele ser la bandeja de entrada. Para obtener información acerca de cómo abrir carpetas diferentes, consulte [abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md).
  
La principal diferencia entre crear una respuesta y crear un mensaje original es que, con una respuesta, la mayoría de las propiedades se basan o copian directamente de las propiedades del mensaje original. Datos adJuntos: propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) de un mensaje, se excluyen específicamente. La lista de destinatarios de un mensaje reply All se crea a partir de la lista del mensaje original con el destinatario representado por la propiedad **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) y se quitan todos los destinatarios de copia oculta. La propiedad **PR_RECEIVED_BY_SEARCH_KEY** representa al usuario actual. 
  
### <a name="to-send-a-reply"></a>Para enviar una respuesta
  
1. Abra el almacén de mensajes predeterminado. Para obtener más información, consulte [abrir el almacén de mensajes predeterminado](opening-the-default-message-store.md).
    
2. Abra la carpeta Bandeja de salida. Para obtener más información, consulte [abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md).
    
3. Llame al método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) de la bandeja de salida para crear la respuesta. 
    
4. Llame al método [IMAPIProp:: CopyTo](imapiprop-copyto.md) del mensaje original para copiar las siguientes propiedades en el mensaje de respuesta: 
    
   - **El\_cuerpo de PR** ([PidTagBody](pidtagbody-canonical-property.md)) o **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), dependiendo de si es compatible o no con el formato de texto enriquecido.
    
   - **PR\_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), si la respuesta va a la lista de destinatarios completa.
    
   - **PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
    
5. No incluya las siguientes propiedades en la llamada a **IMAPIProp:: CopyTo**:
    
    |||
    |:-----|:-----|
    |**Hora\_de\_envío\_del cliente de PR** <br/> |**Hora\_de\_entrega\_del mensaje de PR** <br/> |
    |**Tiempo\_de\_descarga\_de mensajes de PR** <br/> |**Marcas\_de\_mensaje de PR** <br/> |
    |**REPORT\REQUESTED\_de\_entrega\_ del remitente de PR** <br/> |**PR\_.\_que representan** propiedades  <br/> |
    |**EntryID\_de\_confirmación\_de lectura de PR** <br/> |**Confirmación\_\_de\_lectura de PR solicitada** <br/> |
    |**PR\_recibido\_por** propiedades  <br/> |Propiedades del **destinatario de respuesta\_\_de PR**  <br/> |
    |**EntryID\_del\_informe de PR** <br/> |Propiedades del **remitente de PR\_**  <br/> |
    |**RP\_enviadas\_que representan** propiedades  <br/> |**SENTMAIL\_\_de EntryID de PR** <br/> |
    |**Prefijo\_de asunto de PR\_** <br/> | <br/> |
   
6. Agregue texto de separador a la propiedad del cuerpo del mensaje que admita: **PR_BODY**, **PR_HTM**L o **PR_RTF_COMPRESSED**.
    
7. Llamar a [ScCreateConversationIndex](sccreateconversationindex.md), pasando el valor de la propiedad **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) del mensaje original.
    
8. Establezca un prefijo para la respuesta. Si usa el estándar "RE:", concatene estos caracteres al principio de **PR_NORMALIZED_SUBJECT** y establezca **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) en esta nueva cadena. No establezca **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Si usa un prefijo no estándar, como una cadena de más de tres caracteres, almacénelo en **PR_SUBJECT_PREFIX**. 
    
9. Establezca las propiedades **PR_SENT_REPRESENTING** en los valores correspondientes de las propiedades de **PR_RCVD_REPRESENTING** . 
    
10. Establezca cada una de las entradas **de\_PR REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) **y\_PR_REPLY RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) en el identificador de entrada y el nombre para mostrar de un destinatario principal: un destinatario cuyo tipo es MAPI_TO. Mantenga estas propiedades sincronizadas. Es decir, **PR_REPLY_RECIPIENT\_entradas** y **PR_REPLY_RECIPIENT_NAMES** deben contener el mismo número de entradas y una entrada en una posición concreta en una de las propiedades debe corresponder a una entrada en la misma posición en la otra. Inspector. 
    
11. Si la respuesta se envía sólo al remitente del mensaje original, cree una lista de destinatarios de entrada única con el destinatario representado por la propiedad **PR_SENT_REPRESENTING** del mensaje original. Para obtener más información acerca de la creación de una lista de destinatarios, vea [crear una lista de destinatarios](creating-a-recipient-list.md).
    
12. Si la respuesta es una respuesta, cree una lista de destinatarios de la siguiente manera:
    
    1. Llame al método [IMessage:: GetRecipientTable](imessage-getrecipienttable.md) del mensaje original para obtener acceso a su tabla de destinatarios. 
        
    2. Llame a [HrQueryAllRows](hrqueryallrows.md) para recuperar todas las filas de la tabla. DeTermine si cada fila representa un destinatario principal o de copia carbón y debe permanecer en la lista o si representa un destinatario de copia oculta o el usuario y debe quitarse de la lista. 
        
    3. Diferenciar entre tipos de destinatarios mirando la columna **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Esta columna se establecerá en MAPI_TO para los destinatarios principales, MAPI_CC para los destinatarios de copia carbón y MAPI_BCC para los destinatarios de copia oculta. 
        
    4. Compare la columna **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) con la propiedad **PR_RECEIVED_BY_SEARCH_KEY** del mensaje original para determinar si la fila representa al usuario. 
        
    5. Para quitar filas no deseadas de la lista de destinatarios, llame a [MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria asociada con las entradas correspondientes en la estructura [SRowSet](srowset.md) de la tabla de destinatarios. Establezca todos los valores de la matriz de valores de propiedad en cero, todos los miembros de **cValues** en cero, y todos los miembros de **LpProps** en cada [SRow](srow.md) estructura de la **SRowSet** en NULL. 
        
    6. Agregar el remitente a la lista de destinatarios, tal y como se representa en <b0>el<b1></b1>SENT_REPRESENTING_NAME</b0> (<b2>PidTagSentRepresentingName</b2>) y el <b3>PR_SENT_REPRESENTING_ENTRYID</b3> (<b4>PidTagSentRepresentingEntryId</b4>) del mensaje original </a1>. Compruebe que el remitente no esté duplicado en la lista.
        
    7. Llame al método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) del mensaje de respuesta, estableciendo el parámetro _ulFlags_ en cero, para crear una nueva lista de destinatarios para el mensaje de respuesta o reenviado en función de la lista del mensaje original. 
    
13. Llame al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de la respuesta para guardar el mensaje o [IMessage:: SubmitMessage](imessage-submitmessage.md) para guardarlo y enviarlo. 
    
> [!NOTE]
> Antes de llamar a **IMessage:: ModifyRecipients** para almacenar los cambios en la lista de destinatarios, puede permitir a los usuarios realizar modificaciones mediante el formulario de mensaje. Los usuarios pueden agregar a la lista o quitar determinados miembros. Permitir que los usuarios realicen cambios en una lista de destinatarios es una característica de cliente opcional. 
  

