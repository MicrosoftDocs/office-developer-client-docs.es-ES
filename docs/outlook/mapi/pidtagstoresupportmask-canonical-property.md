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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340975"
---
# <a name="pidtagstoresupportmask-canonical-property"></a>Propiedad canónica PidTagStoreSupportMask

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de máscara de marcadores que consultan las aplicaciones cliente para determinar las características de un almacén de mensajes. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_STORE_SUPPORT_MASK  <br/> |
|Identificador:  <br/> |0x340D  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Varios  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad revela las capacidades de un almacén de mensajes a las aplicaciones cliente que tienen previsto enviar un mensaje. Las marcas pueden admitir decisiones de un cliente u otro almacén, por ejemplo, si se envía **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) o solo **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Un cliente nunca debe establecer **PR_STORE_SUPPORT_MASK**; un intento de establecer esta marca devuelve MAPI_E_COMPUTED. 
  
Se pueden configurar uno o varios de los siguientes indicadores para la máscara de **PR_STORE_SUPPORT_MASK** : 
  
STORE_ANSI_OK
  
> (131072, 0x00020000) El almacén de mensajes admite propiedades que contienen caracteres ANSI (8 bits).
    
STORE_ATTACH_OK 
  
> (32, 0x00000020) El almacén de mensajes admite datos adjuntos (OLE o no OLE) a los mensajes. 
    
STORE_CATEGORIZE_OK 
  
> (1024, 0x00000400) El almacén de mensajes admite vistas por categorías de tablas. 
    
STORE_CREATE_OK 
  
> (16, 0x00000010) El almacén de mensajes admite la creación de nuevos mensajes. 
    
STORE_ENTRYID_UNIQUE 
  
> (1, 0x00000001) Los identificadores de entrada de los objetos en el almacén de mensajes son únicos, es decir, nunca se reutiliza durante la vida de la tienda. 
    
STORE_HTML_OK 
  
> (65536, 0x00010000) El almacén de mensajes admite mensajes HTML, almacenados en la propiedad **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)). Si el entorno de desarrollo usa un MAPIDEFS. H que no incluye STORE_HTML_OK, use el valor 0x00010000 en su lugar. 
    
STORE_ITEMPROC
  
> (2097152, 0x00200000) En un almacén de archivos PST ajustado, indica que cuando llega un mensaje nuevo a la tienda, el almacén realiza reglas y procesamiento de filtros de correo no deseado en el mensaje por separado. El almacén llama a [IMAPISupport:: Notify](imapisupport-notify.md), estableciendo **fnevNewMail** en la estructura de [notificación](notification.md) que se pasa como parámetro y, a continuación, pasa los detalles del mensaje nuevo al cliente de escucha. Posteriormente, cuando el cliente en escucha recibe la notificación, no procesa las reglas en el mensaje. 
    
STORE_LOCALSTORE
  
> (524288, 0x00080000) Esta marca está reservada y no debe usarse.
    
STORE_MODIFY_OK 
  
> (8, 0x00000008) El almacén de mensajes admite la modificación de sus mensajes existentes. 
    
STORE_MV_PROPS_OK 
  
> (512, 0x00000200) El almacén de mensajes admite propiedades multivalor, garantiza la estabilidad del orden de los valores en una propiedad con varios valores a lo largo de una operación de guardar y admite la creación de instancias de propiedades multivalor en tablas. 
    
STORE_NOTIFY_OK 
  
> (256, 0x00000100) El almacén de mensajes admite notificaciones. 
    
STORE_OLE_OK 
  
> (64, 0x00000040) El almacén de mensajes admite datos adjuntos OLE. Se puede tener acceso a los datos OLE a través de una interfaz **IStorage** , como la que está disponible a través de la propiedad **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)). 
    
STORE_PUBLIC_FOLDERS 
  
> (16384, 0x00004000) Las carpetas de este almacén son públicas (multiusuario), no privadas (posiblemente varias instancias pero no multiusuario). 
    
STORE_PUSHER_OK
  
> (8388608, 0x00800000) El controlador de protocolo MAPI no rastreará el almacén, y el almacén es responsable de enviar los cambios a través de notificaciones al indizador para que tengan mensajes indizados.
    
STORE_READONLY 
  
> (2, 0x00000002) Todas las interfaces del almacén de mensajes tienen un nivel de acceso de solo lectura. 
    
STORE_RESTRICTION_OK 
  
> (4096, 0x00001000) El almacén de mensajes admite restricciones. 
    
STORE_RTF_OK 
  
> (2048, 0x00000800) El almacén de mensajes admite mensajes con formato de texto enriquecido (RTF), normalmente comprimidos, y el propio almacén mantiene sincronizados **PR_BODY** y **PR_RTF_COMPRESSED** . 
    
STORE_RULES_OK
  
> (268435456, 0x10000000) Indica que las reglas se deben almacenar en este almacén PST incluso si no es el almacén predeterminado. Cuando se usa **STORE_RULES_OK** junto con **NON_EMS_XP_SAVE**, las reglas se pueden ejecutar en almacenes de archivos PST que no son predeterminados.
    
STORE_SEARCH_OK 
  
> (4, 0x00000004) El almacén de mensajes admite carpetas de resultados de búsqueda. 
    
STORE_SORT_OK 
  
> (8192, 0x00002000) El almacén de mensajes admite la ordenación de vistas de tablas. 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080) El almacén de mensajes permite marcar un mensaje para su envío. 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768, 0x00008000) El almacén de mensajes admite el almacenamiento de mensajes RTF en un formulario descomprimido. Una secuencia RTF sin comprimir se identifica por el valor **dwMagicUncompressedRTF** en el encabezado de la secuencia. El valor **dwMagicUncompressedRTF** se define en RTFLIB. H del archivo. 
    
STORE_UNICODE_OK
  
> (262144, 0x00040000) Indica que el almacén de mensajes admite el almacenamiento Unicode. Un cliente puede buscar la presencia de la marca para decidir si desea solicitar o guardar información Unicode en el almacén. 
    
Siempre se puede almacenar una versión RTF de un mensaje, incluso si el almacén de mensajes no es compatible con RTF. Si el bit STORE_RTF_OK no se establece para un almacén en particular, un cliente que mantenga versiones RTF debe llamar a la función [RTFSync](rtfsync.md) para mantener las versiones **PR_BODY** y **PR_RTF_COMPRESSED** sincronizadas para el contenido de texto. RTF siempre se almacena en **PR_RTF_COMPRESSED**, independientemente de si realmente está comprimido o no. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)
  
> Describe el formato de los mensajes usados para enviar información relacionada con carpetas de uso compartido en el cliente.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

