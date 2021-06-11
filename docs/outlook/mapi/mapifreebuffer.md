---
title: MAPIFreeBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIFreeBuffer
api_type:
- HeaderDef
ms.assetid: 9412594f-8acc-4c7e-a668-4ec1da0ad9cf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8794bb233eb69d0f246fb1019954ab718db6f464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410556"
---
# <a name="mapifreebuffer"></a><span data-ttu-id="04bfc-103">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="04bfc-103">MAPIFreeBuffer</span></span>

  
  
<span data-ttu-id="04bfc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04bfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04bfc-105">Libera un búfer de memoria asignado con una llamada a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) o la [función MAPIAllocateMore.](mapiallocatemore.md)</span><span class="sxs-lookup"><span data-stu-id="04bfc-105">Frees a memory buffer allocated with a call to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function or the [MAPIAllocateMore](mapiallocatemore.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="04bfc-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="04bfc-106">Header file:</span></span>  <br/> |<span data-ttu-id="04bfc-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="04bfc-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="04bfc-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="04bfc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="04bfc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="04bfc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="04bfc-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="04bfc-110">Called by:</span></span>  <br/> |<span data-ttu-id="04bfc-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="04bfc-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="04bfc-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="04bfc-112">Parameters</span></span>

 <span data-ttu-id="04bfc-113">_lpBuffer_</span><span class="sxs-lookup"><span data-stu-id="04bfc-113">_lpBuffer_</span></span>
  
> <span data-ttu-id="04bfc-114">[in] Puntero a un búfer de memoria asignado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="04bfc-114">[in] Pointer to a previously allocated memory buffer.</span></span> <span data-ttu-id="04bfc-115">Si se pasa NULL en el  _parámetro lpBuffer,_ **MAPIFreeBuffer** no hace nada.</span><span class="sxs-lookup"><span data-stu-id="04bfc-115">If NULL is passed in the  _lpBuffer_ parameter, **MAPIFreeBuffer** does nothing.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="04bfc-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04bfc-116">Return value</span></span>

<span data-ttu-id="04bfc-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="04bfc-117">S_OK</span></span> 
  
> <span data-ttu-id="04bfc-118">La llamada se ha producido correctamente y ha liberada la memoria solicitada.</span><span class="sxs-lookup"><span data-stu-id="04bfc-118">The call succeeded and freed the memory requested.</span></span> <span data-ttu-id="04bfc-119">**MAPIFreeBuffer** también puede devolver S_OK en ubicaciones ya liberadas o si el bloque de memoria no se asigna con **MAPIAllocateBuffer** y **MAPIAllocateMore**.</span><span class="sxs-lookup"><span data-stu-id="04bfc-119">**MAPIFreeBuffer** can also return S_OK on already freed locations or if memory block is not allocated with **MAPIAllocateBuffer** and **MAPIAllocateMore**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="04bfc-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04bfc-120">Remarks</span></span>

<span data-ttu-id="04bfc-121">Normalmente, cuando una aplicación cliente o un proveedor de servicios llama a [MAPIAllocateBuffer](mapiallocatebuffer.md) o [MAPIAllocateMore,](mapiallocatemore.md)el sistema operativo construye en un búfer de memoria contiguo una o más estructuras complejas con varios niveles de punteros.</span><span class="sxs-lookup"><span data-stu-id="04bfc-121">Usually, when a client application or service provider calls [MAPIAllocateBuffer](mapiallocatebuffer.md) or [MAPIAllocateMore](mapiallocatemore.md), the operating system constructs in one contiguous memory buffer one or more complex structures with multiple levels of pointers.</span></span> <span data-ttu-id="04bfc-122">Cuando una función o método MAPI crea un búfer con dicho contenido, un cliente puede liberar más adelante todas las estructuras contenidas en el búfer pasando a **MAPIFreeBuffer** el puntero al búfer devuelto por la función MAPI que creó el búfer.</span><span class="sxs-lookup"><span data-stu-id="04bfc-122">When a MAPI function or method creates a buffer with such contents, a client can later free all the structures contained in the buffer by passing to **MAPIFreeBuffer** the pointer to the buffer returned by the MAPI function that created the buffer.</span></span> <span data-ttu-id="04bfc-123">Para que un proveedor de servicios pueda liberar un búfer de memoria con **MAPIFreeBuffer,** debe pasar el puntero a ese búfer devuelto con el objeto de soporte técnico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="04bfc-123">For a service provider to free a memory buffer using **MAPIFreeBuffer**, it must pass the pointer to that buffer returned with the provider's support object.</span></span> 
  
<span data-ttu-id="04bfc-124">La llamada a **MAPIFreeBuffer para** liberar un búfer determinado debe realizarse tan pronto como un cliente o proveedor termine de usar este búfer.</span><span class="sxs-lookup"><span data-stu-id="04bfc-124">The call to **MAPIFreeBuffer** to free a particular buffer must be made as soon as a client or provider is finished using this buffer.</span></span> <span data-ttu-id="04bfc-125">Simplemente llamar al [método IMAPISession::Logoff](imapisession-logoff.md) al final de una sesión MAPI no libera automáticamente búferes de memoria.</span><span class="sxs-lookup"><span data-stu-id="04bfc-125">Simply calling the [IMAPISession::Logoff](imapisession-logoff.md) method at the end of a MAPI session does not automatically release memory buffers.</span></span> 
  
<span data-ttu-id="04bfc-126">Un cliente o proveedor de servicios debe funcionar con la suposición de que el puntero pasado en  _lpBuffer_ no es válido después de una devolución correcta de **MAPIFreeBuffer**.</span><span class="sxs-lookup"><span data-stu-id="04bfc-126">A client or service provider should operate on the assumption that the pointer passed in  _lpBuffer_ is invalid after a successful return from **MAPIFreeBuffer**.</span></span> <span data-ttu-id="04bfc-127">Si el puntero indica un bloque de memoria no asignado por el sistema de mensajería a través de **MAPIAllocateBuffer** o **MAPIAllocateMore** o un bloque de memoria libre, el comportamiento de **MAPIFreeBuffer** no está definido.</span><span class="sxs-lookup"><span data-stu-id="04bfc-127">If the pointer indicates either a memory block not allocated by the messaging system through **MAPIAllocateBuffer** or **MAPIAllocateMore** or a free memory block, the behavior of **MAPIFreeBuffer** is undefined.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="04bfc-128">Pasar un puntero nulo a **MAPIFreeBuffer** hace que el código de limpieza de aplicaciones sea más sencillo y más pequeño porque **MAPIFreeBuffer** puede inicializar punteros a NULL y, a continuación, liberarlos en el código de limpieza sin tener que probarlos primero.</span><span class="sxs-lookup"><span data-stu-id="04bfc-128">Passing a null pointer to **MAPIFreeBuffer** makes application cleanup code simpler and smaller because **MAPIFreeBuffer** can initialize pointers to NULL and then free them in the cleanup code without having to test them first.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="04bfc-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="04bfc-129">See also</span></span>



[<span data-ttu-id="04bfc-130">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="04bfc-130">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)

