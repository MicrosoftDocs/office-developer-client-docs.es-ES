---
title: NOTIFCALLBACK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFCALLBACK
api_type:
- COM
ms.assetid: 416008b4-13aa-4387-8c12-f8f2ca252391
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b14529e987b85d1dcbe3689d4e852a9efd39a396
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818418"
---
# <a name="notifcallback"></a><span data-ttu-id="08add-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="08add-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="08add-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="08add-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="08add-105">Define una función de devolución de llamada que llama MAPI para enviar una notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="08add-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="08add-106">Sólo se puede usar esta función de devolución de llamada cuando se ajusta en un objeto de receptor advise creado mediante una llamada a la función [HrAllocAdviseSink](hrallocadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="08add-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08add-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="08add-107">Header file:</span></span>  <br/> |<span data-ttu-id="08add-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08add-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="08add-109">Función definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="08add-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="08add-110">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="08add-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="08add-111">Llamado por una función definida:</span><span class="sxs-lookup"><span data-stu-id="08add-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="08add-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="08add-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="08add-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08add-113">Parameters</span></span>

 <span data-ttu-id="08add-114">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="08add-114">_lpvContext_</span></span>
  
> <span data-ttu-id="08add-115">[entrada] Puntero a un valor arbitrario se pasa a la función de devolución de llamada cuando llama a MAPI.</span><span class="sxs-lookup"><span data-stu-id="08add-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="08add-116">Este valor puede representar una dirección de importancia a la aplicación de cliente o un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="08add-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="08add-117">Normalmente, para el código de C++, el parámetro _lpvContext_ representa un puntero a un objeto de C++.</span><span class="sxs-lookup"><span data-stu-id="08add-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="08add-118">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="08add-118">_cNotification_</span></span>
  
> <span data-ttu-id="08add-119">[entrada] Recuento de las notificaciones de eventos en la matriz indicada por el parámetro _lpNotifications_ .</span><span class="sxs-lookup"><span data-stu-id="08add-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="08add-120">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="08add-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="08add-121">[out] Puntero a la ubicación donde esta función escribe una matriz de estructuras de [notificación](notification.md) que contiene las notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="08add-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="08add-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08add-122">Return value</span></span>

<span data-ttu-id="08add-123">El conjunto de valores devueltos válidos para el prototipo de función **NOTIFCALLBACK** depende de si se implementa la función por una aplicación de cliente o un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="08add-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="08add-124">Los clientes siempre deben devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="08add-124">Clients should always return S_OK.</span></span> <span data-ttu-id="08add-125">Proveedores pueden devolver S_OK o CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="08add-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="08add-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="08add-126">Remarks</span></span>

<span data-ttu-id="08add-127">CALLBACK_DISCONTINUE es un valor devuelto válido para las funciones de devolución de llamada sincrónica solamente; solicita que MAPI detener inmediatamente el procesamiento de las devoluciones de llamada para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="08add-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="08add-128">Cuando se devuelve CALLBACK_DISCONTINUE, MAPI establece el parámetro _lpUlFlags_ a NOTIFY_CANCELED cuando se devuelve desde [IMAPISupport::Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="08add-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="08add-129">Las siguientes son limitaciones en lo que puede hacer una función de devolución de llamada sincrónica:</span><span class="sxs-lookup"><span data-stu-id="08add-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="08add-130">No puede provocar otra notificación sincrónica que se genere.</span><span class="sxs-lookup"><span data-stu-id="08add-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="08add-131">No puede mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="08add-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08add-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="08add-132">See also</span></span>



[<span data-ttu-id="08add-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="08add-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

