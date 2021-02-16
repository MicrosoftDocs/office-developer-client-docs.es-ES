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
  
Describe una restricción de propiedad de comparación, que prueba dos propiedades mediante un operador relacional. 
  
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

**reeste**
  
> Operador relacional que se usará para comparar las dos propiedades. Los valores posibles son los siguientes:
    
  - RELOP_GE: la comparación se realiza en función de un primer valor mayor o igual.
      
  - RELOP_GT: la comparación se realiza en función de un primer valor mayor.
      
  - RELOP_LE: la comparación se realiza en función de un primer valor menor o igual.
      
  - RELOP_LT: la comparación se realiza en función de un primer valor menor.
      
  - RELOP_NE: la comparación se realiza en función de valores no iguales.
      
  - RELOP_RE: la comparación se realiza en función de los valores LIKE (expresión regular).
      
  - RELOP_EQ: la comparación se realiza en función de valores iguales.
    
**ulPropTag1**
  
> Etiqueta de propiedad de la primera propiedad que se va a comparar. 
    
**ulPropTag2**
  
> Etiqueta de propiedad de la segunda propiedad que se va a comparar.
    
## <a name="remarks"></a>Comentarios

El orden de comparación _es (etiqueta de propiedad 1) (operador relacional) (etiqueta de propiedad 2)._ Las propiedades que se deben comparar deben ser del mismo tipo. Al intentar comparar propiedades de diferentes tipos, MAPI o el proveedor de servicios devuelven el valor de error MAPI_E_TOO_COMPLEX del método [IMAPITable](imapitableiunknown.md) al que se pasa la estructura como parámetro. 
  
El resultado de una restricción de valor de propiedad de comparación no está definido cuando una o ambas propiedades no existen. Cuando un cliente requiere un comportamiento bien definido para dicha restricción y no está seguro de si la propiedad existe (por ejemplo, no es una columna obligatoria de una tabla), debe crear una restricción **AND** para unir la restricción de propiedad de comparación con una restricción existente. Use una [estructura SExistRestriction](sexistrestriction.md) para definir la restricción existente y una estructura [SAndRestriction](sandrestriction.md) para definir la **restricción AND.** 
  
Las propiedades especificadas en los miembros **ulPropTag1** y **ulPropTag2** pueden tener varios valores si el proveedor de servicios lo admite. 
  
Para obtener más información acerca **de la estructura SComparePropsRestriction** y las restricciones en general, vea [Acerca de las restricciones](about-restrictions.md).
  
## <a name="see-also"></a>Consulte también

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [Estructuras MAPI](mapi-structures.md)

