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
ms.openlocfilehash: 28c269db15d0c0a81950a61ee9e6629ad067b789
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819580"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a>Propiedad canónica PidTagIdentitySearchKey

  
  
**Hace referencia a**: Outlook 
  
Contiene la clave de búsqueda para la identidad de un proveedor de servicios, tal como se define dentro de un sistema de mensajería. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_IDENTITY_SEARCH_KEY  <br/> |
|Identificador:  <br/> |0x3E05  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad no aparece como una propiedad en cualquier objeto sino sólo como una columna de una tabla de estado. Forma parte de la identidad de la exposición de la fila de la tabla de estado de proveedor de servicios. Identidad del proveedor normalmente hace referencia a su cuenta en el servidor, pero puede hacer referencia a cualquier representación que el proveedor define dentro del sistema de mensajería. 
  
Debe proporcionar un proveedor de servicios de suministro de cualquiera de las propiedades de identidad todos ellos. Los proveedores que pertenecen al mismo servicio de mensajes deben exponer los mismos valores para las propiedades de identidad. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

