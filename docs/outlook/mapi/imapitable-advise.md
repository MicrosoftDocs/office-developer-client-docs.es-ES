---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c9401c163c74ab303ec39c147e0432d1979426b8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418816"
---
# <a name="imapitableadvise"></a><span data-ttu-id="ba404-103">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="ba404-103">IMAPITable::Advise</span></span>

  
  
<span data-ttu-id="ba404-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba404-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba404-105">Registra un objeto receptor de aviso para recibir una notificación de eventos especificados que afectan a la tabla.</span><span class="sxs-lookup"><span data-stu-id="ba404-105">Registers an advise sink object to receive notification of specified events affecting the table.</span></span>
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="ba404-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba404-106">Parameters</span></span>

 <span data-ttu-id="ba404-107">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="ba404-107">_ulEventMask_</span></span>
  
> <span data-ttu-id="ba404-108">[entrada] Valor que indica el tipo de evento que generará la notificación.</span><span class="sxs-lookup"><span data-stu-id="ba404-108">[in] Value indicating the type of event that will generate the notification.</span></span> <span data-ttu-id="ba404-109">Solo el siguiente valor es válido:</span><span class="sxs-lookup"><span data-stu-id="ba404-109">Only the following value is valid:</span></span>
    
 `fnevTableModified`
  
 <span data-ttu-id="ba404-110">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="ba404-110">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="ba404-111">[entrada] Puntero a un objeto receptor de aviso para recibir las notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ba404-111">[in] Pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="ba404-112">Este objeto receptor de aviso debe haber sido ya asignado.</span><span class="sxs-lookup"><span data-stu-id="ba404-112">This advise sink object must have been already allocated.</span></span>
    
 <span data-ttu-id="ba404-113">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="ba404-113">_lpulConnection_</span></span>
  
> <span data-ttu-id="ba404-114">[salida] Puntero a un valor distinto de cero que representa el registro de notificaciones correcto.</span><span class="sxs-lookup"><span data-stu-id="ba404-114">[out] Pointer to a nonzero value that represents the successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ba404-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba404-115">Return value</span></span>

<span data-ttu-id="ba404-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ba404-116">S_OK</span></span> 
  
> <span data-ttu-id="ba404-117">El registro de notificación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ba404-117">The notification registration successfully completed.</span></span>
    
<span data-ttu-id="ba404-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ba404-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="ba404-119">La implementación de la tabla no admite cambios en sus filas y columnas o no admite notificaciones.</span><span class="sxs-lookup"><span data-stu-id="ba404-119">The table implementation either does not support changes to its rows and columns or does not support notification.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba404-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ba404-120">Remarks</span></span>

<span data-ttu-id="ba404-121">Use el **método IMAPITable::Advise** para registrar un objeto de tabla implementado en el proveedor para las devoluciones de llamada de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="ba404-121">Use the **IMAPITable::Advise** method to register a table object implemented in the provider for notification callbacks.</span></span> <span data-ttu-id="ba404-122">Siempre que se produce un cambio en el objeto de tabla, el proveedor comprueba qué bit de máscara de evento se estableció en el parámetro  _ulEventMask_ y, por lo tanto, qué tipo de cambio se produjo.</span><span class="sxs-lookup"><span data-stu-id="ba404-122">Whenever a change occurs to the table object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and thus what type of change occurred.</span></span> <span data-ttu-id="ba404-123">Si se establece un bit, el proveedor llama al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto receptor de aviso indicado por el parámetro  _lpAdviseSink_ para notificar el evento.</span><span class="sxs-lookup"><span data-stu-id="ba404-123">If a bit is set, then the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="ba404-124">Los datos pasados en la estructura de notificación a **la rutina OnNotify** describen el evento.</span><span class="sxs-lookup"><span data-stu-id="ba404-124">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="ba404-125">La llamada a **OnNotify** puede producirse durante la llamada que cambia el objeto o en cualquier momento siguiente.</span><span class="sxs-lookup"><span data-stu-id="ba404-125">The call to **OnNotify** can occur during the call that changes the object, or at any following time.</span></span> <span data-ttu-id="ba404-126">En sistemas que admiten varios subprocesos de ejecución, la llamada a **OnNotify** puede producirse en cualquier subproceso.</span><span class="sxs-lookup"><span data-stu-id="ba404-126">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="ba404-127">Para obtener una forma de convertir una llamada a **OnNotify** que puede ocurrir en un momento inoportuna en uno que sea más seguro de controlar, un proveedor debe usar la función [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md)</span><span class="sxs-lookup"><span data-stu-id="ba404-127">For a way to turn a call to **OnNotify** that might happen at an inopportune time into one that is safer to handle, a provider should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="ba404-128">Para proporcionar notificaciones, el proveedor que implementa **Advise** debe conservar una copia del puntero al objeto receptor _lpAdviseSink;_ para ello, llama al método **IUnknown::AddRef** para que el receptor de avisos mantenga su puntero de objeto hasta que se cancele el registro de notificación con una llamada al método [IMAPITable::Unadvise.](imapitable-unadvise.md)</span><span class="sxs-lookup"><span data-stu-id="ba404-128">To provide notifications, the provider implementing **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, it calls the **IUnknown::AddRef** method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMAPITable::Unadvise](imapitable-unadvise.md) method.</span></span> <span data-ttu-id="ba404-129">La implementación de **Advise** debe asignar un número de conexión al registro de notificación y llamar a **AddRef** en este número de conexión antes de devolverlo en el _parámetro lpulConnection._</span><span class="sxs-lookup"><span data-stu-id="ba404-129">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="ba404-130">Los proveedores de servicios pueden liberar el objeto receptor de avisos antes de cancelar el registro, pero no deben liberar el número de conexión hasta que se haya llamado a \*\* Unadvise \*\*.</span><span class="sxs-lookup"><span data-stu-id="ba404-130">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until \*\* Unadvise \*\* has been called.</span></span> 
  
