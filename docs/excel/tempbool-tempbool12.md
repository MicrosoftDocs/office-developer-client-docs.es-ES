---
title: TempBool/TempBool12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempBool
- TempBool12
keywords:
- función tempbool [excel 2007],Función TempBool12 [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c8c917f0004fe091413ea670f1cc562f1d701fa0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433720"
---
# <a name="tempbooltempbool12"></a>TempBool/TempBool12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de biblioteca de marcos que crea un **XLOPER** /  **XLOPER12** temporal que **contiene Boolean** **TRUE** o **FALSE**.
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a>Parámetros

 _b_ (**int**)
  
Use 0 para devolver **FALSE**; use cualquier otro valor para devolver **TRUE**.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Devuelve un **valor booleano xltypeBool** **que** contiene el valor lógico pasado. 
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo se usa **la función TempBool12** para borrar la barra de estado. La memoria temporal se libera cuando se llama a la función [Excel/Excel12f.](excel-excel12f.md) 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a>Consulte también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

