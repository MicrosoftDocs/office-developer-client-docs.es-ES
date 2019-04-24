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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337131"
---
# <a name="finding-sent-or-saved-messages"></a><span data-ttu-id="ad2d1-103">Buscar mensajes enviados o guardados</span><span class="sxs-lookup"><span data-stu-id="ad2d1-103">Finding Sent or Saved Messages</span></span>

  
  
<span data-ttu-id="ad2d1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad2d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="ad2d1-105">**Para buscar todos los mensajes salientes que haya guardado o enviado**</span><span class="sxs-lookup"><span data-stu-id="ad2d1-105">**To locate all the outgoing messages that you have saved or sent**</span></span>
  
1. <span data-ttu-id="ad2d1-106">Llame a [IMsgStore:: CompareEntryIDs](imsgstore-compareentryids.md) para comparar la carpeta que contiene los mensajes enviados con la carpeta que contiene los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="ad2d1-106">Call [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) to compare the folder that contains your sent messages with the folder that contains your incoming messages.</span></span> 
    
2. <span data-ttu-id="ad2d1-107">Establezca el parámetro _lpEntryID1_ para que apunte a **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) y el parámetro _lpEntryID2_ para que apunte a **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ad2d1-107">Set the  _lpEntryID1_ parameter to point to **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) and the  _lpEntryID2_ parameter to point to **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="ad2d1-108">Tenga en cuenta que si elimina los mensajes después de que se hayan enviado o han movido alguno de los mensajes enviados a otra carpeta, esta estrategia no funcionará.</span><span class="sxs-lookup"><span data-stu-id="ad2d1-108">Be aware that if you either delete messages after they are sent or have moved any of the sent messages to another folder, this strategy will not work.</span></span> 
  
<span data-ttu-id="ad2d1-109">Si al examinar un mensaje entrante observa que faltan las propiedades que normalmente establece un proveedor de transporte, puede dar por hecho que un proveedor de transporte no administró nunca el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ad2d1-109">If in examining an incoming message you notice that the properties that are typically set by a transport provider are missing, you can assume that the message was never handled by a transport provider.</span></span> <span data-ttu-id="ad2d1-110">Entre estas propiedades se incluyen:</span><span class="sxs-lookup"><span data-stu-id="ad2d1-110">These properties include:</span></span>
  
- <span data-ttu-id="ad2d1-111">Propiedades de **PR_RECEIVED_BY**</span><span class="sxs-lookup"><span data-stu-id="ad2d1-111">**PR_RECEIVED_BY** properties</span></span> 
    
- <span data-ttu-id="ad2d1-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad2d1-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad2d1-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad2d1-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad2d1-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad2d1-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad2d1-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad2d1-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad2d1-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad2d1-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span></span>
    

