---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6e3cdcf3579b26776d9e278bb339758d4f56d890
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339280"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción exist que se usa para comprobar si una propiedad determinada existe como una columna en la tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a>Members

 **ulReserved1**
  
> Reserve debe ser cero. 
    
 **ulPropTag**
  
> Etiqueta de propiedad que identifica la columna que se va a probar para la existencia en cada fila.
    
 **ulReserved2**
  
> Reserve debe ser cero.
    
## <a name="remarks"></a>Comentarios

La restricción EXISTS se usa para garantizar resultados significativos para otros tipos de restricciones que implican propiedades, como las restricciones de contenido y propiedades. Cuando se pasa una restricción que implica una propiedad a [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md) y la propiedad no existe, los resultados de la restricción quedan sin definir. Mediante la creación de una restricción **and** que combina la restricción de propiedad con una restricción exist, una persona que llama puede garantizar resultados precisos. 
  
Las restricciones EXISTS no se pueden usar con propiedades de subobjeto que tienen el tipo PT Object. 
  
Para obtener más información acerca de la estructura **SExistRestriction** , consulte [About Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Vea también



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

