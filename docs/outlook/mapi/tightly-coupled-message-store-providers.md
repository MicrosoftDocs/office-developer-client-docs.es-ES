---
title: Proveedores de almacenamiento de mensajes estrechamente acoplados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2eb493d7-bbd1-45b2-bd82-2bc452b2deab
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3c9996dad1e9aa8c291f1cd593d9651994d86141
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413230"
---
# <a name="tightly-coupled-message-store-providers"></a>Proveedores de almacenamiento de mensajes estrechamente acoplados

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de almacenamiento de mensajes pueden acoplarse estrechamente con un proveedor de transporte. El acoplamiento estricto de los proveedores de servicios MAPI implica la implementación de los dos proveedores, de modo que el proveedor de almacén y el proveedor de transporte puedan comunicarse para que el proceso de envío y recepción de mensajes sea más eficiente. La ventaja de hacerlo es que las mejoras de rendimiento pueden producirse cuando dos proveedores de servicios pueden interactuar entre sí directamente en lugar de con una cola MAPI. Para acoplar rigurosamente un proveedor de almacenamiento de mensajes a un proveedor de transporte, el proveedor de transporte debe ubicar el identificador de entrada del proveedor de almacén de mensajes en la propiedad **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) del proveedor de transporte fila de la tabla de estado de MAPI. Esto permite que la cola MAPI Conecte el proveedor de almacén al proveedor de transporte.
  
No es necesario que un proveedor de almacenamiento de mensajes esté estrechamente acoplado a ningún otro proveedor de servicios. El proveedor de servicios más común para acoplar estrechamente un proveedor de almacenamiento de mensajes es un proveedor de transporte. Esto se suele hacer para que el envío y la recepción de mensajes se puedan llevar a cabo sin que intervenga la cola MAPI. Por ejemplo, cuando el usuario envía un mensaje saliente, el proveedor de almacenamiento de mensajes combinado y el proveedor de transporte pueden enviarlo directamente. Los proveedores de servicios combinados no tienen que notificar primero a la cola MAPI que hay un nuevo mensaje para procesar y, a continuación, esperar a que la cola MAPI inicie el proceso de transferencia del mensaje desde el proveedor de almacén de mensajes al proveedor de transporte. Esto tiene ventajas específicas cuando se usa un almacén de mensajes basado en servidor al minimizar el tráfico de red entre el equipo del usuario y el servidor.
  
En general, no hay procedimientos bien especificados para acoplar los proveedores de servicios con precisión. Sin embargo, debe seguir estas instrucciones:
  
- Si el motivo de acoplamiento estricto de los proveedores de servicios es el rendimiento, tenga en cuenta que el acoplamiento toma partes del subsistema MAPI de los procesos de los que normalmente participarían estas partes. Esto implica que las partes individuales del proveedor de servicios combinados deben interactuar entre sí de una manera que simule la interacción que tendrían normalmente con las partes del subsistema MAPI que no se usan.
    
- Cuando los proveedores de servicios muy acoplados interactúan con otros componentes MAPI, deben seguir interactuando con ellos exactamente de la forma en que lo harían si no estuvieran acoplados estrechamente. Por ejemplo, si un usuario usa un proveedor de almacenamiento de mensajes combinado y un proveedor de transporte como almacén de mensajes predeterminado, pero usa un proveedor de transporte independiente para enviar mensajes, como pueden ocurrir cuando un usuario toma un equipo en movimiento y cambia a un PR de transporte remoto ovider: la parte del almacén de mensajes del proveedor de servicios muy acoplado debe seguir interactuando con la cola MAPI como si fuera un proveedor independiente de almacén de mensajes.
    
## <a name="see-also"></a>Vea también



[Desarrollar un proveedor de almacén de mensajes MAPI](developing-a-mapi-message-store-provider.md)

