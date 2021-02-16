---
title: Propiedad canónica PidLidLogDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogDocumentSaved
api_type:
- COM
ms.assetid: 012a3f6e-fd16-4dc9-845d-2bf4cebeaa42
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6f25c1a72882f9236d56532b7259f51512734945
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336921"
---
# <a name="pidlidlogduration-canonical-property"></a>Propiedad canónica PidLidLogDuration

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Representa la duración, en minutos, de un mensaje de diario.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidLogDuration  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Log  <br/> |
|Long ID (LID):  <br/> |0x00008707  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Diario  <br/> |
   
## <a name="remarks"></a>Comentarios

Duración, en minutos, de la actividad que debe ser la diferencia entre las propiedades **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) y **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OJOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para los diarios.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

