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
ms.openlocfilehash: cd6b119bd88fccf80bf2488592a24b3398e6e8af
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594246"
---
# <a name="imapitableadvise"></a><span data-ttu-id="c210a-103">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="c210a-103">IMAPITable::Advise</span></span>

  
  
<span data-ttu-id="c210a-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c210a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c210a-105">Registra un objeto de receptor advise para recibir notificaciones de los eventos que afectan a la tabla.</span><span class="sxs-lookup"><span data-stu-id="c210a-105">Registers an advise sink object to receive notification of specified events affecting the table.</span></span>
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="c210a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c210a-106">Parameters</span></span>

 <span data-ttu-id="c210a-107">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="c210a-107">_ulEventMask_</span></span>
  
> <span data-ttu-id="c210a-108">[entrada] Valor que indica el tipo de evento que se va a generar la notificación.</span><span class="sxs-lookup"><span data-stu-id="c210a-108">[in] Value indicating the type of event that will generate the notification.</span></span> <span data-ttu-id="c210a-109">Sólo el valor siguiente es válido:</span><span class="sxs-lookup"><span data-stu-id="c210a-109">Only the following value is valid:</span></span>
    
 `fnevTableModified`
  
 <span data-ttu-id="c210a-110">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="c210a-110">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="c210a-111">[entrada] Puntero a un objeto de receptor advise para recibir las notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c210a-111">[in] Pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="c210a-112">Debe se han asignado ya este objeto de receptor advise.</span><span class="sxs-lookup"><span data-stu-id="c210a-112">This advise sink object must have been already allocated.</span></span>
    
 <span data-ttu-id="c210a-113">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="c210a-113">_lpulConnection_</span></span>
  
> <span data-ttu-id="c210a-114">[out] Puntero a un valor distinto de cero que representa el registro de notificación correcta.</span><span class="sxs-lookup"><span data-stu-id="c210a-114">[out] Pointer to a nonzero value that represents the successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c210a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c210a-115">Return value</span></span>

<span data-ttu-id="c210a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="c210a-116">S_OK</span></span> 
  
> <span data-ttu-id="c210a-117">El registro de notificación que se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c210a-117">The notification registration successfully completed.</span></span>
    
<span data-ttu-id="c210a-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c210a-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c210a-119">La implementación de la tabla no es compatible con los cambios realizados en sus filas y columnas o no admite la notificación.</span><span class="sxs-lookup"><span data-stu-id="c210a-119">The table implementation either does not support changes to its rows and columns or does not support notification.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c210a-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c210a-120">Remarks</span></span>

<span data-ttu-id="c210a-121">Utilice el método **IMAPITable::Advise** para registrar un objeto de tabla implementado en el proveedor para realizar devoluciones de llamadas de notificación.</span><span class="sxs-lookup"><span data-stu-id="c210a-121">Use the **IMAPITable::Advise** method to register a table object implemented in the provider for notification callbacks.</span></span> <span data-ttu-id="c210a-122">Cada vez que se produce un cambio en el objeto table, el proveedor comprueba qué bit de máscara de eventos se estableció en el parámetro _ulEventMask_ y, por tanto, ¿qué tipo de cambio se ha producido.</span><span class="sxs-lookup"><span data-stu-id="c210a-122">Whenever a change occurs to the table object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and thus what type of change occurred.</span></span> <span data-ttu-id="c210a-123">Si un bit está establecido, a continuación, el proveedor llama al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto de receptor advise indicado por el parámetro _lpAdviseSink_ para notificar el evento.</span><span class="sxs-lookup"><span data-stu-id="c210a-123">If a bit is set, then the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="c210a-124">Datos que se pasan en la estructura de notificación a la rutina de **OnNotify** describen el evento.</span><span class="sxs-lookup"><span data-stu-id="c210a-124">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="c210a-125">La llamada a **OnNotify** puede producirse durante la llamada que cambia el objeto, o en cualquier momento siguiente.</span><span class="sxs-lookup"><span data-stu-id="c210a-125">The call to **OnNotify** can occur during the call that changes the object, or at any following time.</span></span> <span data-ttu-id="c210a-126">En los sistemas que admiten varios subprocesos de ejecución, puede producirse la llamada a **OnNotify** en cualquier subproceso.</span><span class="sxs-lookup"><span data-stu-id="c210a-126">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="c210a-127">Para que una forma de convertir una llamada a **OnNotify** que puede suceder en un momento inoportuno en uno que es más seguro administrar, un proveedor debe usar la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="c210a-127">For a way to turn a call to **OnNotify** that might happen at an inopportune time into one that is safer to handle, a provider should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="c210a-128">Para proporcionar notificaciones, de las necesidades de **Advise** implementación del proveedor para mantener una copia del puntero a la _lpAdviseSink_ aviso objeto receptor; Para ello, se llama al método **IUnknown:: AddRef** para el receptor de notificaciones mantener su puntero del objeto hasta que se cancele el registro de la notificación con una llamada al método [IMAPITable::Unadvise](imapitable-unadvise.md) .</span><span class="sxs-lookup"><span data-stu-id="c210a-128">To provide notifications, the provider implementing **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, it calls the **IUnknown::AddRef** method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMAPITable::Unadvise](imapitable-unadvise.md) method.</span></span> <span data-ttu-id="c210a-129">La implementación de **Advise** debe asignar a un número de conexión para el registro de la notificación y llamar a **AddRef** en este número de conexión antes de devolver en el parámetro _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="c210a-129">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="c210a-130">Proveedores de servicios pueden liberar el objeto de receptor de advise antes de que se ha cancelado el registro, pero no debe liberar el número de conexión hasta \*\* Unadvise \*\* se ha llamado.</span><span class="sxs-lookup"><span data-stu-id="c210a-130">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until \*\* Unadvise \*\* has been called.</span></span> 
  
