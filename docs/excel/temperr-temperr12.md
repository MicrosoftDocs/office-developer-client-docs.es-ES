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
- temperr (función) [excel 2007], TempErr12 (función) [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 22c0ff1b8259fc0e5ee70edb06bb3db53781ff8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815697"
---
# <a name="temperrtemperr12"></a><span data-ttu-id="6900d-104">TempErr/TempErr12</span><span class="sxs-lookup"><span data-stu-id="6900d-104">TempErr/TempErr12</span></span>

 <span data-ttu-id="6900d-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6900d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6900d-106">Función de la biblioteca de Framework que crea un temporal **XLOPER**/ **XLOPER12** que contiene un error de hoja de cálculo de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="6900d-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet error.</span></span> 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a><span data-ttu-id="6900d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6900d-107">Parameters</span></span>

 <span data-ttu-id="6900d-108">_Err_</span><span class="sxs-lookup"><span data-stu-id="6900d-108">_err_</span></span>
  
<span data-ttu-id="6900d-109">El código de error que desee, o su equivalente numérico literal, tal como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="6900d-109">The desired error code, or its literal numeric equivalent, as shown in the following table.</span></span>
  
|<span data-ttu-id="6900d-110">**Error**</span><span class="sxs-lookup"><span data-stu-id="6900d-110">**Error**</span></span>|<span data-ttu-id="6900d-111">**Código de error definido en XLCALL. H**</span><span class="sxs-lookup"><span data-stu-id="6900d-111">**Error code defined in XLCALL.H**</span></span>|<span data-ttu-id="6900d-112">**Equivalente decimal**</span><span class="sxs-lookup"><span data-stu-id="6900d-112">**Decimal equivalent**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6900d-113">#NULL</span><span class="sxs-lookup"><span data-stu-id="6900d-113">#NULL</span></span>  <br/> |<span data-ttu-id="6900d-114">**xlerrNull**</span><span class="sxs-lookup"><span data-stu-id="6900d-114">**xlerrNull**</span></span> <br/> |<span data-ttu-id="6900d-115">0</span><span class="sxs-lookup"><span data-stu-id="6900d-115">0</span></span>  <br/> |
|<span data-ttu-id="6900d-116">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="6900d-116">#DIV/0!</span></span>  <br/> |<span data-ttu-id="6900d-117">**xlerrDiv0**</span><span class="sxs-lookup"><span data-stu-id="6900d-117">**xlerrDiv0**</span></span> <br/> |<span data-ttu-id="6900d-118">7</span><span class="sxs-lookup"><span data-stu-id="6900d-118">7</span></span>  <br/> |
|<span data-ttu-id="6900d-119">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="6900d-119">#VALUE!</span></span>  <br/> |<span data-ttu-id="6900d-120">**xlerrValue**</span><span class="sxs-lookup"><span data-stu-id="6900d-120">**xlerrValue**</span></span> <br/> |<span data-ttu-id="6900d-121">15</span><span class="sxs-lookup"><span data-stu-id="6900d-121">15</span></span>  <br/> |
|<span data-ttu-id="6900d-122">#REF!</span><span class="sxs-lookup"><span data-stu-id="6900d-122">#REF!</span></span>  <br/> |<span data-ttu-id="6900d-123">**xlerrRef**</span><span class="sxs-lookup"><span data-stu-id="6900d-123">**xlerrRef**</span></span> <br/> |<span data-ttu-id="6900d-124">23</span><span class="sxs-lookup"><span data-stu-id="6900d-124">23</span></span>  <br/> |
|<span data-ttu-id="6900d-125">#NAME?</span><span class="sxs-lookup"><span data-stu-id="6900d-125">#NAME?</span></span>  <br/> |<span data-ttu-id="6900d-126">**xlerrName**</span><span class="sxs-lookup"><span data-stu-id="6900d-126">**xlerrName**</span></span> <br/> |<span data-ttu-id="6900d-127">29</span><span class="sxs-lookup"><span data-stu-id="6900d-127">29</span></span>  <br/> |
|<span data-ttu-id="6900d-128">#NUM!</span><span class="sxs-lookup"><span data-stu-id="6900d-128">#NUM!</span></span>  <br/> |<span data-ttu-id="6900d-129">**xlerrNum**</span><span class="sxs-lookup"><span data-stu-id="6900d-129">**xlerrNum**</span></span> <br/> |<span data-ttu-id="6900d-130">36</span><span class="sxs-lookup"><span data-stu-id="6900d-130">36</span></span>  <br/> |
|<span data-ttu-id="6900d-131">#N/A</span><span class="sxs-lookup"><span data-stu-id="6900d-131">#N/A</span></span>  <br/> |<span data-ttu-id="6900d-132">**xlerrNA**</span><span class="sxs-lookup"><span data-stu-id="6900d-132">**xlerrNA**</span></span> <br/> |<span data-ttu-id="6900d-133">42</span><span class="sxs-lookup"><span data-stu-id="6900d-133">42</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="6900d-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6900d-134">Return value</span></span>

<span data-ttu-id="6900d-135">Devuelve un **xltypeBool** que contiene el código de error que se pasó.</span><span class="sxs-lookup"><span data-stu-id="6900d-135">Returns an **xltypeBool** containing the error code passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6900d-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6900d-136">Example</span></span>

<span data-ttu-id="6900d-137">¡En este ejemplo se usa la función **TempErr12** para devolver #VALUE!</span><span class="sxs-lookup"><span data-stu-id="6900d-137">This example uses the **TempErr12** function to return a #VALUE!</span></span> <span data-ttu-id="6900d-138">Error en Excel.</span><span class="sxs-lookup"><span data-stu-id="6900d-138">error to Excel.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6900d-139">La función de biblioteca de Framework **TempErr12** asigna memoria de un búfer interno, que normalmente se libera cuando se llama a la función de Framework **Excel12f** .</span><span class="sxs-lookup"><span data-stu-id="6900d-139">The Framework library function **TempErr12** allocates memory from an internal buffer, which is normally freed when the Framework function **Excel12f** is called.</span></span> <span data-ttu-id="6900d-140">Si en el ejemplo se llama a esta función repetidamente sin **Excel12f** que se llama, se produce una pérdida de memoria.</span><span class="sxs-lookup"><span data-stu-id="6900d-140">If this example function is called repeatedly without **Excel12f** being called, a memory leak occurs.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a><span data-ttu-id="6900d-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="6900d-141">See also</span></span>



[<span data-ttu-id="6900d-142">Funciones de la biblioteca de Framework</span><span class="sxs-lookup"><span data-stu-id="6900d-142">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

