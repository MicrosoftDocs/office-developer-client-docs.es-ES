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
ms.openlocfilehash: b1aa0228cdc8cf6f0b2bb321e62e40127775a6de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820797"
---
# <a name="supporting-named-properties-in-message-stores"></a><span data-ttu-id="fe834-103">Admitir propiedades con nombre en los almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="fe834-103">Supporting Named Properties in Message Stores</span></span>

  
  
<span data-ttu-id="fe834-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe834-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe834-p101">Message objects can have properties in them that are not in the set of properties defined by MAPI. Such properties can be unnamed or named. Unnamed properties must reside in a range of property identifiers defined by MAPI. Named custom properties reside in a different range of property identifiers defined by MAPI. They are typically used by custom message types. Your message store provider must support named properties if it is to be used as the default message store. Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers. For more information, see [Definir nuevas propiedades MAPI](defining-new-mapi-properties.md) and [Compatibilidad con las propiedades con nombre](supporting-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="fe834-p101">Message objects can have properties in them that are not in the set of properties defined by MAPI. Such properties can be unnamed or named. Unnamed properties must reside in a range of property identifiers defined by MAPI. Named custom properties reside in a different range of property identifiers defined by MAPI. They are typically used by custom message types. Your message store provider must support named properties if it is to be used as the default message store. Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers. For more information, see [Defining New MAPI Properties](defining-new-mapi-properties.md) and [Supporting Named Properties](supporting-named-properties.md).</span></span>
  
<span data-ttu-id="fe834-p102">Mensaje la mayor�a de los proveedores que admiten denominados uso una firma �nica asignaci�n de propiedades para todos los objetos en el almac�n de mensajes de almac�n. Esto tiene dos ventajas. En primer lugar, es m�s f�cil implementar firmas de asignaci�n si no hay una sola para realizar un seguimiento de. En segundo lugar, si todos los objetos en el almac�n de mensajes usa la misma firma de asignaci�n, las aplicaciones cliente se asegura de que todos los identificadores de propiedad en los mensajes en el almac�n de mensajes hagan referencia a la misma propiedad con nombre. Esto permite que las aplicaciones de cliente mostrar las columnas de propiedades con nombre en la interfaz de la vista de carpeta.</span><span class="sxs-lookup"><span data-stu-id="fe834-p102">Most message store providers that support named properties use a single mapping signature for all objects in the message store. This has two benefits. First, it is simpler to implement mapping signatures if there is only one to keep track of. Second, if all objects in the message store use the same mapping signature, client applications are assured that all property identifiers on messages in the message store actually refer to the same named property. This enables client applications to display columns for named properties in their folder view interface.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fe834-118">Vea tambi�n</span><span class="sxs-lookup"><span data-stu-id="fe834-118">See also</span></span>



[<span data-ttu-id="fe834-119">Implementaci�n de los mensajes en los almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="fe834-119">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

