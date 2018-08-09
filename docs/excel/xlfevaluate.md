---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- xlfevaluate (función) [excel 2007]
localization_priority: Normal
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e468dc18b8f78f56acaa67c2f23dd53254088ad0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815724"
---
# <a name="xlfevaluate"></a>xlfEvaluate

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Utiliza el analizador de Microsoft Excel y el evaluador de función para evaluar cualquier expresión que se puede insertar en una celda de hoja de cálculo.
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a>Parámetros

 _pxFormulaText (xltypeStr)_
  
La cadena que se va a evaluar. Un signo de igual (=) a la izquierda es opcional. La cadena puede ser cualquier texto que se puede escribir en una celda de hoja de hoja de cálculo o macro legalmente.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Devuelve el resultado de la evaluación de la cadena que puede ser cualquiera de los tipos **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.
  
## <a name="remarks"></a>Comentarios

La cadena puede contener únicamente las funciones, no comandos equivalentes. Es equivalente a presionar la tecla **F9** desde la barra de fórmulas. Si se llama a **xlfEvaluate** desde una función de hoja de cálculo XLL que se ha registrado como seguros para subprocesos, la expresión sólo debe contener las funciones de subprocesos. 
  
El uso principal de la función **xlfEvaluate** es permitir que los archivos DLL averiguar el valor asignado a un nombre definido que está en una hoja o un nombre oculto definidos en el archivo DLL. Tenga en cuenta que dentro de una DLL o XLL, un nombre de hoja de cálculo debe ir precedido con al menos un signo de exclamación (!) para asegurarse de que se interpreta como externa a la DLL. Para obtener más información, vea [los nombres de evaluación y otras expresiones de fórmula de hoja de cálculo](evaluating-names-and-other-worksheet-formula-expressions.md).
  
 **xlfEvaluate** no se puede usar para evaluar las referencias a una hoja de externa que no está abierto. 
  
## <a name="example"></a>Ejemplo

En este ejemplo se utiliza **xlfEvaluate** para convertir el texto "! B38 "para el contenido de la celda B38. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Esta función llama a una macro de comando (**xlcAlert**) y funcionará correctamente sólo cuando se llama a partir de una hoja de macros o como un comando de macro.
  
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

