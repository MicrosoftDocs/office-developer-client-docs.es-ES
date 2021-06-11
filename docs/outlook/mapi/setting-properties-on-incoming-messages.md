---
title: Establecer propiedades en mensajes entrantes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cf4a0501-f42b-4652-a239-003022686475
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d7043004799d534f11aa98770e2e323cbdae95a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432698"
---
# <a name="setting-properties-on-incoming-messages"></a>Establecer propiedades en mensajes entrantes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente dentro del subsistema MAPI esperan una serie de propiedades en cualquier mensaje recibido. Cuando el proveedor de transporte lleva un mensaje a MAPI, debe establecer estas propiedades, ya que es el único proceso con la información necesaria para hacerlo o es al menos el mejor origen de la información.
  
Se recomienda a los proveedores que establezcan los valores de todas estas propiedades en los mensajes entrantes.
  
|**Nombre de propiedad**|**Descripción**|
|:-----|:-----|
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |El asunto del mensaje.  <br/> |
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |Texto del mensaje de texto sin formato.  <br/> |
|**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |Texto de mensaje RTF comprimido.  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |La fecha y hora en que se entregó el mensaje.  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Nombre para mostrar del originador del mensaje.  <br/> |
|**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |La entrada de la libreta de direcciones del originador del mensaje.  <br/> |
|**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |La clave de búsqueda de la libreta de direcciones del originador del mensaje.  <br/> |
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Hora en que el cliente de mensajería del remitente envió el mensaje a su sistema de mensajería.  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Nombre del delegado representativo para el envío.  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |La entrada de la libreta de direcciones del delegado de envío.  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |La clave de búsqueda de la libreta de direcciones del delegado de envío.  <br/> |
|**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |Nombre del delegado representativo para recibir.  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |La entrada de la libreta de direcciones del delegado receptor.  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |La clave de búsqueda de la libreta de direcciones del delegado receptor.  <br/> |
|**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |La lista de nombres para mostrar de destinatarios delegados, separados por un punto y coma y un espacio ("; ").  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |Lista de destinatarios delegados para una respuesta.  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Indica que el destinatario se nombra específicamente como un destinatario "para" (no en un grupo).  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Indica que el destinatario se nombra específicamente como un destinatario "cc" (no en un grupo).  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Indica que el destinatario se nombra específicamente como un destinatario "para", "cc" o "cco" (no en un grupo).  <br/> |
   
Los proveedores que no tienen  asignaciones aparentes pueden establecer el grupo de propiedades PR_SENT_REPRESENTING en los mismos valores que el grupo de **PR_SENDER,** el grupo  de propiedades PR_RCVD_REPRESENTING **en** los mismos valores que el grupo de **PR_RECEIVED_BY** y pueden crear el grupo de propiedades PR_REPLY_RECIPIENT en función de los valores del grupo **PR_SENDER.** Por ejemplo, **PR_SENT_REPRESENTING_NAME** puede establecerse en el mismo valor que **PR_SENDER_NAME**.
  
La **PR_ENTRYID** o **PR_ENTRYLIST** se pueden generar, si es necesario, llamando al método [IMAPISupport::CreateOneOff.](imapisupport-createoneoff.md) El **grupo** PR_SEARCH_KEY de propiedades se puede generar concatenando la propiedad PR_ADDRTYPE asociada con un usuario, dos puntos (:) y la propiedad PR_EMAIL_ADDRESS asociada al usuario y, **a** continuación, cambiando el resultado **a** mayúsculas. La función Windows API **CharUpperBuff** es una función conveniente para usar para este propósito. Lo que se requiere de este proceso es crear una forma canónica de la dirección que se pueda comparar como una cantidad binaria. Tenga en cuenta que esto no es necesario si el proveedor de transporte distingue mayúsculas de minúsculas con respecto a las direcciones de correo electrónico. 
  

