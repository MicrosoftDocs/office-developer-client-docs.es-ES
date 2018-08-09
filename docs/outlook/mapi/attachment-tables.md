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
ms.openlocfilehash: 2fd79cfe18e7d39f26563c87b8fb15553bf32ddf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816455"
---
# <a name="attachment-tables"></a>Tablas de datos adjuntos

**Hace referencia a**: Outlook 
  
Una tabla de datos adjuntos contiene información acerca de todos los objetos de datos adjuntos que están asociados con un mensaje enviado o un mensaje que esté redactando. 
  
Sólo los datos adjuntos que se han guardado mediante una llamada al método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje se incluyen en la tabla. Las tablas de datos adjuntos se implementan los proveedores de almacén de mensajes y usadas por las aplicaciones cliente y los proveedores de transporte. 
  
Puede tener acceso a una tabla de datos adjuntos mediante una llamada a cualquiera de las siguientes opciones:
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md), la solicitud de la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).
    
Tablas de datos adjuntos son dinámicas.
  
Los proveedores de almacén de mensajes no son necesarios para admitir la ordenación en sus tablas de datos adjuntos. Si no se admite la ordenación, se presentarán en la tabla en orden por posición de representación, la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
  
Los proveedores de almacén de mensajes no también necesarios para admitir las restricciones en sus tablas de datos adjuntos. Los proveedores que no admiten restricciones devolver MAPI_E_NO_SUPPORT desde sus implementaciones de [IMAPITable:: Restrict](imapitable-restrict.md) e [IMAPITable:: FindRow](imapitable-findrow.md).
  
Tablas de datos adjuntos pueden ser pequeñas; Hay sólo cuatro columnas en el conjunto de columna necesarios:
  
- **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) 
    
- **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM** es nontransmittable y contiene un valor para identificar de forma exclusiva un dato adjunto en un mensaje. Esta propiedad se usa a menudo como un índice en las filas de la tabla. **PR_ATTACH_NUM** tiene una corta duración; sólo es válida mientras está abierto el mensaje que contiene los datos adjuntos. Su valor se garantiza que permanecen constantes mientras está abierta en la tabla de datos adjuntos. 
  
 **PR_INSTANCE_KEY** es necesario en casi todas las tablas. Se usa para identificar de forma exclusiva una fila concreta. 
  
 **PR_RECORD_KEY** normalmente se usa para identificar de forma única un objeto con fines de comparación. A diferencia de **PR_ATTACH_NUM**, **PR_RECORD_KEY** tiene el mismo ámbito como un identificador de entrada a largo plazo; permanece disponible y válida incluso después de que el mensaje se cierra y se vuelve a abrir. Para obtener más información sobre el uso de las claves de registro en MAPI, vea el [registro de MAPI y las claves de búsqueda](mapi-record-and-search-keys.md).
  
 **PR_RENDERING_POSITION** indica cómo se debe mostrar un dato adjunto en un mensaje de texto enriquecido. Se puede establecer un desplazamiento en caracteres, con el primer carácter del contenido del mensaje, tal como se almacena en la propiedad de **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) que se está desplazamiento 0, o en -1 (0xFFFFFFFF), que indica que los datos adjuntos no se deben representar dentro del mensaje texto en absoluto. No establecer **PR_RENDERING_POSITION** también es una opción. 
  
Cuando una tabla de datos adjuntos se ordena por posición de representación, el proveedor de almacén de mensajes la trata como un valor con signo (PT_LONG). Por lo tanto, los datos adjuntos con posiciones de procesamiento de -1 se ordenan antes de los datos adjuntos con posiciones de procesamiento que reflejen los desplazamientos válidos. 
  
Para obtener más información acerca de la representación de un dato adjunto en un mensaje de texto sin formato, vea [procesar un dato adjunto en texto sin formato](rendering-an-attachment-in-plain-text.md). 
  
Para obtener información acerca de la representación de un dato adjunto en texto con formato como el formato de texto enriquecido (RTF), vea [procesar un dato adjunto en texto RTF](rendering-an-attachment-in-rtf-text.md).
  
Algunas de las propiedades de los proveedores de almacén de mensajes se incluyen normalmente en una tabla de datos adjuntos porque son fáciles de calcular o recuperar son:
  
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

