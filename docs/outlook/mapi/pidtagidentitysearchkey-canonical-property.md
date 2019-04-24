---
title: Propiedad canónica PidTagIdentitySearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentitySearchKey
api_type:
- HeaderDef
ms.assetid: 5fe55ba7-4ecd-4a43-ab5b-2ef595c2cdd9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5f5f5eaa41d6256bed69b2cd9a91208181d5bda1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346637"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a>Propiedad canónica PidTagIdentitySearchKey

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la clave de búsqueda de la identidad de un proveedor de servicios, tal como se define en un sistema de mensajería. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_IDENTITY_SEARCH_KEY  <br/> |
|Identificador:  <br/> |0x3E05  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Estado de MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad no aparece como una propiedad en ningún objeto, sino sólo como una columna en una tabla de estado. Forma parte de la identidad del proveedor de servicios que expone la fila de la tabla de estado. La identidad del proveedor normalmente hace referencia a su cuenta en el servidor, pero puede hacer referencia a cualquier representación que el proveedor defina en el sistema de mensajería. 
  
Un proveedor de servicios que proporcione cualquiera de las propiedades de identidad debe proporcionar todas ellas. Los proveedores que pertenecen al mismo servicio de mensajes deben exponer los mismos valores para las propiedades de identidad. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

