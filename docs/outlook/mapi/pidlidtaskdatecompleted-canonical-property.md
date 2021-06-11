---
title: Propiedad canónica PidLidTaskDateCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDateCompleted
api_type:
- COM
ms.assetid: ae384529-55e2-4da1-9a41-acc292591a7c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3096e7ab2133d2984be0534cb091d61d2c7157bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303216"
---
# <a name="pidlidtaskdatecompleted-canonical-property"></a>Propiedad canónica PidLidTaskDateCompleted

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica la fecha en que el usuario completa la tarea.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskDateCompleted  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|Id. largo (LID):  <br/> |0x0000810F  <br/> |
|Tipo de datos:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Tarea  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se establece, esta propiedad debe tener un componente de hora de medianoche en la zona horaria local, convertida a Hora universal coordinada (UTC).
  
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

