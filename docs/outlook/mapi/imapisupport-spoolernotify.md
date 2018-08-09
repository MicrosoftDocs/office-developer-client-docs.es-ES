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
ms.openlocfilehash: 21ea5faaccb81e763d6d062b6ff567db509d9d35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817549"
---
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="5d8a0-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="5d8a0-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="5d8a0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5d8a0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5d8a0-105">Notifica a la cola MAPI de un cambio de estado o una solicitud de servicio.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="5d8a0-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="5d8a0-106">Parameters</span></span>

 <span data-ttu-id="5d8a0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5d8a0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5d8a0-108">[entrada] Una máscara de bits de marcadores que indica el tipo de notificación.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="5d8a0-109">Los proveedores de transporte pueden establecer todas las marcas excepto NOTIFY_NEWMAIL_RECEIVED; sólo NOTIFY_NEWMAIL_RECEIVED y NOTIFY_READTOSEND son válidos para los proveedores de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="5d8a0-110">Las siguientes marcas son válidas para el parámetro _ulFlags indicado_ :</span><span class="sxs-lookup"><span data-stu-id="5d8a0-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="5d8a0-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="5d8a0-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="5d8a0-112">Registra una solicitud para cambiar la configuración del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="5d8a0-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="5d8a0-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="5d8a0-114">Se ha producido un error irrecuperable al proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="5d8a0-115">Dado que NOTIFY_SENTDEFERRED y NOTIFY_CRITICAL_ERROR usan el parámetro _lpvData_ para las llamadas del proveedor de transporte, estos marcadores son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="5d8a0-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="5d8a0-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="5d8a0-117">Solicita una sección crítica para el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="5d8a0-118">El parámetro _lpvData_ no está definido y debe ser nulo.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="5d8a0-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="5d8a0-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="5d8a0-120">La cola MAPI debe descargar todos los mensajes recibidos recientemente en la siguiente hora disponible.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="5d8a0-121">El parámetro _lpvData_ no está definido y debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="5d8a0-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="5d8a0-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="5d8a0-123">Se ha recibido un mensaje nuevo en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-123">A new message has been received in the message store.</span></span> <span data-ttu-id="5d8a0-124">El parámetro _lpvData_ apunta a una estructura [NEWMAIL_NOTIFICATION](newmail_notification.md) que describe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="5d8a0-125">Este indicador se usa para los proveedores de almacén de mensajes que estén asociados estrechamente con los proveedores de transporte y se omite si el proveedor de almacenamiento se inició sesión con el conjunto de marca MAPI_NO_MAIL.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="5d8a0-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="5d8a0-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="5d8a0-127">Libera una sección crítica que se obtuvieron con una llamada anterior a **SpoolerNotify** con _ulFlags_ establecida en NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="5d8a0-128">El parámetro _lpvData_ no está definido y debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="5d8a0-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="5d8a0-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="5d8a0-130">El proveedor de almacén de transporte o un mensaje está listo para enviar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="5d8a0-131">El parámetro _lpvData_ no está definido y debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="5d8a0-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="5d8a0-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="5d8a0-133">Ahora se debe enviar un mensaje diferido anteriormente, y el proveedor de transporte debe recibir una notificación cuando el mensaje está listo para entregar mediante una llamada al método [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="5d8a0-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="5d8a0-134">El identificador de entrada del mensaje diferido se encuentra en una estructura [SBinary](sbinary.md) que señala _lpvData_.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="5d8a0-135">Dado que NOTIFY_SENTDEFERRED y NOTIFY_CRITICAL_ERROR usan el parámetro _lpvData_ , estos marcadores son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="5d8a0-136">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="5d8a0-136">_lpvData_</span></span>
  
> <span data-ttu-id="5d8a0-137">[entrada] Un puntero a datos asociados aplicables a una notificación.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="5d8a0-138">El parámetro _lpvData_ apunta a datos válidos sólo cuando se establecen los siguientes indicadores (_lpvData_ es NULL cuando _ulFlags_ está establecida en los otros tipos de notificación):</span><span class="sxs-lookup"><span data-stu-id="5d8a0-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="5d8a0-139">**configuración de _ulFlags_**</span><span class="sxs-lookup"><span data-stu-id="5d8a0-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="5d8a0-140">**valor de _lpvData_**</span><span class="sxs-lookup"><span data-stu-id="5d8a0-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5d8a0-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="5d8a0-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="5d8a0-142">Información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="5d8a0-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="5d8a0-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="5d8a0-144">Una estructura **NEWMAIL_NOTIFICATION** que contiene información acerca del mensaje recién enviado.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="5d8a0-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="5d8a0-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="5d8a0-146">Una estructura **SBinary** que contiene el identificador de entrada del mensaje diferido.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="5d8a0-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d8a0-147">Return value</span></span>

<span data-ttu-id="5d8a0-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="5d8a0-148">S_OK</span></span> 
  
> <span data-ttu-id="5d8a0-149">La notificación fue correcta.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5d8a0-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d8a0-150">Remarks</span></span>

<span data-ttu-id="5d8a0-151">Se implementa el método **SpoolerNotify** para mensaje almacenar y objetos de soporte técnico del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="5d8a0-152">Estos proveedores de llamadas **SpoolerNotify** para notificar a la cola MAPI de un cambio de estado o una solicitud de servicio.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="5d8a0-153">**SpoolerNotify** se denomina principalmente por proveedores de transporte y se puede llamar en cualquier momento durante la sesión.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="5d8a0-154">Notas para los proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="5d8a0-154">Notes to Transport Providers</span></span>

<span data-ttu-id="5d8a0-155">Si ha cambiado la configuración del proveedor de transporte, llame **SpoolerNotify** y establezca _ulFlags_ en NOTIFY_CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="5d8a0-156">**SpoolerNotify** responde llamando al método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para consultar un cambio en los tipos de direcciones compatibles.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="5d8a0-157">Si necesita una sección crítica para asegurar el procesamiento ininterrumpido, llame a **SpoolerNotify** con _ulFlags_ establecida en NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="5d8a0-158">Al establecer este indicador informa a la cola de MAPI que no debe llamar a los métodos [IXPLogon::Idle](ixplogon-idle.md) y [IXPLogon::Poll](ixplogon-poll.md) .</span><span class="sxs-lookup"><span data-stu-id="5d8a0-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="5d8a0-159">Mientras tenga abierta una sección crítica, devolver MAPI_E_BUSY cada vez que se llama al método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="5d8a0-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="5d8a0-160">Cuando haya terminado con la sección crítica, realizar otra llamada a **SpoolerNotify** con _ulFlags_ establecida en NOTIFY_NONCRIT.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="5d8a0-161">Por ejemplo, si su proveedor de transporte remoto está en proceso de carga de los mensajes, es posible que necesite permitir que un usuario que escriba un número de teléfono para establecer la conexión remota.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="5d8a0-162">Antes de recorrer el procedimiento de cuadro de diálogo, se debe declarar una sección crítica.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="5d8a0-163">Cuando el usuario cierra el cuadro de diálogo, terminar el procedimiento de cuadro de diálogo, debe liberar la sección crítica.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="5d8a0-164">Cuando se establece _ulFlags_ a NOTIFY_CRITICAL_ERROR, la cola MAPI hace que no hay más llamadas para el proveedor excepto al liberarlo.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="5d8a0-165">Si se llama **SpoolerNotify** con NOTIFY_CRITICAL_ERROR establecer uno de los métodos [IXPLogon::StartMessage](ixplogon-startmessage.md) o [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) , devolver con un valor de error apropiado desde el que **desea iniciar** o ** SubmitMessage ** de llamadas inmediatamente después de la llamada **SpoolerNotify** .</span><span class="sxs-lookup"><span data-stu-id="5d8a0-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or ** SubmitMessage ** call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="5d8a0-166">Si su proveedor de transporte recupera de una condición que previamente ha provocado un error, llame a **SpoolerNotify** con _ulFlags_ establecida en NOTIFY_READYTOSEND.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="5d8a0-167">Esta marca indica que el proveedor de nuevo está listo para administrar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="5d8a0-168">Notas para los proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="5d8a0-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="5d8a0-169">Llamar a **SpoolerNotify**, se pasa el indicador NOTIFY_READYTOSEND en _ulFlags_, antes de realizar su primera llamada a [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) en **IMessage::SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="5d8a0-170">Esta llamada a **SpoolerNotify** debe realizarse sólo una vez por sesión.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="5d8a0-171">Si su proveedor de almacén de mensajes se complementa con un transporte de proveedor y llame a **SpoolerNotify** con conjunto de _ulFlags_ a NOTIFY_NEWMAIL_RECEIVED, la cola MAPI abre el mensaje nuevo y comienza el procesamiento de la función de enlace de mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="5d8a0-172">Una vez completado el procesamiento, la cola MAPI llama al método [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) para informarle de su propio mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="5d8a0-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="5d8a0-173">Para obtener más información sobre cómo llamar a **SpoolerNotify**, vea cualquiera de los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="5d8a0-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="5d8a0-174">Implementar el método FlushQueues</span><span class="sxs-lookup"><span data-stu-id="5d8a0-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="5d8a0-175">Interactuar con el administrador de trabajos en cola MAPI</span><span class="sxs-lookup"><span data-stu-id="5d8a0-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="5d8a0-176">Modelo de recepción del mensaje</span><span class="sxs-lookup"><span data-stu-id="5d8a0-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="5d8a0-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d8a0-177">See also</span></span>



[<span data-ttu-id="5d8a0-178">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="5d8a0-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="5d8a0-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="5d8a0-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="5d8a0-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="5d8a0-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="5d8a0-181">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5d8a0-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

