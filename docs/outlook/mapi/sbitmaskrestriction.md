---
title: SBitMaskRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBitMaskRestriction
api_type:
- COM
ms.assetid: ddd42180-6e4f-410c-9f78-d868a91452dc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: afac8c352ad0a07fcb1cd98683b6a5c87940ab4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424479"
---
# <a name="sbitmaskrestriction"></a>SBitMaskRestriction

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción de máscara de bits, que se usa para **** realizar una operación and bit a bit y probar el resultado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a>Members

 **relBMR**
  
> Operador relacional que describe cómo se debe aplicar la máscara especificada en el miembro **ulMask** a la etiqueta de propiedad. Los valores posibles son los siguientes: 
    
BMR_EQZ 
  
> Realice una operación **** and bit a bit de la máscara en el miembro **ulMask** con la propiedad representada por el miembro **ulPropTag** y pruebe si es igual a cero. 
    
BMR_NEZ 
  
> Realice una operación **** and bit a bit de la máscara en el miembro **ulMask** con la propiedad representada por el miembro **ulPropTag** y pruebe si no es igual a cero. 
    
 **ulPropTag**
  
> Etiqueta de propiedad de la propiedad a la que se aplica la máscara de la máscara.
    
 **ulMask**
  
> Máscara de máscara para aplicar a la propiedad identificada por **ulPropTag**.
    
## <a name="remarks"></a>Comentarios

La estructura **SBitMaskRestriction** realiza una operación **** and bit a bit mediante la máscara de bits descrita en el miembro **ulMask** y el valor de la propiedad descrito por el miembro **ulPropTag** . Si el resultado es cero, BMR_EQZ se cumple. Si es distinto de cero, es decir, si el valor de la propiedad tiene al menos uno de los mismos bits establecidos que **ulMask**, entonces BMR_NEZ se cumple.
  
Para obtener más información acerca de las restricciones y la estructura **SBitMaskRestriction** en general, consulte [About Restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Ver también



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

