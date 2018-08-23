---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e85e2da4d63442dc1fb912c5941be9d6f6f53824
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593791"
---
# <a name="mapireallocatebuffer"></a><span data-ttu-id="f2193-103">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="f2193-103">MAPIReallocateBuffer</span></span>

  
  
<span data-ttu-id="f2193-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2193-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2193-105">Reasigna un búfer de memoria.</span><span class="sxs-lookup"><span data-stu-id="f2193-105">Reallocates a memory buffer.</span></span> <span data-ttu-id="f2193-106">Se utiliza con la función [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="f2193-106">It is used with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2193-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f2193-107">Header file:</span></span>  <br/> |<span data-ttu-id="f2193-108">omapix.h</span><span class="sxs-lookup"><span data-stu-id="f2193-108">omapix.h</span></span>  <br/> |
|<span data-ttu-id="f2193-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f2193-109">Called by:</span></span>  <br/> |<span data-ttu-id="f2193-110">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="f2193-110">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a><span data-ttu-id="f2193-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2193-111">Parameters</span></span>

 <span data-ttu-id="f2193-112">_LPV_</span><span class="sxs-lookup"><span data-stu-id="f2193-112">_lpv_</span></span>
  
> <span data-ttu-id="f2193-113">Un puntero a la memoria que se reasignen.</span><span class="sxs-lookup"><span data-stu-id="f2193-113">A pointer to the memory to be reallocated.</span></span>
    
 <span data-ttu-id="f2193-114">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="f2193-114">_ulSize_</span></span>
  
> <span data-ttu-id="f2193-115">El tamaño, en bytes, del búfer que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="f2193-115">The size, in bytes, of the buffer to be allocated.</span></span>
    
 <span data-ttu-id="f2193-116">_lppv_</span><span class="sxs-lookup"><span data-stu-id="f2193-116">_lppv_</span></span>
  
> <span data-ttu-id="f2193-117">Un puntero al búfer devuelto asignado.</span><span class="sxs-lookup"><span data-stu-id="f2193-117">A pointer to the returned allocated buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f2193-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f2193-118">Remarks</span></span>

 <span data-ttu-id="f2193-119">**MAPIReallocateBuffer** asigna un nuevo bloque de memoria del tamaño solicitado y copia el contenido del búfer que se pasa en este nuevo bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="f2193-119">**MAPIReallocateBuffer** allocates a new block of memory of the requested size and copies the contents of the buffer that is passed into this new block of memory.</span></span> <span data-ttu-id="f2193-120">Si el bloque de memoria que se ha pasado contiene punteros internos, los punteros no cambian para que coincida con la nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="f2193-120">If the block of memory that is passed contains internal pointers, the pointers do not change to match the new location.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f2193-121">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f2193-121">See also</span></span>



[<span data-ttu-id="f2193-122">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="f2193-122">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)

