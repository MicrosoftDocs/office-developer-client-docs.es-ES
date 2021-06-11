---
title: SSizeRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSizeRestriction
api_type:
- COM
ms.assetid: 4e7340d1-3cb9-4276-b83f-1c8f94acb909
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 24ceb7b5358447de3a240756227b86224d2c354c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439089"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción de tamaño que se usa para probar el tamaño de un valor de propiedad. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a>Members

 **relop**
  
> Operador relacional que se usa en la comparación de tamaño. Los valores posibles son los siguientes: 
    
RELOP_GE 
  
> La comparación se realiza en función de un primer valor mayor o igual.
    
RELOP_GT 
  
> La comparación se realiza en función de un primer valor mayor.
    
RELOP_LE 
  
> La comparación se realiza en función de un primer valor menor o igual.
    
RELOP_LT 
  
> La comparación se realiza en función de un primer valor menor.
    
RELOP_NE 
  
> La comparación se realiza en función de valores desiguales.
    
RELOP_RE 
  
> La comparación se realiza en función de los valores LIKE (expresión regular).
    
RELOP_EQ 
  
> La comparación se realiza en función de valores iguales.
    
 **ulPropTag**
  
> Etiqueta de propiedad que identifica la propiedad que se debe probar.
    
 **cb**
  
> Recuento de bytes en el valor de la propiedad.
    
## <a name="remarks"></a>Comentarios

Para obtener una explicación general de cómo funcionan las restricciones, vea [Acerca de las restricciones](about-restrictions.md). 
  
## <a name="see-also"></a>Vea también



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

