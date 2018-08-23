---
title: PropCopyMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PropCopyMore
api_type:
- HeaderDef
ms.assetid: 133d47cf-3592-44f3-8cdd-be402d160ee4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 635525a1c2c3234d724534d225eb07022afc9956
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592125"
---
# <a name="propcopymore"></a><span data-ttu-id="f92d5-103">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="f92d5-103">PropCopyMore</span></span>

  
  
<span data-ttu-id="f92d5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f92d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f92d5-105">Copia un valor de propiedad único desde una ubicación de origen a una ubicación de destino.</span><span class="sxs-lookup"><span data-stu-id="f92d5-105">Copies a single property value from a source location to a destination location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f92d5-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f92d5-106">Header file:</span></span>  <br/> |<span data-ttu-id="f92d5-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f92d5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f92d5-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="f92d5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f92d5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f92d5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f92d5-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f92d5-110">Called by:</span></span>  <br/> |<span data-ttu-id="f92d5-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="f92d5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a><span data-ttu-id="f92d5-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f92d5-112">Parameters</span></span>

 <span data-ttu-id="f92d5-113">_lpSPropValueDest_</span><span class="sxs-lookup"><span data-stu-id="f92d5-113">_lpSPropValueDest_</span></span>
  
> <span data-ttu-id="f92d5-114">[out] Puntero a la ubicación a la que esta función escribe una estructura de [SPropValue](spropvalue.md) define el valor de la propiedad copiados.</span><span class="sxs-lookup"><span data-stu-id="f92d5-114">[out] Pointer to the location to which this function writes an [SPropValue](spropvalue.md) structure defining the copied property value.</span></span> 
    
 <span data-ttu-id="f92d5-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="f92d5-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="f92d5-116">[entrada] Puntero a la estructura [SPropValue](spropvalue.md) que contiene el valor de la propiedad que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="f92d5-116">[in] Pointer to the [SPropValue](spropvalue.md) structure that contains the property value to be copied.</span></span> 
    
 <span data-ttu-id="f92d5-117">_lpfAllocMore_</span><span class="sxs-lookup"><span data-stu-id="f92d5-117">_lpfAllocMore_</span></span>
  
> <span data-ttu-id="f92d5-118">[entrada] Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) que se usará para asignar memoria adicional si la ubicación de destino no es lo suficientemente grande como para contener la propiedad que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="f92d5-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function to be used to allocate additional memory if the destination location is not large enough to hold the property to be copied.</span></span> 
    
 <span data-ttu-id="f92d5-119">_lpvObject_</span><span class="sxs-lookup"><span data-stu-id="f92d5-119">_lpvObject_</span></span>
  
> <span data-ttu-id="f92d5-120">[entrada] Puntero a un objeto para el que **MAPIAllocateMore** asignar espacio si es necesario.</span><span class="sxs-lookup"><span data-stu-id="f92d5-120">[in] Pointer to an object for which **MAPIAllocateMore** will allocate space if necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f92d5-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f92d5-121">Return value</span></span>

<span data-ttu-id="f92d5-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="f92d5-122">S_OK</span></span>
  
> <span data-ttu-id="f92d5-123">El valor de propiedad único se ha copiado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f92d5-123">The single property value was copied successfully.</span></span>
    
<span data-ttu-id="f92d5-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f92d5-124">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="f92d5-125">Se encontró un tipo de propiedad desconocido.</span><span class="sxs-lookup"><span data-stu-id="f92d5-125">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f92d5-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f92d5-126">Remarks</span></span>

<span data-ttu-id="f92d5-127">Una aplicación de cliente o un proveedor de servicios puede usar la función **PropCopyMore** para copiar una propiedad fuera de una tabla que se va a ser liberados para poder utilizarlo en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="f92d5-127">A client application or service provider can use the **PropCopyMore** function to copy a property out of a table that is about to be freed in order to use it elsewhere.</span></span> 
  
 <span data-ttu-id="f92d5-128">**PropCopyMore** no es necesario asignar memoria a menos que el valor de la propiedad copió es de un tipo, como PT_STRING8, que no cabe en una estructura [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="f92d5-128">**PropCopyMore** does not need to allocate memory unless the property value copied is of a type, such as PT_STRING8, that does not fit in an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="f92d5-129">Para estas propiedades de gran tamaño, la función asigna memoria mediante la función de [MAPIAllocateMore](mapiallocatemore.md) a la que se pasa un puntero en el parámetro _lpfAllocMore_ .</span><span class="sxs-lookup"><span data-stu-id="f92d5-129">For these large properties, the function allocates memory using the [MAPIAllocateMore](mapiallocatemore.md) function to which a pointer is passed in the  _lpfAllocMore_ parameter.</span></span> 
  
<span data-ttu-id="f92d5-130">Injudicious uso de memoria de fragmentos de **PropCopyMore** ; Considere la posibilidad de usar la función [ScCopyProps](sccopyprops.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="f92d5-130">Injudicious use of **PropCopyMore** fragments memory; consider using the [ScCopyProps](sccopyprops.md) function instead.</span></span> 
  

