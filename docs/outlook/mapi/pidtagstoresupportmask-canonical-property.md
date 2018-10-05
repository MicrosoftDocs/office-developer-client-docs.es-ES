---
title: Propiedad canónica PidTagStoreSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreSupportMask
api_type:
- COM
ms.assetid: ada5694a-b5b1-471f-be33-906fc052681a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 143e7f0d2cd89cd4e7956cdda05d1bd512db4027
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392336"
---
# <a name="pidtagstoresupportmask-canonical-property"></a>Propiedad canónica PidTagStoreSupportMask

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de indicadores de esa consulta de aplicaciones de cliente para determinar las características de un almacén de mensajes. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_STORE_SUPPORT_MASK  <br/> |
|Identificador:  <br/> |0x340D  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Varios  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad revela las capacidades de un almacén de mensajes a las aplicaciones cliente que se va a enviar un mensaje. Los indicadores pueden admitir las decisiones de un cliente o en otro almacén, por ejemplo, si se enviará un **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) o sólo **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Un cliente que nunca debe establecer **PR_STORE_SUPPORT_MASK**; un intento de establecer esta marca devuelve MAPI_E_COMPUTED. 
  
La máscara de bits **PR_STORE_SUPPORT_MASK** se pueden establecer uno o varios de los siguientes indicadores: 
  
STORE_ANSI_OK
  
> (131072, 0 x 00020000) El almacén de mensajes es compatible con las propiedades que contienen los caracteres ANSI (8 bits).
    
STORE_ATTACH_OK 
  
> (32, 0 x 00000020) El almacén de mensajes es compatible con datos adjuntos (OLE o que no sean OLE) a los mensajes. 
    
STORE_CATEGORIZE_OK 
  
> (1024, 0 x 00000400) El almacén de mensajes es compatible con vistas ordenadas por categorías de las tablas. 
    
STORE_CREATE_OK 
  
> (16, 0 x 00000010) El almacén de mensajes es compatible con la creación de mensajes nuevos. 
    
STORE_ENTRYID_UNIQUE 
  
> (1, 0 x 00000001) Los identificadores de entrada para los objetos en el almacén de mensajes son únicos, es decir, nunca volverá a utilizar durante la vida del almacén. 
    
STORE_HTML_OK 
  
> (65536, 0 x 00010000) El almacén de mensajes es compatible con los mensajes HTML, almacenados en la propiedad **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)). Si el entorno de desarrollo usa un MAPIDEFS. H del proyecto que no se incluyen STORE_HTML_OK, use el valor 0 x 00010000 en su lugar. 
    
STORE_ITEMPROC
  
> (2097152, 0x00200000) En un almacén de archivos PST ajustado, indica que, cuando llegue un nuevo mensaje en el almacén, el almacén de realiza las reglas y filtro de spam por separado de procesamiento en el mensaje. El almacén de las llamadas [IMAPISupport::Notify](imapisupport-notify.md), **fnevNewMail** del valor de la estructura de [notificación](notification.md) que se pasa como un parámetro y, a continuación, pasa los detalles del nuevo mensaje para el cliente de escucha. Posteriormente, cuando el cliente escucha recibe la notificación, no se procesará las reglas en el mensaje. 
    
STORE_LOCALSTORE
  
> (524288, 0 x 00080000) Esta marca está reservada y no debe usarse.
    
STORE_MODIFY_OK 
  
> (8, 0 x 00000008) El almacén de mensajes es compatible con la modificación de los mensajes existentes. 
    
STORE_MV_PROPS_OK 
  
> (512, 0 x 00000200) El almacén de mensajes es compatible con propiedades multivalores, garantiza la estabilidad del orden de valor en una propiedad multivalor a lo largo de un proceso de guardar operación y admite creación de instancias de propiedades multivalor en las tablas. 
    
STORE_NOTIFY_OK 
  
> (256, 0 x 00000100) El almacén de mensajes es compatible con las notificaciones. 
    
STORE_OLE_OK 
  
> (64, 0x00000040) El almacén de mensajes es compatible con los datos adjuntos OLE. Los datos OLE pueden tener acceso a través de una interfaz **IStorage** , como el disponible a través de la propiedad **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)). 
    
STORE_PUBLIC_FOLDERS 
  
> (16384, 0x00004000) Las carpetas en este almacén son pública not (multiusuario), privada (posiblemente de varias instancias, pero no multiusuario). 
    
STORE_PUSHER_OK
  
> (8388608, 0x00800000) El controlador de protocolo MAPI no va a rastrear el almacén y el almacén es responsable de inserción de los cambios a través de notificaciones en el indizador para que los mensajes se indizan.
    
STORE_READONLY 
  
> (2, 0 x 00000002) Todas las interfaces para el almacén de mensajes tienen un nivel de acceso de solo lectura. 
    
STORE_RESTRICTION_OK 
  
> (4096, 0 x 00001000) El almacén de mensajes es compatible con las restricciones. 
    
STORE_RTF_OK 
  
> (2048, 0x00000800) El almacén de mensajes es compatible con los mensajes de formato de texto enriquecido (RTF), normalmente comprimidos, y el propio almacén mantiene **PR_BODY** y **PR_RTF_COMPRESSED** sincronizadas. 
    
STORE_RULES_OK
  
> (268435456, 0 x 10000000) Indica que las reglas se almacenen en este almacén de archivos PST, incluso si no es el almacén predeterminado. Cuando **STORE_RULES_OK** se usa en combinación con **NON_EMS_XP_SAVE**, las reglas son capaces de ejecutar en almacenes de archivos PST ajustado no predeterminados.
    
STORE_SEARCH_OK 
  
> (4, 0 x 00000004) El almacén de mensajes es compatible con las carpetas de resultados de búsqueda. 
    
STORE_SORT_OK 
  
> (8192, 0 x 00002000) El almacén de mensajes es compatible con vistas de ordenación de tablas. 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080) El almacén de mensajes admite marcar un mensaje para el envío. 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768, 0x00008000) El almacén de mensajes admite el almacenamiento de mensajes RTF en formulario sin comprimir. Una secuencia de RTF sin comprimir se identifica mediante el valor **dwMagicUncompressedRTF** en el encabezado de la secuencia. El valor de **dwMagicUncompressedRTF** se define en el RTFLIB. H del proyecto. 
    
STORE_UNICODE_OK
  
> (262144, 0 x 00040000) Indica que el almacén de mensajes admite el almacenamiento de Unicode. Un cliente puede buscar la presencia de la marca de decidir si va a solicitar o guardar información de Unicode en el repositorio. 
    
Una versión RTF de un mensaje puede almacenarse siempre, incluso si el almacén de mensajes es no es compatible con RTF. Si no está establecido el bit STORE_RTF_OK de un almacén determinado, un cliente de mantenimiento de las versiones RTF debe propio llamar a la función [RTFSync](rtfsync.md) para mantener las versiones **PR_BODY** y **PR_RTF_COMPRESSED** sincronizadas para el contenido de texto. RTF siempre se almacena en **PR_RTF_COMPRESSED**, si realmente está comprimido o no. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)
  
> Describe el formato de los mensajes que se utiliza para enviar información relacionada con el uso compartido de carpetas en el cliente.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

