---
title: IMAPISupportGetMemAllocRoutines
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetMemAllocRoutines
api_type:
- COM
ms.assetid: 52d45876-367b-42da-b99a-29cdb71fa5a9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 782c04d05ea5cea811784b031e8a118a9c08cbb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817511"
---
# <a name="imapisupportgetmemallocroutines"></a><span data-ttu-id="c0150-103">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="c0150-103">IMAPISupport::GetMemAllocRoutines</span></span>

  
  
<span data-ttu-id="c0150-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0150-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0150-105">Recupera las direcciones de la memoria de asignación y cancelación de asignación de funciones de MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="c0150-105">Retrieves the addresses of the MAPI memory allocation and deallocation functions ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md)).</span></span>
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="c0150-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0150-106">Parameters</span></span>

 <span data-ttu-id="c0150-107">_lppAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="c0150-107">_lppAllocateBuffer_</span></span>
  
> <span data-ttu-id="c0150-108">[out] Un puntero a un puntero a la función **MAPIAllocateBuffer** .</span><span class="sxs-lookup"><span data-stu-id="c0150-108">[out] A pointer to a pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="c0150-109">**MAPIAllocateBuffer** asigna memoria.</span><span class="sxs-lookup"><span data-stu-id="c0150-109">**MAPIAllocateBuffer** allocates memory.</span></span> 
    
 <span data-ttu-id="c0150-110">_lppAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="c0150-110">_lppAllocateMore_</span></span>
  
> <span data-ttu-id="c0150-111">[out] Un puntero a un puntero a la función **MAPIAllocateMore** .</span><span class="sxs-lookup"><span data-stu-id="c0150-111">[out] A pointer to a pointer to the **MAPIAllocateMore** function.</span></span> <span data-ttu-id="c0150-112">**MAPIAllocateMore** asigna memoria adicional para la memoria que se asignó originalmente mediante el uso de **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="c0150-112">**MAPIAllocateMore** allocates additional memory for memory that was originally allocated by using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="c0150-113">_lppFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="c0150-113">_lppFreeBuffer_</span></span>
  
> <span data-ttu-id="c0150-114">[out] Un puntero a un puntero a la función **MAPIFreeBuffer** .</span><span class="sxs-lookup"><span data-stu-id="c0150-114">[out] A pointer to a pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="c0150-115">**MAPIFreeBuffer** libera memoria.</span><span class="sxs-lookup"><span data-stu-id="c0150-115">**MAPIFreeBuffer** frees memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c0150-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0150-116">Return value</span></span>

<span data-ttu-id="c0150-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0150-117">S_OK</span></span> 
  
> <span data-ttu-id="c0150-118">Las direcciones de función correctamente se han devuelto.</span><span class="sxs-lookup"><span data-stu-id="c0150-118">The function addresses were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0150-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c0150-119">Remarks</span></span>

<span data-ttu-id="c0150-120">El método **IMAPISupport::GetMemAllocRoutines** se implementa para todos los objetos de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="c0150-120">The **IMAPISupport::GetMemAllocRoutines** method is implemented for all support objects.</span></span> <span data-ttu-id="c0150-121">Proveedores de servicios de llamar a **GetMemAllocRoutines** para obtener las direcciones de las funciones de asignación de tres memoria que se pasan a su función de inicialización ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)o [XPProviderInit](xpproviderinit.md)).</span><span class="sxs-lookup"><span data-stu-id="c0150-121">Service providers call **GetMemAllocRoutines** to get the addresses of the three memory allocation functions that are passed to their initialization function ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md), or [XPProviderInit](xpproviderinit.md)).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c0150-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0150-122">See also</span></span>



[<span data-ttu-id="c0150-123">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="c0150-123">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="c0150-124">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="c0150-124">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="c0150-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c0150-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c0150-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0150-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
