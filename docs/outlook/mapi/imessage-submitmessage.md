---
title: IMessageSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SubmitMessage
api_type:
- COM
ms.assetid: 9ce93469-c55d-48d1-9abb-a637716ed4f2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 28786f483c4d2031c334d7b9697db7c5e627fe93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437367"
---
# <a name="imessagesubmitmessage"></a><span data-ttu-id="4df04-103">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="4df04-103">IMessage::SubmitMessage</span></span>

  
  
<span data-ttu-id="4df04-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4df04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4df04-105">Guarda todas las propiedades del mensaje y marca el mensaje como listo para enviarse.</span><span class="sxs-lookup"><span data-stu-id="4df04-105">Saves all of the message's properties and marks the message as ready to be sent.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4df04-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4df04-106">Parameters</span></span>

 <span data-ttu-id="4df04-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4df04-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4df04-108">[entrada] Máscara de bits de marcas usadas para controlar cómo se envía un mensaje.</span><span class="sxs-lookup"><span data-stu-id="4df04-108">[in] Bitmask of flags used to control how a message is submitted.</span></span> <span data-ttu-id="4df04-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="4df04-109">The following flag can be set:</span></span>
    
<span data-ttu-id="4df04-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="4df04-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="4df04-111">MAPI debe enviar el mensaje inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="4df04-111">MAPI should submit the message immediately.</span></span> <span data-ttu-id="4df04-112">Esta marca no está actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="4df04-112">This flag is not currently in use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4df04-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4df04-113">Return value</span></span>

<span data-ttu-id="4df04-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="4df04-114">S_OK</span></span> 
  
> <span data-ttu-id="4df04-115">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="4df04-115">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="4df04-116">MAPI_E_NO_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="4df04-116">MAPI_E_NO_RECIPIENTS</span></span> 
  
> <span data-ttu-id="4df04-117">La tabla de destinatarios del mensaje está vacía.</span><span class="sxs-lookup"><span data-stu-id="4df04-117">The message's recipient table is empty.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4df04-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4df04-118">Remarks</span></span>

<span data-ttu-id="4df04-119">El **método IMessage::SubmitMessage** marca un mensaje como listo para transmitirse.</span><span class="sxs-lookup"><span data-stu-id="4df04-119">The **IMessage::SubmitMessage** method marks a message as ready to be transmitted.</span></span> <span data-ttu-id="4df04-120">MAPI pasa los mensajes al sistema de mensajería subyacente en el orden en que se marcan para su envío.</span><span class="sxs-lookup"><span data-stu-id="4df04-120">MAPI passes messages to the underlying messaging system in the order in which they are marked for sending.</span></span> <span data-ttu-id="4df04-121">Debido a esta funcionalidad, un mensaje puede permanecer en un almacén de mensajes durante algún tiempo antes de que el sistema de mensajería subyacente pueda asumir su responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="4df04-121">Because of this functionality, a message might stay in a message store for some time before the underlying messaging system can take responsibility for it.</span></span> <span data-ttu-id="4df04-122">El orden de recepción en el destino está en el control del sistema de mensajería subyacente y no coincide necesariamente con el orden en que se enviaron los mensajes.</span><span class="sxs-lookup"><span data-stu-id="4df04-122">The order of receipt at the destination is in the underlying messaging system's control and does not necessarily match the order in which messages were sent.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4df04-123">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="4df04-123">Notes to implementers</span></span>

<span data-ttu-id="4df04-124">Llame al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje para guardarlo y, a continuación, compruebe la propiedad PR_MESSAGE_FLAGS **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4df04-124">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it and then check the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="4df04-125">Si se MSGFLAG_RESEND marca, llame a [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md).</span><span class="sxs-lookup"><span data-stu-id="4df04-125">If the MSGFLAG_RESEND flag is set, call [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span></span> <span data-ttu-id="4df04-126">**PrepareSubmit actualiza** el tipo de destinatario y **PR_RESPONSIBILITY** propiedad ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) para todos los destinatarios del mensaje de reenvío.</span><span class="sxs-lookup"><span data-stu-id="4df04-126">**PrepareSubmit** updates the recipient type and **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property for all of the recipients in the resend message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="4df04-127">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="4df04-127">Notes to callers</span></span>

