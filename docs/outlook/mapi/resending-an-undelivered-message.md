---
title: Volver a enviar un mensaje no entregado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 4fd0bf5a542e006ec743dbb7fe03d3331875c6d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820508"
---
# <a name="resending-an-undelivered-message"></a>Volver a enviar un mensaje no entregado
  
**Se aplica a**: Outlook 
  
Un proveedor de transporte envía un informe de no entrega (NDR) cuando no puede entregar un mensaje que ha enviado correctamente. Es hasta el cliente si los usuarios pueden intentar volver a enviar estos mensajes no entregados. En caso de admitir volver a enviar mensajes, puede usar un formulario de MAPI o implementar el suyo propio. El formulario MAPI muestra los nombres de los destinatarios con errores y el motivo del error de entrega, si es posible e incluye un botón que, cuando se selecciona, permite que un usuario a enviar el mensaje.
  
Cuando se recibe un mensaje reciente, debe ser exactamente igual que el mensaje original. El destinatario debe ser no puede diferenciar entre un mensaje que se entregó en su primer intento de transmisión o un intento de subsiguiente. Las respuestas en este mensaje deberían funcionar exactamente como si el mensaje se había se ha enviado correctamente la primera vez.
  
### <a name="to-resend-an-undelivered-message"></a>Volver a enviar un mensaje no entregado
  
1. Llame a [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para crear un nuevo mensaje. 
    
2. Copiar todas las propiedades del mensaje original, excluyendo el ** PR_MESSAGE_RECIPIENTS ** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) (propiedad) y las propiedades **PR_SENDER** y **PR_SENT_REPRESENTING** . Realice las modificaciones de propiedad siguientes: 
    
   - Establezca **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) en el informe ** PR_ORIG_MESSAGE_CLASS ** ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) (propiedad).
    
   - Establecer la marca MSGFLAG_RESEND en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).
    
   - Establezca **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) en la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) del mensaje original.
    
   - Para cada destinatario, establezca MAPI_SUBMITTED en la propiedad **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). 
    
   - Duplicar a cada destinatario con errores. Cambie la propiedad **PR_RECIPIENT_TYPE** para el destinatario duplicado a MAPI_P1. Por lo tanto, para cada destinatario con errores hay ahora dos entradas en la tabla de destinatarios: una con **PR_RECIPIENT_TYPE** establecida en su valor original y la otra con **PR_RECIPIENT_TYPE** establecido en MAPI_P1. 
    
3. Llame a [ScCreateConversationIndex](sccreateconversationindex.md) para establecer una conversación de seguimiento si así lo desea. 
    
4. Llamar al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) del nuevo mensaje para actualizar la lista de destinatarios. 
    
5. Llame a [IMessage::SubmitMessage](imessage-submitmessage.md) para guardar y enviar el mensaje nuevo. 
    

