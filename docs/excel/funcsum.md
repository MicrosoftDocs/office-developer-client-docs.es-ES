---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- función funcsum [excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14db5812165812161cf7031f75338a981251dfd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406944"
---
# <a name="funcsum"></a><span data-ttu-id="7ed17-104">FuncSum</span><span class="sxs-lookup"><span data-stu-id="7ed17-104">FuncSum</span></span>

 <span data-ttu-id="7ed17-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7ed17-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7ed17-106">Ejemplo de función de hoja de cálculo definida por el usuario que toma de 1 a 29 argumentos y calcula su suma.</span><span class="sxs-lookup"><span data-stu-id="7ed17-106">Example user-defined worksheet function that takes 1 to 29 arguments and computes their sum.</span></span> <span data-ttu-id="7ed17-107">Cada argumento puede ser un número único, un intervalo o una matriz.</span><span class="sxs-lookup"><span data-stu-id="7ed17-107">Each argument can be a single number, a range, or an array.</span></span> <span data-ttu-id="7ed17-108">Cuando se carga GENERIC.xll, registra esta función para que se pueda llamar desde la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="7ed17-108">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span> 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a><span data-ttu-id="7ed17-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ed17-109">Parameters</span></span>

 <span data-ttu-id="7ed17-110">_px1-px29_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="7ed17-110">_px1-px29_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="7ed17-111">Punteros a **argumentos XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="7ed17-111">Pointers to **XLOPER12** arguments.</span></span> <span data-ttu-id="7ed17-112">La función acepta cualquier tipo de entrada, pero solo está codificada para funcionar en números, matrices literales de números y rangos que contengan solo números o celdas en blanco.</span><span class="sxs-lookup"><span data-stu-id="7ed17-112">The function accepts any kind of input type but is coded only to operate on numbers, literal arrays of numbers, and ranges containing only numbers or blank cells.</span></span> <span data-ttu-id="7ed17-113">Si se proporcionan menos de 29 argumentos, los argumentos restantes se proporcionan como **xltypeMissing**.</span><span class="sxs-lookup"><span data-stu-id="7ed17-113">If fewer than 29 arguments are supplied, the remaining arguments are supplied as **xltypeMissing**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="7ed17-114">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ed17-114">Property value/Return value</span></span>

<span data-ttu-id="7ed17-115">(**LPXLOPER12 xltypeNum** o **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="7ed17-115">(**LPXLOPER12 xltypeNum** or **xltypeErr**)</span></span>
  
<span data-ttu-id="7ed17-116">La suma de los argumentos o #VALUE!</span><span class="sxs-lookup"><span data-stu-id="7ed17-116">The sum of the arguments or #VALUE!</span></span> <span data-ttu-id="7ed17-117">si hay valores no numéricos en la lista de argumentos proporcionada o en una celda de un rango o elemento de una matriz.</span><span class="sxs-lookup"><span data-stu-id="7ed17-117">if there are non-numerics in the supplied argument list or in a cell in a range or element in an array.</span></span>
  
### <a name="example"></a><span data-ttu-id="7ed17-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ed17-118">Example</span></span>

<span data-ttu-id="7ed17-119">Vea  `\SAMPLES\GENERIC\GENERIC.C` el código fuente de esta función.</span><span class="sxs-lookup"><span data-stu-id="7ed17-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7ed17-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7ed17-120">See also</span></span>



[<span data-ttu-id="7ed17-121">Funciones en la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="7ed17-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

