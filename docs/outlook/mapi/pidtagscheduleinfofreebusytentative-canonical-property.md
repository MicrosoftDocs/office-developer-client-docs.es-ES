---
title: Propiedad canónica PidTagScheduleInfoFreeBusyTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyTentative
api_type:
- COM
ms.assetid: 28453d29-30c5-405b-84d2-5bb5f281756c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 18bc41d9038113b5b813f1cfd02d90b8e982703c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359779"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a>Propiedad canónica PidTagScheduleInfoFreeBusyTentative

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene los bloques de horas para las que el estado de disponibilidad es provisional.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SCHDINFO_FREEBUSY_TENTATIVE  <br/> |
|Identificador:  <br/> |0x6852  <br/> |
|Tipo de datos:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Disponibilidad  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad tiene tantos valores como el número de valores **de PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)). Cada valor binario representa un mes y corresponde al valor en el mismo índice de **PR_SCHDINFO_MONTHS_TENTATIVE**. Los valores binarios se ordenan en el mismo orden que los valores de **PR_SCHDINFO_MONTHS_TENTATIVE**.
  
Cada valor binario tiene uno o más bloques de 4 BYTES y cada uno de ellos contiene la hora de inicio en los dos primeros bytes y la hora de finalización en los dos segundos bytes en formato little-endian. La hora de inicio es el número de minutos entre la medianoche hora universal coordinada (UTC) del primer día del mes y la hora de inicio del evento en UTC. La hora de finalización es el número de minutos entre la medianoche UTC del primer día del mes y la hora de finalización del evento en UTC. Los bloques de 4 BYTES se ordenan en orden ascendente.
  
Los bloques de tiempo consecutivos o superpuestos se combinan en un bloque con la hora de inicio como la hora de inicio del primer bloque y la hora de finalización como la hora de finalización del último bloque. Si un evento se extiende entre varios meses o años, el evento se divide en varios bloques, uno para cada mes. Si no hay eventos provisionales en el intervalo  de publicación, esta propiedad y PR_SCHDINFO_MONTHS_TENTATIVE no deben establecerse o deben eliminarse si ya existen. De lo contrario, esta propiedad debe establecerse. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publica la disponibilidad de un usuario o recurso.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

