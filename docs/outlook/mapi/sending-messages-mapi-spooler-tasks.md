---
title: Env�o de mensajes Tareas de cola de impresi�n MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 81c65f21-03ba-43eb-a6d4-d311e660ac5c
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: eef65990637d9c164ffe75f682e01ed134510e32
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570278"
---
# <a name="sending-messages-mapi-spooler-tasks"></a><span data-ttu-id="95ee3-103">Env�o de mensajes: Tareas de cola de impresi�n MAPI</span><span class="sxs-lookup"><span data-stu-id="95ee3-103">Sending Messages: MAPI Spooler Tasks</span></span>

  
  
<span data-ttu-id="95ee3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95ee3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95ee3-105">La cola MAPI est� implicada en el proceso de transmisi�n de mensajes cuando el almac�n de mensajes no est� asociado estrechamente con un proveedor de transporte, cuando el almac�n de acoplamiento ajustado y el transporte no pueden tratar un destinatario y cuando el mensaje requiere preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="95ee3-105">The MAPI spooler is involved in the message transmission process when the message store is not tightly coupled with a transport provider, when the tightly coupled store and transport cannot handle a recipient, and when the message requires preprocessing.</span></span>
  
 <span data-ttu-id="95ee3-106">**Despu�s de cualquier preprocesamiento es necesario, la cola MAPI realiza los siguientes pasos:**</span><span class="sxs-lookup"><span data-stu-id="95ee3-106">**After any necessary preprocessing, the MAPI spooler performs the following steps:**</span></span>
  
1. <span data-ttu-id="95ee3-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span><span class="sxs-lookup"><span data-stu-id="95ee3-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span></span> 
    
2. <span data-ttu-id="95ee3-108">Tiene el proveedor de transporte para enviar el mensaje a todos los destinatarios que tienen su propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) establecida en FALSE.</span><span class="sxs-lookup"><span data-stu-id="95ee3-108">Has the transport provider send the message to all recipients that have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to FALSE.</span></span> 
    
3. <span data-ttu-id="95ee3-109">Llama a la función apropiada ([RemovePreprocessInfo](removepreprocessinfo.md)) para limpiar cualquier información adicional que se agregó al mensaje para su uso durante el preprocesamiento de si se ha establecido la propiedad **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="95ee3-109">Calls the appropriate function ([RemovePreprocessInfo](removepreprocessinfo.md)) for cleaning up any additional information that was added to the message for use during preprocessing if the **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) property has been set.</span></span> <span data-ttu-id="95ee3-110">This function is specified when the transport provider registers its preprocessor function.</span><span class="sxs-lookup"><span data-stu-id="95ee3-110">This function is specified when the transport provider registers its preprocessor function.</span></span> 
    
4. <span data-ttu-id="95ee3-p102">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:</span><span class="sxs-lookup"><span data-stu-id="95ee3-p102">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:</span></span>
    
  - <span data-ttu-id="95ee3-113">Desbloquea el mensaje.</span><span class="sxs-lookup"><span data-stu-id="95ee3-113">Unlocks the message.</span></span>
    
  - <span data-ttu-id="95ee3-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span><span class="sxs-lookup"><span data-stu-id="95ee3-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span></span> <span data-ttu-id="95ee3-115">A continuación, copia el mensaje a la carpeta identificada por el identificador de entrada en la propiedad **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), si no se ha reemplazado por una mensajería proveedor de enlace del envía el procesamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="95ee3-115">It then copies the message to the folder identified by the entry identifier in the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property, if not superseded by a messaging hook provider's sent message processing.</span></span> <span data-ttu-id="95ee3-116">Por último, elimina el mensaje si la propiedad **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) se ha establecido en TRUE.</span><span class="sxs-lookup"><span data-stu-id="95ee3-116">Finally, it deletes the message if the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property has been set to TRUE.</span></span> 
    

