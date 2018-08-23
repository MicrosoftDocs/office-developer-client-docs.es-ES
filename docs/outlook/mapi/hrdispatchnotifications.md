---
title: HrDispatchNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDispatchNotifications
api_type:
- COM
ms.assetid: 42ec4266-67b9-416e-8b9b-163c95011626
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 60c5d7e980d1dc4d4263a2be2267008dbee1fd4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594701"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="2f15f-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="2f15f-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="2f15f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f15f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f15f-105">Envío de fuerza de todas las notificaciones en la cola.</span><span class="sxs-lookup"><span data-stu-id="2f15f-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f15f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2f15f-106">Header file:</span></span>  <br/> |<span data-ttu-id="2f15f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2f15f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2f15f-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="2f15f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2f15f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2f15f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2f15f-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="2f15f-110">Called by:</span></span>  <br/> |<span data-ttu-id="2f15f-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="2f15f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2f15f-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="2f15f-112">Parameters</span></span>

 <span data-ttu-id="2f15f-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2f15f-113">_ulFlags_</span></span>
  
> <span data-ttu-id="2f15f-114">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2f15f-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2f15f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f15f-115">Return value</span></span>

<span data-ttu-id="2f15f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="2f15f-116">S_OK</span></span>
  
> <span data-ttu-id="2f15f-117">Todas las notificaciones en cola se ha distribuido.</span><span class="sxs-lookup"><span data-stu-id="2f15f-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="2f15f-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="2f15f-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="2f15f-119">Se ha recibido WM_QUIT, mensaje WM_QUERYENDSESSION o WM_ENDSESSION.</span><span class="sxs-lookup"><span data-stu-id="2f15f-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="2f15f-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="2f15f-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="2f15f-121">MAPI no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="2f15f-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2f15f-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2f15f-122">Remarks</span></span>

<span data-ttu-id="2f15f-123">La función **HrDispatchNotifications** hace que MAPI enviar todas las notificaciones que están actualmente en cola en el motor de notificación de MAPI sin tener que esperar un envío de mensaje.</span><span class="sxs-lookup"><span data-stu-id="2f15f-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="2f15f-124">Esto puede tener un efecto beneficioso en el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="2f15f-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="2f15f-125">Para obtener más información, vea [forzar una notificación](forcing-a-notification.md).</span><span class="sxs-lookup"><span data-stu-id="2f15f-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2f15f-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="2f15f-126">Notes to callers</span></span>

<span data-ttu-id="2f15f-127">Algunas aplicaciones de esperen un mensaje de notificación en un bucle de tiempo de espera mediante las funciones de [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) y Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2f15f-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) and [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="2f15f-128">En todos los pero las plataformas más rápidas, dichas aplicaciones podrían experimentar un rendimiento deficiente o incluso bloqueo de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="2f15f-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="2f15f-129">Uso de **HrDispatchNotifications** no sólo reduce el código pero mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="2f15f-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

