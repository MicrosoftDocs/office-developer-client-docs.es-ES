---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9d8eb3f2c52f20ffe57d84823a0ed736337b4d9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818270"
---
# <a name="mapiofflinenotify"></a><span data-ttu-id="2697a-103">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="2697a-103">MAPIOFFLINE_NOTIFY</span></span>

<span data-ttu-id="2697a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2697a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2697a-105">Se trata de la notificación de un cambio en el estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="2697a-105">This is the notification for a change in the connection state.</span></span> <span data-ttu-id="2697a-106">Indica la parte del estado de conexión que ha cambiado, el estado de conexión anterior y el nuevo estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="2697a-106">It indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2697a-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="2697a-107">Quick info</span></span>

<span data-ttu-id="2697a-108">Vea **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="2697a-108">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef struct  
{ 
      ULONG ulSize; 
      MAPIOFFLINE_NOTIFY_TYPE NotifyType; 
      ULONG ulClientToken; 
      union { 
         struct 
           { 
           ULONG ulMask; 
           ULONG ulStateOld; 
           ULONG ulStateNew; 
           } StateChange; 
             } Info; 
} MAPIOFFLINE_NOTIFY;
```

## <a name="members"></a><span data-ttu-id="2697a-109">Members</span><span class="sxs-lookup"><span data-stu-id="2697a-109">Members</span></span>

 <span data-ttu-id="2697a-110">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="2697a-110">_ulSize_</span></span>
  
> <span data-ttu-id="2697a-111">Tamaño de la estructura **MAPIOFFLINE_NOTIFY** .</span><span class="sxs-lookup"><span data-stu-id="2697a-111">Size of the **MAPIOFFLINE_NOTIFY** structure.</span></span> 
    
 <span data-ttu-id="2697a-112">_NotifyType_</span><span class="sxs-lookup"><span data-stu-id="2697a-112">_NotifyType_</span></span>
  
> <span data-ttu-id="2697a-113">Tipo de notificación.</span><span class="sxs-lookup"><span data-stu-id="2697a-113">Type of notification.</span></span> <span data-ttu-id="2697a-114">Tenga en cuenta que se admite solo notificación sobre el cambio del estado de conexión; los únicos valores admitidos son:</span><span class="sxs-lookup"><span data-stu-id="2697a-114">Note that only notification on change of the connection state is supported; the only supported values are:</span></span>
    
   - <span data-ttu-id="2697a-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span><span class="sxs-lookup"><span data-stu-id="2697a-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span></span>
    
   - <span data-ttu-id="2697a-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="2697a-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span></span>
    
   - <span data-ttu-id="2697a-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span><span class="sxs-lookup"><span data-stu-id="2697a-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span></span>
    
 <span data-ttu-id="2697a-118">_ulClientToken_</span><span class="sxs-lookup"><span data-stu-id="2697a-118">_ulClientToken_</span></span>
  
> <span data-ttu-id="2697a-119">Un símbolo (token) definido por el cliente en la estructura **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** en **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="2697a-119">A token defined by the client in the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** structure in **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
    
 <span data-ttu-id="2697a-120">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="2697a-120">_ulMask_</span></span>
  
> <span data-ttu-id="2697a-121">La parte del estado de conexión que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="2697a-121">The part of the connection state that has changed.</span></span> <span data-ttu-id="2697a-122">El único valor admitido es MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="2697a-122">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="2697a-123">_ulStateOld_</span><span class="sxs-lookup"><span data-stu-id="2697a-123">_ulStateOld_</span></span>
  
> <span data-ttu-id="2697a-124">El estado de conexión anterior.</span><span class="sxs-lookup"><span data-stu-id="2697a-124">The old connection state.</span></span> <span data-ttu-id="2697a-125">Los únicos valores admitidos son:</span><span class="sxs-lookup"><span data-stu-id="2697a-125">The only supported values are:</span></span>
    
   - <span data-ttu-id="2697a-126">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="2697a-126">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="2697a-127">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="2697a-127">MAPIOFFLINE_STATE_ONLINE</span></span>
    
 <span data-ttu-id="2697a-128">_ulStateNew_</span><span class="sxs-lookup"><span data-stu-id="2697a-128">_ulStateNew_</span></span>
  
> <span data-ttu-id="2697a-129">El nuevo estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="2697a-129">The new connection state.</span></span> <span data-ttu-id="2697a-130">Los únicos valores admitidos son:</span><span class="sxs-lookup"><span data-stu-id="2697a-130">The only supported values are:</span></span>
    
   - <span data-ttu-id="2697a-131">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="2697a-131">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="2697a-132">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="2697a-132">MAPIOFFLINE_STATE_ONLINE</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2697a-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2697a-133">Remarks</span></span>

<span data-ttu-id="2697a-134">La API de estado sin conexión admite solamente las notificaciones de cambios en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="2697a-134">The Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="2697a-135">Un cliente debe comprobar que Outlook devuelve los siguientes valores antes de examinar el cambio real:</span><span class="sxs-lookup"><span data-stu-id="2697a-135">A client must check that Outlook returns the following values before examining the actual change:</span></span>
  
1.  <span data-ttu-id="2697a-136">*NotifyType* tiene el valor MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE o MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span><span class="sxs-lookup"><span data-stu-id="2697a-136">*NotifyType*  has the value MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE, or MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span></span> <span data-ttu-id="2697a-137">En este caso, el cliente puede asumir que el cambio es un cambio de estado de conexión, y es *información* de la estructura *StateChange* .</span><span class="sxs-lookup"><span data-stu-id="2697a-137">In this case, the client can assume that the change is a connection state change, and  *Info*  is of the structure  *StateChange*  .</span></span> 
    
2.  <span data-ttu-id="2697a-138">*ulMask* tiene el valor MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="2697a-138">*ulMask*  has the value MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span> <span data-ttu-id="2697a-139">En este caso, el cliente puede asumir que el cambio es un cambio de estado de conexión o sin conexión y puede continuar con el examen de *ulStateOld* y *ulStateNew* .</span><span class="sxs-lookup"><span data-stu-id="2697a-139">In this case, the client can assume that the change is an online/offline connection state change, and can proceed with examining  *ulStateOld*  and  *ulStateNew*  .</span></span> 
    
<span data-ttu-id="2697a-140">Es posible que Outlook notifica a un cliente de otros cambios que no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="2697a-140">It is possible that Outlook notifies a client of other changes that are not supported.</span></span> <span data-ttu-id="2697a-141">En esos casos, *NotifyType* no sería uno de los tres valores que se ha indicado anteriormente, o *ulMask* no sería MAPIOFFLINE_STATE_OFFLINE_MASK y el cliente debe omitir el resto de los datos en *información* .</span><span class="sxs-lookup"><span data-stu-id="2697a-141">In such cases,  *NotifyType*  would not be any one of the three values stated previously, or  *ulMask*  would not be MAPIOFFLINE_STATE_OFFLINE_MASK, and the client must ignore the rest of the data in  *Info*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2697a-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="2697a-142">See also</span></span>

- [<span data-ttu-id="2697a-143">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="2697a-143">About the Offline State API</span></span>](about-the-offline-state-api.md)  
- [<span data-ttu-id="2697a-144">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="2697a-144">MAPI Constants</span></span>](mapi-constants.md)  
- [<span data-ttu-id="2697a-145">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="2697a-145">MAPIOFFLINE_NOTIFY_TYPE</span></span>](mapioffline_notify_type.md)

