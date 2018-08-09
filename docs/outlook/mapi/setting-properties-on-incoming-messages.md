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
ms.openlocfilehash: f6233afffd532c420ae170ae45b1bf93d6571865
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820668"
---
# <a name="setting-properties-on-incoming-messages"></a>Establecer propiedades en mensajes entrantes

  
  
**Hace referencia a**: Outlook 
  
Las aplicaciones cliente dentro del subsistema MAPI esperan un número de propiedades en los mensajes recibidos. Cuando el proveedor de transporte aporta un mensaje en MAPI, debe establecer estas propiedades, ya que es el único proceso con la información necesaria para hacerlo, o al menos el mejor origen de la información.
  
Los proveedores se recomienda para establecer los valores de todas estas propiedades en los mensajes entrantes.
  
|**Nombre de la propiedad**|**Descripción**|
|:-----|:-----|
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Asunto al que se refiere el mensaje.  <br/> |
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |Texto del mensaje de texto sin formato.  <br/> |
|**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |Texto del mensaje RTF comprimido.  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |La fecha y la hora que el mensaje se entregó.  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |El nombre para mostrar del remitente del mensaje.  <br/> |
|**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |La entrada de la libreta de direcciones del remitente del mensaje.  <br/> |
|**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |La clave de búsqueda de la libreta de direcciones del remitente del mensaje.  <br/> |
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |El tiempo que el mensaje se envió a su sistema de mensajería por el cliente de mensajería de la dirección del remitente.  <br/> |
|**PR_SENT_REPRESENTING_NAME de MAPI** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |El nombre del delegado representativo para el envío.  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |La entrada de la libreta de direcciones del delegado envío.  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |La clave de búsqueda de la libreta de direcciones del delegado envío.  <br/> |
|**PR_RCVD_REPRESENTING_NAME de MAPI** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |El nombre del delegado representativo para recibir.  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID de MAPI** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |La entrada de la libreta de direcciones del delegado receptora.  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |La clave de búsqueda de la libreta de direcciones del delegado receptora.  <br/> |
|**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |La lista de destinatarios delegada mostrar nombres, separados por un punto y coma y un espacio (";").  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |La lista de destinatarios delegadas para una respuesta.  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Indica que el destinatario se ha llamado específicamente como un destinatario "a" (no en un grupo).  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Indica que el destinatario se ha llamado específicamente como un destinatario "cc" (no en un grupo).  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Indica que el destinatario se ha llamado específicamente como "to", "cc" o "CCO" destinatario (no en un grupo).  <br/> |
   
Proveedores que no tienen asignaciones evidentes pueden establecer el grupo **PR_SENT_REPRESENTING** de propiedades en los mismos valores que el grupo **PR_SENDER** , el grupo **PR_RCVD_REPRESENTING** de propiedades para los mismos valores que el **PR_RECEIVED_BY **de grupo y puede crear el grupo de **PR_REPLY_RECIPIENT** de propiedades basándose en los valores del grupo **PR_SENDER** . Por ejemplo, se puede establecer **PR_SENT_REPRESENTING_NAME de MAPI** en el mismo valor que **PR_SENDER_NAME**.
  
La propiedad de **entrada del objeto** o **PR_ENTRYLIST** puede generarse, si es necesario, llamando al método [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) . El grupo **PR_SEARCH_KEY** de propiedades se puede generar concatenando la propiedad **PR_ADDRTYPE** asociada a un usuario, un signo de dos puntos (:) y la propiedad **PR_EMAIL_ADDRESS** asociada con el usuario, a continuación, cambiar el resultado a mayúsculas . La función de la API de Windows **CharUpperBuff** es una función cómoda a usar para este propósito. De este proceso es necesario realizar una forma canónica de la dirección que se puede comparar como una cantidad binario. Tenga en cuenta que esto no es necesario si el proveedor de transporte distingue mayúsculas de minúsculas con respecto a las direcciones de correo electrónico. 
  

