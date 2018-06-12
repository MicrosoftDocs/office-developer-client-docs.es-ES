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
- tempnum12 (función) [excel 2007], TempNum (función) [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5ebe58dba32c2cf0382bf0811713eaa0a5471dda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815703"
---
# <a name="tempnumtempnum12"></a><span data-ttu-id="f1924-104">TempNum/TempNum12</span><span class="sxs-lookup"><span data-stu-id="f1924-104">TempNum/TempNum12</span></span>

 <span data-ttu-id="f1924-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1924-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f1924-106">Función de la biblioteca de Framework que crea un temporal **XLOPER**/ **XLOPER12** que contiene un número de hoja de cálculo de Microsoft Excel (un doble de 8 bytes IEEE).</span><span class="sxs-lookup"><span data-stu-id="f1924-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet number (an IEEE 8-byte double).</span></span> 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a><span data-ttu-id="f1924-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1924-107">Parameters</span></span>

 <span data-ttu-id="f1924-108">_d._ (**doble**)</span><span class="sxs-lookup"><span data-stu-id="f1924-108">_d_ (**double**)</span></span>
  
<span data-ttu-id="f1924-109">El valor deseado.</span><span class="sxs-lookup"><span data-stu-id="f1924-109">The intended value.</span></span> <span data-ttu-id="f1924-110">Tenga en cuenta que los números de subcaracterísticas normales de IEEE actualmente no son compatibles y se redondean a cero.</span><span class="sxs-lookup"><span data-stu-id="f1924-110">Note that IEEE sub-normal numbers are not currently supported and are rounded to zero.</span></span> <span data-ttu-id="f1924-111">Se admite el infinito negativo.</span><span class="sxs-lookup"><span data-stu-id="f1924-111">Negative infinity is supported.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="f1924-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1924-112">Return value</span></span>

<span data-ttu-id="f1924-113">Devuelve un numéricos **xltypeNum** que contiene el valor que se pasó o cero si el valor pasado fue subcaracterísticas normal.</span><span class="sxs-lookup"><span data-stu-id="f1924-113">Returns a numeric **xltypeNum** containing the value passed in or zero if the passed in value was sub-normal.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f1924-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f1924-114">Example</span></span>

<span data-ttu-id="f1924-115">En este ejemplo se usa la función **TempNum12** para pasar un argumento a **xlfGetWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="f1924-115">This example uses the **TempNum12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="f1924-116">Ver también</span><span class="sxs-lookup"><span data-stu-id="f1924-116">See also</span></span>



[<span data-ttu-id="f1924-117">Funciones de la biblioteca de Framework</span><span class="sxs-lookup"><span data-stu-id="f1924-117">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

