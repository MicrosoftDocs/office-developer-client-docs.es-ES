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
ms.openlocfilehash: 7a3ae7db1fb97e97f7d0939b67f139af62477bf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355268"
---
# <a name="pidtagrecordkey-canonical-property"></a>Propiedad canónica PidTagRecordKey

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un identificador único comparable binario para un objeto específico.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RECORD_KEY  <br/> |
|Identificador:  <br/> |0x0FF9  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propiedades de identificador  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad facilita la búsqueda de referencias a un objeto, como la búsqueda de su fila en una tabla de contenido. Esta propiedad no se puede utilizar para abrir un objeto; Use el identificador de entrada para ese propósito.
  
Un subobjeto Attachment debe identificarse de forma exclusiva en un mensaje por esta propiedad. Este identificador es la única característica de datos adjuntos que se garantiza que permanecerá igual después de cerrar y volver a abrir el mensaje. El proveedor de almacenamiento debe conservar esta propiedad en todas las sesiones para garantizar esta garantía.
  
Para las carpetas, esta propiedad contiene una clave que se usa en la tabla de jerarquía de carpetas. Normalmente, es el mismo valor que el que proporciona la **** propiedad de ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
Para los almacenes de mensajes, esta propiedad es idéntica a la propiedad **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)).
  
En un objeto de almacén de mensajes, esta propiedad debe ser única en todos los proveedores de almacenamiento. Una forma de hacerlo es combinar el valor de la propiedad **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para el almacén (único para ese tipo de proveedor) con una estructura [GUID](guid.md) u otro valor único para el almacén de mensajes específico. 
  
Esta propiedad siempre está disponible a través del método [IMAPIProp:: GetProps](imapiprop-getprops.md) después de la primera llamada al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Algunos proveedores pueden hacer que estén disponibles inmediatamente después de la creación de instancias. 
  
Un cliente o proveedor de servicios puede comparar los valores de esta propiedad mediante memcmp. Esto no es posible para los valores de identificador de entrada. Sin embargo, se garantiza que esta propiedad es única dentro del mismo almacén de mensajes o el mismo contenedor de libretas de direcciones; dos objetos de contenedores distintos pueden tener el mismo valor que esta propiedad.
  
Una de las diferencias entre las claves de registro y de búsqueda es que la clave de registro es específica del objeto, mientras que la clave de búsqueda se puede copiar a otros objetos. Por ejemplo, dos copias del objeto pueden tener el mismo valor de **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), pero deben tener valores diferentes para esta propiedad.
  
En la tabla siguiente se resumen las diferencias **** importantes entre **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) y esta propiedad. 
  
|**Característica**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Necesario en los objetos Attachment  <br/> |No  <br/> |Sí  <br/> |No  <br/> |
|Necesario en objetos Folder  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Obligatorio en objetos de almacén de mensajes  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Obligatorio en objetos de estado  <br/> |Sí  <br/> |No  <br/> |No  <br/> |
|Se pueda crear por cliente  <br/> |No  <br/> |No  <br/> |Sí  <br/> |
|Disponible antes de una llamada a **SaveChanges** <br/> |Posiblemente  <br/> |Posiblemente  <br/> |Mensajes sí otros maybes  <br/> |
|Modificado en una operación de copia  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Modificable por un cliente después de una copia  <br/> |No  <br/> |No  <br/> |Sí  <br/> |
|Único dentro de...  <br/> |Todo el mundo  <br/> |Instancia del proveedor  <br/> |Todo el mundo  <br/> |
|Comparable binario (como con memcmp)  <br/> |No--usar **IMAPISupport:: CompareEntryIDs** <br/> |Sí  <br/> |Sí  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.
    
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

