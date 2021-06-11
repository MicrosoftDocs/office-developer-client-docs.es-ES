---
title: Propiedad canónica PidLidTaskHistory
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskHistory
api_type:
- COM
ms.assetid: 104ef21c-b607-48b7-9b06-bc53b7d9b68a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 39f2e6aeb4026f0b33be08b3bd8123283e5df3e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303013"
---
# <a name="pidlidtaskhistory-canonical-property"></a>Propiedad canónica PidLidTaskHistory

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica el tipo de cambio que se realizó por última vez en la tarea.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskHistory  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|Id. largo (LID):  <br/> |0x0000811A  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tarea  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando se establece el valor de esta propiedad, la propiedad **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) también debe establecerse en la hora actual. En la tabla siguiente se muestran los valores de la propiedad **dispidTaskHistory,** enumerados en orden de disminución de prioridad. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0x00000004  <br/> |La **propiedad dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) ha cambiado.  <br/> |
|0x00000003  <br/> |Se cambió otra propiedad.  <br/> |
|0x00000001  <br/> |El destinatario de la tarea aceptó esta tarea.  <br/> |
|0x00000002  <br/> |El destinatario de la tarea rechazó esta tarea.  <br/> |
|0x00000005  <br/> |La tarea se asignó a un usuario asignado.  <br/> |
|0x00000000  <br/> |No se realizaron cambios.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

