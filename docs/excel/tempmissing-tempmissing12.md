---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- tempmissing (función) [excel 2007], TempMissing12 (función) [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a6db2e1f2917ecd9361043577f4bf203b3267a5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815707"
---
# <a name="tempmissingtempmissing12"></a>TempMissing/TempMissing12

 **Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de la biblioteca de Framework que crea un temporal **XLOPER**/ **XLOPER12** de tipo **xltypeMissing**.
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a>Sintaxis

Esta función no toma ningún parámetro.
  
## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a un **xltypeMissing** **XLOPER**/ **XLOPER12**.
  
## <a name="example"></a>Ejemplo

En este ejemplo se utiliza **TempMissing12** para proporcionar tres argumentos que faltan a **xlcWorkspace** seguido de un **valor Boolean** **FALSE** para suprimir la presentación de las barras de desplazamiento de hoja de cálculo. Los tres primeros argumentos corresponden a otras opciones de área de trabajo que no se ven afectados. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a>Ver también



[Funciones de la biblioteca de Framework](functions-in-the-framework-library.md)

