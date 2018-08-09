---
title: TempInt/TempInt12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempInt
- TempInt12
keywords:
- tempint12 (función) [excel 2007], TempInt (función) [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: eb1dd9be0c0b20e533d9cd8202f8878c43b997be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815706"
---
# <a name="tempinttempint12"></a>TempInt/TempInt12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de la biblioteca de Framework que crea un temporal **XLOPER**/ **XLOPER12** que contiene un número entero. 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a>Parámetros

 _i_
  
El valor entero previsto. Tenga en cuenta que el entero **XLOPER** es un entero de 16 bits (short int), mientras que el entero **XLOPER12** es un entero de 32 bits con signo (int [largo]). 
  
## <a name="return-value"></a>Valor devuelto

Devuelve un entero **xltypeInt** que contiene el valor que se pasó. 
  
## <a name="example"></a>Ejemplo

En este ejemplo se usa la función **TempInt12** para pasar un argumento a **xlfGetWorkspace**.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempIntExample(void)
{
    XLOPER12 xRes;
    Excel12f(xlfGetWorkspace, (LPXLOPER12)&xRes, 1, TempInt12(44));
    Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a>Vea también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

