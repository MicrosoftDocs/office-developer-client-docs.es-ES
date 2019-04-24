---
title: Propiedad canónica PidTagRowType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowType
api_type:
- COM
ms.assetid: d57ce5c8-1f60-4709-b86a-4468c4208dfe
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 962e8c92ae61e8b60862a3ae26a7cdfbf5034e89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359517"
---
# <a name="pidtagrowtype-canonical-property"></a>Propiedad canónica PidTagRowType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor que indica el tipo de una fila en una tabla.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ROW_TYPE  <br/> |
|Identificador:  <br/> |0x0FF5  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI no transmitible  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad aparece sólo en las tablas de contenido. Solo existe una categoría cuando tiene elementos.
  
Esta propiedad puede tener exactamente uno de los siguientes valores:
  
TBL_LEAF_ROW 
  
> Representa los datos reales, en lugar de una fila de categoría.
    
TBL_EMPTY_CATEGORY 
  
> No se usa actualmente.
    
TBL_EXPANDED_CATEGORY 
  
> Se expande la categoría; la interfaz de usuario suele mostrar esto con el signo menos (-) junto a él.
    
TBL_COLLAPSED_CATEGORY 
  
> La categoría está contraída; la interfaz de usuario suele mostrar esto con el signo más (+) junto a él.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Incluye operaciones admitidas para los objetos de la tabla principal.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagRowid](pidtagrowid-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

