---
title: TempNum/TempNum12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempNum
- TempNum12
keywords:
- función tempnum12 [excel 2007],Función TempNum [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cabd44ab828a2cfe22253e9aaf12abf7b7709d69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426635"
---
# <a name="tempnumtempnum12"></a>TempNum/TempNum12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de biblioteca de marcos que crea un **XLOPER** /  **XLOPER12** temporal que contiene un número de hoja de cálculo de Microsoft Excel (doble IEEE de 8 bytes). 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a>Parámetros

 _d_ (**double**)
  
El valor previsto. Tenga en cuenta que los números sub normales ieee no se admiten actualmente y se redondea a cero. Se admite el infinito negativo.
  
## <a name="return-value"></a>Valor devuelto

Devuelve un **xltypeNum numérico** que contiene el valor pasado o cero si el valor pasado era sub normal. 
  
## <a name="example"></a>Ejemplo

En este ejemplo se **usa la función TempNum12** para pasar un argumento a **xlfGetWorkspace**.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempNumExample(void)
{
   XLOPER12 xRes;
   Excel12f(xlfGetWorkspace, &xRes, 1, TempNum12(44));
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Consulte también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

