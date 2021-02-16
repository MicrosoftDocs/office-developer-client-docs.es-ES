---
title: Funciones de la biblioteca de marcos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- funciones de biblioteca de marcos [excel 2007],funciones [Excel 2007], biblioteca de marcos
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4eeb9e5db09592e98e9afb763efaa6be18eb2f7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417549"
---
# <a name="functions-in-the-framework-library"></a><span data-ttu-id="8fa32-104">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="8fa32-104">Functions in the Framework Library</span></span>

<span data-ttu-id="8fa32-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8fa32-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8fa32-106">La Biblioteca de marcos se creó para facilitar la escritura de XLL.</span><span class="sxs-lookup"><span data-stu-id="8fa32-106">The Framework Library was created to help make writing XLLs easier.</span></span> <span data-ttu-id="8fa32-107">Incluye funciones sencillas para administrar la memoria /  **XLOPER XLOPER12,** crear **XLOPER** XLOPER12 temporal, llamar sólidamente a las funciones de devolución de llamada de /  Microsoft Excel (**Excel4**, **Excel4v**, \*\* Excel12 \*\*, \*\* Excel12v \*\*) e imprimir cadenas de depuración en un terminal adjunto.</span><span class="sxs-lookup"><span data-stu-id="8fa32-107">It includes simple functions for managing **XLOPER**/ **XLOPER12** memory, creating temporary **XLOPER**/ **XLOPER12**, robustly calling the Microsoft Excel callback functions (**Excel4**, **Excel4v**, \*\* Excel12 \*\*, \*\* Excel12v \*\*) and printing debugging strings on an attached terminal.</span></span>
  
<span data-ttu-id="8fa32-108">Las funciones incluidas en esta biblioteca ayudan a simplificar un fragmento de código similar al siguiente.</span><span class="sxs-lookup"><span data-stu-id="8fa32-108">The functions included in this library help simplify a piece of code that looks like the following.</span></span>
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

<span data-ttu-id="8fa32-109">El código simplificado es similar al ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="8fa32-109">The simplified code looks like the following example.</span></span>
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

<span data-ttu-id="8fa32-110">En la biblioteca de marcos se incluyen las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="8fa32-110">The following functions are included in the Framework library:</span></span>
  
||
|:-----|
|[<span data-ttu-id="8fa32-111">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="8fa32-111">debugPrintf</span></span>](debugprintf.md) <br/> |
|<span data-ttu-id="8fa32-112">**GetTempMemory**</span><span class="sxs-lookup"><span data-stu-id="8fa32-112">**GetTempMemory**</span></span> <br/> |
|<span data-ttu-id="8fa32-113">**FreeAllTempMemory**</span><span class="sxs-lookup"><span data-stu-id="8fa32-113">**FreeAllTempMemory**</span></span> <br/> |
|[<span data-ttu-id="8fa32-114">InitFramework</span><span class="sxs-lookup"><span data-stu-id="8fa32-114">InitFramework</span></span>](initframework.md) <br/> |
|[<span data-ttu-id="8fa32-115">QuitFramework</span><span class="sxs-lookup"><span data-stu-id="8fa32-115">QuitFramework</span></span>](quitframework.md) <br/> |
   
