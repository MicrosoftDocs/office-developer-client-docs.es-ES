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
ms.openlocfilehash: 01980b2da735838eeffa9afa5a0d139b69e76d0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357319"
---
# <a name="mapiallocatemore"></a><span data-ttu-id="a8ed4-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="a8ed4-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="a8ed4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8ed4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8ed4-105">Asigna un búfer de memoria vinculado a otro búfer previamente asignado con la función [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a8ed4-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8ed4-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a8ed4-106">Header file:</span></span>  <br/> |<span data-ttu-id="a8ed4-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="a8ed4-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="a8ed4-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a8ed4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a8ed4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a8ed4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a8ed4-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a8ed4-110">Called by:</span></span>  <br/> |<span data-ttu-id="a8ed4-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="a8ed4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="a8ed4-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="a8ed4-112">Parameters</span></span>

 <span data-ttu-id="a8ed4-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="a8ed4-113">_cbSize_</span></span>
  
> <span data-ttu-id="a8ed4-114">a Tamaño, en bytes, del nuevo búfer que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="a8ed4-115">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="a8ed4-115">_lpObject_</span></span>
  
> <span data-ttu-id="a8ed4-116">a Puntero a un búfer MAPI existente asignado mediante **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="a8ed4-117">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="a8ed4-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="a8ed4-118">contempla Puntero al búfer devuelto y recién asignado.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a8ed4-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8ed4-119">Return value</span></span>

<span data-ttu-id="a8ed4-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8ed4-120">S_OK</span></span> 
  
> <span data-ttu-id="a8ed4-121">La llamada se realizó correctamente y ha devuelto un puntero a la memoria solicitada.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a8ed4-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a8ed4-122">Remarks</span></span>

<span data-ttu-id="a8ed4-123">Durante el procesamiento de la llamada de **MAPIAllocateMore** , la implementación de la llamada adquiere un bloque de memoria del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="a8ed4-124">El búfer de memoria se asigna en una dirección de bytes con número par.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="a8ed4-125">En las plataformas en las que el acceso de números enteros largos es más eficaz, el sistema operativo asigna el búfer en una dirección cuyo tamaño en bytes es un múltiplo de cuatro.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="a8ed4-126">La única forma de liberar un búfer asignado con **MAPIAllocateMore** es pasar el puntero de búfer especificado en el parámetro _lpObject_ a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a8ed4-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="a8ed4-127">El vínculo entre los búferes de memoria asignados con [MAPIAllocateBuffer](mapiallocatebuffer.md) y **MAPIAllocateMore** permite a **MAPIFreeBuffer** liberar ambos búferes con una sola llamada.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

