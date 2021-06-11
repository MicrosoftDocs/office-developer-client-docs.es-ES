---
title: Tablas de destinatarios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8950623308e85de1d239deb322f65ee867a33ca0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437290"
---
# <a name="recipient-tables"></a>Tablas de destinatarios

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La tabla de destinatarios contiene información sobre todos los destinatarios de un mensaje. Los proveedores de almacén de mensajes implementan tablas de destinatarios y las aplicaciones cliente las usan. Los clientes tienen acceso a una tabla de destinatarios realizando una llamada al método [IMessage::GetRecipientTable,](imessage-getrecipienttable.md) o si el proveedor del almacén de mensajes la admite, al método [IMAPIProp::OpenProperty.](imapiprop-openproperty.md) Los clientes tienen acceso a tablas de destinatarios con **OpenProperty** especificando **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) para la etiqueta de propiedad y IID_IMAPITable para el identificador de interfaz. Los cambios en una tabla de destinatarios se pueden realizar llamando al [método IMessage::ModifyRecipients.](imessage-modifyrecipients.md) 
  
Las tablas de destinatarios tienen un conjunto de columnas diferente en función de si se ha enviado el mensaje. Las siguientes propiedades son el conjunto de columnas requerido en las tablas de destinatarios:
  
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
Las propiedades opcionales son:
  
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
Los mensajes enviados deben incluir estas propiedades adicionales en su conjunto de columnas requerido:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
Según la implementación de un proveedor, las columnas adicionales, **como PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) y [ENTRYID](entryid.md), pueden estar en la tabla.
  
Cualquier proveedor de almacén de mensajes que admita la transmisión de mensajes (como se indica en el bit STORE_SUBMIT_OK que se establece en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) del proveedor, debe ofrecer compatibilidad con un conjunto concreto de restricciones en una implementación de tabla de destinatarios. Las **restricciones AND**, **OR**, exist y property están entre los tipos de restricciones que deben estar disponibles para los usuarios de la tabla de destinatarios. Solo los operadores iguales y no iguales deben ser compatibles con la restricción de propiedades. Estas restricciones deben funcionar con las siguientes propiedades:
  
- **PR_ADDRTYPE**
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_RECIPIENT_TYPE**
    
- **PR_RESPONSIBILITY**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

