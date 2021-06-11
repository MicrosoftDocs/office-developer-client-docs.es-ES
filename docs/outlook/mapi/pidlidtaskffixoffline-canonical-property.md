---
title: Propiedad canónica PidLidTaskFFixOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFFixOffline
api_type:
- COM
ms.assetid: bbaf7df4-2de0-4da3-9125-eb24dfa94cd8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 226e59ef6aa88bc290cf5aeb4d620979f926e1eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303041"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a>Propiedad canónica PidLidTaskFFixOffline

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica la precisión de la **propiedad dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskFFixOffline  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|Id. largo (LID):  <br/> |0x0000812C  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Tarea  <br/> |
   
## <a name="remarks"></a>Comentarios

Si la **propiedad dispidTaskFFixOffline** se establece en FALSE o no se establece, el valor de la propiedad **dispidTaskOwner** es correcto. Si **dispidTaskFFixOffline** se establece en TRUE, el cliente no puede determinar un valor preciso para **dispidTaskOwner**. En ese caso, el cliente puede establecer **dispidTaskOwner** en un nombre de propietario genérico, como "Unknown". Sin embargo, si un cliente encuentra un valor **dispidTaskFFixOffline** de TRUE y puede determinar un nombre de propietario preciso, el cliente debe actualizar **dispidTaskOwner** y establecer **dispidTaskFFixOffline** en FALSE. 
  
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

