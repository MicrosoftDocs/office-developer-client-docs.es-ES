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
ms.openlocfilehash: 9a438fb2b1862d44905a63fda3e5f68b7878cd99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316621"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a>Propiedad canónica PidLidTaskResetReminder

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica si las instancias futuras de tareas periódicas necesitan avisos, aunque **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) sea FALSE.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskResetReminder  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008107  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentarios

Este valor se establece en TRUE cuando se descarta el aviso de la tarea y se establece en FALSE en caso contrario. Si se deja sin conjunto, se supone que el valor predeterminado es FALSE.
  
Como se especifica en [[MS-OBIORMDR],](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)la propiedad **dispidReminderSet** indica si se establece un aviso en la tarea. Sin embargo, esta propiedad solo indica la presencia de un aviso en una sola tarea. No se puede usar solo para determinar si una instancia futura de una tarea periódica necesita un aviso. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OJOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Especifica las propiedades y el modelo de interacción para el correo electrónico y otros avisos de objetos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedad can�nico de PidLidReminderSet](pidlidreminderset-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

