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
ms.openlocfilehash: 0e6226dd0fc9c04070ed3d1dda1770f77fbc585c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583011"
---
# <a name="mapiallocatemore"></a><span data-ttu-id="6d60e-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="6d60e-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="6d60e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d60e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d60e-105">Asigna un búfer de memoria que está vinculado a otro búfer asignado previamente con la función [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="6d60e-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d60e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="6d60e-106">Header file:</span></span>  <br/> |<span data-ttu-id="6d60e-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="6d60e-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="6d60e-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="6d60e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6d60e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6d60e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6d60e-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="6d60e-110">Called by:</span></span>  <br/> |<span data-ttu-id="6d60e-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="6d60e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="6d60e-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d60e-112">Parameters</span></span>

 <span data-ttu-id="6d60e-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="6d60e-113">_cbSize_</span></span>
  
> <span data-ttu-id="6d60e-114">[entrada] Tamaño, en bytes, del búfer de nuevo que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="6d60e-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="6d60e-115">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="6d60e-115">_lpObject_</span></span>
  
> <span data-ttu-id="6d60e-116">[entrada] Puntero a un búfer MAPI existente asignado mediante **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="6d60e-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="6d60e-117">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="6d60e-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="6d60e-118">[out] Puntero para el valor devuelto, recién asignado del búfer.</span><span class="sxs-lookup"><span data-stu-id="6d60e-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6d60e-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d60e-119">Return value</span></span>

<span data-ttu-id="6d60e-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="6d60e-120">S_OK</span></span> 
  
> <span data-ttu-id="6d60e-121">La llamada se ha realizado correctamente y ha devuelto un puntero a la memoria solicitada.</span><span class="sxs-lookup"><span data-stu-id="6d60e-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6d60e-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6d60e-122">Remarks</span></span>

<span data-ttu-id="6d60e-123">**MAPIAllocateMore** durante el procesamiento de la llamada, la implementación llamada adquiere un bloque de memoria del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6d60e-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="6d60e-124">Se asigna el búfer de memoria en una dirección de byte pares.</span><span class="sxs-lookup"><span data-stu-id="6d60e-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="6d60e-125">En las plataformas donde el acceso de entero largo es más eficaz, el sistema operativo asigna el búfer en una dirección cuyo tamaño en bytes es un múltiplo de cuatro.</span><span class="sxs-lookup"><span data-stu-id="6d60e-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="6d60e-126">Es la única forma de liberar un búfer asignado con **MAPIAllocateMore** pasar el puntero de búfer especificado en el parámetro _lpObject_ a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="6d60e-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="6d60e-127">El vínculo entre los búferes de memoria asignada con [MAPIAllocateBuffer](mapiallocatebuffer.md) y **MAPIAllocateMore** permite **MAPIFreeBuffer** liberar ambos búferes con una sola llamada.</span><span class="sxs-lookup"><span data-stu-id="6d60e-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

