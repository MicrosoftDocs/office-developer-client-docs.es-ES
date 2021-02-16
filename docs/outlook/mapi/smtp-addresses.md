---
title: Direcciones SMTP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fb4402100891df8b27c8d26900a4acd05f4183e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419628"
---
# <a name="smtp-addresses"></a>Direcciones SMTP

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El formato de las direcciones de correo electrónico SMTP se define en RFC 822. Los componentes MAPI deben controlar cualquier dirección que cumpla con ese estándar. Sin embargo, hay una forma particular de dirección RFC 822 que codifica mejor las direcciones MAPI:
  
 _nombre para mostrar_ **\<** _email-address_**\>**
  
Los corchetes angulares se incluyen como literales. Los espacios en blanco son comunes en los nombres para mostrar; no es necesario que se entrecomillan. Una dirección típica podría tener este aspecto, que pertenece a uno de los coautores de RFC 1521:
  
Nsb@bellcore.com \<\>
  
Si el nombre para mostrar contiene caracteres que tienen un significado especial en las direcciones SMTP, como @, todo el nombre para mostrar debe ir entre \< comillas dobles. En el correo saliente, si la longitud total de la dirección de correo electrónico más el nombre para mostrar supera los 255 caracteres, se debe descartar el nombre para mostrar.
  
Las partes de una dirección SMTP se asignan a propiedades MAPI de la siguiente manera:
  
|**Componente de dirección SMTP**|**Mapi (propiedad)**|
|:-----|:-----|
| _nombre para mostrar_ para todos los destinatarios  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _nombre para mostrar_ para el campo De  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _nombre para mostrar_ del campo Remitente  <br/> |**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _email-address_ <br/> |**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|implícito, siempre "SMTP"  <br/> |**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
Si no hay ningún nombre para mostrar para una dirección en el correo entrante, se debe usar la dirección de correo electrónico completa en su lugar. El tipo de dirección es siempre SMTP.
  
Las propiedades de destinatario se toman de la tabla de destinatarios del mensaje MAPI; las propiedades del remitente se toman del propio mensaje.
  

