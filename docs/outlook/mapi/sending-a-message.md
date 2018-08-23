---
title: Enviar un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6845c3d86fb3d34119a296ebbae76a7322d7d8c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590914"
---
# <a name="sending-a-message"></a>Enviar un mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando esté listo para enviar un mensaje, llame a su método [IMessage::SubmitMessage](imessage-submitmessage.md) . **SubmitMessage** coloca el mensaje en la cola de salida y establece el indicador MSGFLAG_SUBMIT en la propiedad del mensaje **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).
  
El proveedor de almacén de mensajes, si estrechamente con un proveedor de transporte, muestra el mensaje directamente en el transporte que ofrece para el sistema de mensajería. Si no se estrechamente acoplamiento, el proveedor de almacén de mensajes informa a la cola MAPI que ha cambiado la cola de salida y la cola MAPI transfiere el mensaje a un proveedor de transporte apropiado.
  
Si se permiten a los usuarios cancelar una operación de envío, llame a [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para implementar esta característica. **AbortSubmit** quita el mensaje de la cola de salida. Los usuarios pueden dejar un envío suceda hasta que el mensaje se le da al sistema de mensajería subyacente. 
  
Si **SubmitMessage** devuelve MAPI_E_CORRUPT_DATA, se supone que los datos enviados están ahora perdido. Antes de intentar enviar una segunda vez, volver a escribir el mensaje mediante una llamada a [IMAPIProp::SetProps](imapiprop-setprops.md) y [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Mostrar un error al usuario si estas llamadas **IMAPIProp** producirá un error o si se produce un error en **SubmitMessage** una segunda vez. 
  
Después de una llamada correcta a **SubmitMessage**, liberar cualquier memoria que se ha asignado para la lista de destinatarios y suelte el mensaje y sus datos adjuntos. Una vez que se ha enviado un mensaje, MAPI no permite las operaciones posteriores en los punteros para estos objetos. La única excepción es llamar a **IUnknown:: Release**. No hay otras llamadas se permiten porque muchos de los proveedores de almacén de mensajes invalidarán los identificadores de entrada para los mensajes que se han enviado.
  

