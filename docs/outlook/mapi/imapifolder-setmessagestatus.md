---
title: IMAPIFolderSetMessageStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetMessageStatus
api_type:
- COM
ms.assetid: 42ffbbe0-d678-474a-a016-91c71255613e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fcca6a7e8fa70a2df9042e8b3c2b28825cee9a7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817255"
---
# <a name="imapifoldersetmessagestatus"></a><span data-ttu-id="88103-103">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="88103-103">IMAPIFolder::SetMessageStatus</span></span>

  
  
<span data-ttu-id="88103-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="88103-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="88103-105">Establece el estado asociado a un mensaje (por ejemplo, si ese mensaje está marcado para su eliminación).</span><span class="sxs-lookup"><span data-stu-id="88103-105">Sets the status associated with a message (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a><span data-ttu-id="88103-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88103-106">Parameters</span></span>

 <span data-ttu-id="88103-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="88103-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="88103-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="88103-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="88103-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="88103-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="88103-110">[entrada] Un puntero al identificador de entrada para el mensaje cuyo estado está establecido.</span><span class="sxs-lookup"><span data-stu-id="88103-110">[in] A pointer to the entry identifier for the message whose status is set.</span></span>
    
 <span data-ttu-id="88103-111">_ulNewStatus_</span><span class="sxs-lookup"><span data-stu-id="88103-111">_ulNewStatus_</span></span>
  
> <span data-ttu-id="88103-112">[entrada] El nuevo estado que se asignará.</span><span class="sxs-lookup"><span data-stu-id="88103-112">[in] The new status to be assigned.</span></span> 
    
 <span data-ttu-id="88103-113">_ulNewStatusMask_</span><span class="sxs-lookup"><span data-stu-id="88103-113">_ulNewStatusMask_</span></span>
  
> <span data-ttu-id="88103-114">[entrada] Una máscara de bits de indicadores que se aplica al nuevo estado e indica los indicadores que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="88103-114">[in] A bitmask of flags that is applied to the new status and indicates the flags to be set.</span></span> <span data-ttu-id="88103-115">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="88103-115">The following flags can be set:</span></span>
    
<span data-ttu-id="88103-116">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="88103-116">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="88103-117">El mensaje se ha marcado para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="88103-117">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="88103-118">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="88103-118">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="88103-119">El mensaje no es se muestre.</span><span class="sxs-lookup"><span data-stu-id="88103-119">The message is not to be displayed.</span></span>
    
<span data-ttu-id="88103-120">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="88103-120">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="88103-121">Es el mensaje que se mostrará resaltado.</span><span class="sxs-lookup"><span data-stu-id="88103-121">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="88103-122">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="88103-122">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="88103-123">El mensaje se ha marcado para su eliminación en el almacén de mensajes remoto sin descargar en el cliente local.</span><span class="sxs-lookup"><span data-stu-id="88103-123">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="88103-124">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="88103-124">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="88103-125">El mensaje se ha marcado para la descarga desde el almacén de mensajes remoto para el cliente local.</span><span class="sxs-lookup"><span data-stu-id="88103-125">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="88103-126">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="88103-126">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="88103-127">El mensaje se ha etiquetado con un fin definidas por el cliente.</span><span class="sxs-lookup"><span data-stu-id="88103-127">The message has been tagged for a client-defined purpose.</span></span>
    
 <span data-ttu-id="88103-128">_lpulOldStatus_</span><span class="sxs-lookup"><span data-stu-id="88103-128">_lpulOldStatus_</span></span>
  
> <span data-ttu-id="88103-129">[out] Un puntero al estado anterior del mensaje.</span><span class="sxs-lookup"><span data-stu-id="88103-129">[out] A pointer to the previous status of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="88103-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88103-130">Return value</span></span>

<span data-ttu-id="88103-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="88103-131">S_OK</span></span> 
  
> <span data-ttu-id="88103-132">El estado del mensaje se estableció correctamente.</span><span class="sxs-lookup"><span data-stu-id="88103-132">The message status was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="88103-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="88103-133">Remarks</span></span>

<span data-ttu-id="88103-134">El método **IMAPIFolder::SetMessageStatus** establece el estado del mensaje en el valor que se almacena en su propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="88103-134">The **IMAPIFolder::SetMessageStatus** method sets the message status to the value that is stored in its **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="88103-135">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="88103-135">Notes to implementers</span></span>

<span data-ttu-id="88103-136">Cómo los bits de estado del mensaje se establece, desactivados y usa depende completamente de la implementación, excepto que los bits 0 a 15 están reservados y deben ser cero.</span><span class="sxs-lookup"><span data-stu-id="88103-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> 
  
<span data-ttu-id="88103-137">Implementación del proveedor de transporte remoto de este método debe seguir la semántica que se describen aquí.</span><span class="sxs-lookup"><span data-stu-id="88103-137">A remote transport provider's implementation of this method must follow the semantics described here.</span></span> <span data-ttu-id="88103-138">No hay ninguna consideración especial.</span><span class="sxs-lookup"><span data-stu-id="88103-138">There are no special considerations.</span></span> <span data-ttu-id="88103-139">Los clientes de utilizar este método para configurar los bits MSGSTATUS_REMOTE_DOWNLOAD y MSGSTATUS_REMOTE_DELETE para indicar que un mensaje determinado se va a descargar o eliminar desde el almacén de mensajes remoto.</span><span class="sxs-lookup"><span data-stu-id="88103-139">Clients use this method to set the MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE bits to indicate that a particular message is to be downloaded or deleted from the remote message store.</span></span> <span data-ttu-id="88103-140">Un proveedor de transporte remoto no tiene que implementar el método [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) relacionado.</span><span class="sxs-lookup"><span data-stu-id="88103-140">A remote transport provider does not have to implement the related [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) method.</span></span> <span data-ttu-id="88103-141">Los clientes deben buscar en la tabla de contenido de la carpeta para determinar el estado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="88103-141">Clients must look in the folder's contents table to determine the status of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="88103-142">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="88103-142">Notes to callers</span></span>

<span data-ttu-id="88103-143">Puede usar la propiedad **PR_MSG_STATUS** de un mensaje para la negociación de una operación de bloqueo de mensajes con otros clientes.</span><span class="sxs-lookup"><span data-stu-id="88103-143">You can use the **PR_MSG_STATUS** property of a message to negotiate a message lockout operation with other clients.</span></span> <span data-ttu-id="88103-144">Designar un poco como el bit de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="88103-144">Designate a bit as the lockout bit.</span></span> <span data-ttu-id="88103-145">Para determinar si se ha establecido el bit de bloqueo, examine el valor anterior de estado del mensaje en el parámetro _lpulOldStatus_ .</span><span class="sxs-lookup"><span data-stu-id="88103-145">To determine whether the lockout bit was set, examine the previous value for message status in the  _lpulOldStatus_ parameter.</span></span> <span data-ttu-id="88103-146">Use el resto de los bits en el parámetro _ulNewStatus_ para realizar un seguimiento del estado del mensaje sin interferir con el bit de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="88103-146">Use the other bits in the  _ulNewStatus_ parameter to track message status without interfering with the lockout bit.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="88103-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="88103-147">See also</span></span>



[<span data-ttu-id="88103-148">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="88103-148">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="88103-149">Propiedad canónica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="88103-149">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="88103-150">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="88103-150">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

