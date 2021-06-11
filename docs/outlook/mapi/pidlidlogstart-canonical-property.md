---
title: Propiedad canónica PidLidLogStart
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogStart
api_type:
- COM
ms.assetid: b8c0c871-51d8-4752-ad4b-607463a9f837
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dd5805cb0ee6b172506a532a513d06f57c583eee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337019"
---
# <a name="pidlidlogstart-canonical-property"></a>Propiedad canónica PidLidLogStart

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Representa la fecha y hora de inicio del mensaje de diario.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidLogStart  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Log  <br/> |
|Id. largo (LID):  <br/> |0x00008706  <br/> |
|Tipo de datos:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Diario  <br/> |
   
## <a name="remarks"></a>Comentarios

La hora en la hora universal coordinada (UTC) cuando comenzó la actividad debe ser igual a la propiedad **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona la definición del conjunto de propiedades y las referencias a las Exchange Server de protocolo relacionados.
    
[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones que son permisibles para los diarios.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