|<span data-ttu-id="8fa32-116">**Funciones usadas con XLOPERs**</span><span class="sxs-lookup"><span data-stu-id="8fa32-116">**Functions Used with XLOPERs**</span></span>|<span data-ttu-id="8fa32-117">**Funciones usadas con XLOPER12s**</span><span class="sxs-lookup"><span data-stu-id="8fa32-117">**Functions Used with XLOPER12s**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8fa32-118">Excel</span><span class="sxs-lookup"><span data-stu-id="8fa32-118">Excel</span></span>](excel-excel12f.md) <br/> |[<span data-ttu-id="8fa32-119">Excel12f</span><span class="sxs-lookup"><span data-stu-id="8fa32-119">Excel12f</span></span>](excel-excel12f.md) <br/> |
|[<span data-ttu-id="8fa32-120">TempNum</span><span class="sxs-lookup"><span data-stu-id="8fa32-120">TempNum</span></span>](tempnum-tempnum12.md) <br/> |[<span data-ttu-id="8fa32-121">TempNum12</span><span class="sxs-lookup"><span data-stu-id="8fa32-121">TempNum12</span></span>](tempnum-tempnum12.md) <br/> |
|[<span data-ttu-id="8fa32-122">TempStr</span><span class="sxs-lookup"><span data-stu-id="8fa32-122">TempStr</span></span>](tempstr.md) <br/> |[<span data-ttu-id="8fa32-123">TempStr12</span><span class="sxs-lookup"><span data-stu-id="8fa32-123">TempStr12</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="8fa32-124">TempStrConst</span><span class="sxs-lookup"><span data-stu-id="8fa32-124">TempStrConst</span></span>](tempstrconst-tempstr12.md) <br/> |[<span data-ttu-id="8fa32-125">TempStr12Const</span><span class="sxs-lookup"><span data-stu-id="8fa32-125">TempStr12Const</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="8fa32-126">TempBool</span><span class="sxs-lookup"><span data-stu-id="8fa32-126">TempBool</span></span>](tempbool-tempbool12.md) <br/> |[<span data-ttu-id="8fa32-127">TempBool12</span><span class="sxs-lookup"><span data-stu-id="8fa32-127">TempBool12</span></span>](tempbool-tempbool12.md) <br/> |
|[<span data-ttu-id="8fa32-128">TempInt</span><span class="sxs-lookup"><span data-stu-id="8fa32-128">TempInt</span></span>](tempint-tempint12.md) <br/> |[<span data-ttu-id="8fa32-129">TempInt12</span><span class="sxs-lookup"><span data-stu-id="8fa32-129">TempInt12</span></span>](tempint-tempint12.md) <br/> |
|[<span data-ttu-id="8fa32-130">TempErr</span><span class="sxs-lookup"><span data-stu-id="8fa32-130">TempErr</span></span>](temperr-temperr12.md) <br/> |[<span data-ttu-id="8fa32-131">TempErr12</span><span class="sxs-lookup"><span data-stu-id="8fa32-131">TempErr12</span></span>](temperr-temperr12.md) <br/> |
|[<span data-ttu-id="8fa32-132">TempActiveRef</span><span class="sxs-lookup"><span data-stu-id="8fa32-132">TempActiveRef</span></span>](tempactiveref-tempactiveref12.md) <br/> |[<span data-ttu-id="8fa32-133">TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="8fa32-133">TempActiveRef12</span></span>](tempactiveref-tempactiveref12.md) <br/> |
|[<span data-ttu-id="8fa32-134">TempActiveCell</span><span class="sxs-lookup"><span data-stu-id="8fa32-134">TempActiveCell</span></span>](tempactivecell-tempactivecell12.md) <br/> |[<span data-ttu-id="8fa32-135">TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="8fa32-135">TempActiveCell12</span></span>](tempactivecell-tempactivecell12.md) <br/> |
|[<span data-ttu-id="8fa32-136">TempActiveRow</span><span class="sxs-lookup"><span data-stu-id="8fa32-136">TempActiveRow</span></span>](tempactiverow-tempactiverow12.md) <br/> |[<span data-ttu-id="8fa32-137">TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="8fa32-137">TempActiveRow12</span></span>](tempactiverow-tempactiverow12.md) <br/> |
|[<span data-ttu-id="8fa32-138">TempActiveColumn</span><span class="sxs-lookup"><span data-stu-id="8fa32-138">TempActiveColumn</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |[<span data-ttu-id="8fa32-139">TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="8fa32-139">TempActiveColumn12</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[<span data-ttu-id="8fa32-140">TempMissing</span><span class="sxs-lookup"><span data-stu-id="8fa32-140">TempMissing</span></span>](tempmissing-tempmissing12.md) <br/> |[<span data-ttu-id="8fa32-141">TempMissing12</span><span class="sxs-lookup"><span data-stu-id="8fa32-141">TempMissing12</span></span>](tempmissing-tempmissing12.md) <br/> |
   
<span data-ttu-id="8fa32-142">El uso de estas funciones acorta la cantidad de tiempo necesario para escribir una DLL o XLL.</span><span class="sxs-lookup"><span data-stu-id="8fa32-142">Use of these functions shortens the amount of time required to write a DLL or XLL.</span></span> <span data-ttu-id="8fa32-143">Iniciar el desarrollo desde la aplicación de ejemplo GENERIC también acorta el tiempo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="8fa32-143">Starting development from the sample application GENERIC also shortens development time.</span></span> <span data-ttu-id="8fa32-144">Use GENERIC. C como plantilla para ayudar a configurar el marco de un XLL y, a continuación, reemplazar el código existente por el suyo propio.</span><span class="sxs-lookup"><span data-stu-id="8fa32-144">Use GENERIC.C as a template to help set up the framework of an XLL, and then replace the existing code with your own.</span></span>
  
<span data-ttu-id="8fa32-145">Las funciones **temporales XLOPER** /  **XLOPER12** crean valores **XLOPER** /  **XLOPER12** mediante la memoria de un montón local administrado por la biblioteca de marcos.</span><span class="sxs-lookup"><span data-stu-id="8fa32-145">The temporary **XLOPER**/ **XLOPER12** functions create **XLOPER**/ **XLOPER12** values by using memory from a local heap managed by the Framework library.</span></span> <span data-ttu-id="8fa32-146">Los **valores XLOPER** XLOPER12 siguen siendo válidos hasta que se llama a la función /   **FreeAllTempMemory** o a cualquiera de las funciones de **Excel** o **Excel12f.**</span><span class="sxs-lookup"><span data-stu-id="8fa32-146">The **XLOPER**/ **XLOPER12** values remain valid until you call the **FreeAllTempMemory** function or either of the **Excel** or **Excel12f** functions.</span></span> <span data-ttu-id="8fa32-147">(Las **funciones Excel** y **Excel12f** liberan toda la memoria temporal antes de volver).</span><span class="sxs-lookup"><span data-stu-id="8fa32-147">(The **Excel** and **Excel12f** functions free all temporary memory before returning.)</span></span> 
  
<span data-ttu-id="8fa32-148">Para usar las funciones de biblioteca de Framework, debe incluir framewrk. H en el código C y agregue framewrk. C o FRMWRK32. Archivos LIB en el proyecto de código.</span><span class="sxs-lookup"><span data-stu-id="8fa32-148">To use the Framework library functions, you must include the FRAMEWRK.H file in your C code and add the FRAMEWRK.C or FRMWRK32.LIB files to your code project.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8fa32-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8fa32-149">See also</span></span>

- [<span data-ttu-id="8fa32-150">Referencia de funciones de API de SDK de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="8fa32-150">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

