---
title: Propiedad canónica PidLidTaskStartDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStartDate
api_type:
- COM
ms.assetid: fe87eb3d-21d1-45bb-b848-e141ce1be6a0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3bc475292e47a9ad8dd9565e17640ef95e7b3c76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316684"
---
# <a name="pidlidtaskstartdate-canonical-property"></a>Propiedad canónica PidLidTaskStartDate

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La fecha en la que el usuario espera comenzar la tarea.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskStartDate  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|IDENTIFICADOR largo (LID):  <br/> |0x00008104  <br/> |
|Tipo de datos:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Tarea  <br/> |
   
## <a name="remarks"></a>Comentarios

Si el valor de esta propiedad se deja sin establecer, la tarea no tiene una fecha de inicio. Un valor de "0x5AE980E0" (1.525.252.320) también significa que la tarea no tiene una fecha de inicio. Si la tarea tiene una fecha de inicio, el valor debe tener un componente de tiempo de medianoche y también se deben establecer las propiedades **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) y **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).
  
Esta propiedad se comparte mediante la especificación del Protocolo de marcado inFormativo y la especificación del Protocolo de objetos relacionados con tareas que se encuentra en [[ms-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se admiten en contactos y listas de distribución personales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedad can�nico de PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)
  
[Propiedad can�nico de PidLidCommonStart](pidlidcommonstart-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

