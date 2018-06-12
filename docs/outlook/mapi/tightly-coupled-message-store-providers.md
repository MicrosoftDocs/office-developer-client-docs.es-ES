---
title: Proveedores de almacén de mensajes acoplado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2eb493d7-bbd1-45b2-bd82-2bc452b2deab
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 83ebb739302ca0e12604b9eaf854f273554826ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820855"
---
# <a name="tightly-coupled-message-store-providers"></a>Proveedores de almacén de mensajes acoplado

  
  
**Se aplica a**: Outlook 
  
Los proveedores de almacén de mensajes pueden estar estrechamente acoplados con un proveedor de transporte. Acoplamiento estrechamente significa de proveedores de servicio MAPI implementar los dos proveedores tal que el proveedor de almacenamiento y el proveedor de transporte pueden comunicarse para hacer que el proceso de enviar y recibir mensajes más eficaces. La ventaja de hacerlo es que las mejoras de rendimiento se pueden producir cuando dos proveedores de servicio pueden interactuar con cada una de las demás directamente en lugar de hacerlo por medio de la cola de MAPI. Para asociar estrechamente un proveedor de almacén de mensajes a un proveedor de transporte, el proveedor de transporte debe colocar el identificador de entrada del proveedor de almacén de mensajes en la propiedad **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) en el proveedor de transporte fila en la tabla de estado MAPI. Esto permite que la cola MAPI conectar el proveedor de almacenamiento con el proveedor de transporte.
  
No es necesario que un proveedor de almacén de mensajes nunca se complementa muy bien con cualquier otro proveedor de servicios. El proveedor de servicios más comunes para asociar estrechamente con un proveedor de almacén de mensajes es un proveedor de transporte. Esto se realiza normalmente poder enviar y recibir mensajes puede realizarse sin que implican a la cola de MAPI. Por ejemplo, cuando el usuario envía un mensaje saliente, el proveedor de transporte y el proveedor de almacén de mensajes combinada pueden enviarlo directamente. No es necesario que los proveedores de servicios combinados en primer lugar notificar a cola MAPI que hay un nuevo mensaje para procesar y, a continuación, espere a que la cola MAPI iniciar el proceso de transferir el mensaje desde el proveedor de almacenamiento de mensajes para el proveedor de transporte. Esto tiene ventajas determinadas cuando se utiliza un almacén de mensajes basado en servidor al minimizar el tráfico de red entre el equipo del usuario y el servidor.
  
En general, no hay ningún procedimientos bien especificados para acoplamiento estrechamente los proveedores de servicios. Sin embargo, debe usar las siguientes instrucciones:
  
- Si el motivo de acoplamiento estrechamente los proveedores de servicios es el rendimiento, tenga en cuenta que el acoplamiento toma partes del subsistema MAPI fuera de los procesos que esos elementos normalmente podrían estar involucrados en. Esto implica que los elementos individuales en el proveedor de servicios combinado deben interactúan entre sí de forma que simula la interacción normalmente tendría con los elementos del subsistema MAPI que no se usan.
    
- Cuando interactúan los proveedores de servicios totalmente acoplado con otros componentes de MAPI, deben seguir interactuando con ellos en exactamente de la forma que lo haría si no estaban estrechamente acoplados. Por ejemplo, si un usuario está usando un proveedor de transporte y el proveedor de almacén de mensajes combinada como su almacén de mensajes de forma predeterminada, pero está utilizando un proveedor de transporte independiente para enviar mensajes, como puede suceder cuando un usuario tiene un equipo de viaje y pasa a un precio de transporte remoto ovider: la parte de almacén de mensajes del proveedor de servicios totalmente acoplado aún debe interactuar con la cola MAPI como si se tratase de un proveedor de almacén de mensajes independiente.
    
## <a name="see-also"></a>Ver también



[Desarrollar un proveedor de almac�n de mensajes de MAPI](developing-a-mapi-message-store-provider.md)

