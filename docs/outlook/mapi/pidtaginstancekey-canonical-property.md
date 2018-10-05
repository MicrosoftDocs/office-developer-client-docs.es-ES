---
title: Propiedad canónica PidTagInstanceKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInstanceKey
api_type:
- HeaderDef
ms.assetid: 14fc5571-acc0-4d75-8598-964aee5ba01c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c237149c305a80012d1f06ea4373b892d25daec1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396993"
---
# <a name="pidtaginstancekey-canonical-property"></a>Propiedad canónica PidTagInstanceKey

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor que identifica de forma exclusiva una fila en una tabla. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_INSTANCE_KEY  <br/> |
|Identificador:  <br/> |0x0FF6  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Tabla  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es un valor binario que identifica de forma exclusiva una fila en una vista de tabla. Es una columna necesaria en la mayoría de las tablas. Si se incluye una fila en dos vistas, hay dos claves de instancia diferente. La clave de instancia de una fila puede diferir cada vez que se abre en la tabla, pero permanece constante mientras la tabla está abierto. Filas agregadas mientras una tabla está en uso no volver a usar una clave de instancia que se usó anteriormente. 
  
Utilice las propiedades de **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) o la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) para correlacionar todas las filas de una expansión. Use **PR_INSTANCE_KEY** para buscar una instancia determinada dentro de la expansión. 
  
Cuando se expande una propiedad multivalor en una tabla, se crea una fila para cada instancia de la expansión, es decir, para cada valor de dicha propiedad. Cada fila tiene un valor único para la propiedad **PR_INSTANCE_KEY** , mientras que todas las demás columnas conservan sus valores originales en toda la expansión. 
  
En una ordenación por categorías de una tabla, se pueden agregar filas no correspondiente a los datos reales en el resultado de la ordenación. Cada fila, al igual que todas las filas de todas las tablas, tiene su propia clave de instancia única. 
  
 **PR_INSTANCE_KEY** también se usa en las notificaciones de eventos de tabla. Los miembros **propIndex** y **propPrior** de la estructura [TABLE_NOTIFICATION](table_notification.md) son estructuras [SPropValue](spropvalue.md) contienen valores **PR_INSTANCE_KEY** . El miembro **propIndex** indica la fila que se ha agregado o modificado. El miembro **propPrior** indica la fila antes de la fila se ha agregado o modificada (**PR_NULL** indica un cambio en la primera fila). 
  
Este valor no se copia como parte de la tabla para mostrar. 
  
 **PR_INSTANCE_KEY** es una estructura [MAPIUID](mapiuid.md) . Todas las claves de la instancia se pueden comparar directamente como valores binarios. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.
    
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

