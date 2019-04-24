---
title: ScRelocProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocProps
api_type:
- COM
ms.assetid: 4aafb254-6074-4a7c-b915-d3d33304ac38
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c73fb96c9620a90ab0505b394fcb9853d02dcde5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360693"
---
# <a name="screlocprops"></a><span data-ttu-id="21d85-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="21d85-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="21d85-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21d85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21d85-105">Ajusta los punteros en una matriz [SPropValue](spropvalue.md) después de que la matriz y sus datos se hayan copiado o movido a una nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="21d85-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="21d85-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="21d85-106">Header file:</span></span>  <br/> |<span data-ttu-id="21d85-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="21d85-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="21d85-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="21d85-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="21d85-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="21d85-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="21d85-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="21d85-110">Called by:</span></span>  <br/> |<span data-ttu-id="21d85-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="21d85-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="21d85-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="21d85-112">Parameters</span></span>

 <span data-ttu-id="21d85-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="21d85-113">_cprop_</span></span>
  
> <span data-ttu-id="21d85-114">a Número de propiedades de la matriz señalada por el parámetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="21d85-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="21d85-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="21d85-115">_rgprop_</span></span>
  
> <span data-ttu-id="21d85-116">a Puntero a una matriz de estructuras [SPropValue](spropvalue.md) para las que se van a ajustar los punteros.</span><span class="sxs-lookup"><span data-stu-id="21d85-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="21d85-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="21d85-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="21d85-118">a Puntero a la dirección base original de la matriz señalada por el parámetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="21d85-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="21d85-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="21d85-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="21d85-120">a Puntero a la nueva dirección base de la matriz señalada por el parámetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="21d85-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="21d85-121">_impreso_</span><span class="sxs-lookup"><span data-stu-id="21d85-121">_pcb_</span></span>
  
> <span data-ttu-id="21d85-122">[in, out] Puntero opcional al tamaño, en bytes, de la matriz indicada por el parámetro _pvBaseNew_ .</span><span class="sxs-lookup"><span data-stu-id="21d85-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="21d85-123">Si no es NULL, el parámetro _PCB_ se establece en el número de bytes almacenados en el parámetro _pvD_ .</span><span class="sxs-lookup"><span data-stu-id="21d85-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="21d85-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21d85-124">Return value</span></span>

<span data-ttu-id="21d85-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="21d85-125">S_OK</span></span>
  
> <span data-ttu-id="21d85-126">Los punteros se ajustaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="21d85-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="21d85-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="21d85-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="21d85-128">Uno o ambos parámetros no son válidos o se encontró un tipo de propiedad desconocido.</span><span class="sxs-lookup"><span data-stu-id="21d85-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="21d85-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="21d85-129">Remarks</span></span>

<span data-ttu-id="21d85-130">La función **ScRelocProps** se supone por el hecho de que la matriz de valores de propiedad para la que se ajustan los punteros se asignó originalmente en una sola llamada similar a una llamada a la función **ScCopyProps** .</span><span class="sxs-lookup"><span data-stu-id="21d85-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="21d85-131">Si una aplicación cliente o un proveedor de servicios está trabajando con un valor de propiedad que se genera desde bloques de memoria inconexos, debe usar [ScCopyProps](sccopyprops.md) para copiar las propiedades en su lugar.</span><span class="sxs-lookup"><span data-stu-id="21d85-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="21d85-132">**ScRelocProps** se usa para mantener la validez de los punteros en una matriz [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="21d85-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="21d85-133">Para mantener la validez de los punteros al escribir dicha matriz en un disco y leerlo, realice las operaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="21d85-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="21d85-134">Antes de escribir la matriz y los datos en un disco, llame a **ScRelocProps** en la matriz con el parámetro _pvBaseNew_ que apunta a un valor cero estándar, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="21d85-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="21d85-135">Después de leer la matriz y los datos de un disco, llame a **ScRelocProps** en la matriz con el parámetro _pvBaseOld_ igual al mismo valor estándar usado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="21d85-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="21d85-136">La matriz y los datos deben leerse en un búfer creado con una única asignación.</span><span class="sxs-lookup"><span data-stu-id="21d85-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="21d85-137">El parámetro _PCB_ para **ScRelocProps** es opcional.</span><span class="sxs-lookup"><span data-stu-id="21d85-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="21d85-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="21d85-138">See also</span></span>



[<span data-ttu-id="21d85-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="21d85-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="21d85-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="21d85-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="21d85-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="21d85-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="21d85-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="21d85-142">ScRelocNotifications</span></span>](screlocnotifications.md)

