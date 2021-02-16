---
title: Propiedad canónica PidTagFreeBusyCountMonths
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyCountMonths
api_type:
- HeaderDef
ms.assetid: 278a77f2-65ec-4281-b406-942cc416a476
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 610e9d396442f981b7bcbf126e3086e6885399d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316194"
---
# <a name="pidtagfreebusycountmonths-canonical-property"></a>Propiedad canónica PidTagFreeBusyCountMonths

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el valor para calcular las fechas de inicio y finalización del intervalo de datos de disponibilidad que se publicarán en carpetas públicas.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_FREEBUSY_COUNT_MONTHS  <br/> |
|Identificador:  <br/> |0x6869  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Transmitible definido por clase de mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de esta propiedad debe ser mayor o igual que 0 y menor o igual que 36. Esta propiedad no es obligatoria.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publica la disponibilidad de un usuario o recurso.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.
    
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

