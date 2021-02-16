---
title: TempNum/TempNum12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempNum
- TempNum12
keywords:
- función tempnum12 [excel 2007],Función TempNum [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cabd44ab828a2cfe22253e9aaf12abf7b7709d69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426635"
---
# <a name="tempnumtempnum12"></a><span data-ttu-id="a15cf-104">TempNum/TempNum12</span><span class="sxs-lookup"><span data-stu-id="a15cf-104">TempNum/TempNum12</span></span>

 <span data-ttu-id="a15cf-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a15cf-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a15cf-106">Función de biblioteca de marcos que crea un **XLOPER** /  **XLOPER12** temporal que contiene un número de hoja de cálculo de Microsoft Excel (doble IEEE de 8 bytes).</span><span class="sxs-lookup"><span data-stu-id="a15cf-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet number (an IEEE 8-byte double).</span></span> 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a><span data-ttu-id="a15cf-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a15cf-107">Parameters</span></span>

 <span data-ttu-id="a15cf-108">_d_ (**double**)</span><span class="sxs-lookup"><span data-stu-id="a15cf-108">_d_ (**double**)</span></span>
  
<span data-ttu-id="a15cf-109">El valor previsto.</span><span class="sxs-lookup"><span data-stu-id="a15cf-109">The intended value.</span></span> <span data-ttu-id="a15cf-110">Tenga en cuenta que los números sub normales ieee no se admiten actualmente y se redondea a cero.</span><span class="sxs-lookup"><span data-stu-id="a15cf-110">Note that IEEE sub-normal numbers are not currently supported and are rounded to zero.</span></span> <span data-ttu-id="a15cf-111">Se admite el infinito negativo.</span><span class="sxs-lookup"><span data-stu-id="a15cf-111">Negative infinity is supported.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="a15cf-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a15cf-112">Return value</span></span>

<span data-ttu-id="a15cf-113">Devuelve un **xltypeNum numérico** que contiene el valor pasado o cero si el valor pasado era sub normal.</span><span class="sxs-lookup"><span data-stu-id="a15cf-113">Returns a numeric **xltypeNum** containing the value passed in or zero if the passed in value was sub-normal.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a15cf-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a15cf-114">Example</span></span>

<span data-ttu-id="a15cf-115">En este ejemplo se **usa la función TempNum12** para pasar un argumento a **xlfGetWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="a15cf-115">This example uses the **TempNum12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempNumExample(void)
{
   XLOPER12 xRes;
   Excel12f(xlfGetWorkspace, &xRes, 1, TempNum12(44));
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="a15cf-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a15cf-116">See also</span></span>



[<span data-ttu-id="a15cf-117">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="a15cf-117">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

