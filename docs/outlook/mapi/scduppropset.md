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
ms.openlocfilehash: 5b93f84026cacd8568dc5ceec5574d144f6d1633
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820590"
---
# <a name="scduppropset"></a><span data-ttu-id="a3cf7-103">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="a3cf7-103">ScDupPropset</span></span>

  
  
<span data-ttu-id="a3cf7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a3cf7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a3cf7-105">Duplica una matriz de valores de propiedad en un único bloque de memoria MAPI combinar las operaciones de las funciones [ScCopyProps](sccopyprops.md) y [ScCountProps](sccountprops.md) .</span><span class="sxs-lookup"><span data-stu-id="a3cf7-105">Duplicates a property value array in a single block of MAPI memory combining the operations of the [ScCopyProps](sccopyprops.md) and [ScCountProps](sccountprops.md) functions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3cf7-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a3cf7-106">Header file:</span></span>  <br/> |<span data-ttu-id="a3cf7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a3cf7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a3cf7-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="a3cf7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a3cf7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a3cf7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a3cf7-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a3cf7-110">Called by:</span></span>  <br/> |<span data-ttu-id="a3cf7-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="a3cf7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a><span data-ttu-id="a3cf7-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3cf7-112">Parameters</span></span>

 <span data-ttu-id="a3cf7-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="a3cf7-113">_cprop_</span></span>
  
> <span data-ttu-id="a3cf7-114">[entrada] Recuento de valores de propiedad en la matriz indicada por el parámetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="a3cf7-114">[in] Count of property values in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="a3cf7-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="a3cf7-115">_rgprop_</span></span>
  
> <span data-ttu-id="a3cf7-116">[entrada] Puntero a una matriz de estructuras [SPropValue](spropvalue.md) definición de los valores de propiedad que se va a duplicar.</span><span class="sxs-lookup"><span data-stu-id="a3cf7-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures defining the property values to be duplicated.</span></span> 
    
 <span data-ttu-id="a3cf7-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="a3cf7-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="a3cf7-118">[entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria para la matriz duplicada.</span><span class="sxs-lookup"><span data-stu-id="a3cf7-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory for the duplicated array.</span></span> 
    
 <span data-ttu-id="a3cf7-119">_prgprop_</span><span class="sxs-lookup"><span data-stu-id="a3cf7-119">_prgprop_</span></span>
  
> <span data-ttu-id="a3cf7-120">[out] Puntero a la posición inicial en la memoria donde se almacena la matriz devuelta duplicada de estructuras **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="a3cf7-120">[out] Pointer to the initial position in memory where the returned duplicated array of **SPropValue** structures is stored.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a3cf7-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3cf7-121">Return value</span></span>

<span data-ttu-id="a3cf7-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3cf7-122">S_OK</span></span> 
  
> <span data-ttu-id="a3cf7-123">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="a3cf7-123">The call succeeded and has returned the expected value or values.</span></span>
    

