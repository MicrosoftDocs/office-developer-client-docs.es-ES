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
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a><span data-ttu-id="dc6ec-104">Evaluar los nombres y otras expresiones de fórmulas de la hoja de cálculo</span><span class="sxs-lookup"><span data-stu-id="dc6ec-104">Evaluating names and other worksheet formula expressions</span></span>

<span data-ttu-id="dc6ec-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="dc6ec-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="dc6ec-106">Una de las características más importantes que Excel expone a través de la API de C es la capacidad de convertir cualquier fórmula de cadena que se pueda introducir legalmente en una hoja de cálculo en un valor o una matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-106">One of the most important features that Excel exposes through the C API is the ability to convert any string formula that can legally be entered into a worksheet to a value, or array of values.</span></span> <span data-ttu-id="dc6ec-107">Esto es esencial para los comandos y funciones XLL que deben leer el contenido de los nombres definidos, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-107">This is essential for XLL functions and commands that must read the contents of defined names, for example.</span></span> <span data-ttu-id="dc6ec-108">Esta capacidad se expone a través de la función [xlfEvaluate,](xlfevaluate.md)como se muestra en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-108">This ability is exposed through the [xlfEvaluate function](xlfevaluate.md), as shown in this example.</span></span>
  
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

<span data-ttu-id="dc6ec-109">Tenga en cuenta que, al evaluar el nombre de una hoja de cálculo, ya sea por sí mismo o en una fórmula, debe usar como prefijo el nombre "!", al menos.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-109">Note that when you are evaluating a worksheet name, either on its own or in a formula, you must prefix the name with '!', at least.</span></span> <span data-ttu-id="dc6ec-110">De lo contrario, Excel intenta encontrar el nombre en un espacio de nombres oculto reservado para dll.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-110">Otherwise, Excel tries to find the name in a hidden namespace reserved for DLLs.</span></span> <span data-ttu-id="dc6ec-111">Puede crear y eliminar nombres dll ocultos mediante la [función xlfSetName](xlfsetname.md).</span><span class="sxs-lookup"><span data-stu-id="dc6ec-111">You can create and delete hidden DLL names using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="dc6ec-112">Puede obtener la definición de cualquier nombre definido, ya sea un nombre DLL oculto o un nombre de hoja de cálculo, mediante la función **xlfGetDef.**</span><span class="sxs-lookup"><span data-stu-id="dc6ec-112">You can get the definition of any defined name, whether it is a hidden DLL name or a worksheet name, using the **xlfGetDef** function.</span></span> 
  
<span data-ttu-id="dc6ec-113">La especificación completa del nombre de una hoja de cálculo tiene la siguiente forma:</span><span class="sxs-lookup"><span data-stu-id="dc6ec-113">The full specification for a worksheet name takes the following form:</span></span>
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
<span data-ttu-id="dc6ec-114">Tenga en cuenta que Excel 2007 introdujo varias extensiones de archivo nuevas.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-114">Note that Excel 2007 introduced a number of new file extensions.</span></span> <span data-ttu-id="dc6ec-115">Puede omitir la ruta de acceso, el nombre del libro y el nombre de la hoja donde no haya ambigüedad entre los libros abiertos en esta sesión de Excel.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-115">You can omit the path, the workbook name, and the sheet name where there is no ambiguity among the open workbooks in this Excel session.</span></span> 
  
<span data-ttu-id="dc6ec-116">En el siguiente ejemplo se evalúa la fórmula de la hoja de cálculo  `COUNT(A1:IV65536)` activa y se muestra el resultado.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-116">The next example evaluates the formula  `COUNT(A1:IV65536)` for the active worksheet and displays the result.</span></span> <span data-ttu-id="dc6ec-117">Tenga en cuenta la necesidad de agregar un prefijo "!" a la dirección del rango, que es coherente con la convención de referencia de rango en las hojas de macros XLM.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-117">Note the need to prefix the range address with '!', which is consistent with the range reference convention on XLM macro sheets.</span></span> <span data-ttu-id="dc6ec-118">El XLM de la API de C sigue esta convención:</span><span class="sxs-lookup"><span data-stu-id="dc6ec-118">The C API XLM follows this convention:</span></span> 
  
