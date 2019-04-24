---
title: Compatibilidad de datos adJuntos de mensajes para proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d5fabc40-71e8-4afa-9846-533da605ce6c
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 69d1df5bf206cddd0d25698665c9fd87b81e4ea5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350627"
---
# <a name="supporting-message-attachments-for-message-store-providers"></a>Compatibilidad de datos adJuntos de mensajes para proveedores de almacenamiento de mensajes

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Su proveedor de almacenamiento de mensajes no necesita admitir datos adjuntos de mensajes. Sin embargo, muchas aplicaciones cliente esperan poder agregar datos adjuntos a los mensajes. Si el almacén de mensajes se va a usar para crear o almacenar IPM. Los mensajes de nota, debe admitir datos adjuntos de mensajes. Los proveedores de almacenamiento de mensajes preDeterminados también deben admitir datos adjuntos de mensajes. Para obtener más información, consulte [clases de mensajes MAPI](mapi-message-classes.md)y [almacenes de mensajes](default-message-stores.md)predeterminados.
  
Hay cinco tipos de datos adjuntos compatibles con MAPI: archivos adjuntos, datos adjuntos, datos adjuntos de mensajes, datos adjuntos de objetos OLE y vínculos. Los requisitos para admitir cada tipo son distintos. Los clientes diferencian entre los dos tipos de datos adjuntos por medio de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) en objetos Attachment.
  
Los datos adjuntos auxiliares implican la implementación de la interfaz [IAttach: IMAPIProp](iattachimapiprop.md) . La interfaz **IAttach** no tiene ningún método propio; solo tiene métodos que se heredan de la interfaz [IMAPIProp](imapipropiunknown.md) . Dado que el proveedor de almacenamiento de mensajes ya debe implementar las propiedades de los objetos de mensaje, esto simplifica enormemente la tarea de admitir datos adjuntos. La implementación de **IAttach** básicamente significa ofrecer una manera de que los clientes tengan acceso a una tabla de propiedades para datos adjuntos concretos de los mensajes. 
  
Los datos adjuntos son simplemente archivos adjuntos en los que el contenido de los datos adjuntos se almacena directamente en la propiedad **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de los datos adjuntos. Los datos adjuntos existen principalmente para permitir que los clientes adjunten archivos a un mensaje cuando el remitente y el destinatario del mensaje no tienen acceso a un servidor de archivos común. Para obtener más información, vea la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
  
Los datos adjuntos de mensajes son datos adjuntos para los que el subobjeto Attachment es otro objeto [IMessage: MAPIProp](imessageimapiprop.md) . Como los proveedores de almacenamiento de mensajes ya admiten la interfaz **IMessage** , la compatibilidad con datos adjuntos de mensajes no es difícil. 
  
La compatibilidad con datos adjuntos de objetos OLE significa implementar las interfaces OLE **IStorage**, **IStream**y **IStreamDocfile** . El proveedor de almacenamiento de mensajes debe poder convertir los datos de objeto OLE almacenados en el mensaje en un objeto OLE activo cuando un cliente abre el objeto. 
  
Los vínculos vienen en dos tipos: vínculos a archivos y vínculos a otros mensajes. Vínculos a archivos use el valor ATTACH_BY_REF_ONLY de la propiedad **PR_ATTACH_METHOD** junto con **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) o **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) para especificar la ubicación de un archivo.
  
La forma en que implementan los vínculos a los mensajes puede depender de aspectos del sistema de mensajería local y, como tal, no se puede documentar completamente aquí. Por ejemplo, el envío de un vínculo a un mensaje que se almacena en un almacén de mensajes basado en servidor suele ser sólo cuestión de enviar el identificador de entrada del mensaje vinculado, siempre que tanto el remitente como el destinatario tengan acceso a ese servidor. Otras configuraciones del sistema de mensajería presentan otros requisitos y desafíos para implementar vínculos a los mensajes.
  
## <a name="see-also"></a>Vea también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

