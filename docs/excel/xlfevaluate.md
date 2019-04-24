---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- función xlfevaluate [Excel 2007]
localization_priority: Normal
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 527f7e932a41103c374e327a1bd0dd4c7d8e92a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303930"
---
# <a name="xlfevaluate"></a>xlfEvaluate

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Utiliza el analizador de Microsoft Excel y el evaluador de funciones para evaluar cualquier expresión que se pudiera escribir en una celda de hoja de cálculo.
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a>Parameters

 _pxFormulaText (xltypeStr)_
  
Cadena que se va a evaluar. Un signo igual inicial (=) es opcional. La cadena puede ser cualquier texto que pueda escribirse legalmente en una celda de hoja de cálculo o de hoja de macro.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Devuelve el resultado de evaluar la cadena que puede ser cualquiera de los tipos **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.
  
## <a name="remarks"></a>Comentarios

La cadena solo puede contener funciones, no equivalentes de comando. Equivale a presionar **F9** en la barra de fórmulas. Si se llama a **xlfEvaluate** desde una función de hoja de cálculo XLL que se ha registrado como segura para subprocesos, la expresión solo debe contener funciones seguras para subprocesos. 
  
El uso principal de la función **xlfEvaluate** es permitir a las DLL averiguar el valor asignado a un nombre definido que se encuentra en una hoja o un nombre oculto definido dentro del archivo dll. Tenga en cuenta que dentro de una DLL o XLL, un nombre de hoja de cálculo debe tener como mínimo un signo de exclamación (!) para asegurarse de que se interprete como externo al archivo DLL. Para obtener más información, vea [evaluar nombres y otras expresiones de fórmulas de hoja de cálculo](evaluating-names-and-other-worksheet-formula-expressions.md).
  
 **xlfEvaluate** no se puede usar para evaluar referencias a una hoja externa que no está abierta. 
  
## <a name="example"></a>Ejemplo

En este ejemplo se usa **xlfEvaluate** para convertir el texto "! B38 "para el contenido de la celda B38. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Esta función llama a una macro de comando (**xlcAlert**) y funcionará correctamente sólo cuando se llame desde una hoja de macros o como un comando de macro.
  
```cs
short WINAPI EvaluateExample(void)
{
    XLOPER12 xFormulaText, xRes, xRes2, xInt;
    xFormulaText.xltype = xltypeStr;
    xFormulaText.val.str = L"\004!B38";
    Excel12(xlfEvaluate, &xRes, 1, (LPXLOPER12)&xFormulaText);
    xInt.xltype = xltypeInt;
    xInt.val.w = 2;
    Excel12(xlcAlert, &xRes2, 2, (LPXLOPER12)&xRes, (LPXLOPER12)&xInt);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes2);
    return 1;
}
```

## <a name="see-also"></a>Vea también

- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

