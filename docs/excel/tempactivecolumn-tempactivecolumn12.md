---
title: TempActiveColumn/TempActiveColumn12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveColumn
- TempActiveColumn12
keywords:
- función tempactivecolumn12 [Excel 2007], TempActiveColumn [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d1399a407e3e269b78c7afbde8ff32c126b4b1bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310475"
---
# <a name="tempactivecolumntempactivecolumn12"></a>TempActiveColumn/TempActiveColumn12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Funciones de biblioteca de .NET Framework que crean una**XLOPER12** de **XLOPER**/ temporal que contiene una referencia externa a una columna completa de la hoja activa. 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a>Parameters

 _col_ (**Byte**)
  
Columna a la que se va a hacer referencia. Se basa en cero para que la columna A se pase como 0. En Microsoft Office Excel 2003 y versiones anteriores, y a partir de Excel 2007 ejecutar un libro en modo de compatibilidad, el valor máximo es 255 = 2 ^ 8-1 y es el valor máximo que puede tomar un entero de BYTEs. A partir de Excel 2007, al ejecutar un libro, el valor máximo es 16.383 = 2 ^ 14-1. COL se define como un entero con signo de 32 bits en XLCALL. H.
  
## <a name="return-value"></a>Valor devuelto

Devuelve una referencia externa **xltypeRef** a la columna que se ha pasado. 
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo, se usa **TempActiveColumn12** para seleccionar toda la columna B. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a>Vea también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

