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
ms.openlocfilehash: ad3d9d12e1073610747b0ab078c6d65c09f8c7c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569144"
---
# <a name="mapifreebuffer"></a><span data-ttu-id="66f3b-103">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="66f3b-103">MAPIFreeBuffer</span></span>

  
  
<span data-ttu-id="66f3b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66f3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66f3b-105">Libera un búfer de memoria asignado con una llamada a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) o la función [MAPIAllocateMore](mapiallocatemore.md) .</span><span class="sxs-lookup"><span data-stu-id="66f3b-105">Frees a memory buffer allocated with a call to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function or the [MAPIAllocateMore](mapiallocatemore.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="66f3b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="66f3b-106">Header file:</span></span>  <br/> |<span data-ttu-id="66f3b-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="66f3b-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="66f3b-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="66f3b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="66f3b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="66f3b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="66f3b-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="66f3b-110">Called by:</span></span>  <br/> |<span data-ttu-id="66f3b-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="66f3b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="66f3b-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66f3b-112">Parameters</span></span>

 <span data-ttu-id="66f3b-113">_lpBuffer_</span><span class="sxs-lookup"><span data-stu-id="66f3b-113">_lpBuffer_</span></span>
  
> <span data-ttu-id="66f3b-114">[entrada] Puntero a un búfer de memoria previamente asignado.</span><span class="sxs-lookup"><span data-stu-id="66f3b-114">[in] Pointer to a previously allocated memory buffer.</span></span> <span data-ttu-id="66f3b-115">Si se pasa NULL en el parámetro _lpBuffer_ , **MAPIFreeBuffer** no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="66f3b-115">If NULL is passed in the  _lpBuffer_ parameter, **MAPIFreeBuffer** does nothing.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="66f3b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66f3b-116">Return value</span></span>

<span data-ttu-id="66f3b-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="66f3b-117">S_OK</span></span> 
  
> <span data-ttu-id="66f3b-118">La llamada se ha realizado correctamente y libera la memoria solicitada.</span><span class="sxs-lookup"><span data-stu-id="66f3b-118">The call succeeded and freed the memory requested.</span></span> <span data-ttu-id="66f3b-119">**MAPIFreeBuffer** también puede devolver S_OK en ubicaciones ya liberadas o si no se asigna el bloque de memoria con **MAPIAllocateBuffer** y **MAPIAllocateMore**.</span><span class="sxs-lookup"><span data-stu-id="66f3b-119">**MAPIFreeBuffer** can also return S_OK on already freed locations or if memory block is not allocated with **MAPIAllocateBuffer** and **MAPIAllocateMore**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="66f3b-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="66f3b-120">Remarks</span></span>

<span data-ttu-id="66f3b-121">Normalmente, cuando una aplicación de cliente o un proveedor de servicios llama a [MAPIAllocateBuffer](mapiallocatebuffer.md) o [MAPIAllocateMore](mapiallocatemore.md), las construcciones de sistema operativo en el búfer de memoria contigua uno uno o más estructuras complejas con varios niveles de punteros.</span><span class="sxs-lookup"><span data-stu-id="66f3b-121">Usually, when a client application or service provider calls [MAPIAllocateBuffer](mapiallocatebuffer.md) or [MAPIAllocateMore](mapiallocatemore.md), the operating system constructs in one contiguous memory buffer one or more complex structures with multiple levels of pointers.</span></span> <span data-ttu-id="66f3b-122">Cuando una función de MAPI o un método crea un búfer con dicho contenido, un cliente más adelante puede liberar todas las estructuras contenidas en el búfer, se pasa al **MAPIFreeBuffer** el puntero en el búfer devuelto por la función MAPI que creó el búfer.</span><span class="sxs-lookup"><span data-stu-id="66f3b-122">When a MAPI function or method creates a buffer with such contents, a client can later free all the structures contained in the buffer by passing to **MAPIFreeBuffer** the pointer to the buffer returned by the MAPI function that created the buffer.</span></span> <span data-ttu-id="66f3b-123">Para que un proveedor de servicios liberar un búfer de memoria mediante **MAPIFreeBuffer**, debe pasar el puntero a ese búfer devuelto con objeto de soporte técnico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="66f3b-123">For a service provider to free a memory buffer using **MAPIFreeBuffer**, it must pass the pointer to that buffer returned with the provider's support object.</span></span> 
  
<span data-ttu-id="66f3b-124">La llamada a **MAPIFreeBuffer** para liberar un búfer determinado se debe realizar tan pronto como un cliente o proveedor haya terminado de usar este búfer.</span><span class="sxs-lookup"><span data-stu-id="66f3b-124">The call to **MAPIFreeBuffer** to free a particular buffer must be made as soon as a client or provider is finished using this buffer.</span></span> <span data-ttu-id="66f3b-125">Simplemente la llamada al método [IMAPISession::Logoff](imapisession-logoff.md) al final de una sesión MAPI, búferes de memoria no libera automáticamente.</span><span class="sxs-lookup"><span data-stu-id="66f3b-125">Simply calling the [IMAPISession::Logoff](imapisession-logoff.md) method at the end of a MAPI session does not automatically release memory buffers.</span></span> 
  
<span data-ttu-id="66f3b-126">Un proveedor de cliente o servicio debe funcionar en la suposición de que el puntero se pasan en _lpBuffer_ no es válido después de una devolución de **MAPIFreeBuffer**es correcta.</span><span class="sxs-lookup"><span data-stu-id="66f3b-126">A client or service provider should operate on the assumption that the pointer passed in  _lpBuffer_ is invalid after a successful return from **MAPIFreeBuffer**.</span></span> <span data-ttu-id="66f3b-127">Si el puntero indica un bloque de memoria no asignado por el sistema de mensajería a través de **MAPIAllocateBuffer** o **MAPIAllocateMore** o un bloque de memoria libre, el comportamiento de **MAPIFreeBuffer** no está definido.</span><span class="sxs-lookup"><span data-stu-id="66f3b-127">If the pointer indicates either a memory block not allocated by the messaging system through **MAPIAllocateBuffer** or **MAPIAllocateMore** or a free memory block, the behavior of **MAPIFreeBuffer** is undefined.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="66f3b-128">Pasar un puntero nulo a **MAPIFreeBuffer** hace que código de limpieza de la aplicación más sencilla y más pequeño porque **MAPIFreeBuffer** puede inicializar punteros a NULL y, a continuación, liberarlos en el código de limpieza sin tener que volver a probarlas en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="66f3b-128">Passing a null pointer to **MAPIFreeBuffer** makes application cleanup code simpler and smaller because **MAPIFreeBuffer** can initialize pointers to NULL and then free them in the cleanup code without having to test them first.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="66f3b-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="66f3b-129">See also</span></span>



[<span data-ttu-id="66f3b-130">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="66f3b-130">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)

