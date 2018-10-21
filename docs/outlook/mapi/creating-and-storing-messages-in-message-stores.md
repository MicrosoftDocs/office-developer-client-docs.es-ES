---
title: Crear y almacenar mensajes en los almacenes de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: be718ea3ef4da91d2f85a0229f5a506198a2527f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589178"
---
# <a name="creating-and-storing-messages-in-message-stores"></a>Crear y almacenar mensajes en los almacenes de mensajes

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
La forma en que su proveedor de almacén de mensajes crea y almacena los mensajes en el mecanismo de almacenamiento subyacente depende en gran medida del propio mecanismo de almacenamiento subyacente. En general, sólo necesita escribir código para conservar las propiedades de un mensaje y sus valores.
  
Cuando el proveedor de almacén de mensajes crea un nuevo mensaje, el proveedor debe crear el mensaje con las propiedades necesarias para los mensajes. Encontrará una lista de estas propiedades en la documentación de la interfaz [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Después, las aplicaciones cliente agregan las propiedades adicionales con métodos[IMAPIProp](imapipropiunknown.md). 
  
Cuando el proveedor de almacén de mensajes guarda un mensaje en el mecanismo de almacenamiento subyacente, el proveedor debe revisar las propiedades del mensaje y guardarlas en el mecanismo de almacenamiento subyacente para que se puedan recuperar completamente si el mensaje se abre más tarde.
  
MAPI requiere que las propiedades de las interfaces [IMessage](imessageimapiprop.md) interfaces sean transferidas, lo que significa que los cambios realizados en ellas no se conviertan en permanentes hasta que se llame al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en el mensaje objeto. El proveedor del almacén de mensajes es responsable de implementar este comportamiento. Normalmente no es difícil; significa simplemente mantener las propiedades en memoria mientras se están modificando y confirmarlas en el mecanismo de almacenamiento subyacente cuando se llame a **SaveChanges**. 
  
Algunas propiedades de los objetos de mensaje tienen semántica especial para las aplicaciones cliente con respecto al método **SaveChanges**: 
  
- Algunas propiedades deberían ser de lectura y escritura antes de llamar a **SaveChanges**, pero después solo de lectura. Por ejemplo, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) se establece inicialmente en la aplicación cliente que crea el mensaje (y por lo tanto es de lectura y escritura), pero no pueden cambiarse tras la primera llamada a **SaveChanges**.
    
- Algunas propiedades tienen relaciones especiales con propiedades de la carpeta en la que están o con métodos **IMAPIFolder**. Por ejemplo, la propiedad **PR_MESSAGE_FLAGS** está relacionada con los marcadores usados en la llamada [IMAPIFolder::CreateMessage](imapifolder-createmessage.md). 
    
- Algunas propiedades pueden no estar disponibles hasta que se llame a **SaveChanges** por primera vez. Por ejemplo, la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) puede no estar disponible hasta que se llame a **SaveChanges**. 
    
- Algunas propiedades pueden tener relaciones especiales con otras propiedades en el objeto de mensaje. Por ejemplo, la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) normalmente se deriva de la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) en los proveedores de almacén de mensajes que admiten los mensajes de formato de texto enriquecido.
    
- Algunas propiedades son usadas por más de un tipo de objeto relacionado con los almacenes de mensajes. Por ejemplo, se requiere la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) en los objetos mensaje y carpetas, así como en los objetos almacén de mensajes.
    
Es responsabilidad del proveedor de almacén de mensajes implementar la semántica correcta de estas propiedades.
  
## <a name="see-also"></a>Vea también



[Implementar mensajes en los almacenes de mensajes](implementing-messages-in-message-stores.md)

