---
title: Procesar un mensaje enviado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bd86e5d06e868ebc540d8eb779c059089045cd8a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574184"
---
# <a name="processing-a-sent-message"></a><span data-ttu-id="781bd-103">Procesar un mensaje enviado</span><span class="sxs-lookup"><span data-stu-id="781bd-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="781bd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="781bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="781bd-105">Salida de los mensajes, después de que se han enviado, puede dejarse en la Bandeja de salida carpeta, movido a una carpeta designada para almacenar los mensajes enviados o eliminado.</span><span class="sxs-lookup"><span data-stu-id="781bd-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="781bd-106">El tipo de procesamiento depende de si se han establecido propiedades de almacén del mensaje:</span><span class="sxs-lookup"><span data-stu-id="781bd-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="781bd-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="781bd-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="781bd-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="781bd-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="781bd-109">**PR_DELETE_AFTER_SUBMIT** es una propiedad booleana, establezca en TRUE si se deben eliminar los mensajes después de que se envían y FALSE en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="781bd-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="781bd-110">**PR_SENTMAIL_ENTRYID** es el identificador de entrada de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="781bd-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="781bd-111">Cuando se establece esta propiedad, debe mover los mensajes enviados a la carpeta representada por este identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="781bd-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="781bd-112">Los mensajes guardados normalmente tienen la identidad del almacén de mensajes última o proveedor enviarlos de transporte.</span><span class="sxs-lookup"><span data-stu-id="781bd-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="781bd-113">Debe ser uno o el otro o ninguna de estas propiedades set, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="781bd-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="781bd-114">Sin embargo, si establece **PR_SENTMAIL_ENTRYID**, debe contener un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="781bd-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="781bd-115">En la siguiente tabla se describe cómo estas propiedades afectan a qué hacer con los mensajes enviados.</span><span class="sxs-lookup"><span data-stu-id="781bd-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="781bd-116">Si se establece ninguna de estas propiedades:</span><span class="sxs-lookup"><span data-stu-id="781bd-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="781bd-117">Dejar el mensaje en la carpeta desde la que se envió (normalmente, la Bandeja de salida).</span><span class="sxs-lookup"><span data-stu-id="781bd-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="781bd-118">Si se establece **PR_SENTMAIL_ENTRYID** :</span><span class="sxs-lookup"><span data-stu-id="781bd-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="781bd-119">Mover el mensaje a la carpeta indicada.</span><span class="sxs-lookup"><span data-stu-id="781bd-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="781bd-120">Si se establece **PR_DELETE_AFTER_SUBMIT** :</span><span class="sxs-lookup"><span data-stu-id="781bd-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="781bd-121">Eliminar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="781bd-121">Delete the message.</span></span>  <br/> |
   

