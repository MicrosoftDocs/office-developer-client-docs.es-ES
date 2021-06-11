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
ms.openlocfilehash: 9e7d7ba91791258eca93a2b8bedf95cf121062c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427090"
---
# <a name="imsgstorefinishedmsg"></a><span data-ttu-id="0c15c-103">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="0c15c-103">IMsgStore::FinishedMsg</span></span>

  
  
<span data-ttu-id="0c15c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c15c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c15c-105">Permite al proveedor del almacén de mensajes realizar el procesamiento en un mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="0c15c-105">Enables the message store provider to perform processing on a sent message.</span></span> <span data-ttu-id="0c15c-106">Se llama a este m�todo s�lo por la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="0c15c-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="0c15c-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="0c15c-107">Parameters</span></span>

 <span data-ttu-id="0c15c-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0c15c-108">_ulFlags_</span></span>
  
> <span data-ttu-id="0c15c-109">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0c15c-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="0c15c-110">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="0c15c-110">_cbEntryID_</span></span>
  
> <span data-ttu-id="0c15c-111">[in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="0c15c-111">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="0c15c-112">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="0c15c-112">_lpEntryID_</span></span>
  
> <span data-ttu-id="0c15c-113">[in] Puntero al identificador de entrada del mensaje que se va a procesar.</span><span class="sxs-lookup"><span data-stu-id="0c15c-113">[in] A pointer to the entry identifier of the message to be processed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0c15c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c15c-114">Return value</span></span>

<span data-ttu-id="0c15c-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c15c-115">S_OK</span></span> 
  
> <span data-ttu-id="0c15c-116">El procesamiento en el mensaje enviado se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0c15c-116">Processing on the sent message was successful.</span></span>
    
<span data-ttu-id="0c15c-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0c15c-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0c15c-118">El proveedor del almacén de mensajes no admite el procesamiento de mensajes enviados.</span><span class="sxs-lookup"><span data-stu-id="0c15c-118">The message store provider does not support sent message processing.</span></span> <span data-ttu-id="0c15c-119">Este valor de error se devuelve si el autor de la llamada no es la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="0c15c-119">This error value is returned if the caller is not the MAPI spooler.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c15c-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0c15c-120">Remarks</span></span>

<span data-ttu-id="0c15c-121">El **método IMsgStore::FinishedMsg** realiza el procesamiento en un mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="0c15c-121">The **IMsgStore::FinishedMsg** method performs processing on a sent message.</span></span> <span data-ttu-id="0c15c-122">Este procesamiento puede implicar eliminar el mensaje, moverlo a una carpeta diferente o ambas acciones.</span><span class="sxs-lookup"><span data-stu-id="0c15c-122">This processing can involve deleting the message, moving it to a different folder, or both actions.</span></span> <span data-ttu-id="0c15c-123">El tipo de procesamiento depende de si se establecen las propiedades **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) y **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0c15c-123">The type of processing depends on whether the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) and **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) properties are set.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0c15c-124">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="0c15c-124">Notes to implementers</span></span>

<span data-ttu-id="0c15c-125">En la implementación de **FinishedMsg,** desbloquea el mensaje identificado por  _lpEntryID_ y realiza el procesamiento adecuado.</span><span class="sxs-lookup"><span data-stu-id="0c15c-125">In your implementation of **FinishedMsg**, unlock the message identified by  _lpEntryID_ and perform the appropriate processing.</span></span> <span data-ttu-id="0c15c-126">El mensaje de destino siempre estará bloqueado; la cola MAPI nunca pasa el identificador de entrada de un mensaje desbloqueado a **FinishedMsg**.</span><span class="sxs-lookup"><span data-stu-id="0c15c-126">The target message will always be locked; the MAPI spooler never passes the entry identifier for an unlocked message to **FinishedMsg**.</span></span>
  
<span data-ttu-id="0c15c-127">Es posible que no **se PR_DELETE_AFTER_SUBMIT** o **PR_SENTMAIL_ENTRYID,** ambos están establecidos o se establece uno u otro.</span><span class="sxs-lookup"><span data-stu-id="0c15c-127">It is possible that neither **PR_DELETE_AFTER_SUBMIT** or **PR_SENTMAIL_ENTRYID** is set, both are set, or one or the other is set.</span></span> <span data-ttu-id="0c15c-128">En la tabla siguiente se describe la acción que debe realizar en función de la configuración:</span><span class="sxs-lookup"><span data-stu-id="0c15c-128">The following table describes the action you should take based on the settings:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0c15c-129">Si no se establece ninguna propiedad:</span><span class="sxs-lookup"><span data-stu-id="0c15c-129">If neither property is set:</span></span>  <br/> |<span data-ttu-id="0c15c-130">Deje el mensaje en la carpeta desde la que se envió (normalmente, la Bandeja de salida).</span><span class="sxs-lookup"><span data-stu-id="0c15c-130">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="0c15c-131">Si se establecen ambas propiedades:</span><span class="sxs-lookup"><span data-stu-id="0c15c-131">If both properties are set:</span></span>  <br/> |<span data-ttu-id="0c15c-132">Mueva el mensaje a la carpeta indicada, si lo desea, y, a continuación, elimínelo.</span><span class="sxs-lookup"><span data-stu-id="0c15c-132">Move the message to the indicated folder, if desired, and then delete it.</span></span>  <br/> |
|<span data-ttu-id="0c15c-133">Si PR_SENTMAIL_ENTRYID está establecido:</span><span class="sxs-lookup"><span data-stu-id="0c15c-133">If PR_SENTMAIL_ENTRYID is set:</span></span>  <br/> |<span data-ttu-id="0c15c-134">Mueva el mensaje a la carpeta indicada.</span><span class="sxs-lookup"><span data-stu-id="0c15c-134">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="0c15c-135">Si PR_DELETE_AFTER_SUBMIT está establecido:</span><span class="sxs-lookup"><span data-stu-id="0c15c-135">If PR_DELETE_AFTER_SUBMIT is set:</span></span>  <br/> |<span data-ttu-id="0c15c-136">Elimine el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0c15c-136">Delete the message.</span></span>  <br/> |
   
<span data-ttu-id="0c15c-137">Después de realizar cualquier acción que sea apropiada, llame al método [IMAPISupport::D oSentMail.](imapisupport-dosentmail.md)</span><span class="sxs-lookup"><span data-stu-id="0c15c-137">After you have taken whatever action is appropriate, call the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c15c-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c15c-138">See also</span></span>



[<span data-ttu-id="0c15c-139">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="0c15c-139">IMAPISupport::DoSentMail</span></span>](imapisupport-dosentmail.md)
  
[<span data-ttu-id="0c15c-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0c15c-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

