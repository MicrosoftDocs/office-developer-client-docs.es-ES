---
title: Propiedad canónico PidTagRowType
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 7fdb8781c39d7814ff2c38ff4df4545511d28a5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820132"
---
# <a name="pidtagrowtype-canonical-property"></a>Propiedad canónico PidTagRowType

  
  
**Se aplica a**: Outlook 
  
Contiene un valor que indica el tipo de una fila de una tabla.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ROW_TYPE  <br/> |
|Identificador:  <br/> |0x0FF5  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI no transmisible  <br/> |
   
## <a name="remarks"></a>Notas

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

[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Incluye las operaciones permitidas para los objetos de la tabla principal.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedad canónico PidTagRowid](pidtagrowid-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

