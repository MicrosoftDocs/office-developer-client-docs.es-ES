---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- Función xludf [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 569334847c7612b86f6ddc967f159e2ef425cbbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430647"
---
# <a name="xludf"></a><span data-ttu-id="99341-104">xlUDF</span><span class="sxs-lookup"><span data-stu-id="99341-104">xlUDF</span></span>

<span data-ttu-id="99341-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="99341-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="99341-106">Llama a una función definida por el usuario (UDF).</span><span class="sxs-lookup"><span data-stu-id="99341-106">Calls a user-defined function (UDF).</span></span> <span data-ttu-id="99341-107">Esta función permite a un DLL llamar a Visual Basic para Aplicaciones (VBA) definidas por el usuario, funciones de lenguaje de macros XLM y funciones registradas contenidas en otros complementos.</span><span class="sxs-lookup"><span data-stu-id="99341-107">This function allows a DLL to call Visual Basic for Applications (VBA) user-defined functions, XLM macro language functions, and registered functions contained in other add-ins.</span></span>
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a><span data-ttu-id="99341-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99341-108">Parameters</span></span>

<span data-ttu-id="99341-109">_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** o **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="99341-109">_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="99341-110">Referencia de la función a la que desea llamar.</span><span class="sxs-lookup"><span data-stu-id="99341-110">The reference of the function you want to call.</span></span> <span data-ttu-id="99341-111">Puede ser una referencia de celda de hoja de macros, el nombre registrado de la función como una cadena o el identificador de registro de la función.</span><span class="sxs-lookup"><span data-stu-id="99341-111">This can be a macro sheet cell reference, the registered name of the function as a string, or the register ID of the function.</span></span> <span data-ttu-id="99341-112">Para las funciones de complemento XLL registradas mediante **xlfRegister** o **REGISTER** con el argumento  _pxFunctionText_ proporcionado, el identificador se puede obtener mediante **xlfEvaluate** para buscar el nombre.</span><span class="sxs-lookup"><span data-stu-id="99341-112">For XLL add-in functions registered using **xlfRegister** or **REGISTER** with the argument  _pxFunctionText_ supplied, the ID can be obtained by using **xlfEvaluate** to look up the name.</span></span> 
  
<span data-ttu-id="99341-113">_pxArg1, ..._</span><span class="sxs-lookup"><span data-stu-id="99341-113">_pxArg1, ..._</span></span>
  
<span data-ttu-id="99341-114">Cero o más argumentos para la función definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="99341-114">Zero or more arguments to the user-defined function.</span></span> <span data-ttu-id="99341-115">Cuando se llama a esta función en versiones anteriores a Excel 2007, el número máximo de argumentos adicionales que se pueden pasar es 29, que es 30, incluido  _pxFnRef_.</span><span class="sxs-lookup"><span data-stu-id="99341-115">When you are calling this function in versions earlier than Excel 2007, the maximum number of additional arguments that can be passed is 29, which is 30 including  _pxFnRef_.</span></span> <span data-ttu-id="99341-116">A partir de Excel 2007, este límite se eleva a 254, que es 255, incluido  _pxFnRef_.</span><span class="sxs-lookup"><span data-stu-id="99341-116">Starting in Excel 2007, this limit is raised to 254, which is 255 including  _pxFnRef_.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="99341-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99341-117">Return value</span></span>

<span data-ttu-id="99341-118">Devuelve el valor que devuelva la función definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="99341-118">Returns whatever value the user-defined function returned.</span></span>
  
## <a name="example"></a><span data-ttu-id="99341-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="99341-119">Example</span></span>

<span data-ttu-id="99341-120">En el siguiente ejemplo se **ejecuta TestMacro** en la hoja Macro1 de BOOK1.XLS.</span><span class="sxs-lookup"><span data-stu-id="99341-120">The following example runs **TestMacro** on sheet Macro1 in BOOK1.XLS.</span></span> <span data-ttu-id="99341-121">Asegúrese de que la macro se encuentra en una hoja denominada Macro1.</span><span class="sxs-lookup"><span data-stu-id="99341-121">Make sure that the macro is on a sheet named Macro1.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlUDFExample(void)
{       
   XLOPER12 xMacroName, xMacroRef, xRes;
   xMacroName.xltype = xltypeStr;
   xMacroName.val.str = L"\044[BOOK1.XLSX]Macro1!TestMacro";
   Excel12(xlfEvaluate, &xMacroRef, 1, (LPXLOPER12)&xMacroName);
   Excel12(xlUDF, &xRes, 1, (LPXLOPER12)&xMacroRef);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="99341-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="99341-122">See also</span></span>

- [<span data-ttu-id="99341-123">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="99341-123">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

