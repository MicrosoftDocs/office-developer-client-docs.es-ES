---
title: Funciones de la biblioteca de marcos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- funciones de la biblioteca de marcos [Excel 2007], funciones [Excel 2007], biblioteca de marcos
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4eeb9e5db09592e98e9afb763efaa6be18eb2f7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304056"
---
# <a name="functions-in-the-framework-library"></a><span data-ttu-id="a18cc-104">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="a18cc-104">Functions in the Framework Library</span></span>

<span data-ttu-id="a18cc-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a18cc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a18cc-106">La biblioteca de .NET Framework se creó para facilitar la escritura de XLL.</span><span class="sxs-lookup"><span data-stu-id="a18cc-106">The Framework Library was created to help make writing XLLs easier.</span></span> <span data-ttu-id="a18cc-107">Incluye funciones sencillas para la administración de la memoria**xloper12** de **XLOPER**/ , la creación de **XLOPER**/ **xloper12**temporal, la llamada sólida a las funciones de devolución de llamada de Microsoft Excel (**Excel4**, **Excel4v** , \* \* Excel12 \* \*, \* \* Excel12v \* \*) e imprimir cadenas de depuración en un terminal adjunto.</span><span class="sxs-lookup"><span data-stu-id="a18cc-107">It includes simple functions for managing **XLOPER**/ **XLOPER12** memory, creating temporary **XLOPER**/ **XLOPER12**, robustly calling the Microsoft Excel callback functions (**Excel4**, **Excel4v**, \*\* Excel12 \*\*, \*\* Excel12v \*\*) and printing debugging strings on an attached terminal.</span></span>
  
<span data-ttu-id="a18cc-108">Las funciones incluidas en esta biblioteca ayudan a simplificar una parte del código similar a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="a18cc-108">The functions included in this library help simplify a piece of code that looks like the following.</span></span>
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

<span data-ttu-id="a18cc-109">El código simplificado es similar al ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a18cc-109">The simplified code looks like the following example.</span></span>
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

<span data-ttu-id="a18cc-110">Las siguientes funciones se incluyen en la biblioteca de Framework:</span><span class="sxs-lookup"><span data-stu-id="a18cc-110">The following functions are included in the Framework library:</span></span>
  
||
|:-----|
|[<span data-ttu-id="a18cc-111">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="a18cc-111">debugPrintf</span></span>](debugprintf.md) <br/> |
|<span data-ttu-id="a18cc-112">**GetTempMemory**</span><span class="sxs-lookup"><span data-stu-id="a18cc-112">**GetTempMemory**</span></span> <br/> |
|<span data-ttu-id="a18cc-113">**FreeAllTempMemory**</span><span class="sxs-lookup"><span data-stu-id="a18cc-113">**FreeAllTempMemory**</span></span> <br/> |
|[<span data-ttu-id="a18cc-114">InitFramework</span><span class="sxs-lookup"><span data-stu-id="a18cc-114">InitFramework</span></span>](initframework.md) <br/> |
|[<span data-ttu-id="a18cc-115">QuitFramework</span><span class="sxs-lookup"><span data-stu-id="a18cc-115">QuitFramework</span></span>](quitframework.md) <br/> |
   
