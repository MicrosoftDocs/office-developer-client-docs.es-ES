---
title: Tablas de datos adjuntos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 92a07f7b-d34c-4085-ab11-eadcd918fa1b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4aa800b504e7ffb07d94ace6d8dc30c1463ed637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427446"
---
# <a name="attachment-tables"></a>Tablas de datos adjuntos

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla de datos adjuntos contiene información sobre todos los objetos de datos adjuntos asociados con un mensaje enviado o un mensaje en composición. 
  
Solo los datos adjuntos que se han guardado a través de una llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje se incluyen en la tabla. Los proveedores de almacenes de mensajes implementan las tablas de datos adjuntos y las usan las aplicaciones cliente y los proveedores de transporte. 
  
Se puede tener acceso a una tabla de datos adjuntos llamando a cualquiera de las siguientes opciones:
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md), solicitando la **propiedad PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).
    
Las tablas de datos adjuntos son dinámicas.
  
Los proveedores de almacén de mensajes no son necesarios para admitir la ordenación en sus tablas de datos adjuntos. Si no se admite la ordenación, la tabla debe presentarse en orden mediante la posición de **representación,** la propiedad PR_RENDERING_POSITION ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
  
Los proveedores de almacén de mensajes tampoco son necesarios para admitir restricciones en sus tablas de datos adjuntos. Los proveedores que no admiten restricciones devuelven MAPI_E_NO_SUPPORT de sus implementaciones de [IMAPITable::Restrict](imapitable-restrict.md) e [IMAPITable::FindRow](imapitable-findrow.md).
  
Las tablas de datos adjuntos pueden ser pequeñas; solo hay cuatro columnas en el conjunto de columnas requerido:
  
- **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) 
    
- **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM** no es transmitible y contiene un valor para identificar de forma única los datos adjuntos de un mensaje. Esta propiedad suele usarse como índice en las filas de la tabla. **PR_ATTACH_NUM** tiene una vida útil corta; solo es válido mientras el mensaje que contiene los datos adjuntos está abierto. Se garantiza que su valor permanecerá constante mientras la tabla de datos adjuntos esté abierta. 
  
 **PR_INSTANCE_KEY** se requiere en casi todas las tablas. Se usa para identificar de forma única una fila determinada. 
  
 **PR_RECORD_KEY** se usa normalmente para identificar de forma única un objeto con fines de comparación. A **PR_ATTACH_NUM**, **PR_RECORD_KEY** tiene el mismo ámbito que un identificador de entrada a largo plazo; permanece disponible y válido incluso después de cerrar y volver a abrir el mensaje. Para obtener más información sobre el uso de claves de registro en MAPI, vea [Mapi Record and Search Keys](mapi-record-and-search-keys.md).
  
 **PR_RENDERING_POSITION** indica cómo se debe mostrar un dato adjunto en un mensaje de texto enriquecido. Se puede establecer en un desplazamiento en caracteres, con el primer carácter del contenido del mensaje almacenado en la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) que se desplaza 0, o en -1 (0xFFFFFFFF), lo que indica que los datos adjuntos no deben representarse en el texto del mensaje en absoluto. No establecer **PR_RENDERING_POSITION** también es una opción. 
  
Cuando una tabla de datos adjuntos se ordena por posición de representación, el proveedor del almacén de mensajes la trata como un valor firmado (PT_LONG). Por lo tanto, los datos adjuntos con posiciones de representación de -1 se ordenan antes que los datos adjuntos con posiciones de representación que reflejen desplazamientos válidos. 
  
Para obtener más información acerca de la representación de datos adjuntos en un mensaje de texto sin formato, vea [Rendering an Attachment in Plain Text](rendering-an-attachment-in-plain-text.md). 
  
Para obtener información sobre la representación de datos adjuntos en texto con formato, como formato de texto enriquecido (RTF), vea [Rendering an Attachment in RTF Text](rendering-an-attachment-in-rtf-text.md).
  
Algunas de las propiedades que los proveedores de almacén de mensajes normalmente incluyen en una tabla de datos adjuntos porque son fáciles de calcular o recuperar son:
  
|||
|:-----|:-----|
|**PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))  <br/> |**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md))  <br/> |
|**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |**PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))  <br/> |
|**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))  <br/> |**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md))  <br/> |
|**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Vea también

- [Tablas MAPI](mapi-tables.md)

