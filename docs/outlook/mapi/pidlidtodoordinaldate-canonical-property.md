---
title: Propiedad canónica PidLidToDoOrdinalDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoOrdinalDate
api_type:
- COM
ms.assetid: b6a500fc-07f4-4788-ae46-d179a96a48e2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b0c5e3019efeeb0b9788d81e8730e976bfcc9d75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345279"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a>Propiedad canónica PidLidToDoOrdinalDate

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Determina el criterio de ordenación de los objetos de una lista de tareas tareas consolidadas.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidToDoOrdinalDate  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085A0  <br/> |
|Tipo de datos:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando se marca un objeto, esta propiedad debe establecerse en la hora actual en hora universal coordinada (UTC). 
  
Si el cliente permite a un usuario reordenar las tareas dentro de la lista de tareas consolidadas mediante arrastrar u otros mecanismos, puede usar cualquier algoritmo adecuado para determinar el nuevo valor de esta propiedad para que la tarea aparezca en el lugar correcto cuando esta propiedad se usa como campo de ordenación.
  
Cuando esta propiedad se usa para ordenar objetos y la ordenación da como resultado una empate, la propiedad **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) se usa como separador de empates.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones relacionadas con la marcación.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedad canónica PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

