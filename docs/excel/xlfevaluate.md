---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- Función xlfevaluate [excel 2007]
localization_priority: Normal
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 527f7e932a41103c374e327a1bd0dd4c7d8e92a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439187"
---
# <a name="xlfevaluate"></a><span data-ttu-id="5fbf4-104">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="5fbf4-104">xlfEvaluate</span></span>

 <span data-ttu-id="5fbf4-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5fbf4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5fbf4-106">Usa el analizador de Microsoft Excel y el evaluador de funciones para evaluar cualquier expresión que se pueda especificar en una celda de hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="5fbf4-106">Uses the Microsoft Excel parser and function evaluator to evaluate any expression that could be entered in a worksheet cell.</span></span>
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a><span data-ttu-id="5fbf4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5fbf4-107">Parameters</span></span>

 <span data-ttu-id="5fbf4-108">_pxFormulaText (xltypeStr)_</span><span class="sxs-lookup"><span data-stu-id="5fbf4-108">_pxFormulaText (xltypeStr)_</span></span>
  
<span data-ttu-id="5fbf4-109">Cadena que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="5fbf4-109">The string to be evaluated.</span></span> <span data-ttu-id="5fbf4-110">Un signo igual inicial (=) es opcional.</span><span class="sxs-lookup"><span data-stu-id="5fbf4-110">A leading equal sign (=) is optional.</span></span> <span data-ttu-id="5fbf4-111">La cadena puede ser cualquier texto que se pueda introducir legalmente en una hoja de cálculo o una celda de hoja de macros.</span><span class="sxs-lookup"><span data-stu-id="5fbf4-111">The string can be any text that can legally be entered into a worksheet or macro sheet cell.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="5fbf4-112">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5fbf4-112">Property value/Return value</span></span>

<span data-ttu-id="5fbf4-113">Devuelve el resultado de evaluar la cadena que puede ser cualquiera de los tipos **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="5fbf4-113">Returns the result of evaluating the string which can be any of the types **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5fbf4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5fbf4-114">Remarks</span></span>

<span data-ttu-id="5fbf4-115">La cadena solo puede contener funciones, no equivalentes de comandos.</span><span class="sxs-lookup"><span data-stu-id="5fbf4-115">The string can contain only functions, not command equivalents.</span></span> <span data-ttu-id="5fbf4-116">Equivale a presionar **F9** desde la barra de fórmulas.</span><span class="sxs-lookup"><span data-stu-id="5fbf4-116">It is equivalent to pressing **F9** from the formula bar.</span></span> <span data-ttu-id="5fbf4-117">Si **se llama a xlfEvaluate** desde una función de hoja de cálculo XLL que se ha registrado como segura para subprocesos, la expresión solo debe contener funciones seguras para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="5fbf4-117">If **xlfEvaluate** is called from an XLL worksheet function that has been registered as thread safe, the expression must only contain thread-safe functions.</span></span> 
  
<span data-ttu-id="5fbf4-118">El uso principal de la función **xlfEvaluate** es permitir que las DLL descubran el valor asignado a un nombre definido que se encuentra en una hoja o un nombre oculto definido en la DLL.</span><span class="sxs-lookup"><span data-stu-id="5fbf4-118">The primary use of the **xlfEvaluate** function is to allow DLLs to find out the value assigned to a defined name that is either on a sheet or a hidden name defined within the DLL.</span></span> <span data-ttu-id="5fbf4-119">Tenga en cuenta que dentro de un DLL/XLL, un nombre de hoja de cálculo debe ir precedido de al menos un signo de exclamación (!) para asegurarse de que se interpreta como externo a la DLL.</span><span class="sxs-lookup"><span data-stu-id="5fbf4-119">Note that within a DLL/XLL, a worksheet name must be prefixed with at least an exclamation mark (!) to ensure that it is interpreted as external to the DLL.</span></span> <span data-ttu-id="5fbf4-120">Para obtener más información, vea [Evaluación de nombres y otras expresiones de fórmula](evaluating-names-and-other-worksheet-formula-expressions.md)de hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="5fbf4-120">For more information, see [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).</span></span>
  
 <span data-ttu-id="5fbf4-121">**xlfEvaluate** no se puede usar para evaluar referencias a una hoja externa que no está abierta.</span><span class="sxs-lookup"><span data-stu-id="5fbf4-121">**xlfEvaluate** cannot be used to evaluate references to an external sheet that is not open.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5fbf4-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5fbf4-122">Example</span></span>

<span data-ttu-id="5fbf4-123">En este ejemplo **se usa xlfEvaluate** para crear el texto "! B38" al contenido de la celda B38.</span><span class="sxs-lookup"><span data-stu-id="5fbf4-123">This example uses **xlfEvaluate** to coerce the text "!B38" to the contents of cell B38.</span></span> 
  
 <span data-ttu-id="5fbf4-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="5fbf4-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="5fbf4-125">Esta función llama a una macro de comandos (**xlcAlert**) y sólo funcionará correctamente cuando se llame desde una hoja de macros o como un comando de macro.</span><span class="sxs-lookup"><span data-stu-id="5fbf4-125">This function calls a command macro (**xlcAlert**) and will work correctly only when called from a macro sheet or as a macro command.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="5fbf4-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5fbf4-126">See also</span></span>

- [<span data-ttu-id="5fbf4-127">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="5fbf4-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

