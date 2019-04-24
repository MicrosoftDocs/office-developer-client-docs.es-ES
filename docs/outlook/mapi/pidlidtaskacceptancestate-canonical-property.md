---
title: Propiedad canónica PidLidTaskAcceptanceState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAcceptanceState
api_type:
- COM
ms.assetid: 7012f524-bc66-48ea-85b5-163e05029d35
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b42be4b42d085aba8999a8c3f1a780ed972fa136
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331293"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a>Propiedad canónica PidLidTaskAcceptanceState

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica el estado de aceptación de la tarea.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskDelegValue  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|IDENTIFICADOR largo (LID):  <br/> |0x0000812A  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tarea  <br/> |
   
## <a name="remarks"></a>Comentarios

En la siguiente tabla se muestran los valores posibles para esta propiedad.
  
|**Value**|**Descripción**|
|:-----|:-----|
|0x00000000  <br/> |La tarea no está asignada.  <br/> |
|0x00000001  <br/> |El estado de aceptación de la tarea es desconocido.  <br/> |
|0x00000002  <br/> |El usuario al que se le asigna la tarea aceptó la tarea. Este valor se establece cuando el cliente procesa una aceptación de tarea.  <br/> |
|0x00000003  <br/> |El usuario al que se asigna la tarea rechazó la tarea. Este valor se establece cuando el cliente procesa un rechazo de tarea.  <br/> |
   
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

