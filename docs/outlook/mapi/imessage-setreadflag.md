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
ms.openlocfilehash: 0ae35166f01f597c2c3ab399a1b66e5760ab0dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817650"
---
# <a name="imessagesetreadflag"></a><span data-ttu-id="506bc-103">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="506bc-103">IMessage::SetReadFlag</span></span>

<span data-ttu-id="506bc-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="506bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="506bc-105">Establece o borra el indicador MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje y administra el envío de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="506bc-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message and manages the sending of read reports.</span></span>
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="506bc-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="506bc-106">Parameters</span></span>

<span data-ttu-id="506bc-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="506bc-107">_ulFlags_</span></span>
  
> <span data-ttu-id="506bc-108">[entrada] Máscara de bits de indicadores que controla la configuración de lectura de un mensaje, es decir, marca marca MSGFLAG_READ del mensaje en su propiedad **PR_MESSAGE_FLAGS** y el procesamiento de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="506bc-108">[in] Bitmask of flags that controls the setting of a message's read flag that is, the message's MSGFLAG_READ flag in its **PR_MESSAGE_FLAGS** property and the processing of read reports.</span></span> <span data-ttu-id="506bc-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="506bc-109">The following flags can be set:</span></span> 
    
  - <span data-ttu-id="506bc-110">CLEAR_READ_FLAG: Se debe borrar la marca MSGFLAG_READ en **PR_MESSAGE_FLAGS** y no se debe enviar ningún informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="506bc-110">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="506bc-111">CLEAR_NRN_PENDING: Se debe borrar la marca MSGFLAG_NRN_PENDING en **PR_MESSAGE_FLAGS** y no se debe enviar un informe de no leído.</span><span class="sxs-lookup"><span data-stu-id="506bc-111">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a non-read report should not be sent.</span></span> 
      
  - <span data-ttu-id="506bc-112">CLEAR_RN_PENDING: Se debe borrar la marca MSGFLAG_RN_PENDING en **PR_MESSAGE_FLAGS** y no se debe enviar ningún informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="506bc-112">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="506bc-113">GENERATE_RECEIPT_ONLY: Se debe enviar un informe de lectura si uno está pendiente, pero no debe haber ningún cambio en el estado de la marca MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="506bc-113">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
      
  - <span data-ttu-id="506bc-114">MAPI_DEFERRED_ERRORS: Permite **SetReadFlag** devolver de correctamente, posiblemente antes de que la operación ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="506bc-114">MAPI_DEFERRED_ERRORS: Allows **SetReadFlag** to return successfully, possibly before the operation has completed.</span></span> 
      
  - <span data-ttu-id="506bc-115">SUPPRESS_RECEIPT: Se debe cancelar un informe de lectura pendiente si se solicita un informe de lectura y esta llamada cambia el estado del mensaje de no leído a leer.</span><span class="sxs-lookup"><span data-stu-id="506bc-115">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="506bc-116">Si esta llamada no cambia el estado del mensaje, el proveedor de almacenamiento de mensajes puede pasar por alto esta marca.</span><span class="sxs-lookup"><span data-stu-id="506bc-116">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="506bc-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="506bc-117">Return value</span></span>

<span data-ttu-id="506bc-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="506bc-118">S_OK</span></span> 
  
> <span data-ttu-id="506bc-119">Indicador de lectura del mensaje se ha establecido correctamente o desactivada.</span><span class="sxs-lookup"><span data-stu-id="506bc-119">The message's read flag has been successfully set or cleared.</span></span>
    
<span data-ttu-id="506bc-120">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="506bc-120">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="506bc-121">El proveedor de almacén de mensajes no es compatible con la supresión de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="506bc-121">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="506bc-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="506bc-122">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="506bc-123">Una de las siguientes combinaciones de indicadores se establece en el parámetro _ulFlags indicado_ :</span><span class="sxs-lookup"><span data-stu-id="506bc-123">One of the following combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="506bc-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="506bc-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="506bc-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="506bc-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="506bc-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="506bc-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
## <a name="remarks"></a><span data-ttu-id="506bc-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="506bc-127">Remarks</span></span>

