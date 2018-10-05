---
title: Propiedad canónica PidLidTaskFCreator
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFCreator
api_type:
- COM
ms.assetid: bb88750b-4773-4241-aa38-462a2634dbcb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dfb49fafcc2dc368e84786b526869e0447ccaf8c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387184"
---
# <a name="pidlidtaskfcreator-canonical-property"></a>Propiedad canónica PidLidTaskFCreator

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Indica que la tarea se creó originalmente por el usuario actual o el agente de usuario en lugar de hacerlo mediante el procesamiento de una solicitud de tarea.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskFCreator  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x0000811E  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentarios

El cliente establece esta propiedad en TRUE cuando el usuario crea la tarea y en FALSE cuando se asigna la tarea por otro usuario. Si esta propiedad se deja sin establecer, se supone un valor de TRUE.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

