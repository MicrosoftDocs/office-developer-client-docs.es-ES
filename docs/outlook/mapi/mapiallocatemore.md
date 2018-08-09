---
title: MAPIAllocateMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateMore
api_type:
- HeaderDef
ms.assetid: 3e48f76a-bc97-4cbc-9082-c07dd674b73e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f6f986ae811f2c7a886231a3046038889b82d683
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818251"
---
# <a name="mapiallocatemore"></a><span data-ttu-id="01f00-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="01f00-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="01f00-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01f00-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01f00-105">Asigna un búfer de memoria que está vinculado a otro búfer asignado previamente con la función [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="01f00-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01f00-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="01f00-106">Header file:</span></span>  <br/> |<span data-ttu-id="01f00-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="01f00-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="01f00-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="01f00-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="01f00-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="01f00-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="01f00-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="01f00-110">Called by:</span></span>  <br/> |<span data-ttu-id="01f00-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="01f00-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="01f00-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01f00-112">Parameters</span></span>

 <span data-ttu-id="01f00-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="01f00-113">_cbSize_</span></span>
  
> <span data-ttu-id="01f00-114">[entrada] Tamaño, en bytes, del búfer de nuevo que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="01f00-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="01f00-115">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="01f00-115">_lpObject_</span></span>
  
> <span data-ttu-id="01f00-116">[entrada] Puntero a un búfer MAPI existente asignado mediante **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="01f00-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="01f00-117">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="01f00-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="01f00-118">[out] Puntero para el valor devuelto, recién asignado del búfer.</span><span class="sxs-lookup"><span data-stu-id="01f00-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="01f00-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01f00-119">Return value</span></span>

<span data-ttu-id="01f00-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="01f00-120">S_OK</span></span> 
  
> <span data-ttu-id="01f00-121">La llamada se ha realizado correctamente y ha devuelto un puntero a la memoria solicitada.</span><span class="sxs-lookup"><span data-stu-id="01f00-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01f00-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="01f00-122">Remarks</span></span>

<span data-ttu-id="01f00-123">**MAPIAllocateMore** durante el procesamiento de la llamada, la implementación llamada adquiere un bloque de memoria del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="01f00-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="01f00-124">Se asigna el búfer de memoria en una dirección de byte pares.</span><span class="sxs-lookup"><span data-stu-id="01f00-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="01f00-125">En las plataformas donde el acceso de entero largo es más eficaz, el sistema operativo asigna el búfer en una dirección cuyo tamaño en bytes es un múltiplo de cuatro.</span><span class="sxs-lookup"><span data-stu-id="01f00-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="01f00-126">Es la única forma de liberar un búfer asignado con **MAPIAllocateMore** pasar el puntero de búfer especificado en el parámetro _lpObject_ a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="01f00-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="01f00-127">El vínculo entre los búferes de memoria asignada con [MAPIAllocateBuffer](mapiallocatebuffer.md) y **MAPIAllocateMore** permite **MAPIFreeBuffer** liberar ambos búferes con una sola llamada.</span><span class="sxs-lookup"><span data-stu-id="01f00-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

