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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 06590fe55cb02b1abf036156877fd308548436f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820618"
---
# <a name="screlocprops"></a><span data-ttu-id="ed71b-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="ed71b-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="ed71b-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ed71b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ed71b-105">Ajusta los punteros en una matriz de [SPropValue](spropvalue.md) después de que se han copiado o movido a una nueva ubicación de la matriz y sus datos.</span><span class="sxs-lookup"><span data-stu-id="ed71b-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ed71b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ed71b-106">Header file:</span></span>  <br/> |<span data-ttu-id="ed71b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed71b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ed71b-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="ed71b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ed71b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ed71b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ed71b-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ed71b-110">Called by:</span></span>  <br/> |<span data-ttu-id="ed71b-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="ed71b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="ed71b-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed71b-112">Parameters</span></span>

 <span data-ttu-id="ed71b-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="ed71b-113">_cprop_</span></span>
  
> <span data-ttu-id="ed71b-114">[entrada] Recuento de propiedades de la matriz indicada por el parámetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="ed71b-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="ed71b-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="ed71b-115">_rgprop_</span></span>
  
> <span data-ttu-id="ed71b-116">[entrada] Puntero a una matriz de estructuras [SPropValue](spropvalue.md) para que los punteros son va a ajustar.</span><span class="sxs-lookup"><span data-stu-id="ed71b-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="ed71b-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="ed71b-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="ed71b-118">[entrada] Puntero a la dirección base original de la matriz indicada por el parámetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="ed71b-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="ed71b-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="ed71b-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="ed71b-120">[entrada] Puntero a la nueva dirección de base de la matriz indicada por el parámetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="ed71b-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="ed71b-121">_placa de circuitos impresos_</span><span class="sxs-lookup"><span data-stu-id="ed71b-121">_pcb_</span></span>
  
> <span data-ttu-id="ed71b-122">[entrada, salida] Puntero opcional para el tamaño, en bytes, de la matriz indicada por el parámetro _pvBaseNew_ .</span><span class="sxs-lookup"><span data-stu-id="ed71b-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="ed71b-123">Si no es NULL, el parámetro _pcb_ se establece en el número de bytes que se almacenan en el parámetro _pvD_ .</span><span class="sxs-lookup"><span data-stu-id="ed71b-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ed71b-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed71b-124">Return value</span></span>

<span data-ttu-id="ed71b-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="ed71b-125">S_OK</span></span>
  
> <span data-ttu-id="ed71b-126">Punteros se ajustaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="ed71b-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="ed71b-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ed71b-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="ed71b-128">Uno o ambos parámetros no son válidos, o se encontró un tipo de propiedad desconocido.</span><span class="sxs-lookup"><span data-stu-id="ed71b-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ed71b-129">Notas</span><span class="sxs-lookup"><span data-stu-id="ed71b-129">Remarks</span></span>

<span data-ttu-id="ed71b-130">La función **ScRelocProps** funciona en la suposición de que la matriz de valores de propiedad para la que se ajustan punteros se asignó originalmente en una sola llamada similar a una llamada a la función **ScCopyProps** .</span><span class="sxs-lookup"><span data-stu-id="ed71b-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="ed71b-131">Si una aplicación de cliente o un proveedor de servicios está trabajando con un valor de la propiedad que se genera a partir de disjuntos bloques de memoria, que debe usar [ScCopyProps](sccopyprops.md) para copiar las propiedades en su lugar.</span><span class="sxs-lookup"><span data-stu-id="ed71b-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="ed71b-132">**ScRelocProps** se utiliza para mantener la validez de punteros en una matriz de [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="ed71b-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="ed71b-133">Para mantener la validez de punteros cuando dicha matriz a escritura y lectura de un disco, realice las siguientes operaciones:</span><span class="sxs-lookup"><span data-stu-id="ed71b-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="ed71b-134">Antes de escribir la matriz y los datos en un disco, llame a **ScRelocProps** en la matriz con el parámetro _pvBaseNew_ apuntar a algún valor estándar cero, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ed71b-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="ed71b-135">Después de leer la matriz y los datos de un disco, llame a **ScRelocProps** en la matriz con el parámetro _pvBaseOld_ igual que el mismo valor estándar utilizado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="ed71b-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="ed71b-136">Deben leer la matriz y los datos en un búfer creado con una única asignación.</span><span class="sxs-lookup"><span data-stu-id="ed71b-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="ed71b-137">El parámetro _pcb_ **ScRelocProps** es opcional.</span><span class="sxs-lookup"><span data-stu-id="ed71b-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ed71b-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="ed71b-138">See also</span></span>



[<span data-ttu-id="ed71b-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="ed71b-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="ed71b-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="ed71b-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="ed71b-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="ed71b-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="ed71b-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="ed71b-142">ScRelocNotifications</span></span>](screlocnotifications.md)

