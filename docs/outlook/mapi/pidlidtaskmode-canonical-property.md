---
title: Propiedad canónica PidLidTaskMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMode
api_type:
- COM
ms.assetid: 185db683-301a-4d91-a583-6959853fa1ad
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d0ae319a6b5fa4c901ec7d318c7ebdd216a2adeb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357942"
---
# <a name="pidlidtaskmode-canonical-property"></a>Propiedad canónica PidLidTaskMode

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el estado de asignación de la tarea.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskMode  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Id. largo (LID):  <br/> |0x00008518  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tarea  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor debe ser uno de los siguientes.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0x00000000  <br/> |La tarea no está asignada.  <br/> |
|0x00000001  <br/> |La tarea está incrustada en una solicitud de tarea.  <br/> |
|0x00000002  <br/> |El destinatario de la tarea aceptó la tarea.  <br/> |
|0x00000003  <br/> |El destinatario de la tarea rechazó la tarea.  <br/> |
|0x00000004  <br/> |La tarea está incrustada en una actualización de tarea.  <br/> |
|0x00000005  <br/> |La tarea se asignó al asignador de tareas.  <br/> |
   
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

