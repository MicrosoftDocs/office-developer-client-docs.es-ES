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
ms.openlocfilehash: fbb05efff67fa90c68db86249d4657e489e7bd63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417276"
---
# <a name="imapifoldersetmessagestatus"></a><span data-ttu-id="e2648-103">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="e2648-103">IMAPIFolder::SetMessageStatus</span></span>

  
  
<span data-ttu-id="e2648-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2648-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2648-105">Establece el estado asociado a un mensaje (por ejemplo, si el mensaje está marcado para su eliminación).</span><span class="sxs-lookup"><span data-stu-id="e2648-105">Sets the status associated with a message (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a><span data-ttu-id="e2648-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e2648-106">Parameters</span></span>

 <span data-ttu-id="e2648-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e2648-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="e2648-108">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="e2648-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e2648-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e2648-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="e2648-110">a Un puntero al identificador de entrada para el mensaje cuyo estado es establecido.</span><span class="sxs-lookup"><span data-stu-id="e2648-110">[in] A pointer to the entry identifier for the message whose status is set.</span></span>
    
 <span data-ttu-id="e2648-111">_ulNewStatus_</span><span class="sxs-lookup"><span data-stu-id="e2648-111">_ulNewStatus_</span></span>
  
> <span data-ttu-id="e2648-112">a Nuevo estado que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="e2648-112">[in] The new status to be assigned.</span></span> 
    
 <span data-ttu-id="e2648-113">_ulNewStatusMask_</span><span class="sxs-lookup"><span data-stu-id="e2648-113">_ulNewStatusMask_</span></span>
  
> <span data-ttu-id="e2648-114">a Máscara de máscara de marcadores que se aplica al nuevo estado e indica las marcas que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="e2648-114">[in] A bitmask of flags that is applied to the new status and indicates the flags to be set.</span></span> <span data-ttu-id="e2648-115">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="e2648-115">The following flags can be set:</span></span>
    
<span data-ttu-id="e2648-116">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="e2648-116">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="e2648-117">El mensaje se ha marcado para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="e2648-117">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="e2648-118">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="e2648-118">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="e2648-119">El mensaje no se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="e2648-119">The message is not to be displayed.</span></span>
    
<span data-ttu-id="e2648-120">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="e2648-120">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="e2648-121">El mensaje se mostrará resaltado.</span><span class="sxs-lookup"><span data-stu-id="e2648-121">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="e2648-122">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="e2648-122">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="e2648-123">El mensaje se marcó para ser eliminado en el almacén de mensajes remoto sin descargarse al cliente local.</span><span class="sxs-lookup"><span data-stu-id="e2648-123">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="e2648-124">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="e2648-124">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="e2648-125">El mensaje se marcó para descargar del almacén de mensajes remoto en el cliente local.</span><span class="sxs-lookup"><span data-stu-id="e2648-125">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="e2648-126">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="e2648-126">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="e2648-127">El mensaje se ha etiquetado para un propósito definido por el cliente.</span><span class="sxs-lookup"><span data-stu-id="e2648-127">The message has been tagged for a client-defined purpose.</span></span>
    
 <span data-ttu-id="e2648-128">_lpulOldStatus_</span><span class="sxs-lookup"><span data-stu-id="e2648-128">_lpulOldStatus_</span></span>
  
> <span data-ttu-id="e2648-129">contempla Un puntero al estado anterior del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e2648-129">[out] A pointer to the previous status of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e2648-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2648-130">Return value</span></span>

<span data-ttu-id="e2648-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2648-131">S_OK</span></span> 
  
> <span data-ttu-id="e2648-132">El estado del mensaje se estableció correctamente.</span><span class="sxs-lookup"><span data-stu-id="e2648-132">The message status was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2648-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2648-133">Remarks</span></span>

<span data-ttu-id="e2648-134">El método **IMAPIFolder:: SetMessageStatus** establece el estado del mensaje en el valor que se almacena en su propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e2648-134">The **IMAPIFolder::SetMessageStatus** method sets the message status to the value that is stored in its **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e2648-135">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="e2648-135">Notes to implementers</span></span>

<span data-ttu-id="e2648-136">La forma en que los bits de estado del mensaje se establecen, borran y usan dependen por completo de la implementación, excepto que los bits del 0 al 15 están reservados y deben ser cero.</span><span class="sxs-lookup"><span data-stu-id="e2648-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> 
  
<span data-ttu-id="e2648-137">La implementación de este método de un proveedor de transporte remoto debe seguir la semántica que se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="e2648-137">A remote transport provider's implementation of this method must follow the semantics described here.</span></span> <span data-ttu-id="e2648-138">No hay ninguna consideración especial.</span><span class="sxs-lookup"><span data-stu-id="e2648-138">There are no special considerations.</span></span> <span data-ttu-id="e2648-139">Los clientes usan este método para establecer los bits MSGSTATUS_REMOTE_DOWNLOAD y MSGSTATUS_REMOTE_DELETE para indicar que un mensaje en particular debe descargarse o eliminarse del almacén de mensajes remoto.</span><span class="sxs-lookup"><span data-stu-id="e2648-139">Clients use this method to set the MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE bits to indicate that a particular message is to be downloaded or deleted from the remote message store.</span></span> <span data-ttu-id="e2648-140">Un proveedor de transporte remoto no tiene que implementar el método [IMAPIFolder:: GetMessageStatus](imapifolder-getmessagestatus.md) relacionado.</span><span class="sxs-lookup"><span data-stu-id="e2648-140">A remote transport provider does not have to implement the related [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) method.</span></span> <span data-ttu-id="e2648-141">Los clientes deben buscar en la tabla de contenido de la carpeta para determinar el estado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="e2648-141">Clients must look in the folder's contents table to determine the status of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e2648-142">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="e2648-142">Notes to callers</span></span>

<span data-ttu-id="e2648-143">Puede usar la propiedad **PR_MSG_STATUS** de un mensaje para negociar una operación de bloqueo de mensajes con otros clientes.</span><span class="sxs-lookup"><span data-stu-id="e2648-143">You can use the **PR_MSG_STATUS** property of a message to negotiate a message lockout operation with other clients.</span></span> <span data-ttu-id="e2648-144">Designar un bit como bit de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="e2648-144">Designate a bit as the lockout bit.</span></span> <span data-ttu-id="e2648-145">Para determinar si se estableció el bit de bloqueo, examine el valor anterior del estado del mensaje en el parámetro _lpulOldStatus_ .</span><span class="sxs-lookup"><span data-stu-id="e2648-145">To determine whether the lockout bit was set, examine the previous value for message status in the  _lpulOldStatus_ parameter.</span></span> <span data-ttu-id="e2648-146">Use los otros bits del parámetro _ulNewStatus_ para realizar un seguimiento del estado del mensaje sin interferir con el bit de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="e2648-146">Use the other bits in the  _ulNewStatus_ parameter to track message status without interfering with the lockout bit.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e2648-147">Ver también</span><span class="sxs-lookup"><span data-stu-id="e2648-147">See also</span></span>



[<span data-ttu-id="e2648-148">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="e2648-148">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="e2648-149">Propiedad canónica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="e2648-149">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="e2648-150">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="e2648-150">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

