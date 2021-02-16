---
title: Propiedad canónica PidTagStoreUnicodeMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreUnicodeMask
api_type:
- COM
ms.assetid: a6082162-2a74-4850-a0df-4bdbc67b41d8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e15c259003ed2cb425eb181f4383f3054967b993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437941"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a>Propiedad canónica PidTagStoreUnicodeMask

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de marcas que las aplicaciones cliente deben consultar para determinar las características de un almacén de mensajes.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_STORE_UNICODE_MASK  <br/> |
|Identificador:  <br/> |0x340F  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Almacén de mensajes MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad divulga las capacidades de un almacén de mensajes a las aplicaciones cliente que planean enviarle un mensaje. Las marcas pueden facilitar las decisiones de un cliente u otro almacén, como si se va a enviar **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) o solo **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Un cliente nunca debe establecer esta propiedad. Un intento devuelve **MAPI_E_COMPUTED**. 
  
Se pueden establecer una o varias de las siguientes marcas para esta propiedad: 
  
STORE_ANSI_OK
  
> (131072, 0x00020000) El almacén de mensajes admite propiedades que contienen caracteres del American National Standards Institute (ANSI) (8 bits).
    
STORE_ATTACH_OK 
  
> (32, 0x00000020) El almacén de mensajes admite la vinculación e incrustación de objetos (OLE) o datos adjuntos que no son OLE para los mensajes. 
    
STORE_CATEGORIZE_OK 
  
> (1024, 0x00000400) El almacén de mensajes admite vistas de tablas categorizadas. 
    
STORE_CREATE_OK 
  
> (16, 0x00000010) El almacén de mensajes admite la creación de mensajes nuevos. 
    
STORE_ENTRYID_UNIQUE 
  
> (1, 0x00000001) Los identificadores de entrada de los objetos del almacén de mensajes son únicos, es decir, nunca se reutilizan durante la vida útil del almacén. 
    
STORE_HTML_OK 
  
> (65536, 0x00010000) El almacén de mensajes admite mensajes HTML, almacenados en **la PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)). Tenga en **cuenta STORE_HTML_OK** no se define en las versiones de MAPIDEFS. H que se incluyen con Microsoft Exchange 2000 Server y versiones anteriores. Si el entorno de desarrollo usa un MAPIDEFS. H file that does not include **STORE_HTML_OK**, use the value "0x00010000" instead. 
    
STORE_ITEMPROC
  
> (2097152, 0x00200000) En un almacén pst ajustado, indica que cuando llega un nuevo mensaje al almacén, el almacén realiza reglas y procesamiento de filtro de correo no deseado en el mensaje por separado. El almacén llama a [IMAPISupport::Notify](imapisupport-notify.md), configura **fnevNewMail** en la estructura [de](notification.md) notificación que se pasa como parámetro y, a continuación, pasa los detalles del nuevo mensaje al cliente de escucha. Posteriormente, cuando el cliente en escucha recibe la notificación, no procesa las reglas en el mensaje. 
    
STORE_LOCALSTORE
  
> (524288, 0x00080000) Esta marca está reservada y no debe usarse.
    
STORE_MODIFY_OK 
  
> (8, 0x00000008) El almacén de mensajes admite la modificación de sus mensajes existentes. 
    
STORE_MV_PROPS_OK 
  
> (512, 0x00000200) El almacén de mensajes admite propiedades multivalor, garantiza la estabilidad del orden de los valores en una propiedad multivalor durante una operación de guardado y admite la creación de instancias de propiedades multivalor en tablas. 
    
STORE_NOTIFY_OK 
  
> (256, 0x00000100) El almacén de mensajes admite notificaciones. 
    
STORE_OLE_OK 
  
> (64, 0x00000040) El almacén de mensajes admite datos adjuntos OLE. Se puede tener acceso a los datos OLE a través de una interfaz **IStorage,** como la disponible a través de **la** PR_ATTACH_DATA_OBJ ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)). 
    
STORE_PUBLIC_FOLDERS 
  
> (16384, 0x00004000) Las carpetas de este almacén son públicas (de varios usuarios), no privadas (posiblemente de varias instancias, pero no de varios usuarios). 
    
STORE_PUSHER_OK
  
> (8388608, 0x00800000) El controlador de protocolo MAPI no rastreará el almacén y el almacén es responsable de enviar cualquier cambio a través de notificaciones al indizador para que los mensajes se indicen.
    
STORE_READONLY 
  
> (2, 0x00000002) Todas las interfaces del almacén de mensajes tienen un nivel de acceso de solo lectura. 
    
STORE_RESTRICTION_OK 
  
> (4096, 0x00001000) El almacén de mensajes admite restricciones. 
    
STORE_RTF_OK 
  
> (2048, 0x00000800) El almacén de mensajes admite mensajes con formato de texto enriquecido  (RTF), normalmente comprimidos, y el propio almacén mantiene PR_BODY y **PR_RTF_COMPRESSED** sincronizados. 
    
STORE_SEARCH_OK 
  
> (4, 0x00000004) El almacén de mensajes admite carpetas de resultados de búsqueda. 
    
STORE_SORT_OK 
  
> (8192, 0x00002000) El almacén de mensajes admite la ordenación de vistas de tablas. 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080) El almacén de mensajes admite el marcado de un mensaje para su envío. 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768, 0x00008000) El almacén de mensajes admite el almacenamiento de mensajes de texto de formulario revisable (RTF) sin comprimir. Una secuencia RTF sin comprimir se identifica mediante el valor **dwMagicUncompressedRTF** en el encabezado de secuencia. El **valor dwMagicUncompressedRTF** se define en RTFLIB. Archivo H. 
    
STORE_UNICODE_OK
  
> (262144, 0x00040000) El almacén de mensajes admite propiedades que contienen caracteres Unicode.
    
Siempre se puede almacenar una versión RTF de un mensaje, incluso si el almacén de mensajes no es compatible con RTF. Si el bit STORE_RTF_OK no se establece para un almacén determinado, un cliente que mantiene versiones RTF debe llamar a la función [RTFSync](rtfsync.md) para mantener sincronizadas las versiones **PR_BODY** y **PR_RTF_COMPRESSED** para el contenido de texto. RTF siempre se almacena **en PR_RTF_COMPRESSED**, independientemente de si realmente está comprimido o no. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

