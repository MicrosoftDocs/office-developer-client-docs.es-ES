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
ms.openlocfilehash: 990fe49d39a73c5bf80b9fdda96d2e5997869edf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595422"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción de tamaño que se usa para probar el tamaño de un valor de la propiedad. 
  
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

 **RelOp**
  
> Operador relacional que se usa en la comparación de tamaño. Los valores posibles son los siguientes: 
    
RELOP_GE 
  
> Se realice a la comparación en un primer valor mayor o igual.
    
RELOP_GT 
  
> Se realice a la comparación en un primer valor mayor.
    
RELOP_LE 
  
> Se realice a la comparación en un primer valor menor o igual.
    
RELOP_LT 
  
> Se realice a la comparación en un primer valor menor.
    
RELOP_NE 
  
> Se realice a la comparación en valores iguales.
    
RELOP_RE 
  
> La comparación se realiza en función de como valores (expresión regular).
    
RELOP_EQ 
  
> Se realice a la comparación de valores iguales.
    
 **ulPropTag**
  
> Etiqueta de la propiedad que identifica la propiedad que se debe probar.
    
 **cb**
  
> Recuento de bytes en el valor de la propiedad.
    
## <a name="remarks"></a>Comentarios

Para obtener una descripción general de cómo funcionan las restricciones, vea [Restricciones de sobre](about-restrictions.md). 
  
## <a name="see-also"></a>Recursos adicionales



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

