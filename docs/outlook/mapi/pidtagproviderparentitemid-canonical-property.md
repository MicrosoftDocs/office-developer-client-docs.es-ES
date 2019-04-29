---
title: Propiedad canónica PidTagProviderParentItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0f99cf38e65c75ce1ba74bf72d88e19f4fbfa03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433419"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a>Propiedad canónica PidTagProviderParentItemId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica un identificador para el elemento primario de una carpeta o un elemento en un almacén.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROVIDER_PARENT_ITEMID  <br/> |
|Identificador:  <br/> |0x0EA4  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MAPI no transmitible  <br/> |
   
## <a name="remarks"></a>Comentarios

Los proveedores de almacén pueden especificar un valor para esta propiedad para un elemento primario de una carpeta o un elemento, pero deben mantener el valor igual entre sesiones. Los proveedores de almacenamiento usan esta propiedad para identificar los resultados de la búsqueda que devuelve un motor de búsqueda.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

