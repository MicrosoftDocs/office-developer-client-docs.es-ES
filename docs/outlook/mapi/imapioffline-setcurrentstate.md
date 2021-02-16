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
ms.openlocfilehash: 0b6837b51b09ecd9a60630c613e1806cb10c1d87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421742"
---
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="0155d-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="0155d-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="0155d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0155d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0155d-105">Establece el estado actual de un objeto sin conexión en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0155d-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="0155d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0155d-106">Parameters</span></span>

 <span data-ttu-id="0155d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0155d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0155d-108">[entrada] Modifica el comportamiento de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="0155d-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="0155d-109">Los valores admitidos son:</span><span class="sxs-lookup"><span data-stu-id="0155d-109">The supported values are:</span></span>
    
<span data-ttu-id="0155d-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="0155d-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="0155d-111">Si  _se establece ulFlags_ en este valor, se bloqueará la llamada **SetCurrentState** hasta que se complete el cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="0155d-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="0155d-112">De forma predeterminada, la transición tiene lugar de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="0155d-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="0155d-113">Cuando la transición se produce de forma asincrónica, todas las llamadas **a SetCurrentState** devolverán E_PENDING **hasta** que se complete el cambio.</span><span class="sxs-lookup"><span data-stu-id="0155d-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="0155d-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0155d-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="0155d-115">Establece el estado actual sin bloqueos.</span><span class="sxs-lookup"><span data-stu-id="0155d-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="0155d-116">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="0155d-116">_ulMask_</span></span>
  
> <span data-ttu-id="0155d-117">[entrada] Parte del estado que se debe cambiar.</span><span class="sxs-lookup"><span data-stu-id="0155d-117">[in] The part of the state to change.</span></span> <span data-ttu-id="0155d-118">El único valor admitido es MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="0155d-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="0155d-119">_ulState_</span><span class="sxs-lookup"><span data-stu-id="0155d-119">_ulState_</span></span>
  
> <span data-ttu-id="0155d-120">[entrada] Estado al que se debe cambiar.</span><span class="sxs-lookup"><span data-stu-id="0155d-120">[in] The state to change to.</span></span> <span data-ttu-id="0155d-121">Debe ser uno de estos dos valores:</span><span class="sxs-lookup"><span data-stu-id="0155d-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="0155d-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="0155d-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="0155d-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="0155d-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="0155d-124">_pReserved_</span><span class="sxs-lookup"><span data-stu-id="0155d-124">_pReserved_</span></span>
  
> <span data-ttu-id="0155d-125">Este parámetro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="0155d-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0155d-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0155d-126">Return value</span></span>

<span data-ttu-id="0155d-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="0155d-127">S_OK</span></span>
  
> <span data-ttu-id="0155d-128">El estado del objeto sin conexión ha cambiado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0155d-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="0155d-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="0155d-129">E_PENDING</span></span>
  
> <span data-ttu-id="0155d-130">Esto indica que el estado del objeto sin conexión está cambiando asincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="0155d-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="0155d-131">Esto ocurre cuando  _ulFlags_ se establece en MAPIOFFLINE_FLAG_BLOCK en una llamada **SetCurrentState** anterior y cualquier llamada **SetCurrentState** posterior devolverá este valor hasta que se complete el cambio de estado asincrónico.</span><span class="sxs-lookup"><span data-stu-id="0155d-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0155d-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0155d-132">See also</span></span>



[<span data-ttu-id="0155d-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="0155d-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="0155d-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="0155d-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="0155d-135">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="0155d-135">MAPI Constants</span></span>](mapi-constants.md)

