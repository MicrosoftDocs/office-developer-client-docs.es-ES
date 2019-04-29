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
- función tempint12 [Excel 2007], TempInt [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 16a2222dbc51ad9480dbd5941ca2ed13f65b55e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438753"
---
# <a name="tempinttempint12"></a>TempInt/TempInt12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de biblioteca de Framework que crea un **XLOPER XLOPER**/ **** temporal que contiene un entero. 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a>Parameters

 _k_
  
Valor entero que se va a usar. Tenga en cuenta que el entero **XLOPER** es un entero de 16 bits con signo (Short int), mientras que el entero de **XLOPER12** es un entero de 32 bits firmado ([Long] int). 
  
## <a name="return-value"></a>Valor devuelto

Devuelve un entero **xltypeInt** que contiene el valor que se ha pasado. 
  
## <a name="example"></a>Ejemplo

En este ejemplo, se usa la función **TempInt12** para pasar un argumento a **xlfGetWorkspace**.
  
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

## <a name="see-also"></a>Ver también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

