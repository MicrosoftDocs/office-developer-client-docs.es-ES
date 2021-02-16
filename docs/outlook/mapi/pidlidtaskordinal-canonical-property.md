---
title: Propiedad canónica PidLidTaskOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOrdinal
api_type:
- COM
ms.assetid: 1021860e-4c40-4c22-aa68-b568d046aaf7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a64008da93584529916a9303176bba0aa08d3fac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357963"
---
# <a name="pidlidtaskordinal-canonical-property"></a>Propiedad canónica PidLidTaskOrdinal

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona una ayuda para las tareas de ordenación personalizadas.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskOrdinal  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008123  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad puede quedar sin conjunto. Si se establece, su valor debe ser mayor que "0x800186A0" (-2.147.383.648) y menor que "0x7FFE7960" (2.147.383.648) y debe ser único entre las tareas de la misma carpeta.
  
Siempre que el cliente establece esta propiedad en un número menor que el negativo del valor actual de la propiedad  **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) de la carpeta, el cliente también debe actualizar PR_ORDINAL_MOST en la carpeta. 
  
La **PR_ORDINAL_MOST** propiedad de la carpeta proporciona una forma eficaz de determinar un valor único entre las tareas de la misma carpeta. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OJOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas. 
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

