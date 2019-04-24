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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339749"
---
# <a name="sending-a-message"></a>Envío de un mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando esté listo para enviar un mensaje, llame a su método [IMessage:: SubmitMessage](imessage-submitmessage.md) . **SubmitMessage** coloca el mensaje en la cola de salida y establece la marca MSGFLAG_SUBMIT en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje.
  
El proveedor de almacenamiento de mensajes, si está estrechamente acoplado a un proveedor de transporte, le envía el mensaje directamente al transporte que lo entrega al sistema de mensajería. Si no se combina estrechamente, el proveedor de almacenamiento de mensajes informa a la cola MAPI de que la cola de salida ha cambiado y la cola MAPI transfiere el mensaje a un proveedor de transporte adecuado.
  
Si permite a los usuarios cancelar una operación de envío, llame a [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) para implementar esta característica. **AbortSubmit** quita el mensaje de la cola de salida. Los usuarios pueden impedir que se produzca un envío hasta que se le dé el mensaje al sistema de mensajería subyacente. 
  
Si **SubmitMessage** devuelve MAPI_E_CORRUPT_DATA, asuma que los datos que se están enviando se han perdido. Antes de intentar enviar una segunda vez, vuelva a escribir el mensaje mediante una llamada a [IMAPIProp:: SetProps](imapiprop-setprops.md) y [IMAPIProp:: SaveChanges](imapiprop-savechanges.md). Muestra un error al usuario si se produce un error en las llamadas de **IMAPIProp** o si **SubmitMessage** por segunda vez. 
  
Tras realizar correctamente una llamada a **SubmitMessage**, libere la memoria asignada a la lista de destinatarios y libere el mensaje y sus datos adjuntos. Una vez que se ha enviado un mensaje, MAPI no permite más operaciones en los punteros de estos objetos. La única excepción está llamando a **IUnknown:: Release**. No se permiten otras llamadas porque muchos proveedores de almacenamiento de mensajes invalidan identificadores de entrada para los mensajes enviados.
  

