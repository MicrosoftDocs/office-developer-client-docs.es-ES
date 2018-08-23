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
ms.openlocfilehash: 5a2e4f4b248cb8eefd5ee37c0c90d5ef9c0d0cac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565021"
---
# <a name="finding-sent-or-saved-messages"></a>Buscar mensajes enviados o guardados

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para buscar todos los mensajes salientes que guarda o se envía**
  
1. Llame a [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) para comparar la carpeta que contiene los mensajes enviados con la carpeta que contiene los mensajes entrantes. 
    
2. Establezca el parámetro _lpEntryID1_ para que apunte a **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) y el parámetro _lpEntryID2_ para que apunte a **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).
    
Tenga en cuenta que ya sea eliminar mensajes después de que se envían o han movido a cualquiera de los mensajes enviados a otra carpeta, esta estrategia no funcionará. 
  
Si en el examen de un mensaje entrante tenga en cuenta que faltan las propiedades que se establecen normalmente por un proveedor de transporte, se puede suponer que el mensaje nunca se ha controlado por un proveedor de transporte. Estas propiedades se incluyen:
  
- Propiedades **PR_RECEIVED_BY** 
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))
    
- **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))
    
- **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))
    
- **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))
    