<span data-ttu-id="ba404-131">Una vez que se ha realizado correctamente una llamada a **Advise** y antes de llamar a \*\* Unadvise \*\*, los clientes deben estar preparados para que se pueda liberar el objeto receptor de avisos.</span><span class="sxs-lookup"><span data-stu-id="ba404-131">After a call to **Advise** has succeeded and before \*\* Unadvise \*\* has been called, clients must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="ba404-132">Por lo tanto, un cliente debe liberar el objeto receptor de avisos después de que **advise** vuelva, a menos que tenga un uso específico a largo plazo para él.</span><span class="sxs-lookup"><span data-stu-id="ba404-132">A client should therefore release its advise sink object after **Advise** returns unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="ba404-133">Debido al comportamiento asincrónico de las notificaciones, las implementaciones que cambian la configuración de las columnas de la tabla pueden recibir notificaciones con información organizada en un orden de columna anterior.</span><span class="sxs-lookup"><span data-stu-id="ba404-133">Because of the asynchronous behavior of notification, implementations that change table column settings can receive notifications with information organized in a previous column order.</span></span> <span data-ttu-id="ba404-134">Por ejemplo, se puede devolver una fila de tabla para un mensaje que se acaba de eliminar del contenedor.</span><span class="sxs-lookup"><span data-stu-id="ba404-134">For instance, a table row might be returned for a message that has just been deleted from the container.</span></span> <span data-ttu-id="ba404-135">Dicha notificación se envía cuando se ha realizado el cambio de configuración de columna y se ha enviado información sobre ella, pero la vista de tabla de notificación aún no se ha actualizado con esa información.</span><span class="sxs-lookup"><span data-stu-id="ba404-135">Such a notification is sent when the column setting change has been made and information about it sent but the notification table view has not been updated with that information yet.</span></span>
  
<span data-ttu-id="ba404-136">Para obtener más información sobre el proceso de notificación, vea [Notificación de eventos en MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="ba404-136">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="ba404-137">Para obtener información específica acerca de la notificación de tabla, vea [Acerca de las notificaciones de tabla](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="ba404-137">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="ba404-138">Para obtener información acerca del uso **de los métodos IMAPISupport** para admitir notificaciones, vea [Notificación de eventos auxiliares.](supporting-event-notification.md)</span><span class="sxs-lookup"><span data-stu-id="ba404-138">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ba404-139">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ba404-139">MFCMAPI reference</span></span>

<span data-ttu-id="ba404-140">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ba404-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ba404-141">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ba404-141">**File**</span></span>|<span data-ttu-id="ba404-142">**Función**</span><span class="sxs-lookup"><span data-stu-id="ba404-142">**Function**</span></span>|<span data-ttu-id="ba404-143">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ba404-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ba404-144">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="ba404-144">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="ba404-145">CContestTableListCtrl::NotificationOn</span><span class="sxs-lookup"><span data-stu-id="ba404-145">CContestTableListCtrl::NotificationOn</span></span>  <br/> |<span data-ttu-id="ba404-146">MFCMAPI usa el **método IMAPITable::Advise** para registrar notificaciones con el objeto de permitir que la vista de tabla permanezca actualizada.</span><span class="sxs-lookup"><span data-stu-id="ba404-146">MFCMAPI uses the **IMAPITable::Advise** method to register for notifications to allow the table view to stay current.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba404-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ba404-147">See also</span></span>



[<span data-ttu-id="ba404-148">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="ba404-148">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="ba404-149">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="ba404-149">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="ba404-150">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ba404-150">IMAPITable::Unadvise</span></span>](imapitable-unadvise.md)
  
[<span data-ttu-id="ba404-151">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ba404-151">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="ba404-152">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ba404-152">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="ba404-153">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ba404-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

