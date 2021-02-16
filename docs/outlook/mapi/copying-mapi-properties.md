---
title: Copiar propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ae8e553cf2e19ae1ba06ca09aad84eae9f7d1238
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415050"
---
# <a name="copying-mapi-properties"></a><span data-ttu-id="3f373-103">Copiar propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3f373-103">Copying MAPI Properties</span></span>

  
  
<span data-ttu-id="3f373-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f373-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f373-105">Los clientes y proveedores de servicios pueden copiar una o varias de las propiedades de un objeto con los siguientes métodos **IMAPIProp** y funciones api:</span><span class="sxs-lookup"><span data-stu-id="3f373-105">Clients and service providers can copy one or more of an object's properties with the following **IMAPIProp** methods and API functions:</span></span> 
  
- <span data-ttu-id="3f373-106">El [método IMAPIProp::CopyTo](imapiprop-copyto.md) copia todas las propiedades de un objeto en otro objeto, excluyendo opcionalmente las propiedades seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="3f373-106">The [IMAPIProp::CopyTo](imapiprop-copyto.md) method copies all of an object's properties to another object, optionally excluding selected properties.</span></span> <span data-ttu-id="3f373-107">**CopyTo** se usa para copiar o mover cualquier tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="3f373-107">**CopyTo** is used for copying or moving any type of object.</span></span> 
    
- <span data-ttu-id="3f373-108">El [método IMAPIProp::CopyProps](imapiprop-copyprops.md) copia las propiedades seleccionadas de un objeto.</span><span class="sxs-lookup"><span data-stu-id="3f373-108">The [IMAPIProp::CopyProps](imapiprop-copyprops.md) method copies selected properties of an object.</span></span> <span data-ttu-id="3f373-109">**CopyProps se** usa principalmente con mensajes.</span><span class="sxs-lookup"><span data-stu-id="3f373-109">**CopyProps** is used mainly with messages.</span></span> <span data-ttu-id="3f373-110">Cuando un cliente crea una copia reenviada de un mensaje o una respuesta, **CopyProps** controla la copia de las propiedades apropiadas del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="3f373-110">When a client creates a forwarded copy of a message or a reply, **CopyProps** handles copying the appropriate properties from the original message.</span></span> 
    
- <span data-ttu-id="3f373-111">La [función PropCopyMore](propcopymore.md) copia un único valor de propiedad de una ubicación a otra.</span><span class="sxs-lookup"><span data-stu-id="3f373-111">The [PropCopyMore](propcopymore.md) function copies a single property value from one location to another.</span></span> <span data-ttu-id="3f373-112">Use **PropCopyMore** con precaución.</span><span class="sxs-lookup"><span data-stu-id="3f373-112">Use **PropCopyMore** with caution.</span></span> <span data-ttu-id="3f373-113">Es posible, al copiar un valor cada vez, asignar muchos bloques pequeños de memoria y hacer que la memoria se fragmente.</span><span class="sxs-lookup"><span data-stu-id="3f373-113">It is possible — when copying one value at a time — to allocate many small blocks of memory and cause memory to fragment.</span></span> 
    
- <span data-ttu-id="3f373-114">La [función ScCopyProps](sccopyprops.md) copia los valores de propiedad de forma masiva.</span><span class="sxs-lookup"><span data-stu-id="3f373-114">The [ScCopyProps](sccopyprops.md) function copies property values in bulk.</span></span> <span data-ttu-id="3f373-115">**ScCopyProps puede** copiar valores de propiedad creados a partir de bloques de memoria diferentes.</span><span class="sxs-lookup"><span data-stu-id="3f373-115">**ScCopyProps** can copy property values that have been built from disjointed blocks of memory.</span></span> <span data-ttu-id="3f373-116">Devuelve una nueva matriz de propiedades.</span><span class="sxs-lookup"><span data-stu-id="3f373-116">It returns a new property array.</span></span> 
    
- <span data-ttu-id="3f373-117">Si la matriz de propiedades devuelta por **ScCopyProps** se va a almacenar en el disco, use la función [ScRelocProps](screlocprops.md) para ajustar los punteros.</span><span class="sxs-lookup"><span data-stu-id="3f373-117">If the property array returned by **ScCopyProps** is to be stored on disk, use the [ScRelocProps](screlocprops.md) function to adjust the pointers.</span></span> <span data-ttu-id="3f373-118">Se debe llamar dos veces a **ScRelocProps;** una vez para ajustar las direcciones antes de escribir la operación de datos y, a continuación, otra vez durante la operación de lectura.</span><span class="sxs-lookup"><span data-stu-id="3f373-118">**ScRelocProps** should be called twice; once to adjust the addresses before writing the data operation and then again during the read operation.</span></span> <span data-ttu-id="3f373-119">La **función ScRelocProps** supone que la matriz de valores de propiedad se asignó originalmente en una única asignación.</span><span class="sxs-lookup"><span data-stu-id="3f373-119">The **ScRelocProps** function assumes that the property value array was originally allocated in a single allocation.</span></span> 
    
<span data-ttu-id="3f373-120">Las funciones api descritas en la lista anterior copian propiedades en la memoria en lugar de desde un objeto a otro.</span><span class="sxs-lookup"><span data-stu-id="3f373-120">The API functions described in the preceding list copy properties in memory rather than from one object to another object.</span></span> <span data-ttu-id="3f373-121">Actualmente, estas funciones se admiten, pero es posible que no se puedan usar en una versión futura.</span><span class="sxs-lookup"><span data-stu-id="3f373-121">These functions are presently supported, but might not be supported in a future release.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3f373-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f373-122">See also</span></span>



[<span data-ttu-id="3f373-123">Información general sobre MAPI (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3f373-123">MAPI Property Overview</span></span>](mapi-property-overview.md)

