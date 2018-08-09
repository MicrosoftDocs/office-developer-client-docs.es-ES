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
- tempbool (función) [excel 2007], TempBool12 (función) [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 30874e7b918d8cd780bef60b4b02de1319f0f9ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815700"
---
# <a name="tempbooltempbool12"></a>TempBool/TempBool12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de la biblioteca de Framework que crea un temporal **XLOPER**/ **XLOPER12** que contiene **Boolean** **es TRUE** o **FALSE**.
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a>Parámetros

 _b_ (**int**)
  
Use 0 para devolver **FALSE**; Use cualquier otro valor para devolver **TRUE**.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Devuelve un **Boolean** que contiene el valor lógico que se pasó **xltypeBool** . 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se usa la función **TempBool12** para borrar la barra de estado. Cuando se llama a la función de [Excel/Excel12f](excel-excel12f.md) , se libera memoria temporal. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a>Vea también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

