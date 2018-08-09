---
title: Funciones de la biblioteca de marcos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- funciones de la biblioteca Framework [excel 2007], [Excel 2007], funciones de biblioteca de Framework
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1d3878e376f95be3b277f1bb1a59545eb0a631ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815647"
---
# <a name="functions-in-the-framework-library"></a><span data-ttu-id="84a95-104">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="84a95-104">Functions in the Framework Library</span></span>

<span data-ttu-id="84a95-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="84a95-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="84a95-106">La biblioteca de Framework se creó para facilitar la escritura de los XLL sea más fáciles.</span><span class="sxs-lookup"><span data-stu-id="84a95-106">The Framework Library was created to help make writing XLLs easier.</span></span> <span data-ttu-id="84a95-107">Incluye funciones simples para la gestión **XLOPER**/ memoria**XLOPER12** , creación temporal **XLOPER**/ **XLOPER12**, con solidez al llamar a las funciones de devolución de llamada de Microsoft Excel (**Excel4**, **Excel4v** ** Excel12 **, ** Excel12v **) y la impresión de depuración de cadenas en un terminal adjunto.</span><span class="sxs-lookup"><span data-stu-id="84a95-107">It includes simple functions for managing **XLOPER**/ **XLOPER12** memory, creating temporary **XLOPER**/ **XLOPER12**, robustly calling the Microsoft Excel callback functions (**Excel4**, **Excel4v**, ** Excel12 **, ** Excel12v **) and printing debugging strings on an attached terminal.</span></span>
  
<span data-ttu-id="84a95-108">Las funciones incluidas en esta biblioteca ayudan a simplificar un fragmento de código que es similar a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="84a95-108">The functions included in this library help simplify a piece of code that looks like the following.</span></span>
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

<span data-ttu-id="84a95-109">El código simplificado es similar al ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="84a95-109">The simplified code looks like the following example.</span></span>
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

<span data-ttu-id="84a95-110">En la biblioteca de Framework se incluyen las funciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="84a95-110">The following functions are included in the Framework library:</span></span>
  
||
|:-----|
|[<span data-ttu-id="84a95-111">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="84a95-111">debugPrintf</span></span>](debugprintf.md) <br/> |
|<span data-ttu-id="84a95-112">**GetTempMemory**</span><span class="sxs-lookup"><span data-stu-id="84a95-112">**GetTempMemory**</span></span> <br/> |
|<span data-ttu-id="84a95-113">**FreeAllTempMemory**</span><span class="sxs-lookup"><span data-stu-id="84a95-113">**FreeAllTempMemory**</span></span> <br/> |
|[<span data-ttu-id="84a95-114">InitFramework</span><span class="sxs-lookup"><span data-stu-id="84a95-114">InitFramework</span></span>](initframework.md) <br/> |
|[<span data-ttu-id="84a95-115">QuitFramework</span><span class="sxs-lookup"><span data-stu-id="84a95-115">QuitFramework</span></span>](quitframework.md) <br/> |
   
