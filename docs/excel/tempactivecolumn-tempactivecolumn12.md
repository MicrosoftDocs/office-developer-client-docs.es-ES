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
- función tempactivecolumn12 [excel 2007], función TempActiveColumn [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d1399a407e3e269b78c7afbde8ff32c126b4b1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417878"
---
# <a name="tempactivecolumntempactivecolumn12"></a>TempActiveColumn/TempActiveColumn12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Funciones de biblioteca de marcos que crean un /  **XLOPER XLOPER12** temporal que contiene una referencia externa a toda una columna de la hoja activa. 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a>Parameters

 _col_ (**BYTE**)
  
Columna a la que se debe hacer referencia. Se trata de una base cero para que la columna A se pase como 0. En Microsoft Office Excel 2003 y versiones anteriores, y a partir de Excel 2007 ejecutando un libro en modo de compatibilidad, el valor máximo es 255 = 2^8 - 1 y es el valor máximo que puede tomar un entero BYTE. A partir Excel 2007 que ejecuta un libro, el valor máximo es 16.383 = 2^14 - 1. COL se define como un entero con signo de 32 bits en XLCALL.H.
  
## <a name="return-value"></a>Valor devuelto

Devuelve una **referencia externa xltypeRef** a la columna pasada. 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se **usa TempActiveColumn12 para** seleccionar toda la columna B. 
  
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

