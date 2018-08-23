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
ms.openlocfilehash: 67c86f39898b4bd0c019b9b3095c9449e6e60b1b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567324"
---
# <a name="imessagesubmitmessage"></a><span data-ttu-id="43017-103">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="43017-103">IMessage::SubmitMessage</span></span>

  
  
<span data-ttu-id="43017-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43017-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43017-105">Guarda todas las propiedades del mensaje y marca el mensaje como listo para ser enviado.</span><span class="sxs-lookup"><span data-stu-id="43017-105">Saves all of the message's properties and marks the message as ready to be sent.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="43017-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="43017-106">Parameters</span></span>

 <span data-ttu-id="43017-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="43017-107">_ulFlags_</span></span>
  
> <span data-ttu-id="43017-108">[entrada] Máscara de bits de indicadores que se utilizan para controlar cómo se envía un mensaje.</span><span class="sxs-lookup"><span data-stu-id="43017-108">[in] Bitmask of flags used to control how a message is submitted.</span></span> <span data-ttu-id="43017-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="43017-109">The following flag can be set:</span></span>
    
<span data-ttu-id="43017-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="43017-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="43017-111">MAPI debe enviar el mensaje inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="43017-111">MAPI should submit the message immediately.</span></span> <span data-ttu-id="43017-112">Esta marca no está actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="43017-112">This flag is not currently in use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="43017-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43017-113">Return value</span></span>

<span data-ttu-id="43017-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="43017-114">S_OK</span></span> 
  
> <span data-ttu-id="43017-115">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="43017-115">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="43017-116">MAPI_E_NO_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="43017-116">MAPI_E_NO_RECIPIENTS</span></span> 
  
> <span data-ttu-id="43017-117">Tabla de destinatarios del mensaje está vacía.</span><span class="sxs-lookup"><span data-stu-id="43017-117">The message's recipient table is empty.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43017-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43017-118">Remarks</span></span>

<span data-ttu-id="43017-119">El método **IMessage::SubmitMessage** marca un mensaje como listo para ser transmitidos.</span><span class="sxs-lookup"><span data-stu-id="43017-119">The **IMessage::SubmitMessage** method marks a message as ready to be transmitted.</span></span> <span data-ttu-id="43017-120">MAPI pasa los mensajes al sistema de mensajería subyacente en el orden en que están marcados para el envío.</span><span class="sxs-lookup"><span data-stu-id="43017-120">MAPI passes messages to the underlying messaging system in the order in which they are marked for sending.</span></span> <span data-ttu-id="43017-121">Debido a esta funcionalidad, puede permanecer en un mensaje en un almacén de mensajes para algún tiempo antes de que el sistema de mensajería subyacente puede asumir la responsabilidad de él.</span><span class="sxs-lookup"><span data-stu-id="43017-121">Because of this functionality, a message might stay in a message store for some time before the underlying messaging system can take responsibility for it.</span></span> <span data-ttu-id="43017-122">El orden de recepción en el destino se encuentra en el control del sistema mensajería subyacente y no necesariamente deben coincidir con el orden en que se enviaron mensajes.</span><span class="sxs-lookup"><span data-stu-id="43017-122">The order of receipt at the destination is in the underlying messaging system's control and does not necessarily match the order in which messages were sent.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="43017-123">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="43017-123">Notes to implementers</span></span>

<span data-ttu-id="43017-124">Llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje para guardarlo y, a continuación, compruebe la propiedad del mensaje **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="43017-124">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it and then check the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="43017-125">Si se establece la marca MSGFLAG_RESEND, llame a [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span><span class="sxs-lookup"><span data-stu-id="43017-125">If the MSGFLAG_RESEND flag is set, call [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span></span> <span data-ttu-id="43017-126">**PrepareSubmit** actualiza el tipo de destinatario y la propiedad de **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) para todos los destinatarios en el mensaje de reenvío.</span><span class="sxs-lookup"><span data-stu-id="43017-126">**PrepareSubmit** updates the recipient type and **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property for all of the recipients in the resend message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="43017-127">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="43017-127">Notes to callers</span></span>

<span data-ttu-id="43017-128">Cuando se devuelve en **SubmitMessage** , todos los punteros en el mensaje y sus mensajes asociados subobjetos, carpetas, datos adjuntos, secuencias, tablas y así sucesivamente ya no son válidos.</span><span class="sxs-lookup"><span data-stu-id="43017-128">When **SubmitMessage** returns, all pointers to the message and its associated subobjects messages, folders, attachments, streams, tables, and so on are no longer valid.</span></span> <span data-ttu-id="43017-129">MAPI no permite las operaciones posteriores en estos punteros, salvo llamar a sus métodos **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="43017-129">MAPI does not permit any further operations on these pointers, except for calling their **IUnknown::Release** methods.</span></span> <span data-ttu-id="43017-130">MAPI está diseñada para que después de llamar a **SubmitMessage** , debe liberar el mensaje y todos sus subobjetos.</span><span class="sxs-lookup"><span data-stu-id="43017-130">MAPI is designed such that after **SubmitMessage** is called, you should release the message and all associated subobjects.</span></span> <span data-ttu-id="43017-131">Sin embargo, si **SubmitMessage** devuelve un valor de error que indica la información que falta o no es válido, el mensaje permanece abierto y los punteros siguen siendo válidos.</span><span class="sxs-lookup"><span data-stu-id="43017-131">However, if **SubmitMessage** returns an error value indicating missing or invalid information, the message remains open and the pointers remain valid.</span></span> 
  
<span data-ttu-id="43017-132">Para cancelar una operación de envío, obtener y almacenar un puntero a la propiedad del mensaje de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) antes de que se envíe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="43017-132">To cancel a send operation, get and store a pointer to the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property before the message is submitted.</span></span> <span data-ttu-id="43017-133">Debido a que el identificador de entrada de un mensaje se invalida después de que se ha enviado el mensaje, es necesario guardar antes de llamar a **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="43017-133">Because a message's entry identifier is invalidated after the message has been submitted, it is necessary to save it before calling **SubmitMessage**.</span></span> <span data-ttu-id="43017-134">Para cancelar el envío, seleccione el parámetro _lpEntryId_ para este identificador de entrada y llame a [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span><span class="sxs-lookup"><span data-stu-id="43017-134">To cancel the send, point the  _lpEntryId_ parameter to this entry identifier and call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="43017-135">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="43017-135">MFCMAPI reference</span></span>

<span data-ttu-id="43017-136">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="43017-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="43017-137">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="43017-137">**File**</span></span>|<span data-ttu-id="43017-138">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="43017-138">**Function**</span></span>|<span data-ttu-id="43017-139">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="43017-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="43017-140">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="43017-140">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="43017-141">**CFolderDlg::OnSubmitMessage**</span><span class="sxs-lookup"><span data-stu-id="43017-141">**CFolderDlg::OnSubmitMessage**</span></span> <br/> |<span data-ttu-id="43017-142">MFCMAPI usa el método **IMessage::SubmitMessage** para enviar el mensaje seleccionado.</span><span class="sxs-lookup"><span data-stu-id="43017-142">MFCMAPI uses the **IMessage::SubmitMessage** method to submit the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43017-143">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="43017-143">See also</span></span>



[<span data-ttu-id="43017-144">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="43017-144">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="43017-145">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="43017-145">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="43017-146">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="43017-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

