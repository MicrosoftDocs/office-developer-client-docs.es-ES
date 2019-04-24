---
title: MAPIAllocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateBuffer
api_type:
- HeaderDef
ms.assetid: f1fc7fc5-c71f-44f7-930a-571773eb6809
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 589ad42199e6f2ec1039499dfd9beda044ccc3dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357312"
---
# <a name="mapiallocatebuffer"></a><span data-ttu-id="d3a54-103">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="d3a54-103">MAPIAllocateBuffer</span></span>

  
  
<span data-ttu-id="d3a54-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3a54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3a54-105">Asigna un búfer de memoria.</span><span class="sxs-lookup"><span data-stu-id="d3a54-105">Allocates a memory buffer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3a54-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d3a54-106">Header file:</span></span>  <br/> |<span data-ttu-id="d3a54-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="d3a54-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="d3a54-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d3a54-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d3a54-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d3a54-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d3a54-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d3a54-110">Called by:</span></span>  <br/> |<span data-ttu-id="d3a54-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="d3a54-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="d3a54-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="d3a54-112">Parameters</span></span>

 <span data-ttu-id="d3a54-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="d3a54-113">_cbSize_</span></span>
  
> <span data-ttu-id="d3a54-114">a Tamaño, en bytes, del búfer que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="d3a54-114">[in] Size, in bytes, of the buffer to be allocated.</span></span> 
    
 <span data-ttu-id="d3a54-115">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="d3a54-115">_lppBuffer_</span></span>
  
> <span data-ttu-id="d3a54-116">contempla Puntero al búfer asignado devuelto.</span><span class="sxs-lookup"><span data-stu-id="d3a54-116">[out] Pointer to the returned allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d3a54-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3a54-117">Return value</span></span>

<span data-ttu-id="d3a54-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="d3a54-118">S_OK</span></span> 
  
> <span data-ttu-id="d3a54-119">La llamada se ha realizado correctamente y ha devuelto el búfer de memoria solicitado.</span><span class="sxs-lookup"><span data-stu-id="d3a54-119">The call succeeded and has returned the requested memory buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d3a54-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d3a54-120">Remarks</span></span>

<span data-ttu-id="d3a54-121">Durante el procesamiento de la llamada de **MAPIAllocateBuffer** , la implementación de la llamada adquiere un bloque de memoria del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d3a54-121">During **MAPIAllocateBuffer** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="d3a54-122">El búfer de memoria se asigna en una dirección de bytes con número par.</span><span class="sxs-lookup"><span data-stu-id="d3a54-122">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="d3a54-123">En las plataformas en las que el acceso de números enteros largos es más eficaz, el sistema operativo asigna el búfer en una dirección cuyo tamaño en bytes es un múltiplo de cuatro.</span><span class="sxs-lookup"><span data-stu-id="d3a54-123">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="d3a54-124">Al llamar a la función [MAPIFreeBuffer](mapifreebuffer.md) se libera el búfer de memoria asignado por **MAPIAllocateBuffer**llamando a la función [MAPIAllocateMore](mapiallocatemore.md) y a los búferes vinculados, cuando ya no se necesita memoria.</span><span class="sxs-lookup"><span data-stu-id="d3a54-124">Calling the [MAPIFreeBuffer](mapifreebuffer.md) function releases the memory buffer allocated by **MAPIAllocateBuffer**, by calling the [MAPIAllocateMore](mapiallocatemore.md) function and any buffers linked to it, when the memory is no longer needed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d3a54-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3a54-125">See also</span></span>



[<span data-ttu-id="d3a54-126">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="d3a54-126">MAPIReallocateBuffer</span></span>](mapireallocatebuffer.md)

