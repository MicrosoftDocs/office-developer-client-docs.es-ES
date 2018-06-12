---
title: Propiedad canónico PidLidToDoOrdinalDate
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: d708424ccb15be15746fe8a33eea73a8e0f99323
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819007"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a>Propiedad canónico PidLidToDoOrdinalDate

  
  
**Se aplica a**: Outlook 
  
Determina el criterio de ordenación de objetos en una lista de tareas pendientes consolidada.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidToDoOrdinalDate  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x000085A0  <br/> |
|Tipo de datos:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Tarea  <br/> |
   
## <a name="remarks"></a>Notas

Cuando se marca un objeto, esta propiedad debe establecerse en la hora actual en hora Universal coordinada (UTC). 
  
Si el cliente permite a un usuario cambiar el orden de las tareas de la lista de tareas consolidado a través de arrastrar u otros mecanismos, pueden utilizar cualquier algoritmo adecuado para determinar el nuevo valor de esta propiedad para que la tarea aparezca en el lugar correcto cuando se usa esta propiedad como un ordenar campo Ting.
  
Cuando esta propiedad se usa para ordenar los objetos y los resultados de ordenación en una placa, se utiliza la propiedad **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) como un separador de placa.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones relacionadas con marcas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Ver también



[Propiedad canónico PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

