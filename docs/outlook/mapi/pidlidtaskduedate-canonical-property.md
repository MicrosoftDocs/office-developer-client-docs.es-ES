---
title: Propiedad canónica PidLidTaskDueDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDueDate
api_type:
- COM
ms.assetid: 69ed3d48-3741-4a9a-8f98-51382b850c27
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2e21d164cbb9403d3fa1dc05cf474359a517d64b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303328"
---
# <a name="pidlidtaskduedate-canonical-property"></a>Propiedad canónica PidLidTaskDueDate

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Representa la fecha en la que el usuario espera completar la tarea.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskDueDate  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008105  <br/> |
|Tipo de datos:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentarios

La tarea no tiene fecha de vencimiento si esta propiedad no está establecida o se establece en 0x5AE980E0 (1.525.252.320). Sin embargo, una fecha de vencimiento es opcional solo si no se indica ninguna fecha de inicio en la propiedad **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)). Si la tarea tiene una fecha de vencimiento, el valor debe tener un componente de hora de medianoche y también debe establecerse la propiedad **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)). Si **dispidTaskStartDate** tiene una fecha de inicio, el valor de la propiedad **dispidTaskDueDate** debe ser mayor o igual que el valor de **dispidTaskStartDate**.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Especifica las propiedades y el modelo de interacción para el correo electrónico y otros avisos de objetos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

