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
# <a name="finding-sent-or-saved-messages"></a>Buscar mensajes enviados o guardados

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para buscar todos los mensajes salientes que haya guardado o enviado**
  
1. Llame a [IMsgStore:: CompareEntryIDs](imsgstore-compareentryids.md) para comparar la carpeta que contiene los mensajes enviados con la carpeta que contiene los mensajes entrantes. 
    
2. Establezca el parámetro _lpEntryID1_ para que apunte a **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) y el parámetro _lpEntryID2_ para que apunte a **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).
    
Tenga en cuenta que si elimina los mensajes después de que se hayan enviado o han movido alguno de los mensajes enviados a otra carpeta, esta estrategia no funcionará. 
  
Si al examinar un mensaje entrante observa que faltan las propiedades que normalmente establece un proveedor de transporte, puede dar por hecho que un proveedor de transporte no administró nunca el mensaje. Entre estas propiedades se incluyen:
  
- Propiedades de **PR_RECEIVED_BY** 
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))
    
- **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))
    
- **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))
    
- **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))
    

