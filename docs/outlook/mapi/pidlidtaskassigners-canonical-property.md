---
title: Propiedad canónica PidLidTaskAssigners
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 97a4915d5422f6c5463ed399835172725b83407f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303069"
---
# <a name="pidlidtaskassigners-canonical-property"></a>Propiedad canónica PidLidTaskAssigners

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una pila de entradas que representan a los asignadores de tareas. El asignador de tareas más reciente aparece en la parte superior de la pila.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskMyDelegators  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|Id. largo (LID):  <br/> |0x00008117  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Tarea  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando el cliente recibe una solicitud de tarea, se anexa a esta propiedad, cuya estructura se define en [[MS-OXOTASK],](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)una entrada que representa al remitente de la tarea. Cuando el cliente recibe un rechazo de tarea, el cliente quita la última entrada del asignador de tareas de esta propiedad. Cuando el cliente envía una respuesta de tarea, el cliente la envía al último asignador de tareas que aparece en el valor de esta propiedad.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas 
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

