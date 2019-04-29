---
title: Copia de las propiedades MAPI
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
# <a name="copying-mapi-properties"></a><span data-ttu-id="a74f5-103">Copia de las propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a74f5-103">Copying MAPI Properties</span></span>

  
  
<span data-ttu-id="a74f5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a74f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a74f5-105">Los clientes y los proveedores de servicios pueden copiar una o varias de las propiedades de un objeto con los siguientes métodos de **IMAPIProp** y funciones API:</span><span class="sxs-lookup"><span data-stu-id="a74f5-105">Clients and service providers can copy one or more of an object's properties with the following **IMAPIProp** methods and API functions:</span></span> 
  
- <span data-ttu-id="a74f5-106">El método [IMAPIProp:: CopyTo](imapiprop-copyto.md) copia todas las propiedades de un objeto en otro objeto, opcionalmente excluyendo las propiedades seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="a74f5-106">The [IMAPIProp::CopyTo](imapiprop-copyto.md) method copies all of an object's properties to another object, optionally excluding selected properties.</span></span> <span data-ttu-id="a74f5-107">**CopyTo** se usa para copiar o mover cualquier tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="a74f5-107">**CopyTo** is used for copying or moving any type of object.</span></span> 
    
- <span data-ttu-id="a74f5-108">El método [IMAPIProp:: CopyProps](imapiprop-copyprops.md) copia las propiedades seleccionadas de un objeto.</span><span class="sxs-lookup"><span data-stu-id="a74f5-108">The [IMAPIProp::CopyProps](imapiprop-copyprops.md) method copies selected properties of an object.</span></span> <span data-ttu-id="a74f5-109">**CopyProps** se usa principalmente con mensajes.</span><span class="sxs-lookup"><span data-stu-id="a74f5-109">**CopyProps** is used mainly with messages.</span></span> <span data-ttu-id="a74f5-110">Cuando un cliente crea una copia reenviada de un mensaje o una respuesta, **CopyProps** controla la copia de las propiedades adecuadas del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="a74f5-110">When a client creates a forwarded copy of a message or a reply, **CopyProps** handles copying the appropriate properties from the original message.</span></span> 
    
- <span data-ttu-id="a74f5-111">La función [PropCopyMore](propcopymore.md) copia un único valor de propiedad de una ubicación a otra.</span><span class="sxs-lookup"><span data-stu-id="a74f5-111">The [PropCopyMore](propcopymore.md) function copies a single property value from one location to another.</span></span> <span data-ttu-id="a74f5-112">Use **PropCopyMore** con cuidado.</span><span class="sxs-lookup"><span data-stu-id="a74f5-112">Use **PropCopyMore** with caution.</span></span> <span data-ttu-id="a74f5-113">Es posible, cuando se copia un valor cada vez, para asignar muchos bloques de memoria pequeños y hacer que la memoria se fragmente.</span><span class="sxs-lookup"><span data-stu-id="a74f5-113">It is possible — when copying one value at a time — to allocate many small blocks of memory and cause memory to fragment.</span></span> 
    
- <span data-ttu-id="a74f5-114">La función [ScCopyProps](sccopyprops.md) copia los valores de propiedad en masa.</span><span class="sxs-lookup"><span data-stu-id="a74f5-114">The [ScCopyProps](sccopyprops.md) function copies property values in bulk.</span></span> <span data-ttu-id="a74f5-115">**ScCopyProps** puede copiar los valores de propiedad que se han generado desde bloques de memoria inconexos.</span><span class="sxs-lookup"><span data-stu-id="a74f5-115">**ScCopyProps** can copy property values that have been built from disjointed blocks of memory.</span></span> <span data-ttu-id="a74f5-116">Devuelve una nueva matriz de propiedades.</span><span class="sxs-lookup"><span data-stu-id="a74f5-116">It returns a new property array.</span></span> 
    
- <span data-ttu-id="a74f5-117">Si la matriz de propiedades devuelta por **ScCopyProps** se va a almacenar en el disco, use la función [ScRelocProps](screlocprops.md) para ajustar los punteros.</span><span class="sxs-lookup"><span data-stu-id="a74f5-117">If the property array returned by **ScCopyProps** is to be stored on disk, use the [ScRelocProps](screlocprops.md) function to adjust the pointers.</span></span> <span data-ttu-id="a74f5-118">Se debe llamar dos veces a **ScRelocProps** ; una vez para ajustar las direcciones antes de escribir la operación de datos y de nuevo durante la operación de lectura.</span><span class="sxs-lookup"><span data-stu-id="a74f5-118">**ScRelocProps** should be called twice; once to adjust the addresses before writing the data operation and then again during the read operation.</span></span> <span data-ttu-id="a74f5-119">La función **ScRelocProps** presupone que la matriz de valores de propiedad se asignó originalmente en una única asignación.</span><span class="sxs-lookup"><span data-stu-id="a74f5-119">The **ScRelocProps** function assumes that the property value array was originally allocated in a single allocation.</span></span> 
    
<span data-ttu-id="a74f5-120">Las funciones de la API descritas en la lista anterior copian las propiedades de la memoria en lugar de hacerlo de un objeto a otro objeto.</span><span class="sxs-lookup"><span data-stu-id="a74f5-120">The API functions described in the preceding list copy properties in memory rather than from one object to another object.</span></span> <span data-ttu-id="a74f5-121">Actualmente, estas funciones se admiten, pero es posible que no se admitan en una versión futura.</span><span class="sxs-lookup"><span data-stu-id="a74f5-121">These functions are presently supported, but might not be supported in a future release.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a74f5-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a74f5-122">See also</span></span>



[<span data-ttu-id="a74f5-123">Información general sobre MAPI (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a74f5-123">MAPI Property Overview</span></span>](mapi-property-overview.md)

