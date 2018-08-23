---
title: Propiedad canónica PidLidTaskOwnership
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOwnership
api_type:
- COM
ms.assetid: 805dcb6c-f405-4c4d-8bca-af4bd9cd44fa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5c335d8fab820c9876adbe8f001696a02068460c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591411"
---
# <a name="pidlidtaskownership-canonical-property"></a>Propiedad canónica PidLidTaskOwnership

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica la función del usuario actual con respecto a la tarea.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskOwnership  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008129  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad debe ser uno de los valores siguientes.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0x00000000  <br/> |No se asigna la tarea.  <br/> |
|0x00000001  <br/> |La tarea es copia del asignador de tarea de la tarea.  <br/> |
|0x00000002  <br/> |La tarea es copia del encargado de la tarea de la tarea.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

