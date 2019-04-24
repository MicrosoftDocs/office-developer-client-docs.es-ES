---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- función de Excel [Excel 2007], función Excel12f [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f7ff6afac1737ee869e69fffd3dbed36a908b376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310916"
---
# <a name="excelexcel12f"></a><span data-ttu-id="4d119-104">Excel/Excel12f</span><span class="sxs-lookup"><span data-stu-id="4d119-104">Excel/Excel12f</span></span>

 <span data-ttu-id="4d119-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4d119-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4d119-106">Funciones de la biblioteca de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4d119-106">Framework library functions.</span></span> <span data-ttu-id="4d119-107">**Excel** es un contenedor para la función [Excel4](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="4d119-107">**Excel** is a wrapper for the [Excel4](excel4-excel12.md) function.</span></span> <span data-ttu-id="4d119-108">**Excel12f** es un contenedor para la función [Excel12](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="4d119-108">**Excel12f** is a wrapper for the [Excel12](excel4-excel12.md) function.</span></span> <span data-ttu-id="4d119-109">Cada uno de ellos comprueba que ninguno de los argumentos es cero, lo que indicaría que no se pudo crear un **XLOPER** o **XLOPER12** temporal.</span><span class="sxs-lookup"><span data-stu-id="4d119-109">Each checks to see that none of the arguments is zero, which would indicate that the creation of a temporary **XLOPER** or **XLOPER12** failed.</span></span> <span data-ttu-id="4d119-110">Si se produce un error, cada uno imprime un mensaje de depuración.</span><span class="sxs-lookup"><span data-stu-id="4d119-110">If an error occurs, each prints a debug message.</span></span> <span data-ttu-id="4d119-111">Cuando termine, cada uno liberará toda la memoria temporal que se podría haber creado para los **XLOPER**y **XLOPER12**temporales, s.</span><span class="sxs-lookup"><span data-stu-id="4d119-111">When finished, each frees all temporary memory that might have been created for temporary **XLOPER**s and **XLOPER12**s.</span></span>
  
 <span data-ttu-id="4d119-112">**Excel12f** sólo se puede llamar desde una DLL a partir de la biblioteca API 2007 C de Excel.</span><span class="sxs-lookup"><span data-stu-id="4d119-112">**Excel12f** can only be called from a DLL starting with the Excel 2007 C API library.</span></span> <span data-ttu-id="4d119-113">Además, solo funciona cuando se ejecuta a partir de Excel 2007 y se produce un error con **xlretFailed** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4d119-113">Furthermore, it only works when running starting with Excel 2007, and fails with **xlretFailed** otherwise.</span></span> 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a><span data-ttu-id="4d119-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="4d119-114">Parameters</span></span>

 <span data-ttu-id="4d119-115">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="4d119-115">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="4d119-116">Un número que indica el comando o la función a la que desea llamar.</span><span class="sxs-lookup"><span data-stu-id="4d119-116">A number indicating the command or function you want to call.</span></span> <span data-ttu-id="4d119-117">Para obtener más información, consulte [Excel4/Excel12](excel4-excel12.md).</span><span class="sxs-lookup"><span data-stu-id="4d119-117">For more information, see [Excel4/Excel12](excel4-excel12.md).</span></span>
  
 <span data-ttu-id="4d119-118">_pxRes_</span><span class="sxs-lookup"><span data-stu-id="4d119-118">_pxRes_</span></span>
  
<span data-ttu-id="4d119-119">Un puntero a resultado de la función evaluada.</span><span class="sxs-lookup"><span data-stu-id="4d119-119">A pointer to result of the evaluated function.</span></span> <span data-ttu-id="4d119-120">Cualquier memoria a la que apuntaba el resultado habrá sido asignada por Excel y debe liberarse en una llamada a [xlFree](xlfree.md) una vez que ya no se necesite, o estableciendo **xlbitXLFree** si se devuelve a Excel.</span><span class="sxs-lookup"><span data-stu-id="4d119-120">Any memory pointed to in the result will have been allocated by Excel and should be freed in a call to [xlFree](xlfree.md) once it is no longer needed, or by setting **xlbitXLFree** if returning it to Excel.</span></span> 
  
 <span data-ttu-id="4d119-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="4d119-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="4d119-122">Número de argumentos que se van a pasar a la función.</span><span class="sxs-lookup"><span data-stu-id="4d119-122">The number of arguments that will be passed to the function.</span></span> <span data-ttu-id="4d119-123">A partir de Excel 2007, el límite es de 255 argumentos.</span><span class="sxs-lookup"><span data-stu-id="4d119-123">Starting in Excel 2007, the limit is 255 arguments.</span></span> <span data-ttu-id="4d119-124">En versiones anteriores, el límite es 30.</span><span class="sxs-lookup"><span data-stu-id="4d119-124">In earlier versions, the limit is 30.</span></span>
  
 <span data-ttu-id="4d119-125">_argumento1,..._</span><span class="sxs-lookup"><span data-stu-id="4d119-125">_argument1, ..._</span></span>
  
<span data-ttu-id="4d119-126">Argumentos opcionales de la función.</span><span class="sxs-lookup"><span data-stu-id="4d119-126">The optional arguments to the function.</span></span> <span data-ttu-id="4d119-127">Todos los argumentos deben ser punteros a **XLOPER**s en el caso de **Excel**, o **XLOPER12**s en el caso de **Excel12f**.</span><span class="sxs-lookup"><span data-stu-id="4d119-127">All arguments must be pointers to **XLOPER**s in the case of **Excel**, or **XLOPER12**s in the case of **Excel12f**.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="4d119-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d119-128">Return value</span></span>

<span data-ttu-id="4d119-129">Ambas funciones devuelven los mismos códigos de error y de éxito que **Excel4**, **Excel4v**, **Excel12**y **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="4d119-129">Both functions return the same error and success codes as **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**.</span></span> <span data-ttu-id="4d119-130">Consulte [Excel4/Excel12](excel4-excel12.md) para obtener una descripción completa de estos códigos.</span><span class="sxs-lookup"><span data-stu-id="4d119-130">See [Excel4/Excel12](excel4-excel12.md) for a full description of these codes.</span></span> <span data-ttu-id="4d119-131">Además, estas funciones de marco devuelven **xlretFailed** sin llamar a la API de C si se detecta un puntero nulo a un parámetro.</span><span class="sxs-lookup"><span data-stu-id="4d119-131">In addition, these Framework functions return **xlretFailed** without calling the C API if a NULL pointer to a parameter is detected.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4d119-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d119-132">Example</span></span>

<span data-ttu-id="4d119-133">En este ejemplo se pasa un argumento incorrecto a la función **Excel12f** , que envía un mensaje al depurador.</span><span class="sxs-lookup"><span data-stu-id="4d119-133">This example passes a bad argument to the **Excel12f** function, which sends a message to the debugger.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="4d119-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d119-134">See also</span></span>



[<span data-ttu-id="4d119-135">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="4d119-135">Excel4/Excel12</span></span>](excel4-excel12.md)


[<span data-ttu-id="4d119-136">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="4d119-136">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

