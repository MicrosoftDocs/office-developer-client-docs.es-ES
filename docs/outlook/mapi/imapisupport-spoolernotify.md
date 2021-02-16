---
title: IMAPISupportSpoolerNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerNotify
api_type:
- COM
ms.assetid: d4f153b2-939f-4153-85fb-dc510193848c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 99377d63b4b5cf8731809446b70770f0c24231ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423772"
---
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="e55ab-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="e55ab-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="e55ab-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e55ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e55ab-105">Notifica a la cola MAPI de un cambio de estado o una solicitud de servicio.</span><span class="sxs-lookup"><span data-stu-id="e55ab-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="e55ab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e55ab-106">Parameters</span></span>

 <span data-ttu-id="e55ab-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e55ab-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e55ab-108">[entrada] Máscara de bits de marcas que indica el tipo de notificación.</span><span class="sxs-lookup"><span data-stu-id="e55ab-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="e55ab-109">Los proveedores de transporte pueden establecer todas las marcas excepto las NOTIFY_NEWMAIL_RECEIVED; solo NOTIFY_NEWMAIL_RECEIVED y NOTIFY_READTOSEND son válidos para los proveedores de al almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e55ab-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="e55ab-110">Las siguientes marcas son válidas para el _parámetro ulFlags:_</span><span class="sxs-lookup"><span data-stu-id="e55ab-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="e55ab-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="e55ab-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="e55ab-112">Registra una solicitud para cambiar la configuración del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="e55ab-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="e55ab-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="e55ab-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="e55ab-114">Se ha producido un error irrecuperable al proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="e55ab-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="e55ab-115">Dado que NOTIFY_SENTDEFERRED y NOTIFY_CRITICAL_ERROR usan el parámetro  _lpvData_ para las llamadas del proveedor de transporte, estas marcas son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="e55ab-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="e55ab-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="e55ab-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="e55ab-117">Solicita una sección crítica para el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="e55ab-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="e55ab-118">El  _parámetro lpvData_ no está definido y debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="e55ab-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="e55ab-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="e55ab-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="e55ab-120">La cola MAPI debe descargar los mensajes recién recibidos en la próxima hora disponible.</span><span class="sxs-lookup"><span data-stu-id="e55ab-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="e55ab-121">El  _parámetro lpvData_ no está definido y debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="e55ab-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="e55ab-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="e55ab-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="e55ab-123">Se ha recibido un nuevo mensaje en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e55ab-123">A new message has been received in the message store.</span></span> <span data-ttu-id="e55ab-124">El  _parámetro lpvData_ apunta a una [NEWMAIL_NOTIFICATION](newmail_notification.md) que describe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e55ab-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="e55ab-125">Esta marca se usa para los proveedores de almacenamiento de mensajes estrechamente asociados con los proveedores de transporte y se omite si el proveedor de almacenamiento ha iniciado sesión con la marca MAPI_NO_MAIL establecida.</span><span class="sxs-lookup"><span data-stu-id="e55ab-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="e55ab-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="e55ab-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="e55ab-127">Libera una sección crítica que se obtuvo con una llamada anterior a **SpoolerNotify** con  _ulFlags_ establecido en NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="e55ab-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="e55ab-128">El  _parámetro lpvData_ no está definido y debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="e55ab-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="e55ab-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="e55ab-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="e55ab-130">El proveedor de transporte o almacén de mensajes está listo para enviar mensajes.</span><span class="sxs-lookup"><span data-stu-id="e55ab-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="e55ab-131">El  _parámetro lpvData_ no está definido y debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="e55ab-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="e55ab-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="e55ab-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="e55ab-133">Ahora se debe enviar un mensaje aplazado anteriormente y se debe notificar al proveedor de transporte cuando el mensaje esté listo para entregarse mediante una llamada al método [IXPLogon::SubmitMessage.](ixplogon-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="e55ab-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="e55ab-134">El identificador de entrada del mensaje diferido está contenido en una estructura [SBinary](sbinary.md) a la que  _apunta lpvData_.</span><span class="sxs-lookup"><span data-stu-id="e55ab-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="e55ab-135">Dado que NOTIFY_SENTDEFERRED y NOTIFY_CRITICAL_ERROR usan el parámetro  _lpvData,_ estas marcas son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="e55ab-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="e55ab-136">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="e55ab-136">_lpvData_</span></span>
  
> <span data-ttu-id="e55ab-137">[entrada] Puntero a los datos asociados aplicables a una notificación.</span><span class="sxs-lookup"><span data-stu-id="e55ab-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="e55ab-138">El  _parámetro lpvData_ apunta a datos válidos solo cuando se establecen las siguientes marcas (_lpvData_ es NULL cuando  _ulFlags_ se establece en los otros tipos de notificación):</span><span class="sxs-lookup"><span data-stu-id="e55ab-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="e55ab-139">**_Configuración de ulFlags_**</span><span class="sxs-lookup"><span data-stu-id="e55ab-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="e55ab-140">**_Valor lpvData_**</span><span class="sxs-lookup"><span data-stu-id="e55ab-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e55ab-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="e55ab-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="e55ab-142">Información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="e55ab-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="e55ab-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="e55ab-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="e55ab-144">Una **NEWMAIL_NOTIFICATION** que contiene información sobre el mensaje recién entregado.</span><span class="sxs-lookup"><span data-stu-id="e55ab-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="e55ab-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="e55ab-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="e55ab-146">Estructura **SBinary** que contiene el identificador de entrada del mensaje diferido.</span><span class="sxs-lookup"><span data-stu-id="e55ab-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="e55ab-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e55ab-147">Return value</span></span>

<span data-ttu-id="e55ab-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="e55ab-148">S_OK</span></span> 
  
