---
title: Long-Term identificadores de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b65656992681618aa8a1c53217bdd7101bc2502b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409226"
---
# <a name="long-term-entry-identifiers"></a><span data-ttu-id="51828-103">Long-Term identificadores de entrada</span><span class="sxs-lookup"><span data-stu-id="51828-103">Long-Term Entry Identifiers</span></span>

  
  
<span data-ttu-id="51828-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51828-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51828-105">Un proveedor de servicios asigna un identificador de entrada a largo plazo a un objeto cuando un objeto requiere un identificador con una vida útil prolongada.</span><span class="sxs-lookup"><span data-stu-id="51828-105">A long-term entry identifier is assigned by a service provider to an object when an object requires an identifier with a prolonged lifespan.</span></span> <span data-ttu-id="51828-106">Los identificadores de entrada a largo plazo siempre son válidos durante semanas o meses y pueden ser válidos en otras estaciones de trabajo, según el proveedor.</span><span class="sxs-lookup"><span data-stu-id="51828-106">Long-term entry identifiers are always valid for weeks or months and can be valid on other workstations, depending on the provider.</span></span> <span data-ttu-id="51828-107">Los identificadores a largo plazo creados por proveedores de libretas de direcciones para destinatarios personalizados son universalmente válidos.</span><span class="sxs-lookup"><span data-stu-id="51828-107">The long-term identifiers created by address book providers for custom recipients are universally valid.</span></span> 
  
<span data-ttu-id="51828-108">Los identificadores de entrada a largo plazo se asignan a almacenes de mensajes, carpetas, mensajes, contenedores de libretas de direcciones, usuarios de mensajería y listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="51828-108">Long-term entry identifiers are assigned to message stores, folders, messages, address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="51828-109">Cuando las aplicaciones cliente llaman al método [IMAPIProp::GetProps](imapiprop-getprops.md) de estos objetos, siempre se devuelve un identificador de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="51828-109">When client applications call the [IMAPIProp::GetProps](imapiprop-getprops.md) method of these objects, it is always a long-term entry identifier that is returned.</span></span> 
  
<span data-ttu-id="51828-110">Los identificadores de entrada a largo plazo deben ser únicos en todos los almacenes de mensajes del perfil activo; por lo tanto, cuando se copia un mensaje o carpeta de un almacén de mensajes a otro, se le debe asignar un nuevo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="51828-110">Long-term entry identifiers must be unique across all message stores in the active profile; therefore, when a message or folder is copied from one message store to another, it must be assigned a new entry identifier.</span></span> <span data-ttu-id="51828-111">Cuando se mueve un objeto de almacén de mensajes, el proveedor de almacenamiento de mensajes que implementa el movimiento determina si el identificador de entrada original seguirá siendo válido.</span><span class="sxs-lookup"><span data-stu-id="51828-111">When a message store object is moved, the message store provider that implements the move determines whether the original entry identifier will remain valid.</span></span> <span data-ttu-id="51828-112">Algunos proveedores de servicios asignan nuevos identificadores de entrada a objetos movidos; otros no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="51828-112">Some service providers assign new entry identifiers to moved objects; others do not.</span></span> <span data-ttu-id="51828-113">Si hay un cambio, el nuevo identificador de entrada se incluirá en la información que se pasa a los clientes cuando se les notifica el movimiento.</span><span class="sxs-lookup"><span data-stu-id="51828-113">If there is a change, the new entry identifier will be included in the information passed to clients when they are notified of the move.</span></span> 
  
<span data-ttu-id="51828-114">Normalmente, los proveedores de almacenamiento de mensajes implementan el siguiente comportamiento al mover carpetas:</span><span class="sxs-lookup"><span data-stu-id="51828-114">Typically, message store providers implement the following behavior when they move folders:</span></span>
  
- <span data-ttu-id="51828-115">Cuando se mueve una carpeta de un almacén de mensajes a otro almacén de otro tipo, se garantiza que el identificador de entrada cambie.</span><span class="sxs-lookup"><span data-stu-id="51828-115">When a folder is moved from one message store to another store of a different type, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="51828-116">Cuando se mueve una carpeta de un almacén de mensajes a otro almacén del mismo tipo, el identificador de entrada casi siempre cambia.</span><span class="sxs-lookup"><span data-stu-id="51828-116">When a folder is moved from one message store to another store of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="51828-117">Cuando se mueve una carpeta a otra ubicación dentro del mismo almacén de mensajes, el identificador de entrada puede cambiar o no, según el proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="51828-117">When a folder is moved to another location within the same message store, the entry identifier might or might not change, depending on the message store provider.</span></span>
    
<span data-ttu-id="51828-118">Cambiar el nombre de una carpeta sin cambiar su carpeta principal normalmente no hace que cambie el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="51828-118">Renaming a folder without changing its parent folder usually does not cause the entry identifier to change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="51828-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="51828-119">See also</span></span>



[<span data-ttu-id="51828-120">Identificadores de entrada MAPI</span><span class="sxs-lookup"><span data-stu-id="51828-120">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

