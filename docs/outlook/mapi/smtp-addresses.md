---
title: Direcciones SMTP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 9bc77e3226066dc88bbaf4f4efc324825add8919
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820724"
---
# <a name="smtp-addresses"></a>Direcciones SMTP

  
  
**Se aplica a**: Outlook 
  
El formato de direcciones de correo electrónico de SMTP se define en RFC 822. Componentes MAPI deben controlar todas las direcciones que cumplen con ese estándar. Sin embargo, hay una forma especial de dirección RFC 822 que mejor se codifica las direcciones MAPI:
  
 _nombre para mostrar_ **\<** _dirección de correo electrónico_**\>**
  
Los corchetes angulares se incluyen como literales. Celdas en blanco son comunes en los nombres para mostrar; necesitan no ir entre comillas. Una dirección típica podría ser como éste, que pertenece a uno de los coautores de RFC 1521:
  
Nathaniel Borenstein \<nsb@bellcore.com\>
  
Si el nombre para mostrar contiene caracteres que tienen un significado especial en las direcciones SMTP, como \< o @, el nombre para mostrar completo debe estar entre comillas dobles. En el correo saliente, si la longitud total de la dirección de correo electrónico y Mostrar nombre supera los 255 caracteres, se debe quitar el nombre para mostrar.
  
Las partes de una dirección SMTP se asignarán a propiedades MAPI de la siguiente manera:
  
|**Componente de dirección SMTP**|**Propiedad MAPI**|
|:-----|:-----|
| _nombre para mostrar_ para todos los destinatarios  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _nombre para mostrar_ para el campo  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _nombre para mostrar_ para el campo de remitente  <br/> |**PR_SENT_REPRESENTING_NAME de MAPI** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _dirección de correo electrónico_ <br/> |**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|implícitas, siempre "SMTP"  <br/> |**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
Si no hay ningún nombre para mostrar para una dirección de correo entrante, la dirección de correo electrónico completa debe usarse en su lugar. El tipo de dirección siempre es SMTP.
  
Las propiedades de destinatarios se toman de la tabla de destinatarios del mensaje MAPI; propiedades de remitente se toman desde el propio mensaje.
  

