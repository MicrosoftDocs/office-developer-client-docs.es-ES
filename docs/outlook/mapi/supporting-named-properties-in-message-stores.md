---
title: Admitir propiedades con nombre en los almacenes de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1c73bb5-b44a-4ec6-89e4-0e2228572b2d
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 7e33c49d1ed211abf70e04a8bd3c06ca62e88572
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434924"
---
# <a name="supporting-named-properties-in-message-stores"></a>Admitir propiedades con nombre en los almacenes de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Message objects can have properties in them that are not in the set of properties defined by MAPI. Such properties can be unnamed or named. Unnamed properties must reside in a range of property identifiers defined by MAPI. Named custom properties reside in a different range of property identifiers defined by MAPI. They are typically used by custom message types. Your message store provider must support named properties if it is to be used as the default message store. Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers. For more information, see [Definir nuevas propiedades MAPI](defining-new-mapi-properties.md) and [Compatibilidad con las propiedades con nombre](supporting-named-properties.md).
  
Mensaje la mayor�a de los proveedores que admiten denominados uso una firma �nica asignaci�n de propiedades para todos los objetos en el almac�n de mensajes de almac�n. Esto tiene dos ventajas. En primer lugar, es m�s f�cil implementar firmas de asignaci�n si no hay una sola para realizar un seguimiento de. En segundo lugar, si todos los objetos en el almac�n de mensajes usa la misma firma de asignaci�n, las aplicaciones cliente se asegura de que todos los identificadores de propiedad en los mensajes en el almac�n de mensajes hagan referencia a la misma propiedad con nombre. Esto permite que las aplicaciones de cliente mostrar las columnas de propiedades con nombre en la interfaz de la vista de carpeta.
  
## <a name="see-also"></a>Vea también



[Implementar mensajes en los almacenes de mensajes](implementing-messages-in-message-stores.md)

