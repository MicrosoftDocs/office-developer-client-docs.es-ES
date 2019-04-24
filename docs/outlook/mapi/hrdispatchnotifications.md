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
# <a name="hrdispatchnotifications"></a><span data-ttu-id="a53b4-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="a53b4-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="a53b4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a53b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a53b4-105">Obliga a la distribución de todas las notificaciones en cola.</span><span class="sxs-lookup"><span data-stu-id="a53b4-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a53b4-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a53b4-106">Header file:</span></span>  <br/> |<span data-ttu-id="a53b4-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="a53b4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a53b4-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a53b4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a53b4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a53b4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a53b4-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a53b4-110">Called by:</span></span>  <br/> |<span data-ttu-id="a53b4-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="a53b4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a53b4-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="a53b4-112">Parameters</span></span>

 <span data-ttu-id="a53b4-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a53b4-113">_ulFlags_</span></span>
  
> <span data-ttu-id="a53b4-114">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a53b4-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a53b4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a53b4-115">Return value</span></span>

<span data-ttu-id="a53b4-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a53b4-116">S_OK</span></span>
  
> <span data-ttu-id="a53b4-117">Se han enviado todas las notificaciones en cola.</span><span class="sxs-lookup"><span data-stu-id="a53b4-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="a53b4-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a53b4-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="a53b4-119">Se ha recibido WM_QUIT, WM_QUERYENDSESSION o WM_ENDSESSION.</span><span class="sxs-lookup"><span data-stu-id="a53b4-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="a53b4-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="a53b4-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="a53b4-121">MAPI no se inicializó.</span><span class="sxs-lookup"><span data-stu-id="a53b4-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a53b4-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a53b4-122">Remarks</span></span>

<span data-ttu-id="a53b4-123">La función **HrDispatchNotifications** hace que MAPI Envíe todas las notificaciones que están actualmente en cola en el motor de notificación MAPI sin tener que esperar a que se envíe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a53b4-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="a53b4-124">Esto puede tener un efecto ventajoso en el uso de la memoria.</span><span class="sxs-lookup"><span data-stu-id="a53b4-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="a53b4-125">Para obtener más información, consulte [forzar una notificación](forcing-a-notification.md).</span><span class="sxs-lookup"><span data-stu-id="a53b4-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a53b4-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a53b4-126">Notes to callers</span></span>

<span data-ttu-id="a53b4-127">Algunas aplicaciones esperan un mensaje de notificación en un bucle de tiempo de espera mediante las funciones de Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) y [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a53b4-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) and [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="a53b4-128">En todas las plataformas, excepto en las más rápidas, estas aplicaciones podrían experimentar un rendimiento deficiente o incluso un bloqueo de las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="a53b4-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="a53b4-129">El uso de **HrDispatchNotifications** no solo reduce el código, sino que mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a53b4-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

