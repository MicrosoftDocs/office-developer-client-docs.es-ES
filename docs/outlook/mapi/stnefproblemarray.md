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
ms.openlocfilehash: baa2ac2e859b42234fcb07dd2bf521424ef9b465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820789"
---
# <a name="stnefproblemarray"></a>STnefProblemArray

  
  
**Hace referencia a**: Outlook 
  
Contiene una matriz de estructuras **STnefProblem** que describe uno o varios problemas que se ha producido durante la codificación de procesamiento o descodificación de una secuencia de formato de encapsulación neutro de transporte (TNEF). 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |TNEF.h  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a>Members

 **cProblem**
  
> Recuento de elementos de la matriz especificada en el miembro **aProblem** . 
    
 **aProblem**
  
> Matriz de estructuras [STnefProblem](stnefproblem.md) . Cada estructura contiene información acerca de una propiedad o un problema de procesamiento del atributo. 
    
## <a name="remarks"></a>Comentarios

Si se produce un problema durante atributo o el procesamiento de propiedad, un parámetro de salida en el método [ITnef::ExtractProps](itnef-extractprops.md) y en el método [ITnef::Finish](itnef-finish.md) recibir un puntero a una estructura **STnefProblemArray** y **ExtractProps **y **Finalizar** cada devuelven el valor MAPI_W_ERRORS_RETURNED. Este valor de error indica que un problema surgieron durante el procesamiento y se ha generado una estructura **STnefProblemArray** . 
  
Si no se genera una estructura de **STnefProblem** durante el procesamiento de un atributo o propiedad, la aplicación cliente puede continuar en la suposición de que se ha realizado correctamente en el procesamiento de ese atributo o propiedad. La única excepción se produce cuando surgió el problema durante la descodificación de un bloque de encapsulación. Si se produjo el error durante este proceso de descodificación, se puede devolver MAPI_E_UNABLE_TO_COMPLETE como el [SCODE](scode.md) en la estructura. En este caso, la descodificación del componente correspondiente al bloque se ha detenido y descodificación continúa en otro componente. 
  
## <a name="see-also"></a>Vea también



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[Estructuras MAPI](mapi-structures.md)