- <span data-ttu-id="dc6ec-119">`=A1` Referencia a la celda A1 de la hoja de macros actual.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-119">`=A1` A reference to cell A1 on the current macro sheet.</span></span> <span data-ttu-id="dc6ec-120">(No definido para XLL).</span><span class="sxs-lookup"><span data-stu-id="dc6ec-120">(Not defined for XLLs).</span></span> 
  
- <span data-ttu-id="dc6ec-121">`=!A1` Una referencia a la celda A1 de la hoja activa (que podría ser una hoja de cálculo o una hoja de macros)</span><span class="sxs-lookup"><span data-stu-id="dc6ec-121">`=!A1` A reference to cell A1 on the active sheet (which could be a worksheet or macro sheet)</span></span> 
  
- <span data-ttu-id="dc6ec-122">`=Sheet1!A1` Una referencia a la celda A1 de la hoja especificada, Sheet1 en este caso.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-122">`=Sheet1!A1` A reference to cell A1 on the specified sheet, Sheet1 in this case.</span></span> 
  
- <span data-ttu-id="dc6ec-123">`=[Book1.xls]Sheet1!A1` Referencia a la celda A1 de la hoja especificada del libro especificado.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-123">`=[Book1.xls]Sheet1!A1` A reference to cell A1 on the specified sheet in the specified workbook.</span></span> 
  
<span data-ttu-id="dc6ec-124">En un XLL, una referencia sin un signo de exclamación inicial (**!**) no se puede convertir en un valor.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-124">In an XLL, a reference without a leading exclamation point (**!**) cannot be converted to a value.</span></span> <span data-ttu-id="dc6ec-125">No tiene ningún significado porque no hay ninguna hoja de macros actual.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-125">It has no meaning because there is no current macro sheet.</span></span> <span data-ttu-id="dc6ec-126">Tenga en cuenta que un signo inicial es igual a ( **=** ) es opcional y se omite en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-126">Note that a leading equals sign (**=**) is optional and is omitted in the next example.</span></span>
  
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

<span data-ttu-id="dc6ec-127">También puede usar la función **xlfEvaluate** para recuperar el identificador de registro de una función XLL a partir de su nombre registrado, que se puede usar para llamar a esa función mediante la función [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="dc6ec-127">You can also use the **xlfEvaluate** function to retrieve the registration ID of an XLL function from its registered name, which can then be used to call that function using the [xlUDF function](xludf.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="dc6ec-128">El nombre registrado se puede pasar directamente a la **función xlUDF.**</span><span class="sxs-lookup"><span data-stu-id="dc6ec-128">The registered name can be passed directly to the **xlUDF** function.</span></span> <span data-ttu-id="dc6ec-129">Esto significa que puede evitar tener que evaluar el nombre para obtener el identificador antes de llamar **a xlUDF**.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-129">This means that you can avoid having to evaluate the name to get the ID before calling **xlUDF**.</span></span> <span data-ttu-id="dc6ec-130">Sin embargo, si se va a llamar a la función varias veces, llamarla mediante el identificador de registro es más rápido.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-130">However, if the function is to be called many times, calling it by using the registration ID is faster.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dc6ec-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dc6ec-131">See also</span></span>

- [<span data-ttu-id="dc6ec-132">Evaluación de hojas de cálculo y expresiones de Excel</span><span class="sxs-lookup"><span data-stu-id="dc6ec-132">Excel Worksheet and Expression Evaluation</span></span>](excel-worksheet-and-expression-evaluation.md)
- [<span data-ttu-id="dc6ec-133">Permitir interrupciones de usuarios en operaciones largas</span><span class="sxs-lookup"><span data-stu-id="dc6ec-133">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="dc6ec-134">Introducción al SDK de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="dc6ec-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