<span data-ttu-id="4df04-128">Cuando **SubmitMessage devuelve,** todos los punteros al mensaje y sus subobjetos asociados mensajes, carpetas, datos adjuntos, secuencias, tablas, entre otros, ya no son válidos.</span><span class="sxs-lookup"><span data-stu-id="4df04-128">When **SubmitMessage** returns, all pointers to the message and its associated subobjects messages, folders, attachments, streams, tables, and so on are no longer valid.</span></span> <span data-ttu-id="4df04-129">MAPI no permite ninguna otra operación en estos punteros, excepto para llamar a sus **métodos IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="4df04-129">MAPI does not permit any further operations on these pointers, except for calling their **IUnknown::Release** methods.</span></span> <span data-ttu-id="4df04-130">MAPI está diseñado de tal manera que, después de llamar **a SubmitMessage,** debe liberar el mensaje y todos los subobjetos asociados.</span><span class="sxs-lookup"><span data-stu-id="4df04-130">MAPI is designed such that after **SubmitMessage** is called, you should release the message and all associated subobjects.</span></span> <span data-ttu-id="4df04-131">Sin embargo, **si SubmitMessage** devuelve un valor de error que indica que falta información o que no es válida, el mensaje permanece abierto y los punteros siguen siendo válidos.</span><span class="sxs-lookup"><span data-stu-id="4df04-131">However, if **SubmitMessage** returns an error value indicating missing or invalid information, the message remains open and the pointers remain valid.</span></span> 
  
<span data-ttu-id="4df04-132">Para cancelar una operación de envío, obtenga y almacene un puntero a la propiedad **PR_ENTRYID** del mensaje ([PidTagEntryId](pidtagentryid-canonical-property.md)) antes de que se envíe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="4df04-132">To cancel a send operation, get and store a pointer to the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property before the message is submitted.</span></span> <span data-ttu-id="4df04-133">Dado que el identificador de entrada de un mensaje se invalida después de que se haya enviado el mensaje, es necesario guardarlo antes de llamar **a SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="4df04-133">Because a message's entry identifier is invalidated after the message has been submitted, it is necessary to save it before calling **SubmitMessage**.</span></span> <span data-ttu-id="4df04-134">Para cancelar el envío, apunte el parámetro  _lpEntryId_ a este identificador de entrada y llame a [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span><span class="sxs-lookup"><span data-stu-id="4df04-134">To cancel the send, point the  _lpEntryId_ parameter to this entry identifier and call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4df04-135">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4df04-135">MFCMAPI reference</span></span>

<span data-ttu-id="4df04-136">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="4df04-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4df04-137">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="4df04-137">**File**</span></span>|<span data-ttu-id="4df04-138">**Función**</span><span class="sxs-lookup"><span data-stu-id="4df04-138">**Function**</span></span>|<span data-ttu-id="4df04-139">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="4df04-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4df04-140">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="4df04-140">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="4df04-141">**CFolderDlg::OnSubmitMessage**</span><span class="sxs-lookup"><span data-stu-id="4df04-141">**CFolderDlg::OnSubmitMessage**</span></span> <br/> |<span data-ttu-id="4df04-142">MFCMAPI usa el **método IMessage::SubmitMessage** para enviar el mensaje seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4df04-142">MFCMAPI uses the **IMessage::SubmitMessage** method to submit the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4df04-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4df04-143">See also</span></span>



[<span data-ttu-id="4df04-144">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="4df04-144">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="4df04-145">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4df04-145">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="4df04-146">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="4df04-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

