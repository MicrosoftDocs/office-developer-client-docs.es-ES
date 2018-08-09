---
title: Propiedad canónica PidTagMemberId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberId
api_type:
- HeaderDef
ms.assetid: 64faef3c-27b2-49d2-9d0c-8b9d33f1cb71
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ce6925f40e09261494e4edbcbd7314728debbe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819739"
---
# <a name="pidtagmemberid-canonical-property"></a>Propiedad canónica PidTagMemberId

  
  
**Hace referencia a**: Outlook 
  
Contiene el identificador de un miembro de la tabla que tiene los derechos que se describe en una carpeta de Microsoft Exchange Server o el buzón de correo.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MEMBER_ID  <br/> |
|Identificador:  <br/> |0x6671  <br/> |
|Tipo de datos:  <br/> |PT_I8  <br/> |
|Área:  <br/> |Control de acceso  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad devuelve un identificador único para la tabla. Un identificador de usuario de Active directory está asociado con cada identificador de miembro y viene dado por esta propiedad. Esta propiedad se usa en la interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) para recuperar el identificador de entrada de Active directory de un miembro con derechos explícitos en una carpeta. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Controla la recuperación de listas de permisos de carpeta que se almacenan en el servidor.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

