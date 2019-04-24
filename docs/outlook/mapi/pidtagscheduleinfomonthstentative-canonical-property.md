---
title: Propiedad canónica PidTagScheduleInfoMonthsTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsTentative
api_type:
- COM
ms.assetid: 3179442c-6499-464a-93af-eb0a7a5b0d30
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6fa0579dcd98a0d819e58e62d8a42cb2972a9d1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359762"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a>Propiedad canónica PidTagScheduleInfoMonthsTentative

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene los meses marcados como provisional en el mensaje de disponibilidad.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SCHDINFO_MONTHS_TENTATIVE  <br/> |
|Identificador:  <br/> |0x6851  <br/> |
|Tipo de datos:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Disponibilidad  <br/> |
   
## <a name="remarks"></a>Comentarios

El número de valores de esta propiedad debe estar comprendido entre cero y el número de meses cubiertos por el intervalo de publicación, que es el período entre el **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) y **PR_FREEBUSY_PUBLISH_END **([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) propiedades.
  
Cada valor de esta propiedad tiene un mes y un año codificados. Se calcula mediante la expresión "Year × 16 + Month" donde Year y month se basan en el calendario gregoriano. Los valores se ordenan en orden ascendente y se codifican en formato Little-Endian. Si un evento se extiende por varios meses o varios años, debe haber un valor para cada uno de los meses que se encuentran en el intervalo de publicación. Si no hay ningún evento tentativa en el intervalo de publicación, esta propiedad y **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) no se deben establecer o deben eliminarse si ya existen. De lo contrario, se debe establecer esta propiedad.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publica la disponibilidad de un usuario o recurso.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

