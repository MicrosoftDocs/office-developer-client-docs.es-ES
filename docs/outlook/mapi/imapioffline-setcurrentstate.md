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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321213"
---
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="41ddb-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="41ddb-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="41ddb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41ddb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41ddb-105">Establece el estado actual de un objeto sin conexión en en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="41ddb-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="41ddb-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="41ddb-106">Parameters</span></span>

 <span data-ttu-id="41ddb-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="41ddb-107">_ulFlags_</span></span>
  
> <span data-ttu-id="41ddb-108">a Modifica el comportamiento de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="41ddb-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="41ddb-109">Los valores admitidos son:</span><span class="sxs-lookup"><span data-stu-id="41ddb-109">The supported values are:</span></span>
    
<span data-ttu-id="41ddb-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="41ddb-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="41ddb-111">Si se establece _ulFlags_ en este valor, se bloqueará la llamada **SetCurrentState** hasta que se complete el cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="41ddb-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="41ddb-112">De forma predeterminada, la transición se lleva a cabo de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="41ddb-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="41ddb-113">Cuando la transición se produce asincrónicamente, todas las llamadas **SetCurrentState** devolverán **E_PENDING** hasta que el cambio se complete.</span><span class="sxs-lookup"><span data-stu-id="41ddb-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="41ddb-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="41ddb-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="41ddb-115">Establece el estado actual sin bloquearse.</span><span class="sxs-lookup"><span data-stu-id="41ddb-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="41ddb-116">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="41ddb-116">_ulMask_</span></span>
  
> <span data-ttu-id="41ddb-117">a Parte del estado que se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="41ddb-117">[in] The part of the state to change.</span></span> <span data-ttu-id="41ddb-118">El único valor admitido es MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="41ddb-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="41ddb-119">_ulState_</span><span class="sxs-lookup"><span data-stu-id="41ddb-119">_ulState_</span></span>
  
> <span data-ttu-id="41ddb-120">a Estado al que se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="41ddb-120">[in] The state to change to.</span></span> <span data-ttu-id="41ddb-121">Debe ser uno de estos dos valores:</span><span class="sxs-lookup"><span data-stu-id="41ddb-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="41ddb-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="41ddb-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="41ddb-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="41ddb-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="41ddb-124">_Preserva_</span><span class="sxs-lookup"><span data-stu-id="41ddb-124">_pReserved_</span></span>
  
> <span data-ttu-id="41ddb-125">Este parámetro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="41ddb-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="41ddb-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41ddb-126">Return value</span></span>

<span data-ttu-id="41ddb-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="41ddb-127">S_OK</span></span>
  
> <span data-ttu-id="41ddb-128">El estado del objeto sin conexión se ha cambiado correctamente.</span><span class="sxs-lookup"><span data-stu-id="41ddb-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="41ddb-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="41ddb-129">E_PENDING</span></span>
  
> <span data-ttu-id="41ddb-130">Esto indica que el estado del objeto sin conexión cambia de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="41ddb-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="41ddb-131">Esto ocurre cuando _ulFlags_ se establece en MAPIOFFLINE_FLAG_BLOCK en una llamada a **SetCurrentState** anterior, y cualquier llamada subsiguiente a **SetCurrentState** devolverá este valor hasta que se complete el cambio de estado asincrónico.</span><span class="sxs-lookup"><span data-stu-id="41ddb-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="41ddb-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="41ddb-132">See also</span></span>



[<span data-ttu-id="41ddb-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="41ddb-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="41ddb-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="41ddb-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="41ddb-135">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="41ddb-135">MAPI Constants</span></span>](mapi-constants.md)

