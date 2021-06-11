---
title: Sobre de mensaje
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 613956da-c49b-4836-9fde-4601510e8b89
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ccd14244bf7ee76396dc239437ca19f080edb170
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427195"
---
# <a name="message-envelope"></a>Sobre de mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los encabezados RFC 822 se asignan a las propiedades MAPI de la siguiente manera. PR_SENDER_ es \* una abreviatura de las siguientes 5 propiedades:
  
 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
Se usan abreviaturas similares para PR_SENT_REPRESENTING_ \* y otros grupos de propiedades de mensaje.
  
|**Encabezado SMTP**|**Mapi (propiedad)**|
|:-----|:-----|
|De:  <br/> |Saliente: \* PR_SENDER_; entrante: PR_SENDER_ \* y PR_SENT_REPRESENTING_\*  <br/> |
|Fecha:  <br/> |Saliente: hora actual; inbound: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|Para:  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) para destinatarios donde **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) es MAPI_TO  <br/> |
|Cc:  <br/> |**PR_DISPLAY_NAME** y **PR_EMAIL_ADDRESS** destinatarios donde PR_RECIPIENT_TYPE **se** MAPI_CC  <br/> |
|CCO:  <br/> |**PR_DISPLAY_NAME** y **PR_EMAIL_ADDRESS** para los destinatarios donde **PR_RECIPIENT_TYPE** se MAPI_BCC  <br/> |
|||
|Recibido:  <br/> |No hay ninguna propiedad MAPI correspondiente; poner el nombre de host local y el nombre del componente aquí  <br/> |
|Return-receipt-to:  <br/> |**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) y **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|Responder a:  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) y **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|Asunto:  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) No hay ninguna limitación de longitud determinada.  <br/> |
|Versión MIME:  <br/> |Siempre "1.0"  <br/> |
|||
|X-MS-Attachment:  <br/> |Para la compatibilidad con la puerta de enlace SMTP de MS Mail. _filename mm-dd-yyy hh:mm_Details a continuación.  <br/> |
|||
| _sobre de mensaje SMTP completo_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|nombre de encabezado TBD  <br/> |**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for remitente only._The TBDheader debe usarse para determinar si el remitente es capaz de interpretar el contenido de TNEF en una respuesta.  <br/> |
|MessageID:  <br/> |**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Tipo de contenido  <br/> |Texto/sin formato o multiparte/mixto. Consulte la sección "Contenido del mensaje".  <br/> |
   
El encabezado X-MS-Attachment tiene el formato de cuatro tokens, separados por un espacio:
  
 _hora de fecha de tamaño de nombre_
  
El primer token es el nombre de archivo, que puede contener espacios incrustados, por lo que este encabezado debe analizarse desde la derecha en los mensajes entrantes. El tamaño es en bytes; la fecha tiene el formato  _mm-dd-yyyyy y_ la hora  _como hh:mm._
  
> [!NOTE]
> MessageID no se asigna **a PR_SEARCH_KEY** porque el dominio SMTP tiene requisitos específicos en el formato del identificador de mensaje que hacen imposible codificar un identificador de mensaje MAPI arbitrario. En su lugar, MessageID se asigna **a PR_TNEF_CORRELATION_KEY**. Esta propiedad es una propiedad definida por el transporte que establece el transporte que envía un mensaje saliente y que usa un transporte que recibe un mensaje entrante. Para obtener más información, vea [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md). 
  

