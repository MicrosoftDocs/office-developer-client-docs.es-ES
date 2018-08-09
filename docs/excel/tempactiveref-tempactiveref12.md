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
- tempactiveref (función) [excel 2007], TempActiveRef12 (función) [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5c2e82dcaf9bf562048b5d2582ece1bd262b47eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815698"
---
# <a name="tempactivereftempactiveref12"></a>TempActiveRef/TempActiveRef12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de la biblioteca de Framework que crea un temporal **XLOPER**/ **XLOPER12** que contiene una referencia externa a un bloque rectangular de celdas en la hoja activa. 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a>Parámetros

 _rwFirst_
  
La fila inicial de la referencia.
  
 _rwLast_
  
La fila final de la referencia.
  
Argumentos de fila son de base ceros para que esa fila 1 se pasa como 0. En Microsoft Office Excel 2003 y anteriores versiones y a partir de Excel 2007 que se ejecuta un libro en modo de compatibilidad, el valor máximo es 65.535 = 2 ^ 16-1 y es el valor máximo que puede consultarse por un número entero de WORD. A partir de que ejecuta un libro de Excel 2007, el valor máximo es 1.048.575 = 2 ^ 1 a 20. RW se define como un entero con signo de 32 bits en XLCALL. H.
  
 _colFirst_
  
El número de columna inicial de la referencia.
  
 _colLast_
  
El número de columna final de la referencia.
  
Argumentos de la columna son de base ceros para que esa columna A se pasa como 0. En Excel 2003 y anteriores versiones y a partir de Excel 2007 que se ejecuta un libro en modo de compatibilidad, el valor máximo es 255 = 2 ^ 8-1 y es el valor máximo que se puede adoptar un entero de BYTE. A partir de que ejecuta un libro de Excel 2007, el valor máximo es 16.383 = 2 ^ 14-1. COL se define como un entero con signo de 32 bits en XLCALL. H.
  
## <a name="return-value"></a>Valor devuelto

Devuelve una referencia externa de **xltypeRef** a un bloque rectangular de celdas que se pasó. 
  
## <a name="example"></a>Ejemplo

En este ejemplo se usa la función **TempActiveRef12** para seleccionar las celdas A105:C110. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a>Vea también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

