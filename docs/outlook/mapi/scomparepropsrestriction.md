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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 6ebc4e9cbc79a71a91f1f2f3eec0d40de979ab18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820586"
---
# <a name="scomparepropsrestriction"></a>SComparePropsRestriction

**Se aplica a**: Outlook 
  
Describe una restricción de propiedad compare, que comprueba las propiedades de dos con un operador relacional. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a>Miembros

**RelOp**
  
> Operador relacional debe usar para comparar las dos propiedades. Los valores posibles son los siguientes:
    
  - RELOP_GE: Se realiza la comparación basándose en el primer valor mayor o igual.
      
  - RELOP_GT: Se realiza la comparación basándose en un valor mayor de primera.
      
  - RELOP_LE: Se realiza la comparación basándose en el primer valor menor o igual.
      
  - RELOP_LT: Se realiza la comparación basándose en un valor menor de primera.
      
  - RELOP_NE: Se realiza la comparación basándose en valores desiguales.
      
  - RELOP_RE: La comparación se realiza en función de como valores (expresión regular).
      
  - RELOP_EQ: Se realiza la comparación basándose en valores iguales.
    
**ulPropTag1**
  
> Etiqueta de propiedad de la primera propiedad que se va a comparar. 
    
**ulPropTag2**
  
> Etiqueta de propiedad de la segunda propiedad que se va a comparar.
    
## <a name="remarks"></a>Notas

El orden de comparación es _(etiqueta de la propiedad (1) (operador relacional) (etiqueta de la propiedad 2)_. Las propiedades que se va a comparar con deben ser del mismo tipo. Si se intenta comparar las propiedades de distintos tipos hace que MAPI o el proveedor de servicios devolver el valor de error MAPI_E_TOO_COMPLEX desde el método [IMAPITable](imapitableiunknown.md) a la que la estructura se pasa como un parámetro. 
  
El resultado de una restricción de valor de propiedad de compare no está definido cuando uno o ambos de las propiedades no existen. Cuando un cliente requiere un comportamiento bien definido para esta restricción y no está seguro de si existe la propiedad, (por ejemplo, no es una columna de una tabla necesaria) debe crear una restricción **y** para unirse a la restricción de propiedad comparar con un existe restricción. Usar una estructura [SExistRestriction](sexistrestriction.md) para definir la restricción existe y una estructura [SAndRestriction](sandrestriction.md) para definir la restricción de **y** . 
  
Las propiedades especificadas en los miembros **ulPropTag1** y **ulPropTag2** pueden ser multivalor si lo admite el proveedor de servicios. 
  
Para obtener más información sobre la estructura de **SComparePropsRestriction** y restricciones en general, vea [Acerca de las restricciones](about-restrictions.md).
  
## <a name="see-also"></a>Ver también

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [Estructuras MAPI](mapi-structures.md)

