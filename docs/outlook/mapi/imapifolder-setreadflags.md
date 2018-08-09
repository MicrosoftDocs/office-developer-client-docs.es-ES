---
title: IMAPIFolderSetReadFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetReadFlags
api_type:
- COM
ms.assetid: 95a40c8a-0a8b-46c7-a07a-cbc6a7de8a3c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a52c0501040d77ddb8172b212bf341a08704dcc3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817249"
---
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="098bd-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="098bd-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="098bd-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="098bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="098bd-105">Establece o borra el indicador MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uno o varios de los mensajes de la carpeta y administra el envío de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="098bd-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="098bd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="098bd-106">Parameters</span></span>

<span data-ttu-id="098bd-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="098bd-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="098bd-108">[entrada] Un puntero a una matriz de estructuras [ENTRYLIST](entrylist.md) que identifican el mensaje o los mensajes que han leído marcas para activar o desactivar.</span><span class="sxs-lookup"><span data-stu-id="098bd-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="098bd-109">Si _lpMsgList_ se establece en NULL, la lectura marcas para todos los mensajes de la carpeta se establece o desactivados.</span><span class="sxs-lookup"><span data-stu-id="098bd-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="098bd-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="098bd-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="098bd-111">[entrada] Identificador de la ventana principal del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="098bd-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="098bd-112">El parámetro _ulUIParam_ se omite a menos que se establece la marca MESSAGE_DIALOG en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="098bd-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="098bd-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="098bd-113">_lpProgress_</span></span>
  
