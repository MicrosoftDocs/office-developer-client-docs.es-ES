---
title: Propiedad canónica PidTagScheduleInfoMonthsMerged
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsMerged
api_type:
- COM
ms.assetid: b13b5d7b-413e-4405-8a35-0422477a9e86
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 53bc27b4ddd05b4a52328c605a6d4f673c91afd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336480"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a>Propiedad canónica PidTagScheduleInfoMonthsMerged

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista de los meses durante los cuales los datos de disponibilidad del tipo ocupado o un mensaje de fuera de la oficina (OOF) están presentes en el mensaje de disponibilidad. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SCHDINFO_MONTHS_MERGED  <br/> |
|Identificador:  <br/> |0x684F  <br/> |
|Tipo de datos:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Disponibilidad  <br/> |
   
## <a name="remarks"></a>Comentarios

Los eventos de tipo de disponibilidad provisional no se incluyen en esta propiedad. La sintaxis/formato y las restricciones de esta propiedad son las mismas que las de **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)), pero hacen referencia a citas marcadas como OOF o Busy en el objeto de calendario asociado. 
  
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
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

