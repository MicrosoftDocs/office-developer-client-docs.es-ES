---
title: Propiedad canónica PidTagDepth
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDepth
api_type:
- HeaderDef
ms.assetid: 04d444a5-e97f-48e6-89a5-8a6cb2136408
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 75d390edd06aaf826f6b8c2d996e4e08bf6a7334
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360854"
---
# <a name="pidtagdepth-canonical-property"></a>Propiedad canónica PidTagDepth

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un entero que representa el nivel relativo de sangría, o profundidad, de un objeto en una tabla de jerarquía.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DEPTH  <br/> |
|Identificador:  <br/> |0x3005  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Common MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad también puede especificar el nivel de categorización de una fila en una tabla de contenido o la profundidad de jerarquía en una tabla de jerarquía. La profundidad es de base cero, donde cero representa la categoría más a la izquierda. En todos los casos, el valor de la propiedad representa un valor relativo en lugar de un valor absoluto. En la tabla de jerarquías, por ejemplo, el valor de profundidad es relativo al contenedor desde el que se recuperó la tabla de jerarquía. La profundidad no representa una profundidad absoluta desde el contenedor raíz. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Incluye operaciones admitidas para los objetos de la tabla principal.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[Propiedad canónica PidTagSelectable](pidtagselectable-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

