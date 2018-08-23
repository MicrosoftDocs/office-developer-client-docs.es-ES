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
ms.openlocfilehash: 0520b219c87207a54555ba74050761f6ecc4854a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579602"
---
# <a name="mapiallocatebuffer"></a><span data-ttu-id="857be-103">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="857be-103">MAPIAllocateBuffer</span></span>

  
  
<span data-ttu-id="857be-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="857be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="857be-105">Asigna un búfer de memoria.</span><span class="sxs-lookup"><span data-stu-id="857be-105">Allocates a memory buffer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="857be-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="857be-106">Header file:</span></span>  <br/> |<span data-ttu-id="857be-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="857be-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="857be-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="857be-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="857be-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="857be-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="857be-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="857be-110">Called by:</span></span>  <br/> |<span data-ttu-id="857be-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="857be-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="857be-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="857be-112">Parameters</span></span>

 <span data-ttu-id="857be-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="857be-113">_cbSize_</span></span>
  
> <span data-ttu-id="857be-114">[entrada] Tamaño, en bytes, del búfer que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="857be-114">[in] Size, in bytes, of the buffer to be allocated.</span></span> 
    
 <span data-ttu-id="857be-115">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="857be-115">_lppBuffer_</span></span>
  
> <span data-ttu-id="857be-116">[out] Puntero al búfer devuelto asignado.</span><span class="sxs-lookup"><span data-stu-id="857be-116">[out] Pointer to the returned allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="857be-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="857be-117">Return value</span></span>

<span data-ttu-id="857be-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="857be-118">S_OK</span></span> 
  
> <span data-ttu-id="857be-119">La llamada se ha realizado correctamente y ha devuelto el búfer de memoria solicitada.</span><span class="sxs-lookup"><span data-stu-id="857be-119">The call succeeded and has returned the requested memory buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="857be-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="857be-120">Remarks</span></span>

<span data-ttu-id="857be-121">**MAPIAllocateBuffer** durante el procesamiento de la llamada, la implementación llamada adquiere un bloque de memoria del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="857be-121">During **MAPIAllocateBuffer** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="857be-122">Se asigna el búfer de memoria en una dirección de byte pares.</span><span class="sxs-lookup"><span data-stu-id="857be-122">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="857be-123">En las plataformas donde el acceso de entero largo es más eficaz, el sistema operativo asigna el búfer en una dirección cuyo tamaño en bytes es un múltiplo de cuatro.</span><span class="sxs-lookup"><span data-stu-id="857be-123">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="857be-124">Llamar a las versiones de la función [MAPIFreeBuffer](mapifreebuffer.md) el búfer de memoria asignado por **MAPIAllocateBuffer**, mediante una llamada a la función [MAPIAllocateMore](mapiallocatemore.md) y los búferes vinculado a él, cuando ya no se necesita la memoria.</span><span class="sxs-lookup"><span data-stu-id="857be-124">Calling the [MAPIFreeBuffer](mapifreebuffer.md) function releases the memory buffer allocated by **MAPIAllocateBuffer**, by calling the [MAPIAllocateMore](mapiallocatemore.md) function and any buffers linked to it, when the memory is no longer needed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="857be-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="857be-125">See also</span></span>



[<span data-ttu-id="857be-126">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="857be-126">MAPIReallocateBuffer</span></span>](mapireallocatebuffer.md)

