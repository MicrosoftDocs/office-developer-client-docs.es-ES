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
ms.openlocfilehash: 28afa338b37e747ed441a8767981b7e63808e741
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817049"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="35945-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="35945-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="35945-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35945-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35945-105">Envío de fuerza de todas las notificaciones en la cola.</span><span class="sxs-lookup"><span data-stu-id="35945-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35945-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="35945-106">Header file:</span></span>  <br/> |<span data-ttu-id="35945-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="35945-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="35945-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="35945-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="35945-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="35945-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="35945-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="35945-110">Called by:</span></span>  <br/> |<span data-ttu-id="35945-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="35945-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="35945-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="35945-112">Parameters</span></span>

 <span data-ttu-id="35945-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="35945-113">_ulFlags_</span></span>
  
> <span data-ttu-id="35945-114">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="35945-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="35945-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35945-115">Return value</span></span>

<span data-ttu-id="35945-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="35945-116">S_OK</span></span>
  
> <span data-ttu-id="35945-117">Todas las notificaciones en cola se ha distribuido.</span><span class="sxs-lookup"><span data-stu-id="35945-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="35945-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="35945-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="35945-119">Se ha recibido WM_QUIT, mensaje WM_QUERYENDSESSION o WM_ENDSESSION.</span><span class="sxs-lookup"><span data-stu-id="35945-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="35945-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="35945-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="35945-121">MAPI no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="35945-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="35945-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="35945-122">Remarks</span></span>

<span data-ttu-id="35945-123">La función **HrDispatchNotifications** hace que MAPI enviar todas las notificaciones que están actualmente en cola en el motor de notificación de MAPI sin tener que esperar un envío de mensaje.</span><span class="sxs-lookup"><span data-stu-id="35945-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="35945-124">Esto puede tener un efecto beneficioso en el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="35945-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="35945-125">Para obtener más información, vea [forzar una notificación](forcing-a-notification.md).</span><span class="sxs-lookup"><span data-stu-id="35945-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="35945-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="35945-126">Notes to callers</span></span>

<span data-ttu-id="35945-127">Algunas aplicaciones de esperen un mensaje de notificación en un bucle de tiempo de espera mediante las funciones de [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) y Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) .</span><span class="sxs-lookup"><span data-stu-id="35945-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) and [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="35945-128">En todos los pero las plataformas más rápidas, dichas aplicaciones podrían experimentar un rendimiento deficiente o incluso bloqueo de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="35945-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="35945-129">Uso de **HrDispatchNotifications** no sólo reduce el código pero mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="35945-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

