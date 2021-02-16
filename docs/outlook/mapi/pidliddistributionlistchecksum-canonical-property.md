---
title: Propiedad canónica PidLidDistributionListChecksum
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidDistributionListChecksum
api_type:
- COM
ms.assetid: bd50ab34-caae-4258-8afc-769e3cbc5220
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ac1f0d839b1ea059ec2b8d94556808bea3850862
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357613"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a>Propiedad canónica PidLidDistributionListChecksum

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica la suma de comprobación de redundancia cíclica de 32 bits (CRC-32) para una lista de distribución personal.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidDLChecksum  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x0000804C  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de esta propiedad se puede usar para detectar cuándo se actualizó la propiedad **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) sin actualizar las otras propiedades de miembro de la lista de distribución personal mediante el cálculo del CRC-32 en el valor existente de **dispidDLMembers** y compararlo con el valor de la propiedad **dispidDLChecksum.** 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para contactos y listas de distribución personales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

