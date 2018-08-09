---
title: Propiedad canónica PidLidTaskResetReminder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskResetReminder
api_type:
- COM
ms.assetid: f6da69ff-a913-4a65-bb07-8ad3c5685e5e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a95fc30de7511672cb27c9dd6fbc37b96e822e77
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818994"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a>Propiedad canónica PidLidTaskResetReminder

  
  
**Hace referencia a**: Outlook 
  
Indica si las instancias futuras de tareas repetitivas necesitan avisos, aunque **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) es FALSE.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskResetReminder  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008107  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentarios

Este valor se establece en TRUE cuando aviso de la tarea se descarta y se establece en FALSE en caso contrario. Si se dejan sin establecer, se supone el valor predeterminado es FALSE.
  
Tal como se especifica en [[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), la propiedad **dispidReminderSet** indica si se ha establecido un aviso en la tarea. Sin embargo, esta propiedad sólo indica la presencia de un aviso en una única tarea. Se no se puede usar solo para determinar si una instancia de una tarea periódica futura necesita un aviso. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.
    
[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedad can�nico de PidLidReminderSet](pidlidreminderset-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

