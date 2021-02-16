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
ms.openlocfilehash: 59d0ce192605257dc0aebed46d8093a352fce05f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435288"
---
# <a name="mapireallocatebuffer"></a><span data-ttu-id="a5d04-103">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="a5d04-103">MAPIReallocateBuffer</span></span>

  
  
<span data-ttu-id="a5d04-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5d04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5d04-105">Realloca un búfer de memoria.</span><span class="sxs-lookup"><span data-stu-id="a5d04-105">Reallocates a memory buffer.</span></span> <span data-ttu-id="a5d04-106">Se usa con la [función MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="a5d04-106">It is used with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5d04-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a5d04-107">Header file:</span></span>  <br/> |<span data-ttu-id="a5d04-108">omapix.h</span><span class="sxs-lookup"><span data-stu-id="a5d04-108">omapix.h</span></span>  <br/> |
|<span data-ttu-id="a5d04-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a5d04-109">Called by:</span></span>  <br/> |<span data-ttu-id="a5d04-110">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="a5d04-110">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a><span data-ttu-id="a5d04-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5d04-111">Parameters</span></span>

 <span data-ttu-id="a5d04-112">_lpv_</span><span class="sxs-lookup"><span data-stu-id="a5d04-112">_lpv_</span></span>
  
> <span data-ttu-id="a5d04-113">Puntero a la memoria que se va a reasignar.</span><span class="sxs-lookup"><span data-stu-id="a5d04-113">A pointer to the memory to be reallocated.</span></span>
    
 <span data-ttu-id="a5d04-114">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="a5d04-114">_ulSize_</span></span>
  
> <span data-ttu-id="a5d04-115">Tamaño, en bytes, del búfer que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="a5d04-115">The size, in bytes, of the buffer to be allocated.</span></span>
    
 <span data-ttu-id="a5d04-116">_lppv_</span><span class="sxs-lookup"><span data-stu-id="a5d04-116">_lppv_</span></span>
  
> <span data-ttu-id="a5d04-117">Puntero al búfer asignado devuelto.</span><span class="sxs-lookup"><span data-stu-id="a5d04-117">A pointer to the returned allocated buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5d04-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5d04-118">Remarks</span></span>

 <span data-ttu-id="a5d04-119">**MAPIReallocateBuffer** asigna un nuevo bloque de memoria del tamaño solicitado y copia el contenido del búfer que se pasa a este nuevo bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="a5d04-119">**MAPIReallocateBuffer** allocates a new block of memory of the requested size and copies the contents of the buffer that is passed into this new block of memory.</span></span> <span data-ttu-id="a5d04-120">Si el bloque de memoria que se pasa contiene punteros internos, los punteros no cambian para que coincidan con la nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="a5d04-120">If the block of memory that is passed contains internal pointers, the pointers do not change to match the new location.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a5d04-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a5d04-121">See also</span></span>



[<span data-ttu-id="a5d04-122">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="a5d04-122">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)

