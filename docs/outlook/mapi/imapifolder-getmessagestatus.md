---
title: IMAPIFolderGetMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.GetMessageStatus
api_type:
- COM
ms.assetid: 3ddbb129-5d6b-4eca-aba0-3620609ed0c1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bac363183c15a2d53c15b46724266b6cb5744075
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817244"
---
# <a name="imapifoldergetmessagestatus"></a><span data-ttu-id="1650c-103">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="1650c-103">IMAPIFolder::GetMessageStatus</span></span>

  
  
<span data-ttu-id="1650c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1650c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1650c-105">Obtiene el estado asociado a un mensaje de una carpeta determinada (por ejemplo, si ese mensaje está marcado para su eliminación).</span><span class="sxs-lookup"><span data-stu-id="1650c-105">Obtains the status associated with a message in a particular folder (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a><span data-ttu-id="1650c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1650c-106">Parameters</span></span>

 <span data-ttu-id="1650c-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1650c-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="1650c-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="1650c-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1650c-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1650c-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="1650c-110">[entrada] Un puntero a para el mensaje cuyo estado se obtiene el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="1650c-110">[in] A pointer to the entry identifier for the message whose status is obtained.</span></span>
    
 <span data-ttu-id="1650c-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1650c-111">_ulFlags_</span></span>
  
> <span data-ttu-id="1650c-112">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1650c-112">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1650c-113">_lpulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="1650c-113">_lpulMessageStatus_</span></span>
  
> <span data-ttu-id="1650c-114">[out] Un puntero a un puntero a una máscara de bits de marcadores que indican el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="1650c-114">[out] A pointer to a pointer to a bitmask of flags that indicate the message's status.</span></span> <span data-ttu-id="1650c-115">De 0 a 15 bits están reservados y deben ser cero; 16 a través de 31 bits están disponibles para su uso específico de la implementación.</span><span class="sxs-lookup"><span data-stu-id="1650c-115">Bits 0 through 15 are reserved and must be zero; bits 16 through 31 are available for implementation-specific use.</span></span> <span data-ttu-id="1650c-116">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="1650c-116">The following flags can be set:</span></span>
    
<span data-ttu-id="1650c-117">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="1650c-117">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="1650c-118">El mensaje se ha marcado para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="1650c-118">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="1650c-119">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="1650c-119">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="1650c-120">El mensaje no es se muestre.</span><span class="sxs-lookup"><span data-stu-id="1650c-120">The message is not to be displayed.</span></span> 
    
<span data-ttu-id="1650c-121">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="1650c-121">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="1650c-122">Es el mensaje que se mostrará resaltado.</span><span class="sxs-lookup"><span data-stu-id="1650c-122">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="1650c-123">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="1650c-123">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="1650c-124">El mensaje se ha marcado para su eliminación en el almacén de mensajes remoto sin descargar en el cliente local.</span><span class="sxs-lookup"><span data-stu-id="1650c-124">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="1650c-125">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="1650c-125">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="1650c-126">El mensaje se ha marcado para la descarga desde el almacén de mensajes remoto para el cliente local.</span><span class="sxs-lookup"><span data-stu-id="1650c-126">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="1650c-127">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="1650c-127">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="1650c-128">El mensaje se ha etiquetado con un fin definidas por el cliente.</span><span class="sxs-lookup"><span data-stu-id="1650c-128">The message has been tagged for a client-defined purpose.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1650c-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1650c-129">Return value</span></span>

<span data-ttu-id="1650c-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="1650c-130">S_OK</span></span> 
  
> <span data-ttu-id="1650c-131">El estado del mensaje se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1650c-131">The message status was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1650c-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1650c-132">Remarks</span></span>

<span data-ttu-id="1650c-133">El método **IMAPIFolder::GetMessageStatus** devuelve el estado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="1650c-133">The **IMAPIFolder::GetMessageStatus** method returns the status of a message.</span></span> <span data-ttu-id="1650c-134">Estado del mensaje se almacena en la propiedad del mensaje **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1650c-134">Message status is stored in the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1650c-135">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="1650c-135">Notes to implementers</span></span>

<span data-ttu-id="1650c-136">Cómo los bits de estado del mensaje se establece, desactivados y usa depende completamente de la implementación, excepto que los bits 0 a 15 están reservados y deben ser cero.</span><span class="sxs-lookup"><span data-stu-id="1650c-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> <span data-ttu-id="1650c-137">Si almacena los mensajes en el subárbol IPM, MAPI reserva bits 16 a través de 31 para su uso por los clientes IPM.</span><span class="sxs-lookup"><span data-stu-id="1650c-137">If you store messages in the IPM subtree, MAPI reserves bits 16 through 31 for use by IPM clients.</span></span> <span data-ttu-id="1650c-138">Si almacena los mensajes en otros subárboles, puede utilizar bits 16 a través de 31 para sus propios fines.</span><span class="sxs-lookup"><span data-stu-id="1650c-138">If you store messages in other subtrees, you can use bits 16 through 31 for your own purposes.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1650c-139">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1650c-139">MFCMAPI reference</span></span>

<span data-ttu-id="1650c-140">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1650c-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1650c-141">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="1650c-141">**File**</span></span>|<span data-ttu-id="1650c-142">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="1650c-142">**Function**</span></span>|<span data-ttu-id="1650c-143">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="1650c-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1650c-144">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="1650c-144">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="1650c-145">CMyMAPIFormViewer::GetNextMessage</span><span class="sxs-lookup"><span data-stu-id="1650c-145">CMyMAPIFormViewer::GetNextMessage</span></span>  <br/> |<span data-ttu-id="1650c-146">MFCMAPI usa el método **IMAPIFolder::GetMessageStatus** para obtener el estado del siguiente mensaje que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="1650c-146">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the next message to be displayed.</span></span>  <br/> |
|<span data-ttu-id="1650c-147">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1650c-147">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1650c-148">OpenMessageNonModal y OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="1650c-148">OpenMessageNonModal and OpenMessageModal</span></span>  <br/> |<span data-ttu-id="1650c-149">MFCMAPI usa el método **IMAPIFolder::GetMessageStatus** para obtener el estado del mensaje que se mostrará para pasar al Visor de formulario, que es CMyMAPIFormViewer o [IMAPISession:: ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="1650c-149">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the message to be displayed to pass to the form viewer, which is either CMyMAPIFormViewer or [IMAPISession::ShowForm](imapisession-showform.md).</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1650c-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="1650c-150">See also</span></span>



[<span data-ttu-id="1650c-151">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="1650c-151">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
  
[<span data-ttu-id="1650c-152">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="1650c-152">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="1650c-153">Propiedad canónica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="1650c-153">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="1650c-154">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="1650c-154">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="1650c-155">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="1650c-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

