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
ms.openlocfilehash: 8a6730cca5c75a888afb5ff0a44f1e2a0a6465e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420202"
---
# <a name="sending-messages-mapi-spooler-tasks"></a><span data-ttu-id="d6398-103">Enviar mensajes: tareas de cola MAPI</span><span class="sxs-lookup"><span data-stu-id="d6398-103">Sending Messages: MAPI Spooler Tasks</span></span>

  
  
<span data-ttu-id="d6398-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6398-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6398-105">La cola MAPI est� implicada en el proceso de transmisi�n de mensajes cuando el almac�n de mensajes no est� asociado estrechamente con un proveedor de transporte, cuando el almac�n de acoplamiento ajustado y el transporte no pueden tratar un destinatario y cuando el mensaje requiere preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="d6398-105">The MAPI spooler is involved in the message transmission process when the message store is not tightly coupled with a transport provider, when the tightly coupled store and transport cannot handle a recipient, and when the message requires preprocessing.</span></span>
  
 <span data-ttu-id="d6398-106">**Despu�s de cualquier preprocesamiento es necesario, la cola MAPI realiza los siguientes pasos:**</span><span class="sxs-lookup"><span data-stu-id="d6398-106">**After any necessary preprocessing, the MAPI spooler performs the following steps:**</span></span>
  
1. <span data-ttu-id="d6398-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span><span class="sxs-lookup"><span data-stu-id="d6398-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span></span> 
    
2. <span data-ttu-id="d6398-108">El proveedor de transporte envía el mensaje a todos los destinatarios que tienen su propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) establecida en false.</span><span class="sxs-lookup"><span data-stu-id="d6398-108">Has the transport provider send the message to all recipients that have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to FALSE.</span></span> 
    
3. <span data-ttu-id="d6398-109">Llama a la función adecuada ([RemovePreprocessInfo](removepreprocessinfo.md)) para limpiar cualquier información adicional que se haya agregado al mensaje para usarlo durante el preprocesamiento, si se ha establecido la propiedad **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d6398-109">Calls the appropriate function ([RemovePreprocessInfo](removepreprocessinfo.md)) for cleaning up any additional information that was added to the message for use during preprocessing if the **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) property has been set.</span></span> <span data-ttu-id="d6398-110">This function is specified when the transport provider registers its preprocessor function.</span><span class="sxs-lookup"><span data-stu-id="d6398-110">This function is specified when the transport provider registers its preprocessor function.</span></span> 
    
4. <span data-ttu-id="d6398-p102">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:</span><span class="sxs-lookup"><span data-stu-id="d6398-p102">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:</span></span>
    
  - <span data-ttu-id="d6398-113">Desbloquea el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d6398-113">Unlocks the message.</span></span>
    
  - <span data-ttu-id="d6398-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span><span class="sxs-lookup"><span data-stu-id="d6398-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span></span> <span data-ttu-id="d6398-115">A continuación, se copia el mensaje en la carpeta identificada por el identificador de entrada en la propiedad **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), si no ha sido reemplazado por el procesamiento de mensajes enviado por un proveedor de mensajes de mensajería.</span><span class="sxs-lookup"><span data-stu-id="d6398-115">It then copies the message to the folder identified by the entry identifier in the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property, if not superseded by a messaging hook provider's sent message processing.</span></span> <span data-ttu-id="d6398-116">Por último, elimina el mensaje si la propiedad **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) se ha establecido en true.</span><span class="sxs-lookup"><span data-stu-id="d6398-116">Finally, it deletes the message if the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property has been set to TRUE.</span></span> 
    

