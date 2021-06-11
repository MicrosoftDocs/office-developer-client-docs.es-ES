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
ms.openlocfilehash: b5d1d4456856f1640bbed8589fc0583060cd2520
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342640"
---
# <a name="pidtagmemberid-canonical-property"></a>Propiedad canónica PidTagMemberId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de un miembro de tabla que tiene los derechos descritos en una Microsoft Exchange Server o buzón de correo.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MEMBER_ID  <br/> |
|Identificador:  <br/> |0x6671  <br/> |
|Tipo de datos:  <br/> |PT_I8  <br/> |
|Área:  <br/> |Control de acceso  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad devuelve un identificador único de la tabla. Un identificador de usuario de directorio está asociado a cada identificador de miembro y lo proporciona esta propiedad. La interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) usa esta propiedad para recuperar el identificador de entrada de directorio de un miembro con derechos explícitos en una carpeta. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Controla la recuperación de listas de permisos de carpetas almacenadas en el servidor.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

