---
title: Establecer las propiedades de los mensajes entrantes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cf4a0501-f42b-4652-a239-003022686475
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d7043004799d534f11aa98770e2e323cbdae95a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339364"
---
# <a name="setting-properties-on-incoming-messages"></a>Establecer las propiedades de los mensajes entrantes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente dentro del subsistema MAPI esperan una serie de propiedades en cualquier mensaje recibido. Cuando el proveedor de transporte lleva un mensaje a MAPI, debe establecer estas propiedades, ya que es el único proceso que contiene la información necesaria para hacerlo, o bien es como mínimo la mejor fuente de la información.
  
Se recomienda a los proveedores que establezcan los valores de todas estas propiedades en los mensajes entrantes.
  
|**Nombre de propiedad**|**Descripción**|
|:-----|:-----|
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |El asunto del mensaje.  <br/> |
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |Texto del mensaje de texto sin formato.  <br/> |
|**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |Texto del mensaje RTF comprimido.  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |La fecha y la hora en que se entregó el mensaje.  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |El nombre para mostrar del autor del mensaje.  <br/> |
|**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |La entrada de la libreta de direcciones del autor del mensaje.  <br/> |
|**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |La clave de búsqueda de la libreta de direcciones del autor del mensaje.  <br/> |
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |La hora a la que el cliente de mensajería del remitente envió el mensaje a su sistema de mensajería.  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Nombre del delegado representativo que se va a enviar.  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |La entrada de la libreta de direcciones del delegado remitente.  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |La clave de búsqueda de la libreta de direcciones del delegado remitente.  <br/> |
|**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |Nombre del delegado representativo que se va a recibir.  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |La entrada de la libreta de direcciones del delegado de recepción.  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |La clave de búsqueda de la libreta de direcciones del delegado receptor.  <br/> |
|**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |La lista de nombres para mostrar de destinatarios delegados, separados por punto y coma y espacio (";").  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |La lista de destinatarios delegados para una respuesta.  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Indica que el destinatario se ha nombrado específicamente como destinatario "para" (no en un grupo).  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Indica que el destinatario se ha nombrado específicamente como destinatario "CC" (no en un grupo).  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Indica que el destinatario se ha nombrado específicamente como destinatario "para", "CC" o "CCO" (no pertenece a un grupo).  <br/> |
   
Los proveedores que no tienen ninguna asignación aparente pueden establecer el grupo de propiedades **PR_SENT_REPRESENTING** en los mismos valores que el grupo **PR_SENDER** , el **PR_RCVD_REPRESENTING** grupo de propiedades en los mismos valores que la **PR_RECEIVED_BY **Group y puede compilar el grupo de propiedades **PR_REPLY_RECIPIENT** en función de los valores del grupo **PR_SENDER** . Por ejemplo, **PR_SENT_REPRESENTING_NAME** se puede establecer en el mismo valor que **PR_SENDER_NAME**.
  
La **** propiedad IMAPISupport o **PR_ENTRYLIST** puede generarse, si es necesario, mediante una llamada al método [:: CreateOneOff](imapisupport-createoneoff.md) . El grupo de propiedades **PR_SEARCH_KEY** se puede generar concatenando la propiedad **PR_ADDRTYPE** asociada con un usuario, dos puntos (:) y la propiedad **PR_EMAIL_ADDRESS** asociada con el usuario; a continuación, cambie el resultado a mayúsculas. . La función de la API de Windows **CharUpperBuff** es una función adecuada para usar con este fin. Lo que se necesita en este proceso es crear una forma canónica de la dirección que se puede comparar como una cantidad binaria. Tenga en cuenta que esto no es necesario si el proveedor de transporte distingue mayúsculas de minúsculas con respecto a las direcciones de correo electrónico. 
  

