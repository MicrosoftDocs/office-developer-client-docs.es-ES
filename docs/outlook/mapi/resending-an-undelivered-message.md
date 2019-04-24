---
title: Reenviar un mensaje sin entregar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ddd0c1419531b0822bb98df51f47e12e63dcf242
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328682"
---
# <a name="resending-an-undelivered-message"></a>Reenviar un mensaje sin entregar
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un proveedor de transporte envía un informe de no entrega (NDR) cuando no puede entregar correctamente un mensaje que ha enviado. Depende del cliente si los usuarios pueden intentar volver a enviar estos mensajes no entregados. Si admite el reenvío de mensajes, puede usar un formulario proporcionado por MAPI o implementar el suyo propio. El formulario MAPI muestra los nombres de los destinatarios erróneos y el motivo del error de entrega, si es posible, e incluye un botón que, cuando se selecciona, permite al usuario volver a enviar el mensaje.
  
Cuando se recibe un mensaje reenviado, tiene que tener un aspecto idéntico al del mensaje original. El destinatario no debe ser capaz de diferenciar entre un mensaje que se entregó el primer intento durante la transmisión o un intento posterior. Las respuestas de este mensaje deben funcionar exactamente como si el mensaje se hubiera enviado correctamente la primera vez.
  
### <a name="to-resend-an-undelivered-message"></a>Para reenviar un mensaje no entregado
  
1. Llame a [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) para crear un mensaje nuevo. 
    
2. Copie todas las propiedades del mensaje original, excluida la propiedad * * PR_MESSAGE_RECIPIENTS * * ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) y las propiedades **PR_SENDER** y **PR_SENT_REPRESENTING** . Realice las siguientes modificaciones de propiedad: 
    
   - Establezca **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) en la propiedad * * PR_ORIG_MESSAGE_CLASS * * ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) del informe.
    
   - Establezca la marca MSGFLAG_RESEND en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).
    
   - Establezca **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) en la propiedad del mensaje **** original ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
   - Para cada destinatario, establezca MAPI_SUBMITTED en la propiedad **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). 
    
   - Duplique cada destinatario con error. Cambie la propiedad **PR_RECIPIENT_TYPE** del destinatario duplicado a MAPI_P1. Por lo tanto, para cada destinatario con error hay ahora dos entradas en la tabla de destinatarios: una con **PR_RECIPIENT_TYPE** establecido en su valor original y la otra con **PR_RECIPIENT_TYPE** establecido en MAPI_P1. 
    
3. Llame a [ScCreateConversationIndex](sccreateconversationindex.md) para configurar el seguimiento de conversaciones si lo desea. 
    
4. Llame al método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) del nuevo mensaje para actualizar la lista de destinatarios. 
    
5. Llame a [IMessage:: SubmitMessage](imessage-submitmessage.md) para guardar y enviar el nuevo mensaje. 
    

