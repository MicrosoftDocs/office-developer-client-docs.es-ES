---
title: Propiedad canónica PidLidTaskStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStatus
api_type:
- COM
ms.assetid: 809776b7-ff00-4a52-84b9-8b5fb5f5c3e3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d058b42ad7d1a1b8387aa5b9a1a65ea160d90b02
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386869"
---
# <a name="pidlidtaskstatus-canonical-property"></a>Propiedad canónica PidLidTaskStatus

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Especifica el estado de progreso del usuario en la tarea.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskStatus  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008101  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de esta propiedad debe establecerse en uno de estos procedimientos.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0x00000000  <br/> |El usuario no ha iniciado el trabajo en la tarea. Si se establece este valor, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) debe ser 0,0.  <br/> |
|0x00000001  <br/> |Trabajo del usuario en esta tarea está en curso. Si se establece este valor, **dispidPercentComplete** debe ser mayor que 0,0 y menor que 1,0.  <br/> |
|0x00000002  <br/> |Trabajo del usuario en esta tarea está completado. Si se establece este valor, **dispidPercentComplete** debe ser 1.0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) debe ser la fecha actual y **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) debe ser TRUE.  <br/> |
|0 x 00000003  <br/> |El usuario está esperando a otra persona.  <br/> |
|0 x 00000004  <br/> |El usuario ha diferido el trabajo en la tarea.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones relacionadas con marcas.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para la creación y la ubicación de las carpetas especiales en un buzón de correo.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)
  
[Propiedad canónica PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)
  
[Propiedad canónica PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

