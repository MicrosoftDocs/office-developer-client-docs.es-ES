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
- función tempmissing [Excel 2007], TempMissing12 [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 37c127b2252f18643b34dfc72fd9929885a68d01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310496"
---
# <a name="tempmissingtempmissing12"></a>TempMissing/TempMissing12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de biblioteca de Framework que crea un**XLOPER12** de **XLOPER**/ temporal de tipo **xltypeMissing**.
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a>Parameters

Esta función no toma ningún parámetro.
  
## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a un **** ****/ **XLOPER12**XLOPER de xltypeMissing.
  
## <a name="example"></a>Ejemplo

En este ejemplo se usa **TempMissing12** para proporcionar tres argumentos que faltan a **xlcWorkspace** seguidos de un **valor booleano** de **false** para suprimir la presentación de las barras de desplazamiento de la hoja de cálculo. Los tres primeros argumentos corresponden a otras opciones de configuración del área de trabajo que no se ven afectadas. 
  
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

## <a name="see-also"></a>Vea también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

