---
title: TempActiveRef/TempActiveRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRef
- TempActiveRef12
keywords:
- Función tempactiveref [excel 2007],Función TempActiveRef12 [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58feee8f43e0f90f710c9e4387684dcb6d173a7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415547"
---
# <a name="tempactivereftempactiveref12"></a>TempActiveRef/TempActiveRef12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de biblioteca de marcos que crea un **XLOPER** /  **XLOPER12** temporal que contiene una referencia externa al bloque rectangular de celdas de la hoja activa. 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a>Parámetros

 _rwFirst_
  
Fila inicial de la referencia.
  
 _rwLast_
  
Fila final de la referencia.
  
Los argumentos de fila se basan en cero para que la fila 1 se pase como 0. En Microsoft Office Excel 2003 y versiones anteriores, y a partir de Excel 2007 ejecutando un libro en modo de compatibilidad, el valor máximo es 65.535 = 2^16 - 1 y es el valor máximo que puede tomar un entero de WORD. A partir de Excel 2007 que ejecuta un libro, el valor máximo es 1.048.575 = 2^20 - 1. RW se define como un entero con signo de 32 bits en XLCALL.H.
  
 _colFirst_
  
Número de columna inicial de la referencia.
  
 _colLast_
  
Número de columna final de la referencia.
  
Los argumentos de columna se basan en cero para que la columna A se pase como 0. En Excel 2003 y versiones anteriores, y a partir de Excel 2007 ejecutando un libro en modo de compatibilidad, el valor máximo es 255 = 2^8 - 1 y es el valor máximo que puede tomar un entero BYTE. A partir de Excel 2007 que ejecuta un libro, el valor máximo es 16.383 = 2^14 - 1. COL se define como un entero con signo de 32 bits en XLCALL.H.
  
## <a name="return-value"></a>Valor devuelto

Devuelve una **referencia externa xltypeRef** al bloque rectangular de celdas pasadas. 
  
## <a name="example"></a>Ejemplo

En este ejemplo se usa **la función TempActiveRef12** para seleccionar las celdas A105:C110. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a>Consulte también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