<span data-ttu-id="c210a-131">Después de que se ha realizado correctamente una llamada a **Advise** y antes de \*\* Unadvise \*\* ha sido llamado, es preciso preparar los clientes para que el objeto de receptor advise que liberar.</span><span class="sxs-lookup"><span data-stu-id="c210a-131">After a call to **Advise** has succeeded and before \*\* Unadvise \*\* has been called, clients must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="c210a-132">Un cliente, por tanto, debe liberar su objeto de receptor advise después **Advise** devuelve a menos que tenga un uso a largo plazo específico para él.</span><span class="sxs-lookup"><span data-stu-id="c210a-132">A client should therefore release its advise sink object after **Advise** returns unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="c210a-133">Debido al comportamiento asincrónico de notificación, las implementaciones que cambiar la configuración de columna de tabla pueden recibir notificaciones con información organizada en un orden de la columna anterior.</span><span class="sxs-lookup"><span data-stu-id="c210a-133">Because of the asynchronous behavior of notification, implementations that change table column settings can receive notifications with information organized in a previous column order.</span></span> <span data-ttu-id="c210a-134">Por ejemplo, es posible que devuelve una fila de tabla para un mensaje que sólo se ha eliminado del contenedor.</span><span class="sxs-lookup"><span data-stu-id="c210a-134">For instance, a table row might be returned for a message that has just been deleted from the container.</span></span> <span data-ttu-id="c210a-135">Se envía una notificación cuando se ha realizado el cambio de configuración de columna y envía información acerca de él, pero la vista de tabla de notificación no se ha actualizado con esa información todavía.</span><span class="sxs-lookup"><span data-stu-id="c210a-135">Such a notification is sent when the column setting change has been made and information about it sent but the notification table view has not been updated with that information yet.</span></span>
  
<span data-ttu-id="c210a-136">Para obtener más información sobre el proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="c210a-136">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="c210a-137">Para obtener información específica acerca de la notificación de la tabla, vea [Acerca de las notificaciones de tabla](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="c210a-137">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="c210a-138">Para obtener información acerca del uso de los métodos **IMAPISupport** para admitir la notificación, vea [Compatibilidad con notificación de evento](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="c210a-138">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c210a-139">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c210a-139">MFCMAPI reference</span></span>

<span data-ttu-id="c210a-140">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="c210a-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c210a-141">**File**</span><span class="sxs-lookup"><span data-stu-id="c210a-141">**File**</span></span>|<span data-ttu-id="c210a-142">**Función**</span><span class="sxs-lookup"><span data-stu-id="c210a-142">**Function**</span></span>|<span data-ttu-id="c210a-143">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="c210a-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c210a-144">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="c210a-144">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="c210a-145">CContestTableListCtrl::NotificationOn</span><span class="sxs-lookup"><span data-stu-id="c210a-145">CContestTableListCtrl::NotificationOn</span></span>  <br/> |<span data-ttu-id="c210a-146">MFCMAPI utiliza el método **IMAPITable::Advise** para registrar para que las notificaciones permitir la vista de tabla para mantenerse al día.</span><span class="sxs-lookup"><span data-stu-id="c210a-146">MFCMAPI uses the **IMAPITable::Advise** method to register for notifications to allow the table view to stay current.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c210a-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="c210a-147">See also</span></span>



[<span data-ttu-id="c210a-148">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="c210a-148">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="c210a-149">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="c210a-149">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="c210a-150">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="c210a-150">IMAPITable::Unadvise</span></span>](imapitable-unadvise.md)
  
[<span data-ttu-id="c210a-151">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c210a-151">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="c210a-152">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c210a-152">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="c210a-153">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="c210a-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

