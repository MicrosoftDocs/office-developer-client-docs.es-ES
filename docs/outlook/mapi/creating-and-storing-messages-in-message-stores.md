---
title: Creaci�n y almacenamiento de mensajes en los almacenes de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: be718ea3ef4da91d2f85a0229f5a506198a2527f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589178"
---
# <a name="creating-and-storing-messages-in-message-stores"></a>Creaci�n y almacenamiento de mensajes en los almacenes de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
C�mo el proveedor de almac�n de mensajes se crea y almacena los mensajes en el mecanismo de almacenamiento subyacente depende en gran medida el mecanismo de almacenamiento subyacente propio. En general, s�lo necesita escribir c�digo para conservar las propiedades de un mensaje y sus valores.
  
Cuando el mensaje Almac�n proveedor crea un nuevo mensaje, el proveedor se necesita para crear el mensaje con las propiedades necesarias para los mensajes. Una lista de estas propiedades se puede encontrar en la documentaci�n para el [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) interfaz. A continuaci�n, las aplicaciones cliente agregan las propiedades adicionales con los m�todos de [IMAPIProp](imapipropiunknown.md) . 
  
Cuando el mensaje almac�n de proveedor guarda un mensaje en el mecanismo de almacenamiento subyacente, el proveedor debe recorrer en iteraci�n las propiedades del mensaje y guardarlos en el mecanismo de almacenamiento subyacente que pueden totalmente recuperarse si m�s adelante se abre el mensaje.
  
MAPI requiere que se negocian las propiedades en las interfaces de [IMessage](imessageimapiprop.md) , lo que significa que los cambios realizados en ellos no se convierten en permanentes hasta que se llama al m�todo de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en el objeto de mensaje. El proveedor de almacenamiento de mensajes es responsable de implementar este comportamiento. Normalmente esto no es dif�cil; significa simplemente mantiene las propiedades en la memoria mientras se est�n modificando y confirmar el mecanismo de almacenamiento subyacente cuando se llama a **SaveChanges**. 
  
Algunas propiedades de los objetos de mensaje tienen una sem�ntica especial para las aplicaciones de cliente en relaci�n con el m�todo **SaveChanges**, como se indica a continuaci�n: 
  
- Algunas propiedades deben ser lectura y escritura antes de **SaveChanges** se llama, pero s�lo lectura posteriormente. Por ejemplo, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) se establece inicialmente en la aplicación cliente que crea el mensaje (y, por tanto, es de lectura y escritura), pero no pueden cambiarse tras la primera llamada a **SaveChanges**.
    
- Algunas propiedades tienen relaciones especiales a las propiedades en la carpeta que se encuentran en o a los m�todos de **IMAPIFolder**. Por ejemplo, la propiedad **PR_MESSAGE_FLAGS** est� relacionada con los indicadores utilizados en la llamada de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . 
    
- Algunas propiedades no est�n disponibles hasta que se llama **SaveChanges** por primera vez. Por ejemplo, la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) es posible que no estén disponible hasta que se llama **SaveChanges** . 
    
- Algunas propiedades pueden tener relaciones especiales a otras propiedades en el objeto de mensaje. Por ejemplo, la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) normalmente se deriva de la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) en los proveedores de almacén de mensajes que admiten los mensajes de formato de texto enriquecido.
    
- Algunas propiedades se utilizan por m�s de un tipo de objeto relacionados con los almacenes de mensajes. Por ejemplo, se requiere la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) en la carpeta y el mensaje objetos, así como mensaje almacenar objetos.
    
Es responsabilidad del proveedor de almacenamiento de mensajes para implementar la sem�ntica correcta para esas propiedades.
  
## <a name="see-also"></a>Vea tambi�n



[Implementaci�n de los mensajes en los almacenes de mensajes](implementing-messages-in-message-stores.md)

