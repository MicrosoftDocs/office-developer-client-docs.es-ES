---
title: Sobre del mensaje
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 613956da-c49b-4836-9fde-4601510e8b89
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ccd14244bf7ee76396dc239437ca19f080edb170
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356927"
---
# <a name="message-envelope"></a>Sobre del mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los encabezados de RFC 822 se asignan a las propiedades MAPI de la siguiente manera. PR_SENDER_\* es una abreviatura de las 5 propiedades siguientes:
  
 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
Las abreviaturas similares se usan para\* PR_SENT_REPRESENTING_ y otros grupos de propiedades de mensajes.
  
|**Encabezado SMTP**|**MAPI (propiedad)**|
|:-----|:-----|
|Través  <br/> |Saliente: PR_SENDER_\*; entrante: PR_SENDER_\* y PR_SENT_REPRESENTING_\*  <br/> |
|Obsolet  <br/> |Saliente: hora actual; entrante: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|Hasta  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) para los destinatarios donde **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) es MAPI_TO  <br/> |
|CC  <br/> |**PR_DISPLAY_NAME** y **PR_EMAIL_ADDRESS** para los destinatarios donde **PR_RECIPIENT_TYPE** es MAPI_CC  <br/> |
|Destinatario  <br/> |**PR_DISPLAY_NAME** y **PR_EMAIL_ADDRESS** para los destinatarios donde **PR_RECIPIENT_TYPE** es MAPI_BCC  <br/> |
|||
|Obtenido  <br/> |No hay ninguna propiedad MAPI correspondiente; Escriba aquí el nombre de host local y el nombre del componente  <br/> |
|ReTurn-Receipt-to:  <br/> |**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) y **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|Responder a:  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) y **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|Titular  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) No hay una limitación de longitud específica.  <br/> |
|Versión de MIME:  <br/> |Siempre "1,0"  <br/> |
|||
|X-MS-Attachment:  <br/> |Para la compatibilidad con la puerta de enlace SMTP de Microsoft Mail. _filename Tamaño mm-dd-yyy HH: mm_Details a continuación.  <br/> |
|||
| _sobre de mensaje SMTP completo_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|nombre de encabezado TBD  <br/> |**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for Sender only. _The TBDheader debe usarse para determinar si el remitente es capaz de interpretar el contenido TNEF en una respuesta.  <br/> |
|Identificador  <br/> |**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Tipo de contenido  <br/> |Texto/sin formato o en varias partes/mixto. Vea la sección "contenido del mensaje".  <br/> |
   
El encabezado X-MS-Attachment tiene el formato de cuatro tokens, separados por un espacio:
  
 _nombre tamaño fecha hora_
  
El primer token es el nombre de archivo, que puede contener espacios incrustados, por lo que este encabezado debe analizarse a partir de la derecha en los mensajes entrantes. El tamaño se encuentra en bytes; la fecha tiene el formato _MM-DD-YYYY_ y la hora como _HH: mm._
  
> [!NOTE]
> MessageID no está asignado a **PR_SEARCH_KEY** porque el dominio SMTP tiene requisitos específicos en el formato del identificador de mensaje, lo que hace que sea imposible codificar un identificador de mensaje MAPI arbitrario. En su lugar, MessageID se asigna a **PR_TNEF_CORRELATION_KEY**. Esta propiedad es una propiedad definida por el transporte que establece el transporte que envía un mensaje saliente y lo usa un transporte que recibe un mensaje entrante. Para obtener más información, vea [desarrollar un proveedor de transporte habilitaDo para TNEF](developing-a-tnef-enabled-transport-provider.md). 
  

