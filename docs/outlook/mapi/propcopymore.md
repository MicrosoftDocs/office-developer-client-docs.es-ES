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
ms.openlocfilehash: 827cdb919499a068f7932d8f1f7ec264ddc5b47c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404473"
---
# <a name="propcopymore"></a><span data-ttu-id="0d016-103">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="0d016-103">PropCopyMore</span></span>

  
  
<span data-ttu-id="0d016-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d016-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d016-105">Copia un único valor de propiedad desde una ubicación de origen a una ubicación de destino.</span><span class="sxs-lookup"><span data-stu-id="0d016-105">Copies a single property value from a source location to a destination location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d016-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0d016-106">Header file:</span></span>  <br/> |<span data-ttu-id="0d016-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="0d016-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0d016-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="0d016-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0d016-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0d016-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0d016-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="0d016-110">Called by:</span></span>  <br/> |<span data-ttu-id="0d016-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="0d016-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a><span data-ttu-id="0d016-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="0d016-112">Parameters</span></span>

 <span data-ttu-id="0d016-113">_lpSPropValueDest_</span><span class="sxs-lookup"><span data-stu-id="0d016-113">_lpSPropValueDest_</span></span>
  
> <span data-ttu-id="0d016-114">contempla Puntero a la ubicación a la que esta función escribe una estructura [SPropValue](spropvalue.md) que define el valor de la propiedad copiada.</span><span class="sxs-lookup"><span data-stu-id="0d016-114">[out] Pointer to the location to which this function writes an [SPropValue](spropvalue.md) structure defining the copied property value.</span></span> 
    
 <span data-ttu-id="0d016-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="0d016-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="0d016-116">a Puntero a la estructura [SPropValue](spropvalue.md) que contiene el valor de la propiedad que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="0d016-116">[in] Pointer to the [SPropValue](spropvalue.md) structure that contains the property value to be copied.</span></span> 
    
 <span data-ttu-id="0d016-117">_lpfAllocMore_</span><span class="sxs-lookup"><span data-stu-id="0d016-117">_lpfAllocMore_</span></span>
  
> <span data-ttu-id="0d016-118">a Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) que se va a usar para asignar memoria adicional si la ubicación de destino no es lo suficientemente grande como para contener la propiedad que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="0d016-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function to be used to allocate additional memory if the destination location is not large enough to hold the property to be copied.</span></span> 
    
 <span data-ttu-id="0d016-119">_lpvObject_</span><span class="sxs-lookup"><span data-stu-id="0d016-119">_lpvObject_</span></span>
  
> <span data-ttu-id="0d016-120">a Puntero a un objeto para el que **MAPIAllocateMore** asignará espacio si es necesario.</span><span class="sxs-lookup"><span data-stu-id="0d016-120">[in] Pointer to an object for which **MAPIAllocateMore** will allocate space if necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0d016-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d016-121">Return value</span></span>

<span data-ttu-id="0d016-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d016-122">S_OK</span></span>
  
> <span data-ttu-id="0d016-123">El valor de la propiedad única se ha copiado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0d016-123">The single property value was copied successfully.</span></span>
    
<span data-ttu-id="0d016-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0d016-124">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="0d016-125">Se encontró un tipo de propiedad desconocido.</span><span class="sxs-lookup"><span data-stu-id="0d016-125">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d016-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0d016-126">Remarks</span></span>

<span data-ttu-id="0d016-127">Una aplicación cliente o un proveedor de servicios puede usar la función **PropCopyMore** para copiar una propiedad de una tabla que está a punto de liberarse para poder usarla en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="0d016-127">A client application or service provider can use the **PropCopyMore** function to copy a property out of a table that is about to be freed in order to use it elsewhere.</span></span> 
  
 <span data-ttu-id="0d016-128">**PropCopyMore** no necesita asignar memoria a menos que el valor de la propiedad copiado sea de un tipo, como PT_STRING8, que no quepa en una estructura [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="0d016-128">**PropCopyMore** does not need to allocate memory unless the property value copied is of a type, such as PT_STRING8, that does not fit in an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="0d016-129">Para estas propiedades de gran tamaño, la función asigna memoria mediante la función [MAPIAllocateMore](mapiallocatemore.md) a la que se pasa un puntero en el parámetro _lpfAllocMore_ .</span><span class="sxs-lookup"><span data-stu-id="0d016-129">For these large properties, the function allocates memory using the [MAPIAllocateMore](mapiallocatemore.md) function to which a pointer is passed in the  _lpfAllocMore_ parameter.</span></span> 
  
<span data-ttu-id="0d016-130">Uso inrazonable de la memoria de los fragmentos de **PropCopyMore** ; considere la posibilidad de usar la función [ScCopyProps](sccopyprops.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="0d016-130">Injudicious use of **PropCopyMore** fragments memory; consider using the [ScCopyProps](sccopyprops.md) function instead.</span></span> 
  

