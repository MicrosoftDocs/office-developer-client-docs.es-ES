---
title: IMsgStoreFinishedMsg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.FinishedMsg
api_type:
- COM
ms.assetid: c32493fa-aa42-485b-9ea4-f93b835906df
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8b15f12c9a7ac2041c895b935098f9681e4b3a3c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589955"
---
# <a name="imsgstorefinishedmsg"></a><span data-ttu-id="4fb30-103">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="4fb30-103">IMsgStore::FinishedMsg</span></span>

  
  
<span data-ttu-id="4fb30-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fb30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fb30-105">Permite que el proveedor de almacén de mensajes realizar el procesamiento en un mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="4fb30-105">Enables the message store provider to perform processing on a sent message.</span></span> <span data-ttu-id="4fb30-106">Se llama a este m�todo s�lo por la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="4fb30-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="4fb30-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="4fb30-107">Parameters</span></span>

 <span data-ttu-id="4fb30-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4fb30-108">_ulFlags_</span></span>
  
> <span data-ttu-id="4fb30-109">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4fb30-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4fb30-110">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4fb30-110">_cbEntryID_</span></span>
  
> <span data-ttu-id="4fb30-111">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="4fb30-111">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4fb30-112">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4fb30-112">_lpEntryID_</span></span>
  
> <span data-ttu-id="4fb30-113">[entrada] Un puntero al identificador de entrada del mensaje que va a procesar.</span><span class="sxs-lookup"><span data-stu-id="4fb30-113">[in] A pointer to the entry identifier of the message to be processed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4fb30-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4fb30-114">Return value</span></span>

<span data-ttu-id="4fb30-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="4fb30-115">S_OK</span></span> 
  
> <span data-ttu-id="4fb30-116">Procesamiento en el mensaje enviado era correcta.</span><span class="sxs-lookup"><span data-stu-id="4fb30-116">Processing on the sent message was successful.</span></span>
    
<span data-ttu-id="4fb30-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4fb30-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4fb30-118">El proveedor de almacén de mensajes no es compatible con el procesamiento del mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="4fb30-118">The message store provider does not support sent message processing.</span></span> <span data-ttu-id="4fb30-119">Este valor de error se devuelve si el autor de la llamada no es la cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="4fb30-119">This error value is returned if the caller is not the MAPI spooler.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4fb30-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4fb30-120">Remarks</span></span>

<span data-ttu-id="4fb30-121">El método **IMsgStore::FinishedMsg** realiza procesamiento en un mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="4fb30-121">The **IMsgStore::FinishedMsg** method performs processing on a sent message.</span></span> <span data-ttu-id="4fb30-122">Este proceso puede implicar eliminar el mensaje, mover a una carpeta diferente, o ambas acciones.</span><span class="sxs-lookup"><span data-stu-id="4fb30-122">This processing can involve deleting the message, moving it to a different folder, or both actions.</span></span> <span data-ttu-id="4fb30-123">El tipo de procesamiento depende de si se establecen las propiedades de **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) y **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4fb30-123">The type of processing depends on whether the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) and **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) properties are set.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4fb30-124">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="4fb30-124">Notes to implementers</span></span>

<span data-ttu-id="4fb30-125">En la implementación de **FinishedMsg**, desbloquee el mensaje identificado por _lpEntryID_ y realizar el procesamiento adecuado.</span><span class="sxs-lookup"><span data-stu-id="4fb30-125">In your implementation of **FinishedMsg**, unlock the message identified by  _lpEntryID_ and perform the appropriate processing.</span></span> <span data-ttu-id="4fb30-126">Siempre se bloqueará el mensaje de destino; la cola MAPI nunca pasa el identificador de entrada para un mensaje desbloqueado a **FinishedMsg**.</span><span class="sxs-lookup"><span data-stu-id="4fb30-126">The target message will always be locked; the MAPI spooler never passes the entry identifier for an unlocked message to **FinishedMsg**.</span></span>
  
<span data-ttu-id="4fb30-127">Es posible que ni se establece **PR_DELETE_AFTER_SUBMIT** o **PR_SENTMAIL_ENTRYID** , ambos se establecen o se establece uno u otro.</span><span class="sxs-lookup"><span data-stu-id="4fb30-127">It is possible that neither **PR_DELETE_AFTER_SUBMIT** or **PR_SENTMAIL_ENTRYID** is set, both are set, or one or the other is set.</span></span> <span data-ttu-id="4fb30-128">En la siguiente tabla se describe la acción que debe realizar en función de la configuración:</span><span class="sxs-lookup"><span data-stu-id="4fb30-128">The following table describes the action you should take based on the settings:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4fb30-129">Si se establece ninguna de estas propiedades:</span><span class="sxs-lookup"><span data-stu-id="4fb30-129">If neither property is set:</span></span>  <br/> |<span data-ttu-id="4fb30-130">Dejar el mensaje en la carpeta desde la que se envió (normalmente, la Bandeja de salida).</span><span class="sxs-lookup"><span data-stu-id="4fb30-130">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="4fb30-131">Si se establecen las dos propiedades:</span><span class="sxs-lookup"><span data-stu-id="4fb30-131">If both properties are set:</span></span>  <br/> |<span data-ttu-id="4fb30-132">Mover el mensaje a la carpeta indicada, si así lo desea y, a continuación, elimínela.</span><span class="sxs-lookup"><span data-stu-id="4fb30-132">Move the message to the indicated folder, if desired, and then delete it.</span></span>  <br/> |
|<span data-ttu-id="4fb30-133">Si se establece PR_SENTMAIL_ENTRYID:</span><span class="sxs-lookup"><span data-stu-id="4fb30-133">If PR_SENTMAIL_ENTRYID is set:</span></span>  <br/> |<span data-ttu-id="4fb30-134">Mover el mensaje a la carpeta indicada.</span><span class="sxs-lookup"><span data-stu-id="4fb30-134">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="4fb30-135">Si se establece PR_DELETE_AFTER_SUBMIT:</span><span class="sxs-lookup"><span data-stu-id="4fb30-135">If PR_DELETE_AFTER_SUBMIT is set:</span></span>  <br/> |<span data-ttu-id="4fb30-136">Eliminar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="4fb30-136">Delete the message.</span></span>  <br/> |
   
<span data-ttu-id="4fb30-137">Después de haber tomado cualquier acción es adecuada, llame al método [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) .</span><span class="sxs-lookup"><span data-stu-id="4fb30-137">After you have taken whatever action is appropriate, call the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4fb30-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fb30-138">See also</span></span>



[<span data-ttu-id="4fb30-139">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="4fb30-139">IMAPISupport::DoSentMail</span></span>](imapisupport-dosentmail.md)
  
[<span data-ttu-id="4fb30-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4fb30-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

