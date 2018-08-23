---
title: Propiedad canónica PidTagRecordKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecordKey
api_type:
- COM
ms.assetid: a12fb9a2-799d-4112-b26c-4b2854c47cc2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9add9246cdfb22f7c5ad579f425932f49d4a9ecd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581247"
---
# <a name="pidtagrecordkey-canonical-property"></a>Propiedad canónica PidTagRecordKey

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un identificador binario comparable único para un objeto específico.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RECORD_KEY  <br/> |
|Identificador:  <br/> |0x0FF9  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propiedades de Id.  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad facilita localizar referencias a un objeto, como la búsqueda de la fila correspondiente en una tabla de contenido. Esta propiedad no se puede usar para abrir un objeto; Utilice el identificador de entrada para ese propósito.
  
Un subobjetos datos adjuntos deben identificarse de forma única dentro de un mensaje por esta propiedad. Este identificador es la única característica de datos adjuntos garantizada que permanecen igual después de que el mensaje se cierra y se vuelve a abrir. El proveedor de almacenamiento debe conservar esta propiedad a través de las sesiones para garantizar esta garantía.
  
Para las carpetas, esta propiedad contiene una clave que se usa en la tabla de jerarquía de carpeta. Normalmente, esto es el mismo valor que la proporcionada por la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
Para los almacenes de mensajes, esta propiedad es idéntica a la propiedad **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)).
  
En un objeto de almacén de mensajes, esta propiedad debe ser única entre todos los proveedores de almacén. Una manera de hacerlo es combinar el valor de la propiedad **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para el almacén (exclusivo de ese tipo de proveedor) con una estructura [GUID](guid.md) u otro valor único para el almacén de mensajes específicos. 
  
Esta propiedad siempre está disponible a través del método [IMAPIProp::GetProps](imapiprop-getprops.md) después de la primera llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Algunos proveedores pueden estar disponible inmediatamente después de la creación de instancias. 
  
Un proveedor de servicio o cliente puede comparar los valores de esta propiedad mediante el uso de memcmp. Esto no es posible para los valores de identificador de entrada. Sin embargo, esta propiedad se garantiza que ser únicos en el mismo almacén de mensajes o contenedor libreta; de direcciones dos objetos de los contenedores diferentes pueden tener el mismo valor de esta propiedad.
  
Una distinción entre las claves de registro y la búsqueda es que la clave de registro es específica del objeto, mientras que la clave de búsqueda se puede copiar a otros objetos. Por ejemplo, dos copias del objeto pueden tener el mismo valor de **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), pero deben tener valores distintos para esta propiedad.
  
En la siguiente tabla se resume las diferencias importantes entre la **entrada del objeto**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) y esta propiedad. 
  
|**Característica**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Requerido en los objetos de datos adjuntos  <br/> |No  <br/> |Sí  <br/> |No  <br/> |
|Requerido en los objetos de carpeta  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Necesarios en los objetos de almacén de mensajes  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Requerido en los objetos de estado  <br/> |Sí  <br/> |No  <br/> |No  <br/> |
|Se puede crear por cliente  <br/> |No  <br/> |No  <br/> |Sí  <br/> |
|Disponible antes de una llamada a **SaveChanges** <br/> |Quizá  <br/> |Quizá  <br/> |Los mensajes de otras personas sí quizá  <br/> |
|Cambiado en una operación de copia  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Se pueden cambiar por un cliente después de una copia  <br/> |No  <br/> |No  <br/> |Sí  <br/> |
|UNIQUE dentro de...  <br/> |Todo mundo  <br/> |Instancia de proveedor  <br/> |Todo mundo  <br/> |
|Binario comparable (como sucede con memcmp)  <br/> |No--usar **IMAPISupport:: CompareEntryIDs** <br/> |Sí  <br/> |Sí  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

