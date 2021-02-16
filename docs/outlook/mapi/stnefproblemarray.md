---
title: STnefProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblemArray
api_type:
- COM
ms.assetid: 115d845b-4168-4d49-b880-219ee28baa9a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 721b14f101e87299f654507f94d4a957f905cac1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434266"
---
# <a name="stnefproblemarray"></a>STnefProblemArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de estructuras **STnefProblem** que describen uno o varios problemas de procesamiento que se produjeron durante la codificación o la decodificación de una secuencia de formato de encapsulamiento neutro de transporte (TNEF). 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Tnef.h  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a>Miembros

 **cProblem**
  
> Número de elementos de la matriz especificada en el **miembro aProblem.** 
    
 **aProblem**
  
> Matriz de [estructuras STnefProblem.](stnefproblem.md) Cada estructura contiene información sobre un problema de procesamiento de propiedades o atributos. 
    
## <a name="remarks"></a>Comentarios

Si se produce un problema durante el procesamiento de atributos o propiedades, un parámetro de salida en el método [ITnef::ExtractProps](itnef-extractprops.md) y en el método [ITnef::Finish](itnef-finish.md) cada uno recibe un puntero a una estructura **STnefProblemArray** y **ExtractProps** y **Finish** devuelven cada uno el valor MAPI_W_ERRORS_RETURNED. Este valor de error indica que se produjo un problema durante el procesamiento y se generó una estructura **STnefProblemArray.** 
  
Si no se genera una estructura **STnefProblem** durante el procesamiento de un atributo o propiedad, la aplicación cliente puede continuar con la suposición de que el procesamiento de ese atributo o propiedad se ha hecho correctamente. La única excepción se produce cuando el problema se produjo durante la decodificación de un bloque de encapsulación. Si se produjo el error durante esta descodificación, MAPI_E_UNABLE_TO_COMPLETE puede devolverse como [el SCODE](scode.md) en la estructura. En este caso, la decodificación del componente correspondiente al bloque se detiene y la decodificación continúa en otro componente. 
  
## <a name="see-also"></a>Consulte también



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[Estructuras MAPI](mapi-structures.md)

