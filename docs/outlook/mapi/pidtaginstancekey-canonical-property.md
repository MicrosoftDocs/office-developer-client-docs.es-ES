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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358514"
---
# <a name="pidtaginstancekey-canonical-property"></a>Propiedad canónica PidTagInstanceKey

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor que identifica de forma única una fila de una tabla. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_INSTANCE_KEY  <br/> |
|Identificador:  <br/> |0x0FF6  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Tabla  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es un valor binario que identifica de forma única una fila en una vista de tabla. Es una columna obligatoria en la mayoría de las tablas. Si se incluye una fila en dos vistas, hay dos claves de instancia diferentes. La clave de instancia de una fila puede diferir cada vez que se abre la tabla, pero permanece constante mientras la tabla está abierta. Las filas agregadas mientras se usa una tabla no reutilizan una clave de instancia que se usó anteriormente. 
  
Use las **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) o **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) para correlacionar todas las filas de una expansión. Use **PR_INSTANCE_KEY** para localizar una instancia determinada dentro de la expansión. 
  
Cuando se expande una propiedad multivalor en una tabla, se crea una fila para cada instancia de la expansión, es decir, para cada valor de esa propiedad. Cada fila tiene un valor único para **la propiedad PR_INSTANCE_KEY,** mientras que todas las demás columnas conservan sus valores originales durante toda la expansión. 
  
En una ordenación por categorías de una tabla, las filas que no corresponden a datos reales se pueden agregar al resultado de la ordenación. Cada una de estas filas, al igual que todas las filas de todas las tablas, tiene su propia clave de instancia única. 
  
 **PR_INSTANCE_KEY** también se usa en notificaciones de eventos de tabla. Los **miembros propIndex** y **propPrior** de la [estructura TABLE_NOTIFICATION](table_notification.md) son estructuras [SPropValue](spropvalue.md) que PR_INSTANCE_KEY valores.  El **miembro propIndex** indica la fila que se agregó o cambió. El **miembro propPrior** indica la fila antes de la fila agregada o modificada (**PR_NULL** indica un cambio en la primera fila). 
  
Este valor no se copia como parte de la tabla para mostrar. 
  
 **PR_INSTANCE_KEY** es una [estructura MAPIUID.](mapiuid.md) Todas las claves de instancia se pueden comparar directamente como valores binarios. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.
    
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

