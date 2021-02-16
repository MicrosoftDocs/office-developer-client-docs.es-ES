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
ms.openlocfilehash: 0e2a1a582894e082722d73422fc8bafe34c4230c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434021"
---
# <a name="notifcallback"></a><span data-ttu-id="8df71-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="8df71-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="8df71-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8df71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8df71-105">Define una función de devolución de llamada a la que MAPI llama para enviar una notificación de evento.</span><span class="sxs-lookup"><span data-stu-id="8df71-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="8df71-106">Esta función de devolución de llamada solo se puede usar cuando se encapsula en un objeto receptor de aviso creado llamando a la función [HrAllocAdviseSink.](hrallocadvisesink.md)</span><span class="sxs-lookup"><span data-stu-id="8df71-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8df71-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8df71-107">Header file:</span></span>  <br/> |<span data-ttu-id="8df71-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8df71-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8df71-109">Función definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="8df71-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="8df71-110">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="8df71-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="8df71-111">Función definida llamada por:</span><span class="sxs-lookup"><span data-stu-id="8df71-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="8df71-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="8df71-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="8df71-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8df71-113">Parameters</span></span>

 <span data-ttu-id="8df71-114">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="8df71-114">_lpvContext_</span></span>
  
> <span data-ttu-id="8df71-115">[entrada] Puntero a un valor arbitrario pasado a la función de devolución de llamada cuando MAPI la llama.</span><span class="sxs-lookup"><span data-stu-id="8df71-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="8df71-116">Este valor puede representar una dirección significativa para la aplicación cliente o el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="8df71-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="8df71-117">Normalmente, para el código C++, el  _parámetro lpvContext_ representa un puntero a un objeto C++.</span><span class="sxs-lookup"><span data-stu-id="8df71-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="8df71-118">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="8df71-118">_cNotification_</span></span>
  
> <span data-ttu-id="8df71-119">[entrada] Recuento de notificaciones de eventos en la matriz indicada por el _parámetro lpNotifications._</span><span class="sxs-lookup"><span data-stu-id="8df71-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="8df71-120">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="8df71-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="8df71-121">[salida] Puntero a la ubicación donde esta función escribe una matriz de estructuras [notification](notification.md) que contiene las notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="8df71-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8df71-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8df71-122">Return value</span></span>

<span data-ttu-id="8df71-123">El conjunto de valores devueltos válidos para el prototipo de función **NOTIFCALLBACK** depende de si la función se implementa mediante una aplicación cliente o un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="8df71-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="8df71-124">Los clientes siempre deben devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="8df71-124">Clients should always return S_OK.</span></span> <span data-ttu-id="8df71-125">Los proveedores pueden devolver S_OK o CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="8df71-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8df71-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8df71-126">Remarks</span></span>

<span data-ttu-id="8df71-127">CALLBACK_DISCONTINUE es un valor devuelto válido solo para funciones de devolución de llamada sincrónicas; solicita que MAPI detenga inmediatamente el procesamiento de las devoluciones de llamada para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="8df71-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="8df71-128">Cuando CALLBACK_DISCONTINUE devuelve, MAPI establece el parámetro  _lpUlFlags_ en NOTIFY_CANCELED cuando devuelve de [IMAPISupport::Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="8df71-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="8df71-129">Las siguientes son limitaciones sobre lo que puede hacer una función de devolución de llamada sincrónica:</span><span class="sxs-lookup"><span data-stu-id="8df71-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="8df71-130">No puede provocar que se genere otra notificación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="8df71-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="8df71-131">No puede mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8df71-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8df71-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8df71-132">See also</span></span>



[<span data-ttu-id="8df71-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="8df71-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

