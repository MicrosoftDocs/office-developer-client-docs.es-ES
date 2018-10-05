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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383069"
---
# <a name="pidtagrowtype-canonical-property"></a>Propiedad canónica PidTagRowType

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor que indica el tipo de una fila de una tabla.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ROW_TYPE  <br/> |
|Identificador:  <br/> |0x0FF5  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI no transmisible  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad sólo aparece en las tablas de contenido. Sólo existe una categoría cuando tiene elementos.
  
Esta propiedad puede tener exactamente uno de los siguientes valores:
  
TBL_LEAF_ROW 
  
> Representa los datos reales, en lugar de una fila de la categoría.
    
TBL_EMPTY_CATEGORY 
  
> Actualmente no se utiliza.
    
TBL_EXPANDED_CATEGORY 
  
> La categoría se expande; la interfaz de usuario normalmente muestra esto con el signo menos (-) junto a ella.
    
TBL_COLLAPSED_CATEGORY 
  
> La categoría está contraída; la interfaz de usuario normalmente muestra esto con el signo más (+) situado junto a él.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Incluye las operaciones permitidas para los objetos de la tabla principal.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagRowid](pidtagrowid-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

