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
ms.openlocfilehash: f0cf6fa03d8f38b7d160a8747111445cfdac1ae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820558"
---
# <a name="sbitmaskrestriction"></a>SBitMaskRestriction

  
  
**Hace referencia a**: Outlook 
  
Describe una restricción de máscara de bits que se usa para realizar una operación **AND** bit a bit y el resultado de la prueba. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
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
  
> Operador relacional que describe cómo debe aplicarse la máscara especificada en el miembro **ulMask** en la etiqueta de propiedad. Los valores posibles son los siguientes: 
    
BMR_EQZ 
  
> Realice una operación **AND** bit a bit de la máscara en el miembro **ulMask** con la propiedad representada por el miembro de **ulPropTag** y pruebas para es igual a cero. 
    
BMR_NEZ 
  
> Realice una operación **AND** bit a bit de la máscara en el miembro **ulMask** con la propiedad representada por el miembro de **ulPropTag** y pruebas para no es igual a cero. 
    
 **ulPropTag**
  
> Etiqueta de la propiedad de la propiedad a la que se aplica la máscara de bits.
    
 **ulMask**
  
> Máscara de bits que se aplican a la propiedad identificada por **ulPropTag**.
    
## <a name="remarks"></a>Comentarios

La estructura **SBitMaskRestriction** realiza una operación **AND** bit a bit con la máscara de bits que se describen en el miembro **ulMask** y el valor de la propiedad descrito por el miembro **ulPropTag** . Si el resultado es cero, se cumple BMR_EQZ. Si es distinto de cero, es decir, si el valor de la propiedad tiene al menos uno de los mismos bits establecer como **ulMask**, a continuación, BMR_NEZ está satisfecho.
  
Para obtener más información sobre la estructura de **SBitMaskRestriction** y restricciones en general, vea [Acerca de las restricciones](about-restrictions.md).
  
## <a name="see-also"></a>Vea también



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

