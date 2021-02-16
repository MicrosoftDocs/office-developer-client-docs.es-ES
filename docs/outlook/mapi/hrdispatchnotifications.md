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
ms.openlocfilehash: f4af3f2fd094942c48e02849c60f3e46acb1a5f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348100"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="9bcd6-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="9bcd6-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="9bcd6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bcd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bcd6-105">Fuerza el envío de todas las notificaciones en cola.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9bcd6-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9bcd6-106">Header file:</span></span>  <br/> |<span data-ttu-id="9bcd6-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9bcd6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9bcd6-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="9bcd6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9bcd6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9bcd6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9bcd6-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="9bcd6-110">Called by:</span></span>  <br/> |<span data-ttu-id="9bcd6-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="9bcd6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9bcd6-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9bcd6-112">Parameters</span></span>

 <span data-ttu-id="9bcd6-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9bcd6-113">_ulFlags_</span></span>
  
> <span data-ttu-id="9bcd6-114">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9bcd6-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9bcd6-115">Return value</span></span>

<span data-ttu-id="9bcd6-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="9bcd6-116">S_OK</span></span>
  
> <span data-ttu-id="9bcd6-117">Se han enviado todas las notificaciones en cola.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="9bcd6-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="9bcd6-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="9bcd6-119">WM_QUIT, WM_QUERYENDSESSION o WM_ENDSESSION se recibió.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="9bcd6-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="9bcd6-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="9bcd6-121">MAPI no se inicializó.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9bcd6-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9bcd6-122">Remarks</span></span>

<span data-ttu-id="9bcd6-123">La **función HrDispatchNotifications** hace que MAPI envíe todas las notificaciones que están actualmente en cola en el motor de notificaciones MAPI sin tener que esperar a que se envíe un mensaje.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="9bcd6-124">Esto puede tener un efecto beneficioso en el uso de la memoria.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="9bcd6-125">Para obtener más información, [vea Forzar una notificación.](forcing-a-notification.md)</span><span class="sxs-lookup"><span data-stu-id="9bcd6-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9bcd6-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="9bcd6-126">Notes to callers</span></span>

<span data-ttu-id="9bcd6-127">Algunas aplicaciones esperan un mensaje de notificación en un bucle de tiempo de espera mediante las funciones Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) y [DispatchMessage.](https://msdn.microsoft.com/library/ms644934.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bcd6-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) and [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="9bcd6-128">En todas las plataformas menos las más rápidas, estas aplicaciones pueden experimentar un rendimiento deficiente o incluso bloquear las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="9bcd6-129">El **uso de HrDispatchNotifications** no solo reduce el código, sino que mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

