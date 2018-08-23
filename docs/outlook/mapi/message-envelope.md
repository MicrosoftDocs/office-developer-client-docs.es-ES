---
title: Sobre de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 613956da-c49b-4836-9fde-4601510e8b89
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fd642575a3136eef3193e0bdbe884cf8f54ba337
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571300"
---
# <a name="message-envelope"></a>Sobre de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Encabezados de RFC 822 como se indica a continuación se asignan a las propiedades de MAPI. PR_SENDER_\* es una abreviatura de las siguientes 5 propiedades:
  
 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
Abreviaturas similar se usan para PR_SENT_REPRESENTING_\* y otros grupos de propiedades del mensaje.
  
|**Encabezado de SMTP**|**Propiedad MAPI**|
|:-----|:-----|
|De:  <br/> |Saliente: PR_SENDER_\*; entrante: PR_SENDER_\* y PR_SENT_REPRESENTING_\*  <br/> |
|Fecha:  <br/> |Salida: hora actual; entrante: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|Para:  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) para los destinatarios donde **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) es MAPI_TO  <br/> |
|Cc:  <br/> |**PR_DISPLAY_NAME** y **PR_EMAIL_ADDRESS** para los destinatarios donde **PR_RECIPIENT_TYPE** es MAPI_CC  <br/> |
|CCO:  <br/> |**PR_DISPLAY_NAME** y **PR_EMAIL_ADDRESS** para los destinatarios donde **PR_RECIPIENT_TYPE** es MAPI_BCC  <br/> |
|||
|Recibido:  <br/> |Ninguna propiedad MAPI correspondiente; Ponga el nombre de host local y el nombre del componente aquí  <br/> |
|Retorno de recibo para:  <br/> |**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) y **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|Responder a:  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) y **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|Asunto:  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) No hay limitación de longitud determinada.  <br/> |
|Versión de MIME:  <br/> |Siempre "1.0"  <br/> |
|||
|X-MS-datos adjuntos:  <br/> |Para la compatibilidad con la puerta de enlace de MS de correo SMTP. _filename tamaño mm-dd-yyy hh:mm_Details que aparece a continuación.  <br/> |
|||
| _todo sobre del mensaje SMTP_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|TBD de nombre de encabezado  <br/> |**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for remitente sólo ._The TBDheader debe utilizarse para determinar si el remitente es capaz de interpretar el contenido de TNEF en una respuesta.  <br/> |
|MessageID:  <br/> |**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Tipo de contenido  <br/> |Texto sin formato o multipart/mixed. Vea la sección "Mensaje contenido".  <br/> |
   
El encabezado X-MS-datos adjuntos tiene el formato de los tokens de cuatro, separados por un espacio:
  
 _nombre tamaño fecha hora_
  
El primer token es el nombre de archivo, que puede contener espacios incrustados, por lo que este encabezado se debe analizar desde los mensajes entrantes directamente en. Es el tamaño en bytes; la fecha tiene el formato _mm-dd-aaaa_ y la hora como _hh: mm._
  
> [!NOTE]
> MessageID no está asignado a **PR_SEARCH_KEY** debido a que el dominio SMTP tiene requisitos específicos en el formato del identificador de mensaje, que hacen imposible codificar un identificador de mensaje MAPI arbitrario. En su lugar, MessageID se asigna a **PR_TNEF_CORRELATION_KEY**. Esta propiedad es una propiedad definida por el transporte que se establecen mediante el envío de un mensaje saliente de transporte y utilizada por un transporte recibir un mensaje entrante. Para obtener más información, vea [desarrollar un proveedor de transporte TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md). 
  

