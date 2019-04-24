---
title: IMessageSetReadFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SetReadFlag
api_type:
- COM
ms.assetid: 2d02ebf6-bb8b-42bb-9bd0-870dbae9aeb4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 874dba4aa18190792a52e29064155f5afa0ef44d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349269"
---
# <a name="imessagesetreadflag"></a><span data-ttu-id="dd4cc-103">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="dd4cc-103">IMessage::SetReadFlag</span></span>

<span data-ttu-id="dd4cc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd4cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd4cc-105">Establece o borra la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje y administra el envío de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message and manages the sending of read reports.</span></span>
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="dd4cc-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="dd4cc-106">Parameters</span></span>

<span data-ttu-id="dd4cc-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dd4cc-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dd4cc-108">a Máscara de la máscara que controla la configuración de la marca de lectura de un mensaje es decir, la marca MSGFLAG_READ del mensaje en su propiedad **PR_MESSAGE_FLAGS** y el procesamiento de los informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-108">[in] Bitmask of flags that controls the setting of a message's read flag that is, the message's MSGFLAG_READ flag in its **PR_MESSAGE_FLAGS** property and the processing of read reports.</span></span> <span data-ttu-id="dd4cc-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="dd4cc-109">The following flags can be set:</span></span> 
    
  - <span data-ttu-id="dd4cc-110">CLEAR_READ_FLAG: la marca MSGFLAG_READ debe borrarse en **PR_MESSAGE_FLAGS** y no debe enviarse ningún informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-110">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="dd4cc-111">CLEAR_NRN_PENDING: la marca MSGFLAG_NRN_PENDING se debe borrar en **PR_MESSAGE_FLAGS** y no se debe enviar un informe que no sea de lectura.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-111">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a non-read report should not be sent.</span></span> 
      
  - <span data-ttu-id="dd4cc-112">CLEAR_RN_PENDING: la marca MSGFLAG_RN_PENDING debe borrarse en **PR_MESSAGE_FLAGS** y no debe enviarse ningún informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-112">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="dd4cc-113">GENERATE_RECEIPT_ONLY: se debe enviar un informe de lectura si hay uno pendiente, pero no debe haber ningún cambio en el estado de la marca MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-113">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
      
  - <span data-ttu-id="dd4cc-114">MAPI_DEFERRED_ERRORS: permite que **SetReadFlag** se devuelva correctamente, posiblemente antes de que se haya completado la operación.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-114">MAPI_DEFERRED_ERRORS: Allows **SetReadFlag** to return successfully, possibly before the operation has completed.</span></span> 
      
  - <span data-ttu-id="dd4cc-115">SUPPRESS_RECEIPT: se debe cancelar un informe de lectura pendiente si se ha solicitado un informe de lectura y esta llamada cambia el estado del mensaje de no leído a leído.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-115">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="dd4cc-116">Si esta llamada no cambia el estado del mensaje, el proveedor del almacén de mensajes puede omitir esta marca.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-116">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dd4cc-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd4cc-117">Return value</span></span>

<span data-ttu-id="dd4cc-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="dd4cc-118">S_OK</span></span> 
  
> <span data-ttu-id="dd4cc-119">La marca de lectura del mensaje se ha configurado o borrado correctamente.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-119">The message's read flag has been successfully set or cleared.</span></span>
    
<span data-ttu-id="dd4cc-120">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="dd4cc-120">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="dd4cc-121">El proveedor de almacenamiento de mensajes no admite la supresión de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-121">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="dd4cc-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dd4cc-122">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="dd4cc-123">Una de las siguientes combinaciones de marcas se establece en el parámetro _ulFlags_ :</span><span class="sxs-lookup"><span data-stu-id="dd4cc-123">One of the following combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="dd4cc-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="dd4cc-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="dd4cc-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="dd4cc-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="dd4cc-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="dd4cc-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dd4cc-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dd4cc-127">Remarks</span></span>

<span data-ttu-id="dd4cc-128">El método **IMessage:: SetReadFlag** establece o borra la marca MSGFLAG_READ del mensaje en la propiedad **PR_MESSAGE_FLAGS** y llama a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) para guardar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-128">The **IMessage::SetReadFlag** method sets or clears the message's MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property and calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message.</span></span> <span data-ttu-id="dd4cc-129">Si se establece la marca MSGFLAG_READ, se marca un mensaje como leído, lo que no indica necesariamente que el destinatario previsto haya leído realmente el mensaje.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-129">Setting the MSGFLAG_READ flag marks a message as having been read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="dd4cc-130">**SetReadFlags** también administra el envío de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-130">**SetReadFlags** also manages the sending of read reports.</span></span> <span data-ttu-id="dd4cc-131">Se envía un informe de lectura solo si el remitente ha solicitado uno.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-131">A read report is sent only if the sender has requested one.</span></span> 
  
