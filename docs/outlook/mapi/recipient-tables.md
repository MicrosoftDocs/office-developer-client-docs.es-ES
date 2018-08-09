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
ms.openlocfilehash: cc7635c474b99898d59589f33fcf06cf24697378
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820476"
---
# <a name="recipient-tables"></a>Tablas de destinatarios

  
  
**Hace referencia a**: Outlook 
  
La tabla de destinatarios contiene información acerca de todos los destinatarios de un mensaje. Los proveedores de almacén de mensajes implementan tablas de destinatarios y usan en las aplicaciones cliente. Los clientes de acceso a una tabla de destinatario mediante la realización de una llamada al método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) , o si el mensaje de proveedor de almacén lo admite, al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) . Los clientes de tener acceso a tablas de destinatarios con **OpenProperty** mediante la especificación de **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) para la etiqueta de propiedad y IID_IMAPITable para el identificador de interfaz. Los cambios realizados en una tabla de destinatario pueden estar llamando al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . 
  
Tablas de destinatarios tienen una columna diferente establecer dependiendo de si se ha enviado el mensaje. Las siguientes propiedades que conforman la columna requiere establecer en tablas de destinatarios:
  
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
Las propiedades opcionales son:
  
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
Los mensajes enviados deben incluir estas propiedades adicionales en su conjunto de columna necesarios:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
Dependiendo de la implementación de un proveedor, es posible columnas adicionales, como **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) y la [propiedad ENTRYID](entryid.md), en la tabla.
  
Cualquier proveedor de almacén de mensajes que admite la transmisión de mensajes, indicada por el bit STORE_SUBMIT_OK que se establece en la propiedad del proveedor **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), debe ofrecer compatibilidad con un conjunto determinado de restricciones en una implementación de la tabla de destinatarios. Existe el **y**, **o**, y restricciones de propiedad están entre los tipos de restricciones que deberían estar disponibles para los usuarios de la tabla de destinatarios. Sólo los operadores iguales y no es iguales que necesite ser compatible con la restricción de propiedad. Estas restricciones deben trabajar con las siguientes propiedades:
  
- **PR_ADDRTYPE**
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_RECIPIENT_TYPE**
    
- **PR_RESPONSIBILITY**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

