---
title: ScDupPropset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScDupPropset
api_type:
- COM
ms.assetid: 165ffbd0-54aa-4692-8bd1-09e6ff3762df
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 77a376bba8d65737be84e2af62e65e0419d20957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406020"
---
# <a name="scduppropset"></a><span data-ttu-id="6921b-103">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="6921b-103">ScDupPropset</span></span>

  
  
<span data-ttu-id="6921b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6921b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6921b-105">Duplica una matriz de valores de propiedad en un único bloque de memoria MAPI que combina las operaciones de las funciones [ScCopyProps](sccopyprops.md) y [ScCountProps](sccountprops.md) .</span><span class="sxs-lookup"><span data-stu-id="6921b-105">Duplicates a property value array in a single block of MAPI memory combining the operations of the [ScCopyProps](sccopyprops.md) and [ScCountProps](sccountprops.md) functions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6921b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="6921b-106">Header file:</span></span>  <br/> |<span data-ttu-id="6921b-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="6921b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6921b-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="6921b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6921b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6921b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6921b-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="6921b-110">Called by:</span></span>  <br/> |<span data-ttu-id="6921b-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="6921b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a><span data-ttu-id="6921b-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="6921b-112">Parameters</span></span>

 <span data-ttu-id="6921b-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="6921b-113">_cprop_</span></span>
  
> <span data-ttu-id="6921b-114">a Número de valores de propiedad en la matriz indicada por el parámetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="6921b-114">[in] Count of property values in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="6921b-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="6921b-115">_rgprop_</span></span>
  
> <span data-ttu-id="6921b-116">a Puntero a una matriz de estructuras [SPropValue](spropvalue.md) que define los valores de propiedad que se van a duplicar.</span><span class="sxs-lookup"><span data-stu-id="6921b-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures defining the property values to be duplicated.</span></span> 
    
 <span data-ttu-id="6921b-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="6921b-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="6921b-118">a Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se va a usar para asignar memoria para la matriz duplicada.</span><span class="sxs-lookup"><span data-stu-id="6921b-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory for the duplicated array.</span></span> 
    
 <span data-ttu-id="6921b-119">_prgprop_</span><span class="sxs-lookup"><span data-stu-id="6921b-119">_prgprop_</span></span>
  
> <span data-ttu-id="6921b-120">contempla Puntero a la posición inicial en la memoria donde se almacena la matriz duplicada de estructuras **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="6921b-120">[out] Pointer to the initial position in memory where the returned duplicated array of **SPropValue** structures is stored.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6921b-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6921b-121">Return value</span></span>

<span data-ttu-id="6921b-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="6921b-122">S_OK</span></span> 
  
> <span data-ttu-id="6921b-123">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="6921b-123">The call succeeded and has returned the expected value or values.</span></span>
    

