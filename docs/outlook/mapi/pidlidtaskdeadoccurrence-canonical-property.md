---
title: Propiedad canónica PidLidTaskDeadOccurrence
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDeadOccurrence
api_type:
- COM
ms.assetid: e78287ff-f8cc-45ea-8da8-e7a7359e651c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0b740368aae43549e81cf3f4f6de40526c505b6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303433"
---
# <a name="pidlidtaskdeadoccurrence-canonical-property"></a>Propiedad canónica PidLidTaskDeadOccurrence

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica si se deben generar nuevas ocurrencias.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskDeadOccur  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|IDENTIFICADOR largo (LID):  <br/> |0x00008109  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Tarea  <br/> |
   
## <a name="remarks"></a>Comentarios

Un patrón de periodicidad ya no está en vigor cuando su instancia final está en el pasado o se ha generado su número de instancias especificado. El cliente establece esta propiedad en FALSE para una nueva tarea o en TRUE cuando genera la última instancia de una tarea repetitiva. Cuando se copia una tarea para generar una nueva instancia, esta propiedad se establece en TRUE en la copia, que es la instancia completada.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define varios objetos que modelan el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas. 
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

