---
title: Propiedad canónica PidLidTaskLastUser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastUser
api_type:
- COM
ms.assetid: 914c55e9-cb36-46a4-b5ee-382413fa25f9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 76311a76001b122bdfd984b9dedc37c2ff878fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360448"
---
# <a name="pidlidtasklastuser-canonical-property"></a>Propiedad canónica PidLidTaskLastUser

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Nombra al usuario más reciente que era el propietario de la tarea.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskLastUser  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008122  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentarios

Antes de que un cliente envíe una solicitud de tarea, establece esta propiedad en el nombre del asignador de tareas. Antes de que un cliente envíe una aceptación de tarea, establece esta propiedad en el nombre del usuario al que se asigna la tarea. Antes de que un cliente envíe un rechazo de tarea, establece esta propiedad en el nombre del asignador de tareas.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

