---
title: Buscar mensajes enviados o guardados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 86373fae2753df66d4456cc0fc00f8b289977650
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437423"
---
# <a name="finding-sent-or-saved-messages"></a><span data-ttu-id="67d87-103">Buscar mensajes enviados o guardados</span><span class="sxs-lookup"><span data-stu-id="67d87-103">Finding Sent or Saved Messages</span></span>

  
  
<span data-ttu-id="67d87-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67d87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="67d87-105">**Para buscar todos los mensajes salientes que ha guardado o enviado**</span><span class="sxs-lookup"><span data-stu-id="67d87-105">**To locate all the outgoing messages that you have saved or sent**</span></span>
  
1. <span data-ttu-id="67d87-106">Llame [a IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) para comparar la carpeta que contiene los mensajes enviados con la carpeta que contiene los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="67d87-106">Call [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) to compare the folder that contains your sent messages with the folder that contains your incoming messages.</span></span> 
    
2. <span data-ttu-id="67d87-107">Establezca el parámetro  _lpEntryID1_ para que apunte a **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) y el parámetro  _lpEntryID2_ para que apunte a **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="67d87-107">Set the  _lpEntryID1_ parameter to point to **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) and the  _lpEntryID2_ parameter to point to **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="67d87-108">Tenga en cuenta que si elimina los mensajes después de que se envíen o si ha movido alguno de los mensajes enviados a otra carpeta, esta estrategia no funcionará.</span><span class="sxs-lookup"><span data-stu-id="67d87-108">Be aware that if you either delete messages after they are sent or have moved any of the sent messages to another folder, this strategy will not work.</span></span> 
  
<span data-ttu-id="67d87-109">Si al examinar un mensaje entrante observa que faltan las propiedades que normalmente establece un proveedor de transporte, puede suponer que el mensaje nunca fue manipulado por un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="67d87-109">If in examining an incoming message you notice that the properties that are typically set by a transport provider are missing, you can assume that the message was never handled by a transport provider.</span></span> <span data-ttu-id="67d87-110">Entre estas propiedades se incluyen:</span><span class="sxs-lookup"><span data-stu-id="67d87-110">These properties include:</span></span>
  
- <span data-ttu-id="67d87-111">**PR_RECEIVED_BY** propiedades</span><span class="sxs-lookup"><span data-stu-id="67d87-111">**PR_RECEIVED_BY** properties</span></span> 
    
- <span data-ttu-id="67d87-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67d87-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="67d87-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67d87-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>
    
- <span data-ttu-id="67d87-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67d87-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span></span>
    
- <span data-ttu-id="67d87-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67d87-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span></span>
    
- <span data-ttu-id="67d87-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67d87-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span></span>
    

