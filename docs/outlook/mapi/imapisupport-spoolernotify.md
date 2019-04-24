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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326288"
---
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="8461a-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="8461a-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="8461a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8461a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8461a-105">Notifica a la cola MAPI un cambio de estado o una solicitud de servicio.</span><span class="sxs-lookup"><span data-stu-id="8461a-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="8461a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8461a-106">Parameters</span></span>

 <span data-ttu-id="8461a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8461a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8461a-108">a Máscara de máscara de marcadores que indica el tipo de notificación.</span><span class="sxs-lookup"><span data-stu-id="8461a-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="8461a-109">Los proveedores de transporte pueden establecer todas las marcas excepto NOTIFY_NEWMAIL_RECEIVED; solo NOTIFY_NEWMAIL_RECEIVED y NOTIFY_READTOSEND son válidos para los proveedores de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8461a-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="8461a-110">Las siguientes marcas son válidas para el parámetro _ulFlags_ :</span><span class="sxs-lookup"><span data-stu-id="8461a-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="8461a-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="8461a-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="8461a-112">Registra una solicitud para cambiar la configuración del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="8461a-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="8461a-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="8461a-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="8461a-114">Se ha producido un error irrecuperable en el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="8461a-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="8461a-115">Dado que tanto NOTIFY_SENTDEFERRED como NOTIFY_CRITICAL_ERROR usan el parámetro _lpvData_ para las llamadas de proveedor de transporte, estas marcas se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="8461a-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="8461a-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="8461a-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="8461a-117">Solicita una sección crítica para el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="8461a-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="8461a-118">El parámetro _lpvData_ no está definido y debe ser nulo.</span><span class="sxs-lookup"><span data-stu-id="8461a-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="8461a-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="8461a-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="8461a-120">La cola MAPI debe descargar los mensajes recibidos recientemente en el siguiente momento disponible.</span><span class="sxs-lookup"><span data-stu-id="8461a-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="8461a-121">El parámetro _lpvData_ no está definido y debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="8461a-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="8461a-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="8461a-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="8461a-123">Se ha recibido un mensaje nuevo en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8461a-123">A new message has been received in the message store.</span></span> <span data-ttu-id="8461a-124">El parámetro _lpvData_ apunta a una estructura [NEWMAIL_NOTIFICATION](newmail_notification.md) que describe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8461a-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="8461a-125">Esta marca se usa para los proveedores de almacenamiento de mensajes que están estrechamente asociados con los proveedores de transporte y se omite si el proveedor de almacenamiento inicia sesión con la marca MAPI_NO_MAIL establecida.</span><span class="sxs-lookup"><span data-stu-id="8461a-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="8461a-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="8461a-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="8461a-127">Libera una sección crítica obtenida con una llamada anterior a **SpoolerNotify** con _ULFLAGS_ establecido en NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="8461a-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="8461a-128">El parámetro _lpvData_ no está definido y debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="8461a-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="8461a-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="8461a-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="8461a-130">El proveedor de transporte o de almacenamiento de mensajes está preparado para enviar mensajes.</span><span class="sxs-lookup"><span data-stu-id="8461a-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="8461a-131">El parámetro _lpvData_ no está definido y debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="8461a-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="8461a-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="8461a-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="8461a-133">Ahora debe enviarse un mensaje aplazado anteriormente y el proveedor de transporte debe recibir una notificación cuando el mensaje esté listo para entregarse mediante una llamada al método [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="8461a-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="8461a-134">El identificador de entrada del mensaje aplazado está contenido en una estructura [SBinary](sbinary.md) a la que apunta _lpvData_.</span><span class="sxs-lookup"><span data-stu-id="8461a-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="8461a-135">Como tanto NOTIFY_SENTDEFERRED como NOTIFY_CRITICAL_ERROR usan el parámetro _lpvData_ , estos indicadores se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="8461a-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="8461a-136">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="8461a-136">_lpvData_</span></span>
  
> <span data-ttu-id="8461a-137">a Un puntero a datos asociados aplicables a una notificación.</span><span class="sxs-lookup"><span data-stu-id="8461a-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="8461a-138">El parámetro _lpvData_ apunta a datos válidos solo cuando se establecen los siguientes indicadores (_lpvData_ es NULL cuando _ulFlags_ se establece en los otros tipos de notificación):</span><span class="sxs-lookup"><span data-stu-id="8461a-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="8461a-139">**configuración de _ulFlags_**</span><span class="sxs-lookup"><span data-stu-id="8461a-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="8461a-140">**valor _lpvData_**</span><span class="sxs-lookup"><span data-stu-id="8461a-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8461a-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="8461a-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="8461a-142">Información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="8461a-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="8461a-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="8461a-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="8461a-144">Estructura **NEWMAIL_NOTIFICATION** que contiene información sobre el mensaje recién entregado.</span><span class="sxs-lookup"><span data-stu-id="8461a-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="8461a-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="8461a-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="8461a-146">Estructura **SBinary** que contiene el identificador de entrada del mensaje aplazado.</span><span class="sxs-lookup"><span data-stu-id="8461a-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="8461a-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8461a-147">Return value</span></span>

<span data-ttu-id="8461a-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="8461a-148">S_OK</span></span> 
  
> <span data-ttu-id="8461a-149">La notificación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8461a-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8461a-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8461a-150">Remarks</span></span>

