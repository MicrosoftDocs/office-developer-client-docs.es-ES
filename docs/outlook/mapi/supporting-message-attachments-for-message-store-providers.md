---
title: Compatibilidad con datos adjuntos de mensajes para los proveedores de almacén de mensajes
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d5fabc40-71e8-4afa-9846-533da605ce6c
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: e3d6844f8fe6121d6ea063a9594aaf1fed581ee5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820783"
---
# <a name="supporting-message-attachments-for-message-store-providers"></a>Compatibilidad con datos adjuntos de mensajes para los proveedores de almacén de mensajes

 
  
**Se aplica a**: Outlook 
  
El proveedor de almacén de mensajes no es necesario admitir los datos adjuntos del mensaje. Sin embargo, muchas aplicaciones cliente esperan poder agregar datos adjuntos a los mensajes. Si su almacén de mensajes se usará para crear o almacenar IPM. Tenga en cuenta los mensajes, a continuación, se deben admitir los datos adjuntos del mensaje. Los proveedores de almacén de mensajes predeterminado también deben admitir los datos adjuntos del mensaje. Para obtener más información, vea [Clases de mensaje de MAPI](mapi-message-classes.md)y [Los almacenes de mensajes de forma predeterminada](default-message-stores.md).
  
Hay cinco tipos de datos adjuntos que es compatible con MAPI: archivo de datos adjuntos, datos adjuntos de datos, datos adjuntos de mensajes, datos adjuntos de objetos OLE y vínculos. Los requisitos para admitir cada tipo son diferentes. Los clientes de diferencian entre los dos tipos de datos adjuntos por medio de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) en los objetos de datos adjuntos.
  
Compatibilidad con datos adjuntos significa que la implementación de la [IAttach: IMAPIProp](iattachimapiprop.md) interfaz. La interfaz **IAttach** no tiene métodos de su propio; tiene sólo los métodos que se heredan de la interfaz [IMAPIProp](imapipropiunknown.md) . Debido a que el proveedor de almacenes de mensaje ya debe implementar las propiedades de objetos de mensaje, se simplifica en gran medida la tarea de compatibilidad con los datos adjuntos. Implementar **IAttach** básicamente significa que proporciona una manera para que los clientes tener acceso a una tabla de propiedades para determinados archivos adjuntos en los mensajes. 
  
Datos adjuntos de datos son simplemente datos adjuntos para que el contenido de los datos adjuntos se almacena directamente en la propiedad de **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de un documento adjunto. Datos adjuntos de datos existen principalmente para permitir que los clientes adjuntar archivos a un mensaje cuando el remitente y el destinatario del mensaje no tienen acceso a un servidor de archivos comunes. Para obtener más información, vea la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
  
Datos adjuntos de mensajes son datos adjuntos para que los subobjetos de datos adjuntos es otro [IMessage: MAPIProp](imessageimapiprop.md) objeto. Debido a que los proveedores de almacén de mensajes ya admiten **la interfaz** , la compatibilidad con datos adjuntos de mensajes no es difícil. 
  
Compatibilidad con datos adjuntos de objeto OLE significa que la implementación de las interfaces OLE **IStorage**, **IStream**y **IStreamDocfile** . El proveedor de almacén de mensajes debe ser capaz de convertir los datos de objetos OLE almacenados en el mensaje en un objeto OLE activo cuando un cliente abre el objeto. 
  
Se incluyen vínculos en dos tipos: vínculos a archivos y vínculos a otros mensajes. Vínculos a archivos utilice el valor ATTACH_BY_REF_ONLY para la propiedad **PR_ATTACH_METHOD** junto con **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) o **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) para especificar la ubicación de un archivo.
  
Cómo uno implementa vínculos a los mensajes puede depender de aspectos del sistema de mensajería local y, por lo tanto, no se han documentado completamente aquí. Por ejemplo, enviar un vínculo a un mensaje que se almacena en un almacén de mensajes basado en servidor normalmente es simplemente una cuestión de enviar el identificador de entrada del mensaje vinculado, siempre que el remitente y el destinatario tengan acceso a ese servidor. Otros valores de configuración del sistema mensajería presentan desafíos para la implementación de vínculos a los mensajes y otros requisitos.
  
## <a name="see-also"></a>Ver también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

