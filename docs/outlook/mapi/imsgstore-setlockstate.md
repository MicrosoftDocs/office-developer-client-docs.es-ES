---
title: IMsgStoreSetLockState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetLockState
api_type:
- COM
ms.assetid: 4b1176ec-4126-43f5-856d-cbab8d622825
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2efee531e277b6295b7d4bc299eefc789a805d34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571090"
---
# <a name="imsgstoresetlockstate"></a><span data-ttu-id="f5df9-103">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="f5df9-103">IMsgStore::SetLockState</span></span>

  
  
<span data-ttu-id="f5df9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5df9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5df9-105">Bloquea o desbloquea un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f5df9-105">Locks or unlocks a message.</span></span> <span data-ttu-id="f5df9-106">Se llama a este m�todo s�lo por la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="f5df9-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a><span data-ttu-id="f5df9-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="f5df9-107">Parameters</span></span>

 <span data-ttu-id="f5df9-108">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="f5df9-108">_lpMessage_</span></span>
  
> <span data-ttu-id="f5df9-109">[entrada] Un puntero al mensaje que se va a bloquear o desbloquear.</span><span class="sxs-lookup"><span data-stu-id="f5df9-109">[in] A pointer to the message to lock or unlock.</span></span>
    
 <span data-ttu-id="f5df9-110">_ulLockState_</span><span class="sxs-lookup"><span data-stu-id="f5df9-110">_ulLockState_</span></span>
  
> <span data-ttu-id="f5df9-111">[entrada] Un valor que indica si el mensaje debe ser bloqueado o desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="f5df9-111">[in] A value that indicates whether the message should be locked or unlocked.</span></span> <span data-ttu-id="f5df9-112">Uno de los valores siguientes es válida:</span><span class="sxs-lookup"><span data-stu-id="f5df9-112">One of the following values is valid:</span></span>
    
<span data-ttu-id="f5df9-113">MSG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="f5df9-113">MSG_LOCKED</span></span> 
  
> <span data-ttu-id="f5df9-114">Debe ser bloqueado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f5df9-114">The message should be locked.</span></span> 
    
<span data-ttu-id="f5df9-115">MSG_UNLOCKED</span><span class="sxs-lookup"><span data-stu-id="f5df9-115">MSG_UNLOCKED</span></span> 
  
> <span data-ttu-id="f5df9-116">El mensaje debe ser desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="f5df9-116">The message should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f5df9-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5df9-117">Return value</span></span>

<span data-ttu-id="f5df9-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5df9-118">S_OK</span></span> 
  
> <span data-ttu-id="f5df9-119">El estado de bloqueo del mensaje se estableció correctamente.</span><span class="sxs-lookup"><span data-stu-id="f5df9-119">The lock state of the message was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f5df9-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f5df9-120">Remarks</span></span>

<span data-ttu-id="f5df9-121">El método **IMsgStore::SetLockState** se bloquea o desbloquea un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f5df9-121">The **IMsgStore::SetLockState** method locks or unlocks a message.</span></span> <span data-ttu-id="f5df9-122">**SetLockState** se puede llamar sólo por la cola MAPI mientras está enviando el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f5df9-122">**SetLockState** can be called only by the MAPI spooler while it is sending the message.</span></span> 
  
<span data-ttu-id="f5df9-123">Normalmente, cuando la cola MAPI llama a **SetLockState** para bloquear un mensaje, bloquea sólo el mensaje más antiguo (es decir, el siguiente mensaje en cola para que la cola MAPI enviar).</span><span class="sxs-lookup"><span data-stu-id="f5df9-123">Usually, when the MAPI spooler calls **SetLockState** to lock a message, it locks only the oldest message (that is, the next message queued for the MAPI spooler to send).</span></span> <span data-ttu-id="f5df9-124">Si el mensaje más antiguo en la cola está esperando para un proveedor de transporte disponible temporalmente, y el siguiente mensaje en la cola usa un proveedor de transporte diferentes, la cola MAPI puede empezar a procesar el mensaje posterior.</span><span class="sxs-lookup"><span data-stu-id="f5df9-124">If the oldest message in the queue is waiting for a temporarily unavailable transport provider, and the next message in the queue uses a different transport provider, the MAPI spooler can begin processing the later message.</span></span> <span data-ttu-id="f5df9-125">Comienza el procesamiento bloqueando ese mensaje mediante el uso de **SetLockState**.</span><span class="sxs-lookup"><span data-stu-id="f5df9-125">It begins processing by locking that message by using **SetLockState**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f5df9-126">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="f5df9-126">Notes to implementers</span></span>

<span data-ttu-id="f5df9-127">Después de la cola MAPI ha llamado **SetLockState** con el parámetro _ulLockState_ establecido en MSG_LOCKED, se deben producir un error en las llamadas al método [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para cancelar la transmisión del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f5df9-127">After the MAPI spooler has called **SetLockState** with the  _ulLockState_ parameter set to MSG_LOCKED, calls to the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method to cancel the message's transmission must fail.</span></span> 
  
<span data-ttu-id="f5df9-128">Llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje en su implementación de **SetLockState** para que se guarden los cambios realizados en el mensaje antes de que se recibió la llamada **SetLockState** .</span><span class="sxs-lookup"><span data-stu-id="f5df9-128">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method in your **SetLockState** implementation so that any changes that were made to the message before the **SetLockState** call was received are saved.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f5df9-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f5df9-129">See also</span></span>



[<span data-ttu-id="f5df9-130">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="f5df9-130">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="f5df9-131">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="f5df9-131">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="f5df9-132">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f5df9-132">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

