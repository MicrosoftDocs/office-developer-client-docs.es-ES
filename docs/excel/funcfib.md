---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- función funcfib [excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb8f0c12c27fb2c95007eb5006c1d8b90970f3ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423674"
---
# <a name="funcfib"></a>FuncFib

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de hoja de cálculo definida por el usuario que calcula el número Nésima de Fibonacci. Cuando se carga GENERIC.xll, registra esta función para que se pueda llamar desde la hoja de cálculo.
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a>Parameters

 _pxN_ (**LPXLOPER12**)
  
Valor de N para el que se requiere el número Nésima fibonacci.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

(**xltypeNum LPXLOPER12** si se realiza correctamente **o xltypeErr de lo** contrario) 
  
Número Nésima fibonacci.
  
## <a name="remarks"></a>Comentarios

La función usa una variable estática definida dentro del bloque de funciones como el valor devuelto **XLOPER12**. Esto no es seguro para subprocesos, por lo que esta función y cualquier función de hoja de cálculo que use esta estrategia para devolver **XLOPER** s o **XLOPER12** s, no deben registrarse como seguros para subprocesos a partir de Excel 2007.
  
### <a name="example"></a>Ejemplo

Vea  `\SAMPLES\GENERIC\GENERIC.C` el código fuente de esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones en la DLL genérica](functions-in-the-generic-dll.md)

