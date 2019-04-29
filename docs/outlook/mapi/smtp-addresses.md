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
  
El formato de las direcciones de correo electrónico SMTP se define en RFC 822. Los componentes MAPI deben administrar cualquier dirección que cumpla con ese estándar. Sin embargo, hay una forma determinada de la dirección RFC 822 que mejor codifica las direcciones MAPI:
  
 _Display-Name_ **\<** _dirección de correo electrónico_**\>**
  
Los corchetes angulares se incluyen como literales. Los espacios en blanco son comunes en los nombres para mostrar; no es necesario que se comillas. Una dirección típica puede tener un aspecto similar a este, que pertenece a una de las coautoras de RFC 1521:
  
Nathaniel Borenstein \<NSB@bellcore.com\>
  
Si el nombre para mostrar contiene caracteres que tienen un significado especial en direcciones SMTP, \< como o @, el nombre completo para mostrar debe incluirse entre comillas dobles. En el correo saliente, si la longitud total de la dirección de correo electrónico más el nombre para mostrar supera los 255 caracteres, se debe eliminar el nombre para mostrar.
  
Las partes de una dirección SMTP se asignan a las propiedades MAPI de la siguiente manera:
  
|**Componente de dirección SMTP**|**MAPI (propiedad)**|
|:-----|:-----|
| _Display-Name_ para todos los destinatarios  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _Display-nombre para el_ campo de  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _Display-Name para el_ campo Sender  <br/> |**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _Dirección de correo electrónico_ <br/> |**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|implícito, siempre "SMTP"  <br/> |**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
Si no hay ningún nombre para mostrar para una dirección en el correo entrante, se debe usar la dirección de correo electrónico completa en su lugar. El tipo de dirección siempre es SMTP.
  
Las propiedades de los destinatarios se toman de la tabla de destinatarios del mensaje MAPI; las propiedades del remitente se toman del propio mensaje.
  