<span data-ttu-id="506bc-128">El método **IMessage::SetReadFlag** establece o borra la marca MSGFLAG_READ del mensaje en la propiedad **PR_MESSAGE_FLAGS** y llamadas [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para guardar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="506bc-128">The **IMessage::SetReadFlag** method sets or clears the message's MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property and calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message.</span></span> <span data-ttu-id="506bc-129">Establecer el indicador MSGFLAG_READ marca un mensaje como lectura, que no necesariamente indica que el destinatario realmente ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="506bc-129">Setting the MSGFLAG_READ flag marks a message as having been read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="506bc-130">**SetReadFlags** también administra el envío de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="506bc-130">**SetReadFlags** also manages the sending of read reports.</span></span> <span data-ttu-id="506bc-131">Se envía un informe de lectura sólo si el remitente ha solicitado una.</span><span class="sxs-lookup"><span data-stu-id="506bc-131">A read report is sent only if the sender has requested one.</span></span> 
  
<span data-ttu-id="506bc-132">No se puede modificar la marca de lectura para:</span><span class="sxs-lookup"><span data-stu-id="506bc-132">The read flag cannot be altered for:</span></span>
  
- <span data-ttu-id="506bc-133">Mensajes que no existen.</span><span class="sxs-lookup"><span data-stu-id="506bc-133">Messages that do not exist.</span></span>
    
- <span data-ttu-id="506bc-134">Los mensajes que se han moverán a otro lugar.</span><span class="sxs-lookup"><span data-stu-id="506bc-134">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="506bc-135">Mensajes que están abiertos con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="506bc-135">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="506bc-136">Mensajes que se envían actualmente.</span><span class="sxs-lookup"><span data-stu-id="506bc-136">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="506bc-137">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="506bc-137">Notes to callers</span></span>

<span data-ttu-id="506bc-138">Si ninguno de los indicadores se establecen en el parámetro _ulFlags_ , se aplican las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="506bc-138">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="506bc-139">Si MSGFLAG_READ ya está establecido, no haga nada.</span><span class="sxs-lookup"><span data-stu-id="506bc-139">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="506bc-140">Si no se establece MSGFLAG_READ, configurarla y enviarlas pendientes informes de lectura si se establece la propiedad **PR_READ_RECEIPT_REQUESTED de MAPI** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="506bc-140">If MSGFLAG_READ is not set, set it and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="506bc-141">Si se establecen las marcas de la SUPPRESS_RECEIPT y la GENERATE_RECEIPT_ONLY, la PR_READ_RECEIPT_REQUESTED de MAPI bit, si se establece, se deben borrar y no se debe enviar un informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="506bc-141">If both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, the PR_READ_RECEIPT_REQUESTED bit, if set, should be cleared and a read report should not be sent.</span></span>
  
<span data-ttu-id="506bc-142">Cuando se establece la marca SUPPRESS_RECEIPT:</span><span class="sxs-lookup"><span data-stu-id="506bc-142">When the SUPPRESS_RECEIPT flag is set:</span></span>
  
- <span data-ttu-id="506bc-143">Si MSGFLAG_READ ya está establecido, no haga nada.</span><span class="sxs-lookup"><span data-stu-id="506bc-143">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="506bc-144">Si no se establece MSGFLAG_READ, configurarla y cancelarlas pendientes informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="506bc-144">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="506bc-145">Cuando se establece la marca CLEAR_READ_FLAG, desactive la marca MSGFLAG_READ en propiedad **PR_MESSAGE_FLAGS** de cada mensaje y no enviar los informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="506bc-145">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="506bc-146">Cuando se establece la marca GENERATE_RECEIPT_ONLY, envíe los informes de lectura pendientes.</span><span class="sxs-lookup"><span data-stu-id="506bc-146">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="506bc-147">Hacer MSGFLAG_READ no establecer o borrar.</span><span class="sxs-lookup"><span data-stu-id="506bc-147">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="506bc-148">Cuando se establecen los indicadores de la SUPPRESS_RECEIPT y la GENERATE_RECEIPT_ONLY, establezca la propiedad PR_READ_RECEIPT_REQUESTED de MAPI en FALSE si se configura y no enviar un informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="506bc-148">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set the PR_READ_RECEIPT_REQUESTED property to FALSE if it is set and do not send a read report.</span></span>
  
<span data-ttu-id="506bc-149">Puede optimizar el comportamiento de informe mediante la supresión de la generación de informes de lectura en determinadas condiciones.</span><span class="sxs-lookup"><span data-stu-id="506bc-149">You can optimize report behavior by suppressing the generation of read reports under certain conditions.</span></span> <span data-ttu-id="506bc-150">Sin embargo, si no se admiten la supresión de informes y un cliente llama a **SetReadFlag** con el conjunto de marca SUPPRESS_RECEIPT, devolver MAPI_E_NO_SUPPRESS.</span><span class="sxs-lookup"><span data-stu-id="506bc-150">However, if you do not support the suppression of reports and a client calls **SetReadFlag** with the SUPPRESS_RECEIPT flag set, return MAPI_E_NO_SUPPRESS.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="506bc-151">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="506bc-151">MFCMAPI reference</span></span>

<span data-ttu-id="506bc-152">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="506bc-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="506bc-153">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="506bc-153">**File**</span></span>|<span data-ttu-id="506bc-154">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="506bc-154">**Function**</span></span>|<span data-ttu-id="506bc-155">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="506bc-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="506bc-156">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="506bc-156">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="506bc-157">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="506bc-157">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="506bc-158">MFCMAPI usa el método **IMessage::SetReadFlag** para establecer marcas de lectura en los mensajes seleccionados.</span><span class="sxs-lookup"><span data-stu-id="506bc-158">MFCMAPI uses the **IMessage::SetReadFlag** method to set read flags on selected messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="506bc-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="506bc-159">See also</span></span>

- [<span data-ttu-id="506bc-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="506bc-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)  
- [<span data-ttu-id="506bc-161">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="506bc-161">IMAPIFolder::SetReadFlags</span></span>](imapifolder-setreadflags.md)  
- [<span data-ttu-id="506bc-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="506bc-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)  
- [<span data-ttu-id="506bc-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="506bc-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md) 
- [<span data-ttu-id="506bc-164">Propiedad canónica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="506bc-164">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md) 
- [<span data-ttu-id="506bc-165">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="506bc-165">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
- [<span data-ttu-id="506bc-166">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="506bc-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

