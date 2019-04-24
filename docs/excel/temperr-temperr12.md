---
title: TempErr/TempErr12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempErr
- TempErr12
keywords:
- función templator [Excel 2007], función TempErr12 [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 68a0addc36ecf1b4491ab1e4f5b10f359bbc59c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310349"
---
# <a name="temperrtemperr12"></a><span data-ttu-id="12301-104">TempErr/TempErr12</span><span class="sxs-lookup"><span data-stu-id="12301-104">TempErr/TempErr12</span></span>

 <span data-ttu-id="12301-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="12301-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="12301-106">Función de biblioteca de .NET Framework que crea un**XLOPER12** de **XLOPER**/ temporal que contiene un error de hoja de cálculo de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="12301-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet error.</span></span> 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a><span data-ttu-id="12301-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="12301-107">Parameters</span></span>

 <span data-ttu-id="12301-108">_err_</span><span class="sxs-lookup"><span data-stu-id="12301-108">_err_</span></span>
  
<span data-ttu-id="12301-109">El código de error deseado, o su equivalente numérico literal, como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="12301-109">The desired error code, or its literal numeric equivalent, as shown in the following table.</span></span>
  
|<span data-ttu-id="12301-110">**Error**</span><span class="sxs-lookup"><span data-stu-id="12301-110">**Error**</span></span>|<span data-ttu-id="12301-111">**Código de error definido en XLCALL. H**</span><span class="sxs-lookup"><span data-stu-id="12301-111">**Error code defined in XLCALL.H**</span></span>|<span data-ttu-id="12301-112">**Equivalente decimal**</span><span class="sxs-lookup"><span data-stu-id="12301-112">**Decimal equivalent**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="12301-113">#NULL</span><span class="sxs-lookup"><span data-stu-id="12301-113">#NULL</span></span>  <br/> |<span data-ttu-id="12301-114">**xlerrNull**</span><span class="sxs-lookup"><span data-stu-id="12301-114">**xlerrNull**</span></span> <br/> |<span data-ttu-id="12301-115">comprendi</span><span class="sxs-lookup"><span data-stu-id="12301-115">0</span></span>  <br/> |
|<span data-ttu-id="12301-116">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="12301-116">#DIV/0!</span></span>  <br/> |<span data-ttu-id="12301-117">**xlerrDiv0**</span><span class="sxs-lookup"><span data-stu-id="12301-117">**xlerrDiv0**</span></span> <br/> |<span data-ttu-id="12301-118">0,7</span><span class="sxs-lookup"><span data-stu-id="12301-118">7</span></span>  <br/> |
|<span data-ttu-id="12301-119">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="12301-119">#VALUE!</span></span>  <br/> |<span data-ttu-id="12301-120">**xlerrValue**</span><span class="sxs-lookup"><span data-stu-id="12301-120">**xlerrValue**</span></span> <br/> |<span data-ttu-id="12301-121">15</span><span class="sxs-lookup"><span data-stu-id="12301-121">15</span></span>  <br/> |
|<span data-ttu-id="12301-122">#REF!</span><span class="sxs-lookup"><span data-stu-id="12301-122">#REF!</span></span>  <br/> |<span data-ttu-id="12301-123">**xlerrRef**</span><span class="sxs-lookup"><span data-stu-id="12301-123">**xlerrRef**</span></span> <br/> |<span data-ttu-id="12301-124">veintitrés</span><span class="sxs-lookup"><span data-stu-id="12301-124">23</span></span>  <br/> |
|<span data-ttu-id="12301-125">#NAME?</span><span class="sxs-lookup"><span data-stu-id="12301-125">#NAME?</span></span>  <br/> |<span data-ttu-id="12301-126">**xlerrName**</span><span class="sxs-lookup"><span data-stu-id="12301-126">**xlerrName**</span></span> <br/> |<span data-ttu-id="12301-127">32</span><span class="sxs-lookup"><span data-stu-id="12301-127">29</span></span>  <br/> |
|<span data-ttu-id="12301-128">#NUM!</span><span class="sxs-lookup"><span data-stu-id="12301-128">#NUM!</span></span>  <br/> |<span data-ttu-id="12301-129">**xlerrNum**</span><span class="sxs-lookup"><span data-stu-id="12301-129">**xlerrNum**</span></span> <br/> |<span data-ttu-id="12301-130">36</span><span class="sxs-lookup"><span data-stu-id="12301-130">36</span></span>  <br/> |
|<span data-ttu-id="12301-131">#N/A</span><span class="sxs-lookup"><span data-stu-id="12301-131">#N/A</span></span>  <br/> |<span data-ttu-id="12301-132">**xlerrNA**</span><span class="sxs-lookup"><span data-stu-id="12301-132">**xlerrNA**</span></span> <br/> |<span data-ttu-id="12301-133">42</span><span class="sxs-lookup"><span data-stu-id="12301-133">42</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="12301-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12301-134">Return value</span></span>

<span data-ttu-id="12301-135">Devuelve una **xltypeBool** que contiene el código de error que se ha pasado.</span><span class="sxs-lookup"><span data-stu-id="12301-135">Returns an **xltypeBool** containing the error code passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="12301-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="12301-136">Example</span></span>

<span data-ttu-id="12301-137">En este ejemplo se usa la función **TempErr12** para devolver un #VALUE!</span><span class="sxs-lookup"><span data-stu-id="12301-137">This example uses the **TempErr12** function to return a #VALUE!</span></span> <span data-ttu-id="12301-138">error a Excel.</span><span class="sxs-lookup"><span data-stu-id="12301-138">error to Excel.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="12301-139">La función **TempErr12** de la biblioteca de Marcos asigna memoria de un búfer interno, que normalmente se libera cuando se llama a la función **Excel12f** de Framework.</span><span class="sxs-lookup"><span data-stu-id="12301-139">The Framework library function **TempErr12** allocates memory from an internal buffer, which is normally freed when the Framework function **Excel12f** is called.</span></span> <span data-ttu-id="12301-140">Si se llama a esta función de ejemplo repetidamente sin llamar a **Excel12f** , se produce una pérdida de memoria.</span><span class="sxs-lookup"><span data-stu-id="12301-140">If this example function is called repeatedly without **Excel12f** being called, a memory leak occurs.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a><span data-ttu-id="12301-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="12301-141">See also</span></span>



[<span data-ttu-id="12301-142">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="12301-142">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

