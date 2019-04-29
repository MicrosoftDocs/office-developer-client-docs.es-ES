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
ms.openlocfilehash: 621c20376cc671a2ff9d1406bfb6248846e1bc81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418641"
---
# <a name="imapifoldergetmessagestatus"></a><span data-ttu-id="aceb4-103">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="aceb4-103">IMAPIFolder::GetMessageStatus</span></span>

  
  
<span data-ttu-id="aceb4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aceb4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aceb4-105">Obtiene el estado asociado a un mensaje en una carpeta determinada (por ejemplo, si el mensaje está marcado para su eliminación).</span><span class="sxs-lookup"><span data-stu-id="aceb4-105">Obtains the status associated with a message in a particular folder (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a><span data-ttu-id="aceb4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="aceb4-106">Parameters</span></span>

 <span data-ttu-id="aceb4-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="aceb4-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="aceb4-108">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="aceb4-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="aceb4-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="aceb4-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="aceb4-110">a Un puntero al identificador de entrada del mensaje cuyo estado se obtiene.</span><span class="sxs-lookup"><span data-stu-id="aceb4-110">[in] A pointer to the entry identifier for the message whose status is obtained.</span></span>
    
 <span data-ttu-id="aceb4-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aceb4-111">_ulFlags_</span></span>
  
> <span data-ttu-id="aceb4-112">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="aceb4-112">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="aceb4-113">_lpulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="aceb4-113">_lpulMessageStatus_</span></span>
  
> <span data-ttu-id="aceb4-114">contempla Un puntero a un puntero a una máscara de máscara de marcas que indica el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="aceb4-114">[out] A pointer to a pointer to a bitmask of flags that indicate the message's status.</span></span> <span data-ttu-id="aceb4-115">Los bits del 0 al 15 están reservados y deben ser cero; los bits 16 a 31 están disponibles para uso específico de la implementación.</span><span class="sxs-lookup"><span data-stu-id="aceb4-115">Bits 0 through 15 are reserved and must be zero; bits 16 through 31 are available for implementation-specific use.</span></span> <span data-ttu-id="aceb4-116">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="aceb4-116">The following flags can be set:</span></span>
    
<span data-ttu-id="aceb4-117">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="aceb4-117">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="aceb4-118">El mensaje se ha marcado para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="aceb4-118">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="aceb4-119">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="aceb4-119">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="aceb4-120">El mensaje no se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="aceb4-120">The message is not to be displayed.</span></span> 
    
<span data-ttu-id="aceb4-121">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="aceb4-121">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="aceb4-122">El mensaje se mostrará resaltado.</span><span class="sxs-lookup"><span data-stu-id="aceb4-122">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="aceb4-123">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="aceb4-123">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="aceb4-124">El mensaje se marcó para ser eliminado en el almacén de mensajes remoto sin descargarse al cliente local.</span><span class="sxs-lookup"><span data-stu-id="aceb4-124">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="aceb4-125">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="aceb4-125">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="aceb4-126">El mensaje se marcó para descargar del almacén de mensajes remoto en el cliente local.</span><span class="sxs-lookup"><span data-stu-id="aceb4-126">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="aceb4-127">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="aceb4-127">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="aceb4-128">El mensaje se ha etiquetado para un propósito definido por el cliente.</span><span class="sxs-lookup"><span data-stu-id="aceb4-128">The message has been tagged for a client-defined purpose.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aceb4-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aceb4-129">Return value</span></span>

<span data-ttu-id="aceb4-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="aceb4-130">S_OK</span></span> 
  
> <span data-ttu-id="aceb4-131">El estado del mensaje se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="aceb4-131">The message status was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aceb4-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aceb4-132">Remarks</span></span>

<span data-ttu-id="aceb4-133">El método **IMAPIFolder:: GetMessageStatus** devuelve el estado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="aceb4-133">The **IMAPIFolder::GetMessageStatus** method returns the status of a message.</span></span> <span data-ttu-id="aceb4-134">El estado del mensaje se almacena en la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="aceb4-134">Message status is stored in the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="aceb4-135">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="aceb4-135">Notes to implementers</span></span>

<span data-ttu-id="aceb4-136">La forma en que los bits de estado del mensaje se establecen, borran y usan dependen por completo de la implementación, excepto que los bits del 0 al 15 están reservados y deben ser cero.</span><span class="sxs-lookup"><span data-stu-id="aceb4-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> <span data-ttu-id="aceb4-137">Si almacena mensajes en el subárbol IPM, MAPI reserva los bits 16 a 31 para que los usen los clientes IPM.</span><span class="sxs-lookup"><span data-stu-id="aceb4-137">If you store messages in the IPM subtree, MAPI reserves bits 16 through 31 for use by IPM clients.</span></span> <span data-ttu-id="aceb4-138">Si almacena mensajes en otros subárboles, puede usar bits 16 a 31 para sus propios fines.</span><span class="sxs-lookup"><span data-stu-id="aceb4-138">If you store messages in other subtrees, you can use bits 16 through 31 for your own purposes.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="aceb4-139">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="aceb4-139">MFCMAPI reference</span></span>

<span data-ttu-id="aceb4-140">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="aceb4-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="aceb4-141">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="aceb4-141">**File**</span></span>|<span data-ttu-id="aceb4-142">**Función**</span><span class="sxs-lookup"><span data-stu-id="aceb4-142">**Function**</span></span>|<span data-ttu-id="aceb4-143">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="aceb4-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aceb4-144">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="aceb4-144">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="aceb4-145">CMyMAPIFormViewer:: GetNextMessage</span><span class="sxs-lookup"><span data-stu-id="aceb4-145">CMyMAPIFormViewer::GetNextMessage</span></span>  <br/> |<span data-ttu-id="aceb4-146">MFCMAPI usa el método **IMAPIFolder:: GetMessageStatus** para obtener el estado del siguiente mensaje que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="aceb4-146">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the next message to be displayed.</span></span>  <br/> |
|<span data-ttu-id="aceb4-147">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="aceb4-147">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="aceb4-148">OpenMessageNonModal y OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="aceb4-148">OpenMessageNonModal and OpenMessageModal</span></span>  <br/> |<span data-ttu-id="aceb4-149">MFCMAPI usa el método **IMAPIFolder:: GetMessageStatus** para obtener el estado del mensaje que se mostrará para pasar al visor de formularios, que es CMyMAPIFormViewer o [IMAPISession:: ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="aceb4-149">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the message to be displayed to pass to the form viewer, which is either CMyMAPIFormViewer or [IMAPISession::ShowForm](imapisession-showform.md).</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aceb4-150">Ver también</span><span class="sxs-lookup"><span data-stu-id="aceb4-150">See also</span></span>



[<span data-ttu-id="aceb4-151">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="aceb4-151">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
  
[<span data-ttu-id="aceb4-152">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="aceb4-152">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="aceb4-153">Propiedad canónica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="aceb4-153">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="aceb4-154">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="aceb4-154">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="aceb4-155">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="aceb4-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

