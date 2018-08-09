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
- tempactivecell12 (función) [excel 2007], TempActiveCell (función) [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8ad409a76195d67fa61e7991ce6527c40e0a3265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815695"
---
# <a name="tempactivecelltempactivecell12"></a>TempActiveCell/TempActiveCell12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Funciones de la biblioteca de Framework que creación un temporal **XLOPER**/ **XLOPER12** que contiene una referencia externa a una celda de la hoja activa. 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a>Parámetros

 _row_
  
Para hacer referencia a la fila. Argumentos de fila son de base ceros para que esa fila 1 se pasa como 0. En Microsoft Office Excel 2003 y anteriores versiones y a partir de Excel 2007 que se ejecuta un libro en modo de compatibilidad, el valor máximo es 65.535 = 2 ^ 16-1 y es el valor máximo que puede consultarse por un número entero de WORD. A partir de que ejecuta un libro de Excel 2007, el valor máximo es 1.048.575 = 2 ^ 1 a 20. RW se define como un entero con signo de 32 bits en XLCALL. H.
  
 _Col_
  
Para hacer referencia a la columna. Esto es basado en cero, por lo que una columna se pasa como 0. En Excel 2003 y anteriores versiones y a partir de Excel 2007 que se ejecuta un libro en modo de compatibilidad, el valor máximo es 255 = 2 ^ 8-1 y es el valor máximo que se puede adoptar un entero de BYTE. A partir de que ejecuta un libro de Excel 2007, el valor máximo es 16.383 = 2 ^ 14-1. COL se define como un entero con signo de 32 bits en XLCALL. H.
  
## <a name="return-value"></a>Valor devuelto

Devuelve una referencia externa de **xltypeRef** a la celda que se pasó. 
  
## <a name="example"></a>Ejemplo

El siguiente ejemplo utiliza **TempActiveCell12** para mostrar el contenido de B94 en la hoja activa. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a>Vea también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

