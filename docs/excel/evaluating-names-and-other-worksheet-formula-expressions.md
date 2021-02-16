---
title: Evaluar los nombres y otras expresiones de fórmulas de la hoja de cálculo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- expression evaluation [excel 2007],worksheets [Excel 2007], name evaluation,evaluating expressions [Excel 2007],assessing worksheet names [Excel 2007],expressions [Excel 2007], evaluating,names [Excel 2007], evaluating,name evaluation [Excel 2007],strings [Excel 2007], converting to values,xlfEvaluate function [Excel 2007],worksheets [Excel 2007], expression evaluation
localization_priority: Normal
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97328cbc57a9144a133524774e3be10a84a96bf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406867"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a>Evaluar los nombres y otras expresiones de fórmulas de la hoja de cálculo

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Una de las características más importantes que Excel expone a través de la API de C es la capacidad de convertir cualquier fórmula de cadena que se pueda introducir legalmente en una hoja de cálculo en un valor o una matriz de valores. Esto es esencial para los comandos y funciones XLL que deben leer el contenido de los nombres definidos, por ejemplo. Esta capacidad se expone a través de la función [xlfEvaluate,](xlfevaluate.md)como se muestra en este ejemplo.
  
```C
int WINAPI evaluate_name_example(void)
{
  wchar_t *expression = L"\016!MyDefinedName";
  XLOPER12 xNameText, xNameValue;
  xNameText.xltype = xltypeStr;
  xNameText.val.str = expression;
// Try to evaluate the name. Will fail with a #NAME? error
// if MyDefinedName is not defined in the active workbook.
  Excel12(xlfEvaluate, &xNameValue, 1, &xNameText);
// Attempt to convert the value to a string and display it in
// an alert dialog. This fails if xNameValue is an error value.
  Excel12(xlcAlert, 0, 1, &xNameValue);
// Must free xNameValue in case MyDefinedName evaluated to a string
  Excel12(xlFree, 0, 1, &xNameValue);
  return 1;
}
```

Tenga en cuenta que, al evaluar el nombre de una hoja de cálculo, ya sea por sí mismo o en una fórmula, debe usar como prefijo el nombre "!", al menos. De lo contrario, Excel intenta encontrar el nombre en un espacio de nombres oculto reservado para dll. Puede crear y eliminar nombres dll ocultos mediante la [función xlfSetName](xlfsetname.md). Puede obtener la definición de cualquier nombre definido, ya sea un nombre DLL oculto o un nombre de hoja de cálculo, mediante la función **xlfGetDef.** 
  
La especificación completa del nombre de una hoja de cálculo tiene la siguiente forma:
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
Tenga en cuenta que Excel 2007 introdujo varias extensiones de archivo nuevas. Puede omitir la ruta de acceso, el nombre del libro y el nombre de la hoja donde no haya ambigüedad entre los libros abiertos en esta sesión de Excel. 
  
En el siguiente ejemplo se evalúa la fórmula de la hoja de cálculo  `COUNT(A1:IV65536)` activa y se muestra el resultado. Tenga en cuenta la necesidad de agregar un prefijo "!" a la dirección del rango, que es coherente con la convención de referencia de rango en las hojas de macros XLM. El XLM de la API de C sigue esta convención: 
  
- `=A1` Referencia a la celda A1 de la hoja de macros actual. (No definido para XLL). 
  
- `=!A1` Una referencia a la celda A1 de la hoja activa (que podría ser una hoja de cálculo o una hoja de macros) 
  
- `=Sheet1!A1` Una referencia a la celda A1 de la hoja especificada, Sheet1 en este caso. 
  
- `=[Book1.xls]Sheet1!A1` Referencia a la celda A1 de la hoja especificada del libro especificado. 
  
En un XLL, una referencia sin un signo de exclamación inicial (**!**) no se puede convertir en un valor. No tiene ningún significado porque no hay ninguna hoja de macros actual. Tenga en cuenta que un signo inicial es igual a ( **=** ) es opcional y se omite en el siguiente ejemplo.
  
```C
int WINAPI evaluate_expression_example(void)
{
    wchar_t *expression = L"\022COUNT(!A1:IV65536)";
    XLOPER12 xExprText, xExprValue;
    xExprText.xltype = xltypeStr;
    xExprText.val.str = expression;
// Try to evaluate the formula.
    Excel12(xlfEvaluate, &xExprValue, 1, &xExprText);
// Attempt to convert the value to a string and display it in
// an alert dialog. Will fail if xExprValue is an error.
    Excel12(xlcAlert, 0, 1, &xExprValue);
// Not strictly necessary, as COUNT never returns a string
// but does no harm.
    Excel12(xlFree, 0, 1, &xExprValue);
    return 1;
}
```

También puede usar la función **xlfEvaluate** para recuperar el identificador de registro de una función XLL a partir de su nombre registrado, que se puede usar para llamar a esa función mediante la función [xlUDF](xludf.md).
  
> [!NOTE]
> El nombre registrado se puede pasar directamente a la **función xlUDF.** Esto significa que puede evitar tener que evaluar el nombre para obtener el identificador antes de llamar **a xlUDF**. Sin embargo, si se va a llamar a la función varias veces, llamarla mediante el identificador de registro es más rápido. 
  
## <a name="see-also"></a>Consulte también

- [Evaluación de hojas de cálculo y expresiones de Excel](excel-worksheet-and-expression-evaluation.md)
- [Permitir interrupciones de usuarios en operaciones largas](permitting-user-breaks-in-lengthy-operations.md)
- [Introducción al SDK de XLL de Excel](getting-started-with-the-excel-xll-sdk.md)