|<span data-ttu-id="a18cc-116">**Funciones utilizadas con XLOPER**</span><span class="sxs-lookup"><span data-stu-id="a18cc-116">**Functions Used with XLOPERs**</span></span>|<span data-ttu-id="a18cc-117">**Funciones utilizadas con Xloper12**</span><span class="sxs-lookup"><span data-stu-id="a18cc-117">**Functions Used with XLOPER12s**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a18cc-118">Excel</span><span class="sxs-lookup"><span data-stu-id="a18cc-118">Excel</span></span>](excel-excel12f.md) <br/> |[<span data-ttu-id="a18cc-119">Excel12f</span><span class="sxs-lookup"><span data-stu-id="a18cc-119">Excel12f</span></span>](excel-excel12f.md) <br/> |
|[<span data-ttu-id="a18cc-120">TempNum</span><span class="sxs-lookup"><span data-stu-id="a18cc-120">TempNum</span></span>](tempnum-tempnum12.md) <br/> |[<span data-ttu-id="a18cc-121">TempNum12</span><span class="sxs-lookup"><span data-stu-id="a18cc-121">TempNum12</span></span>](tempnum-tempnum12.md) <br/> |
|[<span data-ttu-id="a18cc-122">TempStr</span><span class="sxs-lookup"><span data-stu-id="a18cc-122">TempStr</span></span>](tempstr.md) <br/> |[<span data-ttu-id="a18cc-123">TempStr12</span><span class="sxs-lookup"><span data-stu-id="a18cc-123">TempStr12</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="a18cc-124">TempStrConst</span><span class="sxs-lookup"><span data-stu-id="a18cc-124">TempStrConst</span></span>](tempstrconst-tempstr12.md) <br/> |[<span data-ttu-id="a18cc-125">TempStr12Const</span><span class="sxs-lookup"><span data-stu-id="a18cc-125">TempStr12Const</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="a18cc-126">TempBool</span><span class="sxs-lookup"><span data-stu-id="a18cc-126">TempBool</span></span>](tempbool-tempbool12.md) <br/> |[<span data-ttu-id="a18cc-127">TempBool12</span><span class="sxs-lookup"><span data-stu-id="a18cc-127">TempBool12</span></span>](tempbool-tempbool12.md) <br/> |
|[<span data-ttu-id="a18cc-128">TempInt</span><span class="sxs-lookup"><span data-stu-id="a18cc-128">TempInt</span></span>](tempint-tempint12.md) <br/> |[<span data-ttu-id="a18cc-129">TempInt12</span><span class="sxs-lookup"><span data-stu-id="a18cc-129">TempInt12</span></span>](tempint-tempint12.md) <br/> |
|[<span data-ttu-id="a18cc-130">Templating</span><span class="sxs-lookup"><span data-stu-id="a18cc-130">TempErr</span></span>](temperr-temperr12.md) <br/> |[<span data-ttu-id="a18cc-131">TempErr12</span><span class="sxs-lookup"><span data-stu-id="a18cc-131">TempErr12</span></span>](temperr-temperr12.md) <br/> |
|[<span data-ttu-id="a18cc-132">TempActiveRef</span><span class="sxs-lookup"><span data-stu-id="a18cc-132">TempActiveRef</span></span>](tempactiveref-tempactiveref12.md) <br/> |[<span data-ttu-id="a18cc-133">TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="a18cc-133">TempActiveRef12</span></span>](tempactiveref-tempactiveref12.md) <br/> |
|[<span data-ttu-id="a18cc-134">TempActiveCell</span><span class="sxs-lookup"><span data-stu-id="a18cc-134">TempActiveCell</span></span>](tempactivecell-tempactivecell12.md) <br/> |[<span data-ttu-id="a18cc-135">TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="a18cc-135">TempActiveCell12</span></span>](tempactivecell-tempactivecell12.md) <br/> |
|[<span data-ttu-id="a18cc-136">TempActiveRow</span><span class="sxs-lookup"><span data-stu-id="a18cc-136">TempActiveRow</span></span>](tempactiverow-tempactiverow12.md) <br/> |[<span data-ttu-id="a18cc-137">TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="a18cc-137">TempActiveRow12</span></span>](tempactiverow-tempactiverow12.md) <br/> |
|[<span data-ttu-id="a18cc-138">TempActiveColumn</span><span class="sxs-lookup"><span data-stu-id="a18cc-138">TempActiveColumn</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |[<span data-ttu-id="a18cc-139">TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="a18cc-139">TempActiveColumn12</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[<span data-ttu-id="a18cc-140">TempMissing</span><span class="sxs-lookup"><span data-stu-id="a18cc-140">TempMissing</span></span>](tempmissing-tempmissing12.md) <br/> |[<span data-ttu-id="a18cc-141">TempMissing12</span><span class="sxs-lookup"><span data-stu-id="a18cc-141">TempMissing12</span></span>](tempmissing-tempmissing12.md) <br/> |
   
<span data-ttu-id="a18cc-142">El uso de estas funciones reduce la cantidad de tiempo necesario para escribir una DLL o XLL.</span><span class="sxs-lookup"><span data-stu-id="a18cc-142">Use of these functions shortens the amount of time required to write a DLL or XLL.</span></span> <span data-ttu-id="a18cc-143">Si se inicia el desarrollo a partir de la aplicación de muestra genérica también se reduce el tiempo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="a18cc-143">Starting development from the sample application GENERIC also shortens development time.</span></span> <span data-ttu-id="a18cc-144">Usar GENERIC. C como plantilla para ayudar a configurar el marco de un XLL y, a continuación, reemplace el código existente por el suyo propio.</span><span class="sxs-lookup"><span data-stu-id="a18cc-144">Use GENERIC.C as a template to help set up the framework of an XLL, and then replace the existing code with your own.</span></span>
  
<span data-ttu-id="a18cc-145">Las funciones de**xloper12** de **XLOPER**/ temporales crean valores **XLOPER**/ **xloper12** mediante la memoria de un montón local administrado por la biblioteca de Framework.</span><span class="sxs-lookup"><span data-stu-id="a18cc-145">The temporary **XLOPER**/ **XLOPER12** functions create **XLOPER**/ **XLOPER12** values by using memory from a local heap managed by the Framework library.</span></span> <span data-ttu-id="a18cc-146">Los valores de**XLOPER12** de **XLOPER**/ siguen siendo válidos hasta que se llama a la función **FreeAllTempMemory** o a cualquiera de las funciones **Excel** o **Excel12f** .</span><span class="sxs-lookup"><span data-stu-id="a18cc-146">The **XLOPER**/ **XLOPER12** values remain valid until you call the **FreeAllTempMemory** function or either of the **Excel** or **Excel12f** functions.</span></span> <span data-ttu-id="a18cc-147">(Las funciones **Excel** y **Excel12f** liberan toda la memoria temporal antes de devolverse).</span><span class="sxs-lookup"><span data-stu-id="a18cc-147">(The **Excel** and **Excel12f** functions free all temporary memory before returning.)</span></span> 
  
<span data-ttu-id="a18cc-148">Para usar las funciones de la biblioteca de Marcos, debe incluir FRAMEWRK. H en el código C y agregue FRAMEWRK. C o FRMWRK32. LIB a su proyecto de código.</span><span class="sxs-lookup"><span data-stu-id="a18cc-148">To use the Framework library functions, you must include the FRAMEWRK.H file in your C code and add the FRAMEWRK.C or FRMWRK32.LIB files to your code project.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a18cc-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="a18cc-149">See also</span></span>

- [<span data-ttu-id="a18cc-150">Referencia de funciones de API de SDK de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="a18cc-150">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

