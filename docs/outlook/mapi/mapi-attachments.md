---
title: Datos adjuntos de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e6c6ad9-1e07-4234-a5ef-18020d7ce468
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 90fbec8b61499f383228823d69b041a21199a22e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417836"
---
# <a name="mapi-attachments"></a>Datos adjuntos de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Algunos proveedores de almac�n de mensajes que los clientes puedan asociar se agreg� informaci�n en forma de archivos, objetos OLE, los mensajes o datos binarios con los mensajes. Esta informaci�n se ha agregado se denomina datos adjuntos de un mensaje. Debido a que los datos adjuntos se crean, mantienen y tener acceso s�lo a trav�s de sus mensajes, se consideran subobjetos de mensaje. En lugar de tener un identificador de entrada para obtener acceso, los datos adjuntos tienen conocidos n�mero secuencial como un n�mero de datos adjuntos. Este n�mero identifica de forma exclusiva los datos adjuntos de su mensaje, pero no necesariamente en el almac�n de mensajes. Dos mensajes diferentes pueden tener diferentes datos adjuntos con el mismo n�mero de datos adjuntos. Los números de datos adJuntos son válidos siempre que el mensaje esté abierto y se almacenen en la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).
  
Para obtener acceso a informaci�n de resumen acerca de todos los datos adjuntos de un mensaje, los clientes recuperar su tabla de datos adjuntos. En la tabla de datos adjuntos se incluye informaci�n que los clientes pueden usar para tener acceso a datos adjuntos directamente, como su n�mero de datos adjuntos y la clave de registro. Los clientes pueden recuperar una tabla de datos adjuntos por:
  
- Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
- Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Message store providers are expected to support both of these approaches. El método **OpenProperty** requiere que la persona que llama especifique IID_IMAPITable como identificador de interfaz y **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) como etiqueta de propiedad. **PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table. Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method. For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
 **PR_MESSAGE_ATTACHMENTS** se pueden usar: 
  
- Con **IMAPIProp::OpenProperty** para tener acceso a una tabla de datos adjuntos o un destinatario. 
    
- With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- En una restricci�n de subobjetos para indicar que la restricci�n secundarias debe aplicar a los datos adjuntos.
    
For more information, see [Tablas de datos adjuntos](attachment-tables.md).
  

