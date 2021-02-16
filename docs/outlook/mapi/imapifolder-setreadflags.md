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
ms.openlocfilehash: 15504ecc88188ed7bc4eed0e64b1871dbc6a5e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406916"
---
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="ac374-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="ac374-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="ac374-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac374-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac374-105">Establece o borra la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uno o varios de los mensajes de la carpeta y administra el envío de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="ac374-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ac374-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac374-106">Parameters</span></span>

<span data-ttu-id="ac374-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="ac374-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="ac374-108">[entrada] Puntero a una matriz de [estructuras ENTRYLIST](entrylist.md) que identifican el mensaje o los mensajes que tienen marcas de lectura para establecer o borrar.</span><span class="sxs-lookup"><span data-stu-id="ac374-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="ac374-109">Si  _lpMsgList se_ establece en NULL, se establecen o borran las marcas de lectura de todos los mensajes de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="ac374-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="ac374-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ac374-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="ac374-111">[entrada] Identificador de la ventana principal del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="ac374-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="ac374-112">El _parámetro ulUIParam_ se omite a menos que MESSAGE_DIALOG marca esté establecida en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="ac374-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="ac374-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="ac374-113">_lpProgress_</span></span>
  
> <span data-ttu-id="ac374-114">[entrada] Puntero a un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="ac374-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="ac374-115">Si se pasa NULL en  _lpProgress,_ el proveedor del almacén de mensajes muestra un indicador de progreso mediante la implementación de MAPI.</span><span class="sxs-lookup"><span data-stu-id="ac374-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="ac374-116">El  _parámetro lpProgress_ se omite a menos que MESSAGE_DIALOG marca esté establecida en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="ac374-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="ac374-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ac374-117">_ulFlags_</span></span>
  
> <span data-ttu-id="ac374-118">[entrada] Máscara de bits de marcas que controla la configuración de la marca de lectura de un mensaje y el procesamiento de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="ac374-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="ac374-119">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="ac374-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="ac374-120">CLEAR_READ_FLAG: la MSGFLAG_READ debe borrarse en **PR_MESSAGE_FLAGS** y no se debe enviar un informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="ac374-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="ac374-121">CLEAR_NRN_PENDING: la MSGFLAG_NRN_PENDING debe borrarse en **PR_MESSAGE_FLAGS** y no se debe enviar un informe no leído.</span><span class="sxs-lookup"><span data-stu-id="ac374-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="ac374-122">CLEAR_RN_PENDING: la MSGFLAG_RN_PENDING debe borrarse en **PR_MESSAGE_FLAGS** y no se debe enviar un informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="ac374-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="ac374-123">GENERATE_RECEIPT_ONLY: se debe enviar un informe de lectura si hay uno pendiente, pero no debe haber ningún cambio en el estado de la marca MSGFLAG_READ lectura.</span><span class="sxs-lookup"><span data-stu-id="ac374-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="ac374-124">MAPI_DEFERRED_ERRORS: permite que **SetReadFlags** vuelva correctamente, posiblemente antes de que se complete la operación.</span><span class="sxs-lookup"><span data-stu-id="ac374-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="ac374-125">MESSAGE_DIALOG: muestra un indicador de progreso mientras continúa la operación.</span><span class="sxs-lookup"><span data-stu-id="ac374-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="ac374-126">SUPPRESS_RECEIPT: se debe cancelar un informe de lectura pendiente si se ha solicitado un informe de lectura y esta llamada cambia el estado del mensaje de no leído a leído.</span><span class="sxs-lookup"><span data-stu-id="ac374-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="ac374-127">Si esta llamada no cambia el estado del mensaje, el proveedor del almacén de mensajes puede omitir esta marca.</span><span class="sxs-lookup"><span data-stu-id="ac374-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ac374-128">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="ac374-128">Return values</span></span>

<span data-ttu-id="ac374-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac374-129">S_OK</span></span> 
  
> <span data-ttu-id="ac374-130">La marca de lectura del mensaje o los mensajes especificados se estableció o despejado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ac374-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="ac374-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="ac374-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="ac374-132">El proveedor del almacén de mensajes no admite la supresión de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="ac374-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="ac374-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ac374-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="ac374-134">Una de las siguientes combinaciones incompatibles de marcas se establece en el _parámetro ulFlags:_</span><span class="sxs-lookup"><span data-stu-id="ac374-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="ac374-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="ac374-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="ac374-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="ac374-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="ac374-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="ac374-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="ac374-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="ac374-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="ac374-139">La llamada se ha realizado correctamente, pero no todos los mensajes se han procesado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ac374-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="ac374-140">Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="ac374-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="ac374-141">Para probar esta advertencia, use la **macro HR_FAILED** datos.</span><span class="sxs-lookup"><span data-stu-id="ac374-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="ac374-142">Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="ac374-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac374-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ac374-143">Remarks</span></span>

