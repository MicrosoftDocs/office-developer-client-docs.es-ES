---
title: Propiedad canónica PidTagEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEntryId
api_type:
- HeaderDef
ms.assetid: ca02e873-c2d2-4d58-8df8-c05fbcdc8fba
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f3d49faba9d1e9cc8609ee55f7fb3c329e9ae947
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593042"
---
# <a name="pidtagentryid-canonical-property"></a>Propiedad canónica PidTagEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un identificador de entrada MAPI utilizado para abrir y editar las propiedades de un determinado objeto MAPI. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ENTRYID  <br/> |
|Identificador:  <br/> |0x0FFF  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propiedades de Id.  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad identifica un objeto para **OpenEntry** crear una instancia y proporciona acceso a todas sus propiedades a través de la interfaz derivada adecuada de **IMAPIProp**. 
  
Esta propiedad es una de las propiedades de la dirección base para todos los usuarios de mensajería. 
  
Esta propiedad puede contener una a largo plazo o un identificador a corto plazo. Los identificadores a corto plazo son más fácil y rápida a la construcción, pero se encuentra limitada en su alcance y la duración, normalmente a la sesión actual y la estación de trabajo. Que se usan con frecuencia para objetos de carácter temporal, como las filas de tabla o entradas del cuadro de diálogo y posteriormente son abandonados. Identificadores a largo plazo se utilizan para los objetos de una naturaleza más amplia y de larga duración. 
  
Esta propiedad siempre está disponible a través del método [IMAPIProp::GetProps](imapiprop-getprops.md) después de la primera llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Algunos proveedores de servicios pueden estar disponible inmediatamente después de la creación de instancias. El proveedor siempre debe devolver un identificador de entrada a largo plazo de **GetProps**. Por lo tanto, para convertir un identificador a corto plazo en a largo plazo, simplemente abra el objeto y obtener su esta propiedad a través de **GetProps**. 
  
En la siguiente tabla se resume las diferencias importantes entre esta propiedad, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) y **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). 
  
|**Característica**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Requerido en los objetos de datos adjuntos  <br/> |No  <br/> |Sí  <br/> |No  <br/> |
|Requerido en los objetos de carpeta  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Necesarios en los objetos de almacén de mensajes  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Requerido en los objetos de estado  <br/> |Sí  <br/> |No  <br/> |No  <br/> |
|Creado por cliente  <br/> |No  <br/> |No  <br/> |Sí  <br/> |
|Disponible antes de la llamada a **SaveChanges** <br/> |Depende de implementación del proveedor  <br/> |Depende de implementación del proveedor  <br/> |Para los mensajes, sí. Para otras personas, depende de implementación del proveedor.  <br/> |
|Cambiado en una operación de copia  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Se pueden cambiar después de una copia de los clientes  <br/> |No  <br/> |No  <br/> |Sí  <br/> |
|Único en  <br/> |Todo mundo  <br/> |Instancia de proveedor  <br/> |Todo mundo  <br/> |
|Binario comparable (como sucede con memcmp)  <br/> |No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Sí  <br/> |Sí  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.
    
[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Controla la recuperación de listas de permisos de carpeta que se almacenan en el servidor.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.
    
[[MS-OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)
  
> Especifica el esquema y los métodos que se utilizan para solicitar información de disponibilidad para los usuarios y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedad canónica PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