<span data-ttu-id="dd4cc-132">No se puede modificar la marca de lectura para:</span><span class="sxs-lookup"><span data-stu-id="dd4cc-132">The read flag cannot be altered for:</span></span>
  
- <span data-ttu-id="dd4cc-133">Mensajes que no existen.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-133">Messages that do not exist.</span></span>
    
- <span data-ttu-id="dd4cc-134">Mensajes que se movieron en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-134">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="dd4cc-135">Mensajes que están abiertos con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-135">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="dd4cc-136">Mensajes que se envían actualmente.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-136">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="dd4cc-137">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="dd4cc-137">Notes to callers</span></span>

<span data-ttu-id="dd4cc-138">Si no se establece ninguno de los indicadores en el parámetro _ulFlags_ , se aplican las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="dd4cc-138">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="dd4cc-139">Si MSGFLAG_READ ya está establecido, no haga nada.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-139">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="dd4cc-140">Si no se establece MSGFLAG_READ, establézcalo y envíe los informes de lectura pendientes si se establece la propiedad **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dd4cc-140">If MSGFLAG_READ is not set, set it and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="dd4cc-141">Si se establecen las dos marcas SUPPRESS_RECEIPT y GENERATE_RECEIPT_ONLY, se debe borrar el bit PR_READ_RECEIPT_REQUESTED, si se establece, y no se debe enviar un informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-141">If both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, the PR_READ_RECEIPT_REQUESTED bit, if set, should be cleared and a read report should not be sent.</span></span>
  
<span data-ttu-id="dd4cc-142">Cuando se establece la marca SUPPRESS_RECEIPT:</span><span class="sxs-lookup"><span data-stu-id="dd4cc-142">When the SUPPRESS_RECEIPT flag is set:</span></span>
  
- <span data-ttu-id="dd4cc-143">Si MSGFLAG_READ ya está establecido, no haga nada.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-143">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="dd4cc-144">Si no se establece MSGFLAG_READ, establézcalo y cancele los informes de lectura pendientes.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-144">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="dd4cc-145">Cuando se establece la marca CLEAR_READ_FLAG, borre la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** de cada mensaje y no envíe ningún informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-145">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="dd4cc-146">Cuando se establece la marca GENERATE_RECEIPT_ONLY, enviar los informes de lectura pendientes.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-146">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="dd4cc-147">No establezca ni borre MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-147">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="dd4cc-148">Cuando se establecen las dos marcas SUPPRESS_RECEIPT y GENERATE_RECEIPT_ONLY, se establece la propiedad PR_READ_RECEIPT_REQUESTED en FALSE si se establece y no se envía un informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-148">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set the PR_READ_RECEIPT_REQUESTED property to FALSE if it is set and do not send a read report.</span></span>
  
<span data-ttu-id="dd4cc-149">Puede optimizar el comportamiento del informe suprimiendo la generación de informes de lectura en determinadas condiciones.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-149">You can optimize report behavior by suppressing the generation of read reports under certain conditions.</span></span> <span data-ttu-id="dd4cc-150">Sin embargo, si no admite la supresión de informes y un cliente llama a **SetReadFlag** con el conjunto de marcas SUPPRESS_RECEIPT, devuelve MAPI_E_NO_SUPPRESS.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-150">However, if you do not support the suppression of reports and a client calls **SetReadFlag** with the SUPPRESS_RECEIPT flag set, return MAPI_E_NO_SUPPRESS.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dd4cc-151">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="dd4cc-151">MFCMAPI reference</span></span>

<span data-ttu-id="dd4cc-152">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dd4cc-153">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="dd4cc-153">**File**</span></span>|<span data-ttu-id="dd4cc-154">**Función**</span><span class="sxs-lookup"><span data-stu-id="dd4cc-154">**Function**</span></span>|<span data-ttu-id="dd4cc-155">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="dd4cc-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dd4cc-156">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="dd4cc-156">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="dd4cc-157">CFolderDlg:: OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="dd4cc-157">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="dd4cc-158">MFCMAPI usa el método **IMessage:: SetReadFlag** para establecer las marcas de lectura en los mensajes seleccionados.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-158">MFCMAPI uses the **IMessage::SetReadFlag** method to set read flags on selected messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dd4cc-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd4cc-159">See also</span></span>

- [<span data-ttu-id="dd4cc-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="dd4cc-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)  
- [<span data-ttu-id="dd4cc-161">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="dd4cc-161">IMAPIFolder::SetReadFlags</span></span>](imapifolder-setreadflags.md)  
- [<span data-ttu-id="dd4cc-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="dd4cc-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)  
- [<span data-ttu-id="dd4cc-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="dd4cc-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md) 
- [<span data-ttu-id="dd4cc-164">Propiedad canónica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="dd4cc-164">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md) 
- [<span data-ttu-id="dd4cc-165">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dd4cc-165">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
- [<span data-ttu-id="dd4cc-166">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="dd4cc-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

