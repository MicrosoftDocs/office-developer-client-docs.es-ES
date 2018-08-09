---
title: Evaluación de nombres y otras expresiones de fórmula de la hoja de cálculo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- evaluación de la expresión [excel 2007], hojas de cálculo [Excel 2007], evaluación de nombre, la evaluación de expresiones [Excel 2007], evaluar los nombres de hoja de cálculo [Excel 2007], expresiones [Excel 2007], evaluar, nombres [Excel 2007], evaluar, nombre evaluación [Excel 2007] , cadenas [Excel 2007], convertir en valores, xlfEvaluate (función) [Excel 2007], hojas de cálculo [Excel 2007], la evaluación de expresiones
localization_priority: Normal
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9d726d89c859e2f7428b459971d5d13586f144e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815550"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a>Evaluación de nombres y otras expresiones de fórmula de la hoja de cálculo

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Una de las características más importantes que Excel se expone a través de la API C es la capacidad para convertir cualquier fórmula de cadena que legalmente puede especificarse en una hoja de cálculo a un valor o matriz de valores. Esto es esencial para funciones XLL y los comandos que se deben leer el contenido de nombres definidos, por ejemplo. Esta capacidad se expone a través de la [función xlfEvaluate](xlfevaluate.md), tal como se muestra en este ejemplo.
  
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

Tenga en cuenta que, al evaluar a un nombre de hoja de cálculo, en su propio o en una fórmula, debe anteponer el nombre con '!', al menos. De lo contrario, Excel intenta encontrar el nombre en un espacio de nombres oculto reservado para archivos DLL. Puede crear y eliminar los nombres de archivo DLL ocultos mediante la [función xlfSetName](xlfsetname.md). Para obtener la definición de cualquier nombre definido, ya sea un nombre de archivo DLL oculto o un nombre de hoja de cálculo, mediante la función **xlfGetDef** . 
  
La especificación completa de un nombre de hoja de cálculo tiene el siguiente formato:
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
Tenga en cuenta que Excel 2007 introdujo a un número de nuevas extensiones de archivo. Puede omitir la ruta de acceso, el nombre del libro y el nombre de la hoja donde no hay ninguna ambigüedad entre los libros abiertos en esta sesión de Excel. 
  
En el ejemplo siguiente se evalúa la fórmula `COUNT(A1:IV65536)` para la hoja de cálculo activa y muestra el resultado. Tenga en cuenta la necesidad de prefijo de la dirección del rango con '!', que es coherente con la convención de referencia de rango en hojas de macro XLM. El XLM de API de C sigue esta convención: 
  
- `=A1`Una referencia a la celda A1 de la hoja de macros actual. (No definidos para XLL). 
  
- `=!A1`Una referencia a la celda A1 de la hoja activa (que puede ser una hoja de cálculo u hoja de macro) 
  
- `=Sheet1!A1`Una referencia a la celda A1 de la hoja especificada, Sheet1 en este caso. 
  
- `=[Book1.xls]Sheet1!A1`Una referencia a la celda A1 de la hoja especificada en el libro especificado. 
  
En un XLL, una referencia sin un punto de exclamación a la izquierda (**!**) no se puede convertir en un valor. No tiene ningún significado porque no hay ninguna hoja de macro actual. Tenga en cuenta que líderes en un signo igual (**=**) es opcional y se omite en el ejemplo siguiente.
  
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

También puede usar la función **xlfEvaluate** para recuperar el identificador de registro de una función XLL desde su nombre registrado, que, a continuación, se puede utilizar para llamar a esa función mediante la [función xlUDF](xludf.md).
  
> [!NOTE]
> El nombre registrado se puede pasar directamente a la función **xlUDF** . Esto significa que se puede evitar tener que volver a evaluar el nombre para obtener el identificador antes de llamar a **xlUDF**. Sin embargo, si la función que se va a llamar tantas veces, llamar a él mediante el registro del que identificador es más rápido. 
  
## <a name="see-also"></a>Vea también

- [Evaluación de expresiones y hojas de cálculo de Excel](excel-worksheet-and-expression-evaluation.md)
- [Permitir interrupciones de usuarios en operaciones largas](permitting-user-breaks-in-lengthy-operations.md)
- [Introducción al SDK de XLL de Excel](getting-started-with-the-excel-xll-sdk.md)