> <span data-ttu-id="098bd-114">[entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="098bd-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="098bd-115">Si se pasa NULL en _lpProgress_, el proveedor de almacén de mensajes muestra un indicador de progreso mediante la implementación de MAPI.</span><span class="sxs-lookup"><span data-stu-id="098bd-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="098bd-116">El parámetro _lpProgress_ se omite a menos que se establece la marca MESSAGE_DIALOG en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="098bd-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="098bd-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="098bd-117">_ulFlags_</span></span>
  
> <span data-ttu-id="098bd-118">[entrada] Una máscara de bits de indicadores que controla la configuración de indicador de lectura de un mensaje y el procesamiento de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="098bd-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="098bd-119">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="098bd-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="098bd-120">CLEAR_READ_FLAG: Se debe borrar la marca MSGFLAG_READ en **PR_MESSAGE_FLAGS** y no se debe enviar un informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="098bd-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="098bd-121">CLEAR_NRN_PENDING: Se debe borrar la marca MSGFLAG_NRN_PENDING en **PR_MESSAGE_FLAGS** y no se debe enviar un informe de no leído.</span><span class="sxs-lookup"><span data-stu-id="098bd-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="098bd-122">CLEAR_RN_PENDING: Se debe borrar la marca MSGFLAG_RN_PENDING en **PR_MESSAGE_FLAGS** y no se debe enviar un informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="098bd-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="098bd-123">GENERATE_RECEIPT_ONLY: Se debe enviar un informe de lectura si uno está pendiente, pero no debe haber ningún cambio en el estado de la marca MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="098bd-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="098bd-124">MAPI_DEFERRED_ERRORS: Permite **SetReadFlags** devolver de correctamente, posiblemente antes de que la operación ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="098bd-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="098bd-125">MESSAGE_DIALOG: Muestra un indicador de progreso mientras se realiza la operación.</span><span class="sxs-lookup"><span data-stu-id="098bd-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="098bd-126">SUPPRESS_RECEIPT: Se debe cancelar un informe de lectura pendiente si se solicita un informe de lectura y esta llamada cambia el estado del mensaje de no leído a leer.</span><span class="sxs-lookup"><span data-stu-id="098bd-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="098bd-127">Si esta llamada no cambia el estado del mensaje, el proveedor de almacenamiento de mensajes puede pasar por alto esta marca.</span><span class="sxs-lookup"><span data-stu-id="098bd-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="098bd-128">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="098bd-128">Return values</span></span>

<span data-ttu-id="098bd-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="098bd-129">S_OK</span></span> 
  
> <span data-ttu-id="098bd-130">El indicador de lectura para el mensaje especificado o los mensajes se ha establecido correctamente o se desactiva.</span><span class="sxs-lookup"><span data-stu-id="098bd-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="098bd-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="098bd-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="098bd-132">El proveedor de almacén de mensajes no es compatible con la supresión de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="098bd-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="098bd-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="098bd-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="098bd-134">Una de las siguientes combinaciones incompatibles de flags se establece en el parámetro _ulFlags indicado_ :</span><span class="sxs-lookup"><span data-stu-id="098bd-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="098bd-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="098bd-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="098bd-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="098bd-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="098bd-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="098bd-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="098bd-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="098bd-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="098bd-139">La llamada se ha realizado correctamente, pero no todos los mensajes se han procesado correctamente.</span><span class="sxs-lookup"><span data-stu-id="098bd-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="098bd-140">Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="098bd-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="098bd-141">Para probar esta advertencia, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="098bd-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="098bd-142">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="098bd-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="098bd-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="098bd-143">Remarks</span></span>

<span data-ttu-id="098bd-144">El método **IMAPIFolder::SetReadFlags** establece o borra el indicador MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** de uno o varios de los mensajes de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="098bd-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="098bd-145">Establecer el indicador MSGFLAG_READ marca un mensaje como lectura, que no necesariamente indica que el destinatario realmente ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="098bd-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="098bd-146">**SetReadFlags** también administra el envío de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="098bd-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="098bd-147">No se puede cambiar la marca de lectura para los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="098bd-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="098bd-148">Mensajes que no existen.</span><span class="sxs-lookup"><span data-stu-id="098bd-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="098bd-149">Los mensajes que se han moverán a otro lugar.</span><span class="sxs-lookup"><span data-stu-id="098bd-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="098bd-150">Mensajes que están abiertos con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="098bd-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="098bd-151">Mensajes que se envían actualmente.</span><span class="sxs-lookup"><span data-stu-id="098bd-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="098bd-152">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="098bd-152">Notes to implementers</span></span>

<span data-ttu-id="098bd-153">Puede decidir no compatible con el envío de informes de lectura y la solicitud para suprimir informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="098bd-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="098bd-154">Para evitar la eliminación de un informe de lectura, devolver MAPI_E_NO_SUPPRESS cuando se llama a **SetReadFlags** con SUPPRESS_RECEIPT establecido en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="098bd-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="098bd-155">Cuando el parámetro _lpMsgList_ apunta a más de un mensaje, realizar la operación más completo posible para cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="098bd-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="098bd-156">No detiene la operación de forma prematura a menos que se produzca un error que está fuera de su control, como la falta de memoria, está quedando sin espacio en disco o daños en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="098bd-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="098bd-157">Si ninguno de los indicadores se establecen en el parámetro _ulFlags_ , se aplican las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="098bd-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="098bd-158">Si MSGFLAG_READ ya está establecido, no haga nada.</span><span class="sxs-lookup"><span data-stu-id="098bd-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="098bd-159">Si no se establece MSGFLAG_READ, establézcalo inmediatamente y enviarlas pendientes informes de lectura si se establece la propiedad **PR_READ_RECEIPT_REQUESTED de MAPI** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="098bd-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="098bd-160">Cuando se establece la marca SUPPRESS_RECEIPT, se aplican las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="098bd-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="098bd-161">Si MSGFLAG_READ ya está establecido, no haga nada.</span><span class="sxs-lookup"><span data-stu-id="098bd-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="098bd-162">Si no se establece MSGFLAG_READ, configurarla y cancelarlas pendientes informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="098bd-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="098bd-163">Cuando se establece la marca CLEAR_READ_FLAG, desactive la marca MSGFLAG_READ en propiedad **PR_MESSAGE_FLAGS** de cada mensaje y no enviar los informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="098bd-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="098bd-164">Cuando se establece la marca GENERATE_RECEIPT_ONLY, envíe los informes de lectura pendientes.</span><span class="sxs-lookup"><span data-stu-id="098bd-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="098bd-165">Hacer MSGFLAG_READ no establecer o borrar.</span><span class="sxs-lookup"><span data-stu-id="098bd-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="098bd-166">Cuando se establecen los indicadores de la SUPPRESS_RECEIPT y la GENERATE_RECEIPT_ONLY, establecer **PR_READ_RECEIPT_REQUESTED de MAPI** en FALSE si se configura y no enviar un informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="098bd-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="098bd-167">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="098bd-167">Notes to callers</span></span>

<span data-ttu-id="098bd-168">Espera a que estos valores devueltos en las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="098bd-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="098bd-169">**Condición**</span><span class="sxs-lookup"><span data-stu-id="098bd-169">**Condition**</span></span>|<span data-ttu-id="098bd-170">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="098bd-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="098bd-171">**SetReadFlags** procesadas correctamente todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="098bd-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="098bd-172">S_OK</span><span class="sxs-lookup"><span data-stu-id="098bd-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="098bd-173">**SetReadFlags** no pudo procesar correctamente todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="098bd-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="098bd-174">MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="098bd-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="098bd-175">**SetReadFlags** no pudo completar.</span><span class="sxs-lookup"><span data-stu-id="098bd-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="098bd-176">Cualquier valor de error excepto MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="098bd-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="098bd-177">Cuando **SetReadFlags** es no se puede completar, no asuma que se ha realizado ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="098bd-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="098bd-178">**SetReadFlags** es posible que han sido capaces establecer o borrar la marca MSGFLAG_READ para uno o varios de los mensajes antes de encontrar el error.</span><span class="sxs-lookup"><span data-stu-id="098bd-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="098bd-179">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="098bd-179">MFCMAPI reference</span></span>

<span data-ttu-id="098bd-180">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="098bd-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="098bd-181">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="098bd-181">**File**</span></span>|<span data-ttu-id="098bd-182">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="098bd-182">**Function**</span></span>|<span data-ttu-id="098bd-183">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="098bd-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="098bd-184">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="098bd-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="098bd-185">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="098bd-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="098bd-186">MFCMAPI usa el método **IMAPIFolder::SetReadFlags** para establecer manualmente el estado de lectura en los mensajes especificados.</span><span class="sxs-lookup"><span data-stu-id="098bd-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="098bd-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="098bd-187">See also</span></span>

- [<span data-ttu-id="098bd-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="098bd-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="098bd-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="098bd-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="098bd-190">Propiedad canónica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="098bd-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="098bd-191">Propiedad canónica PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="098bd-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="098bd-192">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="098bd-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- [<span data-ttu-id="098bd-193">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="098bd-193">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)  
- [<span data-ttu-id="098bd-194">Uso de macros para el control de errores</span><span class="sxs-lookup"><span data-stu-id="098bd-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