> <span data-ttu-id="e55ab-149">La notificación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e55ab-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e55ab-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e55ab-150">Remarks</span></span>

<span data-ttu-id="e55ab-151">El **método IMAPISupport::SpoolerNotify** se implementa para objetos de soporte de almacén de mensajes y proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="e55ab-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="e55ab-152">Estos proveedores llaman **a SpoolerNotify para** notificar a la cola MAPI de un cambio de estado o una solicitud de servicio.</span><span class="sxs-lookup"><span data-stu-id="e55ab-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="e55ab-153">Los proveedores de transporte llaman principalmente a SpoolerNotify y se puede llamar a **SpoolerNotify** en cualquier momento durante la sesión.</span><span class="sxs-lookup"><span data-stu-id="e55ab-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="e55ab-154">Notas para proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="e55ab-154">Notes to Transport Providers</span></span>

<span data-ttu-id="e55ab-155">Si ha cambiado la configuración del proveedor de transporte, llame a **SpoolerNotify** y establezca  _ulFlags_ en NOTIFY_CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="e55ab-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="e55ab-156">**SpoolerNotify** responde llamando al método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para consultar un cambio en los tipos de direcciones admitidos.</span><span class="sxs-lookup"><span data-stu-id="e55ab-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="e55ab-157">Si necesita una sección crítica para garantizar un procesamiento ininterrumpido, llame a **SpoolerNotify** con  _ulFlags_ establecido en NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="e55ab-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="e55ab-158">Al establecer esta marca se informa a la cola MAPI de que no debe llamar a los métodos [IXPLogon::Idle](ixplogon-idle.md) e [IXPLogon::P oll.](ixplogon-poll.md)</span><span class="sxs-lookup"><span data-stu-id="e55ab-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="e55ab-159">Mientras tenga abierta una sección crítica, MAPI_E_BUSY cada vez que se llame al método [IMAPIStatus::ValidateState.](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="e55ab-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="e55ab-160">Cuando haya terminado con la sección crítica, realice otra llamada a **SpoolerNotify** con  _ulFlags_ establecido en NOTIFY_NONCRIT.</span><span class="sxs-lookup"><span data-stu-id="e55ab-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="e55ab-161">Por ejemplo, si su proveedor de transporte remoto está cargando mensajes, es posible que tenga que permitir que un usuario escriba un número de teléfono para establecer la conexión remota.</span><span class="sxs-lookup"><span data-stu-id="e55ab-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="e55ab-162">Antes de recorrer en bucle el procedimiento del cuadro de diálogo, debe declarar una sección crítica.</span><span class="sxs-lookup"><span data-stu-id="e55ab-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="e55ab-163">Cuando el usuario cierre el cuadro de diálogo, finalizando el procedimiento del cuadro de diálogo, debe liberar la sección crítica.</span><span class="sxs-lookup"><span data-stu-id="e55ab-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="e55ab-164">Cuando se establece  _ulFlags_ en NOTIFY_CRITICAL_ERROR, la cola MAPI no realiza ninguna otra llamada al proveedor excepto para liberarla.</span><span class="sxs-lookup"><span data-stu-id="e55ab-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="e55ab-165">Si llama NOTIFY_CRITICAL_ERROR **SpoolerNotify** con un conjunto desde los métodos [IXPLogon::StartMessage](ixplogon-startmessage.md) o [IXPLogon::SubmitMessage,](ixplogon-submitmessage.md) vuelva con un valor de error apropiado de la llamada **StartMessage** o \*\* SubmitMessage \*\* inmediatamente después de la llamada **SpoolerNotify.**</span><span class="sxs-lookup"><span data-stu-id="e55ab-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or \*\* SubmitMessage \*\* call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="e55ab-166">Si el proveedor de transporte se recuperó de una condición que anteriormente causó un error, llame a **SpoolerNotify** con  _ulFlags_ establecido en NOTIFY_READYTOSEND.</span><span class="sxs-lookup"><span data-stu-id="e55ab-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="e55ab-167">Esta marca indica que el proveedor está de nuevo listo para administrar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="e55ab-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="e55ab-168">Notas para proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="e55ab-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="e55ab-169">Llame a **SpoolerNotify**, pasando la marca NOTIFY_READYTOSEND en  _ulFlags_, antes de realizar la primera llamada a [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) en **IMessage::SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="e55ab-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="e55ab-170">Esta llamada a **SpoolerNotify** solo debe realizarse una vez por sesión.</span><span class="sxs-lookup"><span data-stu-id="e55ab-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="e55ab-171">Si el proveedor de almacenamiento de mensajes está estrechamente unido a un proveedor de transporte y llama a **SpoolerNotify** con  _ulFlags_ establecido en NOTIFY_NEWMAIL_RECEIVED, la cola MAPI abre el nuevo mensaje y comienza a procesar la nueva función de enlace de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e55ab-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="e55ab-172">Una vez completado el procesamiento, la cola MAPI llama al método [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) para informarle de su propio mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="e55ab-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="e55ab-173">Para obtener más información acerca de **cómo llamar a SpoolerNotify,** consulte cualquiera de los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="e55ab-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="e55ab-174">Implementación del método FlushQueues</span><span class="sxs-lookup"><span data-stu-id="e55ab-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="e55ab-175">Interactuar con la cola MAPI</span><span class="sxs-lookup"><span data-stu-id="e55ab-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="e55ab-176">Modelo de recepción de mensajes</span><span class="sxs-lookup"><span data-stu-id="e55ab-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="e55ab-177">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e55ab-177">See also</span></span>



[<span data-ttu-id="e55ab-178">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="e55ab-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="e55ab-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="e55ab-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="e55ab-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="e55ab-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="e55ab-181">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e55ab-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

