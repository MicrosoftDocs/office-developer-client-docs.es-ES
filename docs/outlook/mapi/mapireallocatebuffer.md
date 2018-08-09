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
ms.openlocfilehash: 26dcc31f2ebdd1892f966bfb95fda1a65c5140cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818276"
---
# <a name="mapireallocatebuffer"></a><span data-ttu-id="701f7-103">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="701f7-103">MAPIReallocateBuffer</span></span>

  
  
<span data-ttu-id="701f7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="701f7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="701f7-105">Reasigna un búfer de memoria.</span><span class="sxs-lookup"><span data-stu-id="701f7-105">Reallocates a memory buffer.</span></span> <span data-ttu-id="701f7-106">Se utiliza con la función [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="701f7-106">It is used with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="701f7-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="701f7-107">Header file:</span></span>  <br/> |<span data-ttu-id="701f7-108">omapix.h</span><span class="sxs-lookup"><span data-stu-id="701f7-108">omapix.h</span></span>  <br/> |
|<span data-ttu-id="701f7-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="701f7-109">Called by:</span></span>  <br/> |<span data-ttu-id="701f7-110">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="701f7-110">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a><span data-ttu-id="701f7-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="701f7-111">Parameters</span></span>

 <span data-ttu-id="701f7-112">_LPV_</span><span class="sxs-lookup"><span data-stu-id="701f7-112">_lpv_</span></span>
  
> <span data-ttu-id="701f7-113">Un puntero a la memoria que se reasignen.</span><span class="sxs-lookup"><span data-stu-id="701f7-113">A pointer to the memory to be reallocated.</span></span>
    
 <span data-ttu-id="701f7-114">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="701f7-114">_ulSize_</span></span>
  
> <span data-ttu-id="701f7-115">El tamaño, en bytes, del búfer que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="701f7-115">The size, in bytes, of the buffer to be allocated.</span></span>
    
 <span data-ttu-id="701f7-116">_lppv_</span><span class="sxs-lookup"><span data-stu-id="701f7-116">_lppv_</span></span>
  
> <span data-ttu-id="701f7-117">Un puntero al búfer devuelto asignado.</span><span class="sxs-lookup"><span data-stu-id="701f7-117">A pointer to the returned allocated buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="701f7-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="701f7-118">Remarks</span></span>

 <span data-ttu-id="701f7-119">**MAPIReallocateBuffer** asigna un nuevo bloque de memoria del tamaño solicitado y copia el contenido del búfer que se pasa en este nuevo bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="701f7-119">**MAPIReallocateBuffer** allocates a new block of memory of the requested size and copies the contents of the buffer that is passed into this new block of memory.</span></span> <span data-ttu-id="701f7-120">Si el bloque de memoria que se ha pasado contiene punteros internos, los punteros no cambian para que coincida con la nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="701f7-120">If the block of memory that is passed contains internal pointers, the pointers do not change to match the new location.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="701f7-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="701f7-121">See also</span></span>



[<span data-ttu-id="701f7-122">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="701f7-122">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)

