---
title: Propiedad canónica PidLidCleanGlobalObjectId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c48fa333d407492b69da5287fa75c565bfd10e11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349220"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a>Propiedad canónica PidLidCleanGlobalObjectId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el **objectId**global limpio.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidCleanGlobalObjId  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Meeting  <br/> |
|IDENTIFICADOR largo (LID):  <br/> |grave  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Comentarios

El formato de esta propiedad es el mismo que el de **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)). El valor de esta propiedad debe ser igual al valor de **LID_GLOBAL_OBJID**, excepto que los campos YH, Il, M y D deben ser cero. Todos los objetos que hacen referencia a una instancia de una serie periódica (incluida una instancia huérfana), así como la propia serie periódica, tendrán el mismo valor para esta propiedad.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