<span data-ttu-id="ac374-144">El **método IMAPIFolder::SetReadFlags** establece o borra la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** de uno o varios de los mensajes de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="ac374-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="ac374-145">Al establecer MSGFLAG_READ marca un mensaje como leído, lo que no indica necesariamente que el destinatario deseado haya leído realmente el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ac374-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="ac374-146">**SetReadFlags** también administra el envío de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="ac374-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="ac374-147">La marca de lectura no se puede cambiar para lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ac374-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="ac374-148">Mensajes que no existen.</span><span class="sxs-lookup"><span data-stu-id="ac374-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="ac374-149">Mensajes que se han movido a otro lugar.</span><span class="sxs-lookup"><span data-stu-id="ac374-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="ac374-150">Mensajes abiertos con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ac374-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="ac374-151">Mensajes que se envían actualmente.</span><span class="sxs-lookup"><span data-stu-id="ac374-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="ac374-152">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="ac374-152">Notes to implementers</span></span>

<span data-ttu-id="ac374-153">Puede decidir no admitir el envío de informes de lectura y la solicitud para suprimir los informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="ac374-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="ac374-154">Para evitar suprimir un informe de lectura, devuelva MAPI_E_NO_SUPPRESS cuando se llame a **SetReadFlags** con SUPPRESS_RECEIPT establecido en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="ac374-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="ac374-155">Cuando el  _parámetro lpMsgList_ apunta a más de un mensaje, realice la operación lo más completa posible para cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="ac374-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="ac374-156">No detenga la operación antes de tiempo a menos que se produzca un error que esté fuera de su control, como que se queme la memoria, que se esté quedando sin espacio en disco o que el almacén de mensajes esté dañado.</span><span class="sxs-lookup"><span data-stu-id="ac374-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="ac374-157">Si no se establece ninguna de las marcas en el  _parámetro ulFlags,_ se aplican las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="ac374-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="ac374-158">Si MSGFLAG_READ ya está establecido, no haga nada.</span><span class="sxs-lookup"><span data-stu-id="ac374-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="ac374-159">Si MSGFLAG_READ no está establecido, estapórelo inmediatamente y envíe los informes de lectura pendientes si se establece la propiedad **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ac374-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="ac374-160">Cuando se SUPPRESS_RECEIPT marca, se aplican las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="ac374-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="ac374-161">Si MSGFLAG_READ ya está establecido, no haga nada.</span><span class="sxs-lookup"><span data-stu-id="ac374-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="ac374-162">Si MSGFLAG_READ no está establecido, estad léalo y cancele los informes de lectura pendientes.</span><span class="sxs-lookup"><span data-stu-id="ac374-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="ac374-163">Cuando se CLEAR_READ_FLAG marca, borre la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** de cada mensaje y no envíe ningún informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="ac374-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="ac374-164">Cuando se GENERATE_RECEIPT_ONLY marca, envíe los informes de lectura pendientes.</span><span class="sxs-lookup"><span data-stu-id="ac374-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="ac374-165">No establecer ni borrar el MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="ac374-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="ac374-166">Cuando se establecen SUPPRESS_RECEIPT y GENERATE_RECEIPT_ONLY, establezca **PR_READ_RECEIPT_REQUESTED** en FALSE si está establecido y no envíe un informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="ac374-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ac374-167">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ac374-167">Notes to callers</span></span>

<span data-ttu-id="ac374-168">Espere estos valores devueltos en las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="ac374-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="ac374-169">**Condition**</span><span class="sxs-lookup"><span data-stu-id="ac374-169">**Condition**</span></span>|<span data-ttu-id="ac374-170">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="ac374-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ac374-171">**SetReadFlags** ha procesado correctamente todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="ac374-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="ac374-172">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac374-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="ac374-173">**SetReadFlags** no pudo procesar correctamente todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="ac374-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="ac374-174">MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ac374-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="ac374-175">**SetReadFlags** no se pudo completar.</span><span class="sxs-lookup"><span data-stu-id="ac374-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="ac374-176">Cualquier valor de error excepto MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ac374-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="ac374-177">Cuando **SetReadFlags** no se puede completar, no suponga que no se ha realizado ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="ac374-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="ac374-178">**Es posible que SetReadFlags** haya podido establecer o borrar la marca MSGFLAG_READ para uno o varios de los mensajes antes de encontrar el error.</span><span class="sxs-lookup"><span data-stu-id="ac374-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ac374-179">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ac374-179">MFCMAPI reference</span></span>

<span data-ttu-id="ac374-180">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ac374-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ac374-181">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ac374-181">**File**</span></span>|<span data-ttu-id="ac374-182">**Función**</span><span class="sxs-lookup"><span data-stu-id="ac374-182">**Function**</span></span>|<span data-ttu-id="ac374-183">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ac374-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac374-184">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ac374-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="ac374-185">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="ac374-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="ac374-186">MFCMAPI usa el **método IMAPIFolder::SetReadFlags** para establecer manualmente el estado de lectura en los mensajes especificados.</span><span class="sxs-lookup"><span data-stu-id="ac374-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac374-187">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ac374-187">See also</span></span>

- [<span data-ttu-id="ac374-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="ac374-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="ac374-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="ac374-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="ac374-190">Propiedad canónica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="ac374-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="ac374-191">Propiedad canónica PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="ac374-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="ac374-192">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ac374-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- [<span data-ttu-id="ac374-193">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="ac374-193">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)  
- [<span data-ttu-id="ac374-194">Uso de macros para el control de errores</span><span class="sxs-lookup"><span data-stu-id="ac374-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

