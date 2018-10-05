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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391559"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a>Propiedad canónica PidTagScheduleInfoMonthsTentative

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene los meses marcados como provisionales en el mensaje de disponibilidad.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SCHDINFO_MONTHS_TENTATIVE  <br/> |
|Identificador:  <br/> |0x6851  <br/> |
|Tipo de datos:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Libre/ocupado  <br/> |
   
## <a name="remarks"></a>Comentarios

El número de valores de esta propiedad debe estar comprendido entre cero y el número de meses cubierto por el intervalo de publicación, que es el período entre la **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) y **PR_FREEBUSY_PUBLISH_END **Propiedades ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)).
  
Cada valor de esta propiedad tiene un mes y año codificado en ella. Esto se calcula mediante el uso de la expresión "año × 16 + mes" donde el mes y el año se basan en el calendario gregoriano. Los valores se ordenan en orden ascendente y se codifican en formato "little-endian". Si un evento es repartido por varios meses o años varios, debe ser un valor para cada uno de los meses que se encuentran en el intervalo de publicación. Si no hay ningún evento provisional en el intervalo de publicación, a continuación, esta propiedad y **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) no se deben establecer o se deben eliminar si ya existen. De lo contrario, se debe establecer esta propiedad.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publica la disponibilidad de un usuario o recurso.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

