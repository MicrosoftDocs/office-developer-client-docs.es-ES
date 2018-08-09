---
title: Identificadores de entrada a largo plazo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 589420db48edb348a22f34ce72b948f4d8207ae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818043"
---
# <a name="long-term-entry-identifiers"></a><span data-ttu-id="039e9-103">Identificadores de entrada a largo plazo</span><span class="sxs-lookup"><span data-stu-id="039e9-103">Long-Term Entry Identifiers</span></span>

  
  
<span data-ttu-id="039e9-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="039e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="039e9-105">Cuando un objeto requiere un identificador con una duración de tiempo prolongado, se asigna un identificador de entrada a largo plazo por un proveedor de servicios a un objeto.</span><span class="sxs-lookup"><span data-stu-id="039e9-105">A long-term entry identifier is assigned by a service provider to an object when an object requires an identifier with a prolonged lifespan.</span></span> <span data-ttu-id="039e9-106">Los identificadores de entrada a largo plazo siempre son válidos para semanas o meses y pueden ser válidos en otras estaciones de trabajo, según el proveedor.</span><span class="sxs-lookup"><span data-stu-id="039e9-106">Long-term entry identifiers are always valid for weeks or months and can be valid on other workstations, depending on the provider.</span></span> <span data-ttu-id="039e9-107">Los identificadores a largo plazo creados por los proveedores de la libreta de direcciones para los destinatarios personalizados son válidos todo el mundo.</span><span class="sxs-lookup"><span data-stu-id="039e9-107">The long-term identifiers created by address book providers for custom recipients are universally valid.</span></span> 
  
<span data-ttu-id="039e9-108">Los identificadores de entrada a largo plazo se asignan a los almacenes de mensajes, carpetas, mensajes, contenedores de la libreta de direcciones, mensajería a los usuarios y distribución listas.</span><span class="sxs-lookup"><span data-stu-id="039e9-108">Long-term entry identifiers are assigned to message stores, folders, messages, address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="039e9-109">Cuando las aplicaciones cliente de llaman al método [IMAPIProp::GetProps](imapiprop-getprops.md) de estos objetos, siempre es un identificador de entrada a largo plazo que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="039e9-109">When client applications call the [IMAPIProp::GetProps](imapiprop-getprops.md) method of these objects, it is always a long-term entry identifier that is returned.</span></span> 
  
<span data-ttu-id="039e9-110">Los identificadores de entrada a largo plazo deben ser únicos en todos los almacenes de mensajes en el perfil activo; por lo tanto, cuando un mensaje o una carpeta se copia desde el almacén de mensajes de uno a otro, se debe asignar un nuevo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="039e9-110">Long-term entry identifiers must be unique across all message stores in the active profile; therefore, when a message or folder is copied from one message store to another, it must be assigned a new entry identifier.</span></span> <span data-ttu-id="039e9-111">Cuando se mueve un objeto de almacén de mensajes, el proveedor de almacén de mensajes que implementa el movimiento determina si el identificador de entrada original seguirá siendo válido.</span><span class="sxs-lookup"><span data-stu-id="039e9-111">When a message store object is moved, the message store provider that implements the move determines whether the original entry identifier will remain valid.</span></span> <span data-ttu-id="039e9-112">Algunos proveedores de servicios de asignan los identificadores de entrada nueva a los objetos que se ha movido; otros no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="039e9-112">Some service providers assign new entry identifiers to moved objects; others do not.</span></span> <span data-ttu-id="039e9-113">Si se produce un cambio, el nuevo identificador de entrada se incluirá en la información que se pasan a los clientes cuando reciben notificaciones del movimiento.</span><span class="sxs-lookup"><span data-stu-id="039e9-113">If there is a change, the new entry identifier will be included in the information passed to clients when they are notified of the move.</span></span> 
  
<span data-ttu-id="039e9-114">Normalmente, los proveedores de almacén de mensajes implementan el siguiente comportamiento cuando se mueven las carpetas:</span><span class="sxs-lookup"><span data-stu-id="039e9-114">Typically, message store providers implement the following behavior when they move folders:</span></span>
  
- <span data-ttu-id="039e9-115">Cuando se mueve una carpeta desde el almacén de mensajes de uno a otro almacén de un tipo diferente, se garantiza que el identificador de entrada cambia.</span><span class="sxs-lookup"><span data-stu-id="039e9-115">When a folder is moved from one message store to another store of a different type, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="039e9-116">Cuando se mueve una carpeta desde el almacén de mensajes de uno a otro almacén del mismo tipo, casi siempre se cambia el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="039e9-116">When a folder is moved from one message store to another store of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="039e9-117">Cuando se mueve una carpeta a otra ubicación dentro del mismo almacén de mensajes, el identificador de entrada puede o no puede cambiar, según el proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="039e9-117">When a folder is moved to another location within the same message store, the entry identifier might or might not change, depending on the message store provider.</span></span>
    
<span data-ttu-id="039e9-118">Cambio de nombre de una carpeta sin cambiar su carpeta principal normalmente no hace que el identificador de entrada cambiar.</span><span class="sxs-lookup"><span data-stu-id="039e9-118">Renaming a folder without changing its parent folder usually does not cause the entry identifier to change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="039e9-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="039e9-119">See also</span></span>



[<span data-ttu-id="039e9-120">Identificadores de entrada MAPI</span><span class="sxs-lookup"><span data-stu-id="039e9-120">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

