---
title: Envío de un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 01fd66033da0f24948913f47a752d555eca655fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423625"
---
# <a name="sending-a-message"></a>Envío de un mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando esté listo para enviar un mensaje, llame a su [método IMessage::SubmitMessage.](imessage-submitmessage.md) **SubmitMessage** coloca el mensaje en la cola saliente y establece la marca MSGFLAG_SUBMIT en la propiedad PR_MESSAGE_FLAGS **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje.
  
El proveedor de almacén de mensajes, si está estrechamente unido a un proveedor de transporte, proporciona el mensaje directamente al transporte que lo entrega al sistema de mensajería. Si no está estrechamente acoplado, el proveedor del almacén de mensajes informa a la cola MAPI de que la cola saliente ha cambiado y la cola MAPI transfiere el mensaje a un proveedor de transporte adecuado.
  
Si permite que los usuarios cancelen una operación de envío, llame a [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para implementar esta característica. **AbortSubmit** quita el mensaje de la cola saliente. Se puede permitir a los usuarios detener un envío hasta que el mensaje se entrega al sistema de mensajería subyacente. 
  
Si **SubmitMessage** devuelve MAPI_E_CORRUPT_DATA, suponga que los datos que se envían ahora se pierden. Antes de intentar enviar una segunda vez, vuelva a escribir el mensaje llamando a [IMAPIProp::SetProps](imapiprop-setprops.md) e [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Muestra un error al usuario si estas llamadas **IMAPIProp** fallan o **si SubmitMessage falla** una segunda vez. 
  
Después de una llamada correcta a **SubmitMessage**, libere cualquier memoria asignada para la lista de destinatarios y libere el mensaje y sus datos adjuntos. Una vez enviado un mensaje, MAPI no permite ninguna otra operación en los punteros de estos objetos. La única excepción es llamar **a IUnknown::Release**. No se permiten otras llamadas porque muchos proveedores de almacenes de mensajes invalidan los identificadores de entrada de los mensajes que se han enviado.
  

