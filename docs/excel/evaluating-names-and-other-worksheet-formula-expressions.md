---
title: Evaluar los nombres y otras expresiones de fórmulas de la hoja de cálculo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- evaluación de expresiones [Excel 2007], hojas de cálculo [Excel 2007], evaluación de nombres, evaluación de expresiones [Excel 2007], evaluación de nombres de hojas de cálculo [Excel 2007], expresiones [Excel 2007], evaluación, nombres [Excel 2007], evaluación, evaluación de nombres [Excel 2007] , cadenas [Excel 2007], convertir a valores, función xlfEvaluate [Excel 2007], hojas de cálculo [Excel 2007], evaluación de expresión
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
  
Una de las características más importantes que Excel expone mediante la API de C es la capacidad para convertir cualquier fórmula de cadena que pueda especificarse legalmente en una hoja de cálculo a un valor o una matriz de valores. Esto es esencial para las funciones y los comandos XLL que deben leer el contenido de los nombres definidos, por ejemplo. Esta capacidad se expone a través de la [función xlfEvaluate](xlfevaluate.md), como se muestra en este ejemplo.
  
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

Tenga en cuenta que al evaluar el nombre de una hoja de cálculo, ya sea por sí mismo o en una fórmula, debe anteponer "!" al nombre. De lo contrario, Excel intenta buscar el nombre en un espacio de nombres oculto reservado para dll. Puede crear y eliminar nombres de DLL ocultos mediante la [función xlfSetName](xlfsetname.md). Puede obtener la definición de cualquier nombre definido, ya sea un nombre de DLL oculto o un nombre de hoja de cálculo, mediante la función **xlfGetDef** . 
  
La especificación completa de un nombre de hoja de cálculo tiene el siguiente formato:
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
Tenga en cuenta que Excel 2007 ha incluido una serie de nuevas extensiones de archivo. Puede omitir la ruta de acceso, el nombre del libro y el nombre de la hoja donde no hay ninguna ambigüedad entre los libros abiertos en esta sesión de Excel. 
  
En el siguiente ejemplo se evalúa la `COUNT(A1:IV65536)` fórmula de la hoja de cálculo activa y se muestra el resultado. Tenga en cuenta la necesidad de anteponer '! ' a la dirección del rango, lo que es coherente con la Convención de referencia del rango en las hojas de macros XLM. La API de C XLM sigue esta Convención: 
  
- `=A1`Una referencia a la celda a1 en la hoja de macros actual. (No se define para XLL). 
  
- `=!A1`Una referencia a la celda a1 en la hoja activa (que puede ser una hoja de cálculo o una hoja de macro) 
  
- `=Sheet1!A1`Una referencia a la celda a1 en la hoja especificada, Sheet1 en este caso. 
  
- `=[Book1.xls]Sheet1!A1`Referencia a la celda a1 de la hoja especificada en el libro especificado. 
  
En un XLL, una referencia sin un signo de exclamación inicial (**!**) no se puede convertir en un valor. No tiene significado porque no hay ninguna hoja de macros activa. Tenga en cuenta que el signo igual (**=**) inicial es opcional y se omite en el ejemplo siguiente.
  
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

También puede usar la función **xlfEvaluate** para recuperar el identificador de registro de una función XLL a partir de su nombre registrado, que se puede usar para llamar a esa función mediante la [función xlUDF](xludf.md).
  
> [!NOTE]
> El nombre registrado se puede pasar directamente a la función **xlUDF** . Esto significa que puede evitar tener que evaluar el nombre para obtener el identificador antes de llamar a **xlUDF**. Sin embargo, si se va a llamar a la función muchas veces, llamar a ella con el identificador de registro es más rápido. 
  
## <a name="see-also"></a>Ver también

- [Evaluación de hojas de cálculo y expresiones de Excel](excel-worksheet-and-expression-evaluation.md)
- [Permitir interrupciones de usuarios en operaciones largas](permitting-user-breaks-in-lengthy-operations.md)
- [Introducción al SDK de XLL de Excel](getting-started-with-the-excel-xll-sdk.md)

