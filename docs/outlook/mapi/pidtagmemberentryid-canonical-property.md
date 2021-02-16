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
ms.openlocfilehash: 83a645b49e5bb48051bbaedb26058d2da053348b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433041"
---
# <a name="pidtagmemberentryid-canonical-property"></a>Propiedad canónica PidTagMemberEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de entrada de objeto de directorio de un miembro de tabla de lista de control de acceso del sistema (SACL).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MEMBER_ENTRYID  <br/> |
|Identificador:  <br/> |0x0FFF  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Reglas del lado servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se usa en la interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) para identificar de forma única a una persona o rol al que se aplica el SACL. Después de crear un miembro en la tabla SACL, **el ENTRYID** no se puede cambiar. Para cambiarlo, debe eliminar el miembro de tabla y volver a crearlo con un **ENTRYID diferente.**
  
## <a name="related-resources"></a>Recursos relacionados

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

