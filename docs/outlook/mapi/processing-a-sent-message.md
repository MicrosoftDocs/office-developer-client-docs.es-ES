---
title: Procesamiento de un mensaje enviado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 880731bf204778cde21da6cd9024a3ca86c6f6a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434679"
---
# <a name="processing-a-sent-message"></a><span data-ttu-id="873b1-103">Procesamiento de un mensaje enviado</span><span class="sxs-lookup"><span data-stu-id="873b1-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="873b1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="873b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="873b1-105">Los mensajes salientes, una vez enviados, se pueden dejar en la carpeta Bandeja de salida, mover a una carpeta designada para contener los mensajes enviados o eliminarse.</span><span class="sxs-lookup"><span data-stu-id="873b1-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="873b1-106">El tipo de procesamiento depende de si ha establecido o no las propiedades del almacén de mensajes:</span><span class="sxs-lookup"><span data-stu-id="873b1-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="873b1-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="873b1-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="873b1-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="873b1-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="873b1-109">**PR_DELETE_AFTER_SUBMIT** es una propiedad booleana, establecida en TRUE si los mensajes deben eliminarse después de que se envíen y FALSE en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="873b1-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="873b1-110">**PR_SENTMAIL_ENTRYID** es el identificador de entrada de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="873b1-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="873b1-111">Cuando se establece esta propiedad, debe mover los mensajes enviados a la carpeta representada por este identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="873b1-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="873b1-112">Los mensajes guardados normalmente tienen la identidad del último almacén de mensajes o proveedor de transporte para enviarlos.</span><span class="sxs-lookup"><span data-stu-id="873b1-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="873b1-113">Una u otra, o ninguna de estas propiedades debe establecerse, pero no ambas.</span><span class="sxs-lookup"><span data-stu-id="873b1-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="873b1-114">Sin embargo, si establece **PR_SENTMAIL_ENTRYID**, debe contener un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="873b1-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="873b1-115">En la tabla siguiente se describe cómo afectan estas propiedades a lo que se hace con los mensajes enviados.</span><span class="sxs-lookup"><span data-stu-id="873b1-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="873b1-116">Si no se establece ninguna propiedad:</span><span class="sxs-lookup"><span data-stu-id="873b1-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="873b1-117">Deje el mensaje en la carpeta desde la que se envió (normalmente, la Bandeja de salida).</span><span class="sxs-lookup"><span data-stu-id="873b1-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="873b1-118">Si **PR_SENTMAIL_ENTRYID** está establecido:</span><span class="sxs-lookup"><span data-stu-id="873b1-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="873b1-119">Mueva el mensaje a la carpeta indicada.</span><span class="sxs-lookup"><span data-stu-id="873b1-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="873b1-120">Si **PR_DELETE_AFTER_SUBMIT** está establecido:</span><span class="sxs-lookup"><span data-stu-id="873b1-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="873b1-121">Elimine el mensaje.</span><span class="sxs-lookup"><span data-stu-id="873b1-121">Delete the message.</span></span>  <br/> |
   

