---
title: TempActiveCell/TempActiveCell12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveCell
- TempActiveCell12
keywords:
- función tempactivecell12 [excel 2007],Función TempActiveCell [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f9bdb4cd9919d0e52654a3996ede99c4d1b35cc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413195"
---
# <a name="tempactivecelltempactivecell12"></a>TempActiveCell/TempActiveCell12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Funciones de biblioteca de marcos que crean un **XLOPER** /  **XLOPER12** temporal que contiene una referencia externa a una celda de la hoja activa. 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a>Parámetros

 _row_
  
Fila a la que se va a hacer referencia. Los argumentos de fila se basan en cero para que la fila 1 se pase como 0. En Microsoft Office Excel 2003 y versiones anteriores, y a partir de Excel 2007 ejecutando un libro en modo de compatibilidad, el valor máximo es 65.535 = 2^16 - 1 y es el valor máximo que puede tomar un entero de WORD. A partir de Excel 2007 que ejecuta un libro, el valor máximo es 1.048.575 = 2^20 - 1. RW se define como un entero con signo de 32 bits en XLCALL.H.
  
 _col_
  
Columna a la que se va a hacer referencia. Esto es de base cero para que la columna A se pase como 0. En Excel 2003 y versiones anteriores, y a partir de Excel 2007 ejecutando un libro en modo de compatibilidad, el valor máximo es 255 = 2^8 - 1 y es el valor máximo que puede tomar un entero BYTE. A partir de Excel 2007 que ejecuta un libro, el valor máximo es 16.383 = 2^14 - 1. COL se define como un entero con signo de 32 bits en XLCALL.H.
  
## <a name="return-value"></a>Valor devuelto

Devuelve una **referencia externa xltypeRef** a la celda pasada. 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se **usa TempActiveCell12 para** mostrar el contenido de B94 en la hoja activa. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a>Consulte también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

