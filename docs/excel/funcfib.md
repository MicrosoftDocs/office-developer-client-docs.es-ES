---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- funcfib (función) [excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8d1c97ea57e968aaedffca6b37ded3d875e87413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815632"
---
# <a name="funcfib"></a>FuncFib

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de hoja de cálculo definida por el usuario de ejemplo que calcula el número de Fibonacci n. Cuando se carga GENERIC.xll, registra esta función para que se pueda llamar desde la hoja de cálculo.
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a>Parámetros

 _pxN_ (**LPXLOPER12**)
  
El valor de N para la que se requiere el número de Fibonacci n.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

(**xltypeNum LPXLOPER12** si se realiza correctamente o **xltypeErr** en caso contrario) 
  
El número de Fibonacci n.
  
## <a name="remarks"></a>Comentarios

La función utiliza una variable estática definida dentro del bloque de función como el valor devuelto **XLOPER12**. Esto no es seguro para subprocesos y, por lo que esta función y cualquier función de hoja de cálculo que utiliza esta estrategia para devolver **XLOPER**s o s **XLOPER12**, no se deben registrar como subprocesos de inicio en Excel 2007.
  
### <a name="example"></a>Ejemplo

Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones de la DLL genérica](functions-in-the-generic-dll.md)

