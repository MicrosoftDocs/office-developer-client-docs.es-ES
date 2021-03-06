---
title: Compatibilidad de datos adjuntos de mensajes para proveedores de almacén de mensajes
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d5fabc40-71e8-4afa-9846-533da605ce6c
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 69d1df5bf206cddd0d25698665c9fd87b81e4ea5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412138"
---
# <a name="supporting-message-attachments-for-message-store-providers"></a>Compatibilidad de datos adjuntos de mensajes para proveedores de almacén de mensajes

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El proveedor del almacén de mensajes no necesita admitir datos adjuntos de mensajes. Sin embargo, muchas aplicaciones cliente esperan poder agregar datos adjuntos a los mensajes. Si el almacén de mensajes se usará para crear o almacenar IPM. Tenga en cuenta los mensajes y, a continuación, debe admitir datos adjuntos de mensajes. Los proveedores de almacén de mensajes predeterminados también deben admitir datos adjuntos de mensajes. Para obtener más información, vea [Mapi Message Classes](mapi-message-classes.md)y Default Message [Stores](default-message-stores.md).
  
Hay cinco tipos de datos adjuntos compatibles con MAPI: datos adjuntos de archivos, datos adjuntos, datos adjuntos de mensajes, datos adjuntos de objetos OLE y vínculos. Los requisitos para admitir cada tipo son diferentes. Los clientes diferencian entre los dos tipos de datos adjuntos **mediante la** propiedad PR_ATTACH_METHOD ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) en objetos de datos adjuntos.
  
Admitir datos adjuntos significa implementar la [interfaz IAttach : IMAPIProp.](iattachimapiprop.md) La **interfaz IAttach** no tiene métodos propios; solo tiene métodos heredados de la [interfaz IMAPIProp.](imapipropiunknown.md) Dado que el proveedor del almacén de mensajes ya debe implementar propiedades para objetos de mensaje, esto simplifica enormemente la tarea de admitir datos adjuntos. La implementación **de IAttach** básicamente significa proporcionar una forma de que los clientes obtengan acceso a una tabla de propiedades para datos adjuntos concretos en los mensajes. 
  
Los datos adjuntos son simplemente datos adjuntos para los que el contenido de los datos adjuntos se almacena directamente en la propiedad PR_ATTACH_DATA_BIN **(** [PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)). Los datos adjuntos existen principalmente para permitir a los clientes adjuntar archivos a un mensaje cuando el remitente y el destinatario del mensaje no tienen acceso a un servidor de archivos común. Para obtener más información, **vea la propiedad PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
  
Los datos adjuntos de mensajes son datos adjuntos para los que el subobjeto attachment es otro [objeto IMessage : MAPIProp.](imessageimapiprop.md) Dado que los proveedores de almacén de mensajes ya admiten la **interfaz IMessage,** no es difícil admitir datos adjuntos de mensajes. 
  
Admitir datos adjuntos de objetos OLE significa implementar las interfaces OLE **IStorage,** **IStream** e **IStreamDocfile.** El proveedor del almacén de mensajes debe poder convertir los datos de objetos OLE almacenados en el mensaje en un objeto OLE activo cuando un cliente abre el objeto. 
  
Los vínculos se incluyen en dos tipos: vínculos a archivos y vínculos a otros mensajes. Los vínculos a archivos usan el valor ATTACH_BY_REF_ONLY de la propiedad **PR_ATTACH_METHOD** junto con **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) o **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) para especificar la ubicación de un archivo.
  
La forma en que se implementan los vínculos a los mensajes puede depender de aspectos del sistema de mensajería local y, como tal, no se puede documentar completamente aquí. Por ejemplo, el envío de un vínculo a un mensaje almacenado en un almacén de mensajes basado en servidor suele ser solo cuestión de enviar el identificador de entrada del mensaje vinculado, siempre que tanto el remitente como el destinatario tengan acceso a ese servidor. Otras configuraciones del sistema de mensajería presentan otros requisitos y desafíos para implementar vínculos a mensajes.
  
## <a name="see-also"></a>Vea también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

