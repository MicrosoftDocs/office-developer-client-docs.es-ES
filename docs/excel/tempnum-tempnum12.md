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
- tempnum12 (función) [excel 2007], TempNum (función) [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5ebe58dba32c2cf0382bf0811713eaa0a5471dda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815703"
---
# <a name="tempnumtempnum12"></a>TempNum/TempNum12

 **Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de la biblioteca de Framework que crea un temporal **XLOPER**/ **XLOPER12** que contiene un número de hoja de cálculo de Microsoft Excel (un doble de 8 bytes IEEE). 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a>Sintaxis

 _d._ (**doble**)
  
El valor deseado. Tenga en cuenta que los números de subcaracterísticas normales de IEEE actualmente no son compatibles y se redondean a cero. Se admite el infinito negativo.
  
## <a name="return-value"></a>Valor devuelto

Devuelve un numéricos **xltypeNum** que contiene el valor que se pasó o cero si el valor pasado fue subcaracterísticas normal. 
  
## <a name="example"></a>Ejemplo

En este ejemplo se usa la función **TempNum12** para pasar un argumento a **xlfGetWorkspace**.
  
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

## <a name="see-also"></a>Ver también



[Funciones de la biblioteca de Framework](functions-in-the-framework-library.md)