<span data-ttu-id="8461a-151">El método **IMAPISupport:: SpoolerNotify** se implementa para los objetos de soporte de proveedor de transporte y almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8461a-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="8461a-152">Estos proveedores llaman a **SpoolerNotify** para notificar a la cola de MAPI un cambio en el estado o una solicitud de servicio.</span><span class="sxs-lookup"><span data-stu-id="8461a-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="8461a-153">Los proveedores de transporte llaman principalmente a **SpoolerNotify** , que pueden llamarse en cualquier momento durante la sesión.</span><span class="sxs-lookup"><span data-stu-id="8461a-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="8461a-154">Notas para los proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="8461a-154">Notes to Transport Providers</span></span>

<span data-ttu-id="8461a-155">Si ha cambiado la configuración de su proveedor de transporte, llame a **SpoolerNotify** y establezca _ulFlags_ en NOTIFY_CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="8461a-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="8461a-156">**SpoolerNotify** responde llamando al método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) para consultar un cambio en los tipos de direcciones admitidos.</span><span class="sxs-lookup"><span data-stu-id="8461a-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="8461a-157">Si necesita una sección crítica para garantizar un procesamiento sin interrupciones, llame a **SpoolerNotify** con _ULFLAGS_ establecido en NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="8461a-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="8461a-158">Al establecer esta marca se informa a la cola MAPI de que no debe llamar a los métodos [IXPLogon:: idle](ixplogon-idle.md) y [IXPLogon::P Oll](ixplogon-poll.md) .</span><span class="sxs-lookup"><span data-stu-id="8461a-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="8461a-159">Mientras tenga una sección crítica abierta, devuelva MAPI_E_BUSY cada vez que se llame al método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="8461a-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="8461a-160">Cuando haya terminado con la sección crítica, realice otra llamada a **SpoolerNotify** con _ULFLAGS_ establecido en NOTIFY_NONCRIT.</span><span class="sxs-lookup"><span data-stu-id="8461a-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="8461a-161">Por ejemplo, si el proveedor de transporte remoto se encuentra en el proceso de carga de mensajes, es posible que deba permitir a un usuario que escriba un número de teléfono para establecer la conexión remota.</span><span class="sxs-lookup"><span data-stu-id="8461a-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="8461a-162">Antes de recorrer en bucle el procedimiento de cuadro de diálogo, debe declarar una sección crítica.</span><span class="sxs-lookup"><span data-stu-id="8461a-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="8461a-163">Cuando el usuario cierra el cuadro de diálogo y finaliza el procedimiento de cuadro de diálogo, debe liberar la sección crítica.</span><span class="sxs-lookup"><span data-stu-id="8461a-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="8461a-164">Al establecer _ulFlags_ en NOTIFY_CRITICAL_ERROR, la cola MAPI no realiza más llamadas al proveedor excepto para liberarla.</span><span class="sxs-lookup"><span data-stu-id="8461a-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="8461a-165">Si llama a **SpoolerNotify** con NOTIFY_CRITICAL_ERROR establecido desde los métodos [IXPLogon:: StartMessage](ixplogon-startmessage.md) o [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) , devuelve con un valor de error adecuado de la **StartMessage** o \* \* SubmitMessage \* \* llamada inmediatamente después de la llamada a **SpoolerNotify** .</span><span class="sxs-lookup"><span data-stu-id="8461a-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or \*\* SubmitMessage \*\* call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="8461a-166">Si el proveedor de transporte se recuperó a partir de una condición que antes producía un error, llame a **SpoolerNotify** con _ULFLAGS_ establecido en NOTIFY_READYTOSEND.</span><span class="sxs-lookup"><span data-stu-id="8461a-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="8461a-167">Esta marca indica que el proveedor está de nuevo preparado para controlar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="8461a-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="8461a-168">Notas a los proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="8461a-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="8461a-169">Llame a **SpoolerNotify**, pasando la marca NOTIFY_READYTOSEND en _ulFlags_, antes de realizar la primera llamada a [IMAPISupport::P Reparesubmit](imapisupport-preparesubmit.md) en **IMessage:: SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="8461a-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="8461a-170">Esta llamada a **SpoolerNotify** debe realizarse una sola vez por sesión.</span><span class="sxs-lookup"><span data-stu-id="8461a-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="8461a-171">Si su proveedor de almacenamiento de mensajes está estrechamente acoplado a un proveedor de transporte y llama a **SpoolerNotify** con _ULFLAGS_ establecido en NOTIFY_NEWMAIL_RECEIVED, la cola MAPI abre el nuevo mensaje y comienza el procesamiento de la nueva función de enlace de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8461a-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="8461a-172">Una vez finalizado el procesamiento, la cola MAPI llama al método [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) para informarle de su propio mensaje.</span><span class="sxs-lookup"><span data-stu-id="8461a-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="8461a-173">Para obtener más información acerca de cómo llamar a **SpoolerNotify**, vea cualquiera de los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="8461a-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="8461a-174">Implementar el método FlushQueues</span><span class="sxs-lookup"><span data-stu-id="8461a-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="8461a-175">Interacción con la cola MAPI</span><span class="sxs-lookup"><span data-stu-id="8461a-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="8461a-176">Modelo de recepción de mensajes</span><span class="sxs-lookup"><span data-stu-id="8461a-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="8461a-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="8461a-177">See also</span></span>



[<span data-ttu-id="8461a-178">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="8461a-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="8461a-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="8461a-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="8461a-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="8461a-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="8461a-181">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8461a-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

