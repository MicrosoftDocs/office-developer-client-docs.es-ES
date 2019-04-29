---
title: SComparePropsRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SComparePropsRestriction
api_type:
- COM
ms.assetid: 3231a91a-1ef2-4dd8-9f3e-79ca56d2eae9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 513ec0db4e99e687d8aeb9e1d6acdef73df4d158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440006"
---
# <a name="scomparepropsrestriction"></a>SComparePropsRestriction

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción de comparación de propiedades, que prueba dos propiedades mediante un operador relacional. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a>Members

**relop**
  
> Operador relacional que se va a usar para comparar las dos propiedades. Los valores posibles son los siguientes:
    
  - RELOP_GE: la comparación se realiza en función de un valor mayor o igual al primero.
      
  - RELOP_GT: la comparación se realiza en función de un primer valor superior.
      
  - RELOP_LE: la comparación se realiza en función de un valor menor o igual al primero.
      
  - RELOP_LT: la comparación se realiza en función de un valor primero menor.
      
  - RELOP_NE: la comparación se realiza en función de valores desiguales.
      
  - RELOP_RE: la comparación se realiza en función de los valores LIKE (expresión regular).
      
  - RELOP_EQ: la comparación se realiza en función de los valores iguales.
    
**ulPropTag1**
  
> Etiqueta de propiedad de la primera propiedad que se va a comparar. 
    
**ulPropTag2**
  
> Etiqueta de propiedad de la segunda propiedad que se va a comparar.
    
## <a name="remarks"></a>Comentarios

El orden de comparación es _(etiqueta de propiedad 1) (operador relacional) (etiqueta de propiedad 2)_. Las propiedades que se van a comparar deben ser del mismo tipo. Al intentar comparar propiedades de distintos tipos, MAPI o el proveedor de servicios devuelven el valor de error MAPI_E_TOO_COMPLEX del método [IMAPITable](imapitableiunknown.md) al que se pasa la estructura como parámetro. 
  
El resultado de una restricción del valor de la propiedad Compare no está definido cuando no existe una o ambas propiedades. Cuando un cliente requiere un comportamiento bien definido para dicha restricción y no está seguro de si la propiedad existe (por ejemplo, no es una columna obligatoria de una tabla), debe crear una restricción **and** para unirse a la restricción de propiedad Compare con EXISTS. limitado. Use una estructura [SExistRestriction](sexistrestriction.md) para definir la restricción EXISTS y una estructura [SAndRestriction](sandrestriction.md) para definir la restricción **and** . 
  
Las propiedades especificadas en los miembros **ulPropTag1** y **ulPropTag2** pueden tener varios valores si el proveedor de servicios lo admite. 
  
Para obtener más información acerca de las restricciones y la estructura **SComparePropsRestriction** en general, consulte [About Restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Ver también

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [Estructuras MAPI](mapi-structures.md)

