---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- función funcsum [Excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14db5812165812161cf7031f75338a981251dfd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304063"
---
# <a name="funcsum"></a>FuncSum

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Ejemplo de función de hoja de cálculo definida por el usuario que toma de 1 a 29 argumentos y calcula su suma. Cada argumento puede ser un solo número, un rango o una matriz. Cuando se carga GENERIC. XLL, se registra esta función para que se pueda llamar desde la hoja de cálculo. 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a>Parameters

 _PX1-px29_ (**LPXLOPER12**)
  
Argumentos punteros a **XLOPER12** . La función acepta cualquier tipo de tipo de entrada, pero se codifica únicamente para operar con números, matrices literales de números e intervalos que solo contienen números o celdas en blanco. Si se proporcionan menos de 29 argumentos, los demás argumentos se proporcionan como **xltypeMissing**.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

(**LPXLOPER12 xltypeNum** o **xltypeErr**)
  
La suma de los argumentos o #VALUE! Si no hay numéricos en la lista de argumentos proporcionada o en una celda de un intervalo o elemento de una matriz.
  
### <a name="example"></a>Ejemplo

Consulte `\SAMPLES\GENERIC\GENERIC.C` para obtener el código fuente de esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones en la DLL genérica](functions-in-the-generic-dll.md)