|<span data-ttu-id="84a95-116">**Funciones usadas con XLOPER**</span><span class="sxs-lookup"><span data-stu-id="84a95-116">**Functions Used with XLOPERs**</span></span>|<span data-ttu-id="84a95-117">**Funciones usadas con XLOPER12s**</span><span class="sxs-lookup"><span data-stu-id="84a95-117">**Functions Used with XLOPER12s**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84a95-118">Excel</span><span class="sxs-lookup"><span data-stu-id="84a95-118">Excel</span></span>](excel-excel12f.md) <br/> |[<span data-ttu-id="84a95-119">Excel12f</span><span class="sxs-lookup"><span data-stu-id="84a95-119">Excel12f</span></span>](excel-excel12f.md) <br/> |
|[<span data-ttu-id="84a95-120">TempNum</span><span class="sxs-lookup"><span data-stu-id="84a95-120">TempNum</span></span>](tempnum-tempnum12.md) <br/> |[<span data-ttu-id="84a95-121">TempNum12</span><span class="sxs-lookup"><span data-stu-id="84a95-121">TempNum12</span></span>](tempnum-tempnum12.md) <br/> |
|[<span data-ttu-id="84a95-122">TempStr</span><span class="sxs-lookup"><span data-stu-id="84a95-122">TempStr</span></span>](tempstr.md) <br/> |[<span data-ttu-id="84a95-123">TempStr12</span><span class="sxs-lookup"><span data-stu-id="84a95-123">TempStr12</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="84a95-124">TempStrConst</span><span class="sxs-lookup"><span data-stu-id="84a95-124">TempStrConst</span></span>](tempstrconst-tempstr12.md) <br/> |[<span data-ttu-id="84a95-125">TempStr12Const</span><span class="sxs-lookup"><span data-stu-id="84a95-125">TempStr12Const</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="84a95-126">TempBool</span><span class="sxs-lookup"><span data-stu-id="84a95-126">TempBool</span></span>](tempbool-tempbool12.md) <br/> |[<span data-ttu-id="84a95-127">TempBool12</span><span class="sxs-lookup"><span data-stu-id="84a95-127">TempBool12</span></span>](tempbool-tempbool12.md) <br/> |
|[<span data-ttu-id="84a95-128">TempInt</span><span class="sxs-lookup"><span data-stu-id="84a95-128">TempInt</span></span>](tempint-tempint12.md) <br/> |[<span data-ttu-id="84a95-129">TempInt12</span><span class="sxs-lookup"><span data-stu-id="84a95-129">TempInt12</span></span>](tempint-tempint12.md) <br/> |
|[<span data-ttu-id="84a95-130">TempErr</span><span class="sxs-lookup"><span data-stu-id="84a95-130">TempErr</span></span>](temperr-temperr12.md) <br/> |[<span data-ttu-id="84a95-131">TempErr12</span><span class="sxs-lookup"><span data-stu-id="84a95-131">TempErr12</span></span>](temperr-temperr12.md) <br/> |
|[<span data-ttu-id="84a95-132">TempActiveRef</span><span class="sxs-lookup"><span data-stu-id="84a95-132">TempActiveRef</span></span>](tempactiveref-tempactiveref12.md) <br/> |[<span data-ttu-id="84a95-133">TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="84a95-133">TempActiveRef12</span></span>](tempactiveref-tempactiveref12.md) <br/> |
|[<span data-ttu-id="84a95-134">TempActiveCell</span><span class="sxs-lookup"><span data-stu-id="84a95-134">TempActiveCell</span></span>](tempactivecell-tempactivecell12.md) <br/> |[<span data-ttu-id="84a95-135">TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="84a95-135">TempActiveCell12</span></span>](tempactivecell-tempactivecell12.md) <br/> |
|[<span data-ttu-id="84a95-136">TempActiveRow</span><span class="sxs-lookup"><span data-stu-id="84a95-136">TempActiveRow</span></span>](tempactiverow-tempactiverow12.md) <br/> |[<span data-ttu-id="84a95-137">TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="84a95-137">TempActiveRow12</span></span>](tempactiverow-tempactiverow12.md) <br/> |
|[<span data-ttu-id="84a95-138">TempActiveColumn</span><span class="sxs-lookup"><span data-stu-id="84a95-138">TempActiveColumn</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |[<span data-ttu-id="84a95-139">TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="84a95-139">TempActiveColumn12</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[<span data-ttu-id="84a95-140">TempMissing</span><span class="sxs-lookup"><span data-stu-id="84a95-140">TempMissing</span></span>](tempmissing-tempmissing12.md) <br/> |[<span data-ttu-id="84a95-141">TempMissing12</span><span class="sxs-lookup"><span data-stu-id="84a95-141">TempMissing12</span></span>](tempmissing-tempmissing12.md) <br/> |
   
<span data-ttu-id="84a95-142">Uso de estas funciones reduce la cantidad de tiempo necesaria para escribir una DLL o XLL.</span><span class="sxs-lookup"><span data-stu-id="84a95-142">Use of these functions shortens the amount of time required to write a DLL or XLL.</span></span> <span data-ttu-id="84a95-143">Iniciar el desarrollo de la aplicación de ejemplo genérico también reduce el tiempo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="84a95-143">Starting development from the sample application GENERIC also shortens development time.</span></span> <span data-ttu-id="84a95-144">Use genérico. C como una plantilla para ayudar a configurar el marco de trabajo de un XLL y, a continuación, reemplace el código existente por el suyo propio.</span><span class="sxs-lookup"><span data-stu-id="84a95-144">Use GENERIC.C as a template to help set up the framework of an XLL, and then replace the existing code with your own.</span></span>
  
<span data-ttu-id="84a95-145">El temporal **XLOPER**/ **XLOPER12** funciones creación **XLOPER**/ **XLOPER12** valores mediante el uso de memoria de un montón local administrado por la biblioteca de Framework.</span><span class="sxs-lookup"><span data-stu-id="84a95-145">The temporary **XLOPER**/ **XLOPER12** functions create **XLOPER**/ **XLOPER12** values by using memory from a local heap managed by the Framework library.</span></span> <span data-ttu-id="84a95-146">El **XLOPER**/ **XLOPER12** valores permanecen válidos hasta que se llame a la función **FreeAllTempMemory** o cualquiera de las funciones de **Excel** o **Excel12f** .</span><span class="sxs-lookup"><span data-stu-id="84a95-146">The **XLOPER**/ **XLOPER12** values remain valid until you call the **FreeAllTempMemory** function or either of the **Excel** or **Excel12f** functions.</span></span> <span data-ttu-id="84a95-147">(Las funciones de **Excel** y **Excel12f** gratuita de toda la memoria temporal antes de devolver).</span><span class="sxs-lookup"><span data-stu-id="84a95-147">(The **Excel** and **Excel12f** functions free all temporary memory before returning.)</span></span> 
  
<span data-ttu-id="84a95-148">Para usar las funciones de la biblioteca de Framework, debe incluir el FRAMEWRK. Según se trate de archivos en el código de C y agregar la FRAMEWRK. C o FRMWRK32. Archivos de LIB a su proyecto de código.</span><span class="sxs-lookup"><span data-stu-id="84a95-148">To use the Framework library functions, you must include the FRAMEWRK.H file in your C code and add the FRAMEWRK.C or FRMWRK32.LIB files to your code project.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="84a95-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="84a95-149">See also</span></span>

- [<span data-ttu-id="84a95-150">Referencia de funciones de API de SDK de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="84a95-150">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

