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
ms.openlocfilehash: 680fd16771b62d705808a04d768115a076e54750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415540"
---
# <a name="imapisupportgetmemallocroutines"></a><span data-ttu-id="97e1a-103">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="97e1a-103">IMAPISupport::GetMemAllocRoutines</span></span>

  
  
<span data-ttu-id="97e1a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97e1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97e1a-105">Recupera las direcciones de las funciones de asignación y desasignación de memoria MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="97e1a-105">Retrieves the addresses of the MAPI memory allocation and deallocation functions ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md)).</span></span>
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="97e1a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="97e1a-106">Parameters</span></span>

 <span data-ttu-id="97e1a-107">_lppAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="97e1a-107">_lppAllocateBuffer_</span></span>
  
> <span data-ttu-id="97e1a-108">contempla Un puntero a un puntero a la función **MAPIAllocateBuffer** .</span><span class="sxs-lookup"><span data-stu-id="97e1a-108">[out] A pointer to a pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="97e1a-109">**MAPIAllocateBuffer** asigna memoria.</span><span class="sxs-lookup"><span data-stu-id="97e1a-109">**MAPIAllocateBuffer** allocates memory.</span></span> 
    
 <span data-ttu-id="97e1a-110">_lppAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="97e1a-110">_lppAllocateMore_</span></span>
  
> <span data-ttu-id="97e1a-111">contempla Un puntero a un puntero a la función **MAPIAllocateMore** .</span><span class="sxs-lookup"><span data-stu-id="97e1a-111">[out] A pointer to a pointer to the **MAPIAllocateMore** function.</span></span> <span data-ttu-id="97e1a-112">**MAPIAllocateMore** asigna memoria adicional para la memoria que se asignó originalmente mediante **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="97e1a-112">**MAPIAllocateMore** allocates additional memory for memory that was originally allocated by using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="97e1a-113">_lppFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="97e1a-113">_lppFreeBuffer_</span></span>
  
> <span data-ttu-id="97e1a-114">contempla Un puntero a un puntero a la función **MAPIFreeBuffer** .</span><span class="sxs-lookup"><span data-stu-id="97e1a-114">[out] A pointer to a pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="97e1a-115">**MAPIFreeBuffer** libera memoria.</span><span class="sxs-lookup"><span data-stu-id="97e1a-115">**MAPIFreeBuffer** frees memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="97e1a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97e1a-116">Return value</span></span>

<span data-ttu-id="97e1a-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="97e1a-117">S_OK</span></span> 
  
> <span data-ttu-id="97e1a-118">Las direcciones de la función se devolvieron correctamente.</span><span class="sxs-lookup"><span data-stu-id="97e1a-118">The function addresses were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="97e1a-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97e1a-119">Remarks</span></span>

<span data-ttu-id="97e1a-120">El método **IMAPISupport:: GetMemAllocRoutines** se implementa para todos los objetos de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="97e1a-120">The **IMAPISupport::GetMemAllocRoutines** method is implemented for all support objects.</span></span> <span data-ttu-id="97e1a-121">Los proveedores de servicios llaman a **GetMemAllocRoutines** para obtener las direcciones de las tres funciones de asignación de memoria que se pasan a su función de inicialización ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)o [XPProviderInit](xpproviderinit.md)).</span><span class="sxs-lookup"><span data-stu-id="97e1a-121">Service providers call **GetMemAllocRoutines** to get the addresses of the three memory allocation functions that are passed to their initialization function ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md), or [XPProviderInit](xpproviderinit.md)).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="97e1a-122">Ver también</span><span class="sxs-lookup"><span data-stu-id="97e1a-122">See also</span></span>



[<span data-ttu-id="97e1a-123">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="97e1a-123">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="97e1a-124">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="97e1a-124">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="97e1a-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="97e1a-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="97e1a-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="97e1a-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

