---
title: Propiedad canónica PidLidTaskState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskState
api_type:
- COM
ms.assetid: 06d1f8a3-53e1-4c9a-9703-75de7a11a772
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f2cd536a2f287e880388457586f6bdfa9f67f2b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590851"
---
# <a name="pidlidtaskstate-canonical-property"></a>Propiedad canónica PidLidTaskState

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica el estado actual de la asignación de la tarea.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskState  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008113  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de esta propiedad debe ser una de las siguientes opciones.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0x00000000  <br/> |Esta tarea se creó para corresponden a una tarea que se ha incrustado en un rechazo de la tarea, pero no se pudo encontrar localmente.  <br/> |
|0x00000001  <br/> |No se asigna la tarea.  <br/> |
|0x00000002  <br/> |La tarea es copia del encargado de la tarea de una tarea asignada.  <br/> |
|0 x 00000003  <br/> |La tarea es copia del asignador de tarea de una tarea asignada.  <br/> |
|0 x 00000004  <br/> |La tarea es copia del asignador de tarea de una tarea rechazada.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para la creación y la ubicación de las carpetas especiales en un buzón de correo.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

