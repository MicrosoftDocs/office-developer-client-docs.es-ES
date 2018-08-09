---
title: Propiedad canónica PidTagMemberEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberEntryId
api_type:
- HeaderDef
ms.assetid: b1e166fd-7e15-4371-8510-63001317fb90
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3139f7cc60d19048fb17c64101f279ce377e9b26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819731"
---
# <a name="pidtagmemberentryid-canonical-property"></a>Propiedad canónica PidTagMemberEntryId

  
  
**Hace referencia a**: Outlook 
  
Contiene el identificador de entrada de objeto de Active directory de un miembro de tabla del sistema (SACL) de la lista de control de acceso.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MEMBER_ENTRYID  <br/> |
|Identificador:  <br/> |0x0FFF  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Reglas del servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se usa con la interfaz de [IExchangeModifyTable](iexchangemodifytableiunknown.md) para identificar de forma exclusiva una persona o la función a la que se aplica la SACL. Una vez creado un miembro de la tabla SACL, no se puede cambiar la **propiedad ENTRYID** . Para cambiarlo, debe eliminar al miembro de la tabla y volver a crearlo con una **propiedad ENTRYID**de diferentes.
  
## <a name="related-resources"></a>Recursos relacionados

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

