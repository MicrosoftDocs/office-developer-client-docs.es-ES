---
title: IMAPIOfflineSetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.SetCurrentState
api_type:
- COM
ms.assetid: c0aa0df2-79f9-2558-7eb6-accae9bef4b2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 15e2d5c2aca595c3a06d215cd069c23da3e48125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817374"
---
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="8a113-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="8a113-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="8a113-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8a113-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8a113-105">Establece el estado actual de un objeto sin conexión a en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8a113-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="8a113-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="8a113-106">Parameters</span></span>

 <span data-ttu-id="8a113-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8a113-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8a113-108">[entrada] Modifica el comportamiento de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="8a113-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="8a113-109">Los valores admitidos son:</span><span class="sxs-lookup"><span data-stu-id="8a113-109">The supported values are:</span></span>
    
<span data-ttu-id="8a113-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="8a113-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="8a113-111">Al establecer _ulFlags_ en este valor se bloqueará la llamada **SetCurrentState** hasta que se complete el cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="8a113-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="8a113-112">De forma predeterminada la transición tiene lugar de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8a113-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="8a113-113">Cuando la transición se está deshaciendo la desprotección de forma asincrónica, todas las llamadas de **SetCurrentState** devolverá **E_PENDING** hasta que se complete el cambio.</span><span class="sxs-lookup"><span data-stu-id="8a113-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="8a113-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="8a113-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="8a113-115">Establece el estado actual sin bloquear.</span><span class="sxs-lookup"><span data-stu-id="8a113-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="8a113-116">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="8a113-116">_ulMask_</span></span>
  
> <span data-ttu-id="8a113-117">[entrada] La parte de que cambie el estado.</span><span class="sxs-lookup"><span data-stu-id="8a113-117">[in] The part of the state to change.</span></span> <span data-ttu-id="8a113-118">El único valor admitido es MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="8a113-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="8a113-119">_ulState_</span><span class="sxs-lookup"><span data-stu-id="8a113-119">_ulState_</span></span>
  
> <span data-ttu-id="8a113-120">[entrada] El estado para cambiar a.</span><span class="sxs-lookup"><span data-stu-id="8a113-120">[in] The state to change to.</span></span> <span data-ttu-id="8a113-121">Debe ser uno de estos dos valores:</span><span class="sxs-lookup"><span data-stu-id="8a113-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="8a113-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="8a113-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="8a113-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="8a113-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="8a113-124">_Conserva_</span><span class="sxs-lookup"><span data-stu-id="8a113-124">_pReserved_</span></span>
  
> <span data-ttu-id="8a113-125">Este parámetro está reservado para uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="8a113-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8a113-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a113-126">Return value</span></span>

<span data-ttu-id="8a113-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a113-127">S_OK</span></span>
  
> <span data-ttu-id="8a113-128">Se cambió correctamente el estado del objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8a113-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="8a113-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="8a113-129">E_PENDING</span></span>
  
> <span data-ttu-id="8a113-130">Esto indica que el estado del objeto sin conexión está cambiando de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8a113-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="8a113-131">Esto se produce cuando _ulFlags_ está establecida en MAPIOFFLINE_FLAG_BLOCK en una anterior llamada **SetCurrentState** , y cualquier llamada **SetCurrentState** subsiguiente devolverá este valor hasta que se complete el cambio de estado asincrónico.</span><span class="sxs-lookup"><span data-stu-id="8a113-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8a113-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a113-132">See also</span></span>



[<span data-ttu-id="8a113-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="8a113-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="8a113-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="8a113-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="8a113-135">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="8a113-135">MAPI Constants</span></span>](mapi-constants.md)

