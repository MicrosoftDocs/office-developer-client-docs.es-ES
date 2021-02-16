---
title: Propiedad canónica PidTagMemberName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberName
api_type:
- HeaderDef
ms.assetid: e19129bf-d07c-4d2e-9d4d-edbfda088ea7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a119cf1446600153e433c4aae99037d9810015c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342486"
---
# <a name="pidtagmembername-canonical-property"></a>Propiedad canónica PidTagMemberName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre para mostrar de un miembro de la tabla de lista de control de acceso (ACL).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W  <br/> |
|Identificador:  <br/> |0x6672  <br/> |
|Tipo de datos:  <br/> |PT_STRING8  <br/> |
|Área:  <br/> |Control de acceso  <br/> |
   
## <a name="remarks"></a>Comentarios

La interfaz [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) usa estas propiedades para mostrar el nombre de un miembro de una tabla ACL, que es una persona o un rol con derechos explícitos en una carpeta o buzón. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Controla la recuperación de listas de permisos de carpeta almacenadas en el servidor.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

