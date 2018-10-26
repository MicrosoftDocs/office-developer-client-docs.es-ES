---
title: IMAPISupportDoSentMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoSentMail
api_type:
- COM
ms.assetid: 4bb65c2a-9926-42da-9161-47836e8de40a
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 82490dbe597ebd3f7198aa7e0c904a10202ecd77
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568213"
---
# <a name="imapisupportdosentmail"></a><span data-ttu-id="0d730-103">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="0d730-103">IMAPISupport::DoSentMail</span></span>

  
  
<span data-ttu-id="0d730-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d730-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d730-105">Procesa un mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="0d730-105">Processes a sent message.</span></span>
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="0d730-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="0d730-106">Parameters</span></span>

 <span data-ttu-id="0d730-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0d730-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0d730-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0d730-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="0d730-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="0d730-109">_lpMessage_</span></span>
  
> <span data-ttu-id="0d730-110">[entrada] Un puntero al mensaje abierto para el que se debe generar un mensaje en la carpeta designada para contener los elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="0d730-110">[in] A pointer to the open message for which a message should be generated in the folder designated to hold sent items.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0d730-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d730-111">Return value</span></span>

<span data-ttu-id="0d730-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d730-112">S_OK</span></span> 
  
> <span data-ttu-id="0d730-113">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="0d730-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d730-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0d730-114">Remarks</span></span>

<span data-ttu-id="0d730-p101">The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.</span><span class="sxs-lookup"><span data-stu-id="0d730-p101">The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.</span></span>
  
 <span data-ttu-id="0d730-118">**DoSentMail** realiza las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="0d730-118">**DoSentMail** performs the following tasks:</span></span> 
  
- <span data-ttu-id="0d730-119">Comprueba el mensaje para la propiedad **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) determinar si se debe eliminar el mensaje después de enviarlo.</span><span class="sxs-lookup"><span data-stu-id="0d730-119">Checks the message for the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to determine whether the message should be deleted after sending.</span></span>
    
- <span data-ttu-id="0d730-120">Determina la ubicaci�n de la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="0d730-120">Determines the location of the Sent Items folder.</span></span>
    
- <span data-ttu-id="0d730-121">Inicia el enlace del mensaje de procesamiento para los enlaces definidos en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="0d730-121">Initiates message hook processing for any hooks set on the Sent Items folder.</span></span>
    
- <span data-ttu-id="0d730-122">Mueve el mensaje a la carpeta Elementos enviados, la carpeta Elementos eliminados, o a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="0d730-122">Moves the message to the Sent Items folder, Deleted Items folder, or to another folder.</span></span>
    
- <span data-ttu-id="0d730-123">Libera el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0d730-123">Releases the message.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0d730-124">Vea tambi�n</span><span class="sxs-lookup"><span data-stu-id="0d730-124">See also</span></span>



[<span data-ttu-id="0d730-125">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="0d730-125">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="0d730-126">Propiedad can�nico de PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="0d730-126">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)
  
[<span data-ttu-id="0d730-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d730-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

