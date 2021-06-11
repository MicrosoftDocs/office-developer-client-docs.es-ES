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
ms.openlocfilehash: feb34cdbf8ba917936c3272bcaaf6eff040ddc3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328591"
---
# <a name="pidtagentryid-canonical-property"></a>Propiedad canónica PidTagEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un identificador de entrada MAPI usado para abrir y editar propiedades de un objeto MAPI determinado. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ENTRYID  <br/> |
|Identificador:  <br/> |0x0FFF  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propiedades de id.  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad identifica un objeto para **que OpenEntry** cree una instancia y proporciona acceso a todas sus propiedades a través de la interfaz derivada adecuada de **IMAPIProp**. 
  
Esta propiedad es una de las propiedades de dirección base para todos los usuarios de mensajería. 
  
Esta propiedad puede contener un identificador a largo plazo o a corto plazo. Los identificadores a corto plazo son más fáciles y rápidos de construir, pero están limitados en su ámbito y duración, normalmente a la sesión y estación de trabajo actuales. Se usan normalmente para objetos de carácter temporal, como filas de tabla o entradas de cuadro de diálogo, y luego se abandonan. Los identificadores a largo plazo se usan para objetos de una naturaleza más amplia y de larga duración. 
  
Esta propiedad siempre está disponible a través del método [IMAPIProp::GetProps](imapiprop-getprops.md) después de la primera llamada al método [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Algunos proveedores de servicios pueden hacer que esté disponible inmediatamente después de la creación de instancias. El proveedor siempre debe devolver un identificador de entrada a largo plazo de **GetProps**. Por lo tanto, para convertir un identificador a corto plazo en a largo plazo, simplemente abra el objeto y obtenga su propiedad a través **de GetProps**. 
  
En la tabla siguiente se resumen las diferencias importantes entre esta propiedad, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) y **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). 
  
|**Característica**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Obligatorio en objetos de datos adjuntos  <br/> |No  <br/> |Sí  <br/> |No  <br/> |
|Obligatorio en objetos de carpeta  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Obligatorio en objetos de almacén de mensajes  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Obligatorio en objetos de estado  <br/> |Sí  <br/> |No  <br/> |No  <br/> |
|Creado por el cliente  <br/> |No  <br/> |No  <br/> |Sí  <br/> |
|Disponible antes de llamar a **SaveChanges** <br/> |Depende de la implementación del proveedor  <br/> |Depende de la implementación del proveedor  <br/> |En el caso de los mensajes, sí. Para otros, depende de la implementación del proveedor.  <br/> |
|Cambiado en una operación de copia  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Modificable por cliente después de una copia  <br/> |No  <br/> |No  <br/> |Sí  <br/> |
|Único dentro  <br/> |Mundo entero  <br/> |Instancia de proveedor  <br/> |Mundo entero  <br/> |
|Binario comparable (como con memcmp)  <br/> |No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Sí  <br/> |Sí  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de listas de usuarios, contactos, grupos y recursos.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Controla la recuperación de listas de permisos de carpetas almacenadas en el servidor.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica métodos para conectarse y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.
    
[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)
  
> Especifica el esquema y los métodos que se usan para solicitar información de disponibilidad para usuarios y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

