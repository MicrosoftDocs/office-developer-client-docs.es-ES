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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421091"
---
# <a name="screlocprops"></a><span data-ttu-id="1ca6a-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="1ca6a-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="1ca6a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ca6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ca6a-105">Ajusta los punteros de una matriz [SPropValue](spropvalue.md) después de que la matriz y sus datos se hayan copiado o movido a una nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="1ca6a-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ca6a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1ca6a-106">Header file:</span></span>  <br/> |<span data-ttu-id="1ca6a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ca6a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1ca6a-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="1ca6a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1ca6a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1ca6a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1ca6a-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="1ca6a-110">Called by:</span></span>  <br/> |<span data-ttu-id="1ca6a-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="1ca6a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="1ca6a-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ca6a-112">Parameters</span></span>

 <span data-ttu-id="1ca6a-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="1ca6a-113">_cprop_</span></span>
  
> <span data-ttu-id="1ca6a-114">[entrada] Número de propiedades de la matriz a las que apunta el _parámetro rgprop._</span><span class="sxs-lookup"><span data-stu-id="1ca6a-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="1ca6a-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="1ca6a-115">_rgprop_</span></span>
  
> <span data-ttu-id="1ca6a-116">[entrada] Puntero a una matriz de [estructuras SPropValue](spropvalue.md) para las que se van a ajustar los punteros.</span><span class="sxs-lookup"><span data-stu-id="1ca6a-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="1ca6a-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="1ca6a-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="1ca6a-118">[entrada] Puntero a la dirección base original de la matriz a la que apunta el _parámetro rgprop._</span><span class="sxs-lookup"><span data-stu-id="1ca6a-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="1ca6a-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="1ca6a-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="1ca6a-120">[entrada] Puntero a la nueva dirección base de la matriz a la que apunta el _parámetro rgprop._</span><span class="sxs-lookup"><span data-stu-id="1ca6a-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="1ca6a-121">_indeste_</span><span class="sxs-lookup"><span data-stu-id="1ca6a-121">_pcb_</span></span>
  
> <span data-ttu-id="1ca6a-122">[entrada, salida] Puntero opcional al tamaño, en bytes, de la matriz indicada por el _parámetro pvBaseNew._</span><span class="sxs-lookup"><span data-stu-id="1ca6a-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="1ca6a-123">Si no es NULL, el parámetro _byte_ se establece en el número de bytes almacenados en el _parámetro pvD._</span><span class="sxs-lookup"><span data-stu-id="1ca6a-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1ca6a-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ca6a-124">Return value</span></span>

<span data-ttu-id="1ca6a-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ca6a-125">S_OK</span></span>
  
> <span data-ttu-id="1ca6a-126">Los punteros se ajustaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="1ca6a-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="1ca6a-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1ca6a-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="1ca6a-128">Uno o ambos parámetros no eran válidos o se encontró un tipo de propiedad desconocido.</span><span class="sxs-lookup"><span data-stu-id="1ca6a-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ca6a-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ca6a-129">Remarks</span></span>

<span data-ttu-id="1ca6a-130">La función **ScRelocProps** funciona presupuestando que la matriz de valores de propiedad para la que se ajustan los punteros se asignó originalmente en una sola llamada similar a una llamada a la función **ScCopyProps.**</span><span class="sxs-lookup"><span data-stu-id="1ca6a-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="1ca6a-131">Si una aplicación cliente o un proveedor de servicios está trabajando con un valor de propiedad creado a partir de bloques de memoria diferentes, debe usar [ScCopyProps](sccopyprops.md) para copiar propiedades en su lugar.</span><span class="sxs-lookup"><span data-stu-id="1ca6a-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="1ca6a-132">**ScRelocProps se** usa para mantener la validez de los punteros en una matriz [SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="1ca6a-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="1ca6a-133">Para mantener la validez de los punteros al escribir y leer una matriz de este tipo en un disco, realice las siguientes operaciones:</span><span class="sxs-lookup"><span data-stu-id="1ca6a-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="1ca6a-134">Antes de escribir la matriz y los datos en un disco, llame a **ScRelocProps** en la matriz con el parámetro  _pvBaseNew_ que señale a algún valor estándar cero, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1ca6a-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="1ca6a-135">Después de leer la matriz y los datos de un disco, llame a **ScRelocProps** en la matriz con el parámetro  _pvBaseOld_ igual al mismo valor estándar usado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="1ca6a-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="1ca6a-136">La matriz y los datos deben leerse en un búfer creado con una única asignación.</span><span class="sxs-lookup"><span data-stu-id="1ca6a-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="1ca6a-137">El  _parámetro de momento_ de **ScRelocProps** es opcional.</span><span class="sxs-lookup"><span data-stu-id="1ca6a-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1ca6a-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1ca6a-138">See also</span></span>



[<span data-ttu-id="1ca6a-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="1ca6a-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="1ca6a-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="1ca6a-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="1ca6a-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="1ca6a-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="1ca6a-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="1ca6a-142">ScRelocNotifications</span></span>](screlocnotifications.md)

