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
ms.openlocfilehash: 9eeede2a430f5186daf429dd6ed59f312ae334be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348751"
---
# <a name="imsgstoresetlockstate"></a><span data-ttu-id="4ddd7-103">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="4ddd7-103">IMsgStore::SetLockState</span></span>

  
  
<span data-ttu-id="4ddd7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ddd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ddd7-105">Bloquea o desbloquea un mensaje.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-105">Locks or unlocks a message.</span></span> <span data-ttu-id="4ddd7-106">Se llama a este m�todo s�lo por la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a><span data-ttu-id="4ddd7-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="4ddd7-107">Parameters</span></span>

 <span data-ttu-id="4ddd7-108">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="4ddd7-108">_lpMessage_</span></span>
  
> <span data-ttu-id="4ddd7-109">a Un puntero al mensaje que se va a bloquear o desbloquear.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-109">[in] A pointer to the message to lock or unlock.</span></span>
    
 <span data-ttu-id="4ddd7-110">_ulLockState_</span><span class="sxs-lookup"><span data-stu-id="4ddd7-110">_ulLockState_</span></span>
  
> <span data-ttu-id="4ddd7-111">a Un valor que indica si el mensaje debe estar bloqueado o desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-111">[in] A value that indicates whether the message should be locked or unlocked.</span></span> <span data-ttu-id="4ddd7-112">Uno de los siguientes valores es válido:</span><span class="sxs-lookup"><span data-stu-id="4ddd7-112">One of the following values is valid:</span></span>
    
<span data-ttu-id="4ddd7-113">MSG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="4ddd7-113">MSG_LOCKED</span></span> 
  
> <span data-ttu-id="4ddd7-114">El mensaje debe estar bloqueado.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-114">The message should be locked.</span></span> 
    
<span data-ttu-id="4ddd7-115">MSG_UNLOCKED</span><span class="sxs-lookup"><span data-stu-id="4ddd7-115">MSG_UNLOCKED</span></span> 
  
> <span data-ttu-id="4ddd7-116">El mensaje debe estar desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-116">The message should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4ddd7-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ddd7-117">Return value</span></span>

<span data-ttu-id="4ddd7-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="4ddd7-118">S_OK</span></span> 
  
> <span data-ttu-id="4ddd7-119">El estado de bloqueo del mensaje se estableció correctamente.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-119">The lock state of the message was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4ddd7-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ddd7-120">Remarks</span></span>

<span data-ttu-id="4ddd7-121">El método **IMsgStore:: SetLockState** bloquea o desbloquea un mensaje.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-121">The **IMsgStore::SetLockState** method locks or unlocks a message.</span></span> <span data-ttu-id="4ddd7-122">Solo puede llamar a **SetLockState** la cola MAPI mientras envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-122">**SetLockState** can be called only by the MAPI spooler while it is sending the message.</span></span> 
  
<span data-ttu-id="4ddd7-123">Normalmente, cuando la cola MAPI llama a **SetLockState** para bloquear un mensaje, bloquea sólo el mensaje más antiguo (es decir, el siguiente mensaje que se pone en cola para que lo envíe la cola MAPI).</span><span class="sxs-lookup"><span data-stu-id="4ddd7-123">Usually, when the MAPI spooler calls **SetLockState** to lock a message, it locks only the oldest message (that is, the next message queued for the MAPI spooler to send).</span></span> <span data-ttu-id="4ddd7-124">Si el mensaje más antiguo de la cola está esperando a un proveedor de transporte no disponible temporalmente y el siguiente mensaje de la cola usa un proveedor de transporte diferente, la cola MAPI puede empezar a procesar el mensaje posterior.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-124">If the oldest message in the queue is waiting for a temporarily unavailable transport provider, and the next message in the queue uses a different transport provider, the MAPI spooler can begin processing the later message.</span></span> <span data-ttu-id="4ddd7-125">Comienza el procesamiento bloqueando el mensaje mediante **SetLockState**.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-125">It begins processing by locking that message by using **SetLockState**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4ddd7-126">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="4ddd7-126">Notes to implementers</span></span>

<span data-ttu-id="4ddd7-127">Una vez que la cola MAPI llamó a **SetLockState** con el parámetro _ULLOCKSTATE_ establecido en MSG_LOCKED, las llamadas al método [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) para cancelar la transmisión del mensaje deben producir un error.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-127">After the MAPI spooler has called **SetLockState** with the  _ulLockState_ parameter set to MSG_LOCKED, calls to the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method to cancel the message's transmission must fail.</span></span> 
  
<span data-ttu-id="4ddd7-128">Llame al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del mensaje en la implementación de **SetLockState** para que se guarden todos los cambios realizados en el mensaje antes de que se haya recibido la llamada **SetLockState** .</span><span class="sxs-lookup"><span data-stu-id="4ddd7-128">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method in your **SetLockState** implementation so that any changes that were made to the message before the **SetLockState** call was received are saved.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4ddd7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ddd7-129">See also</span></span>



[<span data-ttu-id="4ddd7-130">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="4ddd7-130">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="4ddd7-131">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="4ddd7-131">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="4ddd7-132">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4ddd7-132">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

