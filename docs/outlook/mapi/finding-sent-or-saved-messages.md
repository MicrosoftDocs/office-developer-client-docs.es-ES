---
title: Buscar enviados o los mensajes guardados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 6e8b618e477475e8e7f45c266791086af63d8bfb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816826"
---
# <a name="finding-sent-or-saved-messages"></a><span data-ttu-id="bb866-103">Buscar enviados o los mensajes guardados</span><span class="sxs-lookup"><span data-stu-id="bb866-103">Finding Sent or Saved Messages</span></span>

  
  
<span data-ttu-id="bb866-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb866-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="bb866-105">**Para buscar todos los mensajes salientes que guarda o se envía**</span><span class="sxs-lookup"><span data-stu-id="bb866-105">**To locate all the outgoing messages that you have saved or sent**</span></span>
  
1. <span data-ttu-id="bb866-106">Llame a [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) para comparar la carpeta que contiene los mensajes enviados con la carpeta que contiene los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="bb866-106">Call [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) to compare the folder that contains your sent messages with the folder that contains your incoming messages.</span></span> 
    
2. <span data-ttu-id="bb866-107">Establezca el parámetro _lpEntryID1_ para que apunte a **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) y el parámetro _lpEntryID2_ para que apunte a **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bb866-107">Set the  _lpEntryID1_ parameter to point to **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) and the  _lpEntryID2_ parameter to point to **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="bb866-108">Tenga en cuenta que ya sea eliminar mensajes después de que se envían o han movido a cualquiera de los mensajes enviados a otra carpeta, esta estrategia no funcionará.</span><span class="sxs-lookup"><span data-stu-id="bb866-108">Be aware that if you either delete messages after they are sent or have moved any of the sent messages to another folder, this strategy will not work.</span></span> 
  
<span data-ttu-id="bb866-109">Si en el examen de un mensaje entrante tenga en cuenta que faltan las propiedades que se establecen normalmente por un proveedor de transporte, se puede suponer que el mensaje nunca se ha controlado por un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="bb866-109">If in examining an incoming message you notice that the properties that are typically set by a transport provider are missing, you can assume that the message was never handled by a transport provider.</span></span> <span data-ttu-id="bb866-110">Estas propiedades se incluyen:</span><span class="sxs-lookup"><span data-stu-id="bb866-110">These properties include:</span></span>
  
- <span data-ttu-id="bb866-111">Propiedades **PR_RECEIVED_BY**</span><span class="sxs-lookup"><span data-stu-id="bb866-111">**PR_RECEIVED_BY** properties</span></span> 
    
- <span data-ttu-id="bb866-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bb866-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="bb866-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bb866-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>
    
- <span data-ttu-id="bb866-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bb866-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span></span>
    
- <span data-ttu-id="bb866-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bb866-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span></span>
    
- <span data-ttu-id="bb866-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bb866-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span></span>
    

