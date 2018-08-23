---
title: Copiar las propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 556ea9faedf0d9a02b0cff1bb2f1750289cc4d1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565084"
---
# <a name="copying-mapi-properties"></a><span data-ttu-id="015e2-103">Copiar las propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="015e2-103">Copying MAPI Properties</span></span>

  
  
<span data-ttu-id="015e2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="015e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="015e2-105">Los clientes y proveedores de servicios pueden copiar una o varias de las propiedades de un objeto con los siguientes métodos de **IMAPIProp** y funciones de la API:</span><span class="sxs-lookup"><span data-stu-id="015e2-105">Clients and service providers can copy one or more of an object's properties with the following **IMAPIProp** methods and API functions:</span></span> 
  
- <span data-ttu-id="015e2-106">El método [IMAPIProp::CopyTo](imapiprop-copyto.md) copia todas las propiedades de un objeto a otro objeto, y, opcionalmente, excluyendo las propiedades seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="015e2-106">The [IMAPIProp::CopyTo](imapiprop-copyto.md) method copies all of an object's properties to another object, optionally excluding selected properties.</span></span> <span data-ttu-id="015e2-107">**CopyTo** se usa para copiar o mover cualquier tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="015e2-107">**CopyTo** is used for copying or moving any type of object.</span></span> 
    
- <span data-ttu-id="015e2-108">El método [IMAPIProp::CopyProps](imapiprop-copyprops.md) copia las propiedades seleccionadas de un objeto.</span><span class="sxs-lookup"><span data-stu-id="015e2-108">The [IMAPIProp::CopyProps](imapiprop-copyprops.md) method copies selected properties of an object.</span></span> <span data-ttu-id="015e2-109">**CopyProps** se usa principalmente con los mensajes.</span><span class="sxs-lookup"><span data-stu-id="015e2-109">**CopyProps** is used mainly with messages.</span></span> <span data-ttu-id="015e2-110">Cuando un cliente crea una copia de un mensaje o una respuesta, reenvío controladores **CopyProps** copiar las propiedades adecuadas del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="015e2-110">When a client creates a forwarded copy of a message or a reply, **CopyProps** handles copying the appropriate properties from the original message.</span></span> 
    
- <span data-ttu-id="015e2-111">La función [PropCopyMore](propcopymore.md) copia un valor de propiedad único de una ubicación a otra.</span><span class="sxs-lookup"><span data-stu-id="015e2-111">The [PropCopyMore](propcopymore.md) function copies a single property value from one location to another.</span></span> <span data-ttu-id="015e2-112">Utilice **PropCopyMore** con precaución.</span><span class="sxs-lookup"><span data-stu-id="015e2-112">Use **PropCopyMore** with caution.</span></span> <span data-ttu-id="015e2-113">Es posible, al copiar un valor en un momento: para asignar muchos bloques pequeños de memoria y hacer que la memoria a fragmentar.</span><span class="sxs-lookup"><span data-stu-id="015e2-113">It is possible — when copying one value at a time — to allocate many small blocks of memory and cause memory to fragment.</span></span> 
    
- <span data-ttu-id="015e2-114">La función [ScCopyProps](sccopyprops.md) copia valores de propiedad de forma masiva.</span><span class="sxs-lookup"><span data-stu-id="015e2-114">The [ScCopyProps](sccopyprops.md) function copies property values in bulk.</span></span> <span data-ttu-id="015e2-115">**ScCopyProps** puede copiar los valores de propiedad que se han generado desde disjuntos bloques de memoria.</span><span class="sxs-lookup"><span data-stu-id="015e2-115">**ScCopyProps** can copy property values that have been built from disjointed blocks of memory.</span></span> <span data-ttu-id="015e2-116">Devuelve una matriz de propiedad nuevo.</span><span class="sxs-lookup"><span data-stu-id="015e2-116">It returns a new property array.</span></span> 
    
- <span data-ttu-id="015e2-117">Si la matriz de propiedad devuelta por **ScCopyProps** es se almacenen en el disco, utilice la función [ScRelocProps](screlocprops.md) para ajustar los punteros.</span><span class="sxs-lookup"><span data-stu-id="015e2-117">If the property array returned by **ScCopyProps** is to be stored on disk, use the [ScRelocProps](screlocprops.md) function to adjust the pointers.</span></span> <span data-ttu-id="015e2-118">**ScRelocProps** debe llamarse dos veces; una vez para ajustar las direcciones antes de escribir la operación de datos y, a continuación, vuelva a durante la operación de lectura.</span><span class="sxs-lookup"><span data-stu-id="015e2-118">**ScRelocProps** should be called twice; once to adjust the addresses before writing the data operation and then again during the read operation.</span></span> <span data-ttu-id="015e2-119">La función **ScRelocProps** se supone que la matriz de valores de propiedad se ha asignado originalmente en una única asignación.</span><span class="sxs-lookup"><span data-stu-id="015e2-119">The **ScRelocProps** function assumes that the property value array was originally allocated in a single allocation.</span></span> 
    
<span data-ttu-id="015e2-120">Las funciones de la API que se describen en las propiedades de copia de lista anterior en la memoria, en lugar de un objeto a otro objeto.</span><span class="sxs-lookup"><span data-stu-id="015e2-120">The API functions described in the preceding list copy properties in memory rather than from one object to another object.</span></span> <span data-ttu-id="015e2-121">Estas funciones se admiten actualmente, pero es posible que no se admite en una futura versión.</span><span class="sxs-lookup"><span data-stu-id="015e2-121">These functions are presently supported, but might not be supported in a future release.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="015e2-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="015e2-122">See also</span></span>



[<span data-ttu-id="015e2-123">Información general sobre MAPI (propiedad)</span><span class="sxs-lookup"><span data-stu-id="015e2-123">MAPI Property Overview</span></span>](mapi-property-overview.md)

