---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- funcsum (función) [excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 0b991cf5cdae90522abc9512193ee556e4c6e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815640"
---
# <a name="funcsum"></a><span data-ttu-id="0b25b-104">FuncSum</span><span class="sxs-lookup"><span data-stu-id="0b25b-104">FuncSum</span></span>

 <span data-ttu-id="0b25b-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0b25b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0b25b-106">Función de hoja de cálculo definida por el usuario de ejemplo que toma argumentos de 1 a 29 y calcula su suma.</span><span class="sxs-lookup"><span data-stu-id="0b25b-106">Example user-defined worksheet function that takes 1 to 29 arguments and computes their sum.</span></span> <span data-ttu-id="0b25b-107">Cada argumento puede ser un número único, un intervalo o una matriz.</span><span class="sxs-lookup"><span data-stu-id="0b25b-107">Each argument can be a single number, a range, or an array.</span></span> <span data-ttu-id="0b25b-108">Cuando se carga GENERIC.xll, registra esta función para que se pueda llamar desde la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="0b25b-108">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span> 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a><span data-ttu-id="0b25b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b25b-109">Parameters</span></span>

 <span data-ttu-id="0b25b-110">_px1 px29_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="0b25b-110">_px1-px29_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="0b25b-111">Punteros a **XLOPER12** argumentos.</span><span class="sxs-lookup"><span data-stu-id="0b25b-111">Pointers to **XLOPER12** arguments.</span></span> <span data-ttu-id="0b25b-112">La función acepta cualquier tipo de tipo de entrada, pero se codifica sólo para funcionar en números, matrices literales de números y los rangos que contengan sólo números o celdas en blanco.</span><span class="sxs-lookup"><span data-stu-id="0b25b-112">The function accepts any kind of input type but is coded only to operate on numbers, literal arrays of numbers, and ranges containing only numbers or blank cells.</span></span> <span data-ttu-id="0b25b-113">Si se proporcionan menos de 29 argumentos, se proporcionan los argumentos restantes como **xltypeMissing**.</span><span class="sxs-lookup"><span data-stu-id="0b25b-113">If fewer than 29 arguments are supplied, the remaining arguments are supplied as **xltypeMissing**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="0b25b-114">Propiedad valor y valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b25b-114">Property value/Return value</span></span>

<span data-ttu-id="0b25b-115">(**LPXLOPER12 xltypeNum** o **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="0b25b-115">(**LPXLOPER12 xltypeNum** or **xltypeErr**)</span></span>
  
<span data-ttu-id="0b25b-116">¡La suma de los argumentos o #VALUE!</span><span class="sxs-lookup"><span data-stu-id="0b25b-116">The sum of the arguments or #VALUE!</span></span> <span data-ttu-id="0b25b-117">Si hay valores no numéricos en la lista de argumento proporcionado o en una celda de un rango o elemento de una matriz.</span><span class="sxs-lookup"><span data-stu-id="0b25b-117">if there are non-numerics in the supplied argument list or in a cell in a range or element in an array.</span></span>
  
### <a name="example"></a><span data-ttu-id="0b25b-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0b25b-118">Example</span></span>

<span data-ttu-id="0b25b-119">Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función.</span><span class="sxs-lookup"><span data-stu-id="0b25b-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b25b-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="0b25b-120">See also</span></span>



[<span data-ttu-id="0b25b-121">Funciones en el archivo DLL genérica</span><span class="sxs-lookup"><span data-stu-id="0b25b-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

