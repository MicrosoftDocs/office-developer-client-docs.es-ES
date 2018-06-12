---
title: Propiedad canónico PidTagDepth
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 25af87004ef5616a6c6fc575c647fdd1794d710f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819431"
---
# <a name="pidtagdepth-canonical-property"></a>Propiedad canónico PidTagDepth

  
  
**Se aplica a**: Outlook 
  
Contiene un número entero que representa el nivel de sangría, o profundidad, de un objeto en una tabla de jerarquías relativo.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DEPTH  <br/> |
|Identificador:  <br/> |0x3005  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI comunes  <br/> |
   
## <a name="remarks"></a>Notas

Esta propiedad también puede especificar el nivel de la categorización de una fila en una tabla de contenido o la profundidad de jerarquía en una tabla de jerarquía. La profundidad está basada en cero, donde cero representa la categoría más a la izquierda. En todos los casos, el valor de la propiedad representa un valor relativo en lugar de un valor absoluto. En la tabla de jerarquía, por ejemplo, el valor de profundidad es en relación con el contenedor desde el que se ha recuperado en la tabla de jerarquía. La profundidad no representan una profundidad absoluta desde el contenedor raíz. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Incluye las operaciones permitidas para los objetos de la tabla principal.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedad canónico PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[Propiedad canónico PidTagSelectable](pidtagselectable-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

