---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- función de Excel [excel 2007], Excel12f (función) [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 56034984852713496465c3d1f79a9989fc47df1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815563"
---
# <a name="excelexcel12f"></a><span data-ttu-id="a5926-104">Excel/Excel12f</span><span class="sxs-lookup"><span data-stu-id="a5926-104">Excel/Excel12f</span></span>

 <span data-ttu-id="a5926-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a5926-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a5926-106">Funciones de la biblioteca de Framework.</span><span class="sxs-lookup"><span data-stu-id="a5926-106">Framework library functions.</span></span> <span data-ttu-id="a5926-107">**Excel** es un contenedor para la función de [Excel4](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="a5926-107">**Excel** is a wrapper for the [Excel4](excel4-excel12.md) function.</span></span> <span data-ttu-id="a5926-108">**Excel12f** es un contenedor para la función [Excel12](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="a5926-108">**Excel12f** is a wrapper for the [Excel12](excel4-excel12.md) function.</span></span> <span data-ttu-id="a5926-109">Cada uno de ellos se comprueba que ninguno de los argumentos es cero, lo que podría indicar que no se pudieron la creación de un temporal **XLOPER** o **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="a5926-109">Each checks to see that none of the arguments is zero, which would indicate that the creation of a temporary **XLOPER** or **XLOPER12** failed.</span></span> <span data-ttu-id="a5926-110">Si se produce un error, cada uno de ellos se imprime un mensaje de depuración.</span><span class="sxs-lookup"><span data-stu-id="a5926-110">If an error occurs, each prints a debug message.</span></span> <span data-ttu-id="a5926-111">Cuando haya terminado, cada uno de ellos libera toda la memoria temporal que se han creado para temporal s **XLOPER**y **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="a5926-111">When finished, each frees all temporary memory that might have been created for temporary **XLOPER**s and **XLOPER12**s.</span></span>
  
 <span data-ttu-id="a5926-112">**Excel12f** sólo se pueden llamar desde una DLL a partir de la biblioteca de API de C de Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="a5926-112">**Excel12f** can only be called from a DLL starting with the Excel 2007 C API library.</span></span> <span data-ttu-id="a5926-113">Además, sólo funciona cuando se ejecuta comenzando con Excel 2007 y se produce un error con **xlretFailed** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a5926-113">Furthermore, it only works when running starting with Excel 2007, and fails with **xlretFailed** otherwise.</span></span> 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a><span data-ttu-id="a5926-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5926-114">Parameters</span></span>

 <span data-ttu-id="a5926-115">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="a5926-115">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="a5926-116">Un número que indica el comando o la función que desea llamar.</span><span class="sxs-lookup"><span data-stu-id="a5926-116">A number indicating the command or function you want to call.</span></span> <span data-ttu-id="a5926-117">Para obtener más información, vea [Excel4/Excel12](excel4-excel12.md).</span><span class="sxs-lookup"><span data-stu-id="a5926-117">For more information, see [Excel4/Excel12](excel4-excel12.md).</span></span>
  
 <span data-ttu-id="a5926-118">_pxRes_</span><span class="sxs-lookup"><span data-stu-id="a5926-118">_pxRes_</span></span>
  
<span data-ttu-id="a5926-119">Un puntero al resultado de la función evaluada.</span><span class="sxs-lookup"><span data-stu-id="a5926-119">A pointer to result of the evaluated function.</span></span> <span data-ttu-id="a5926-120">Cualquier memoria señalado en el resultado habrá se hayan asignado mediante Excel y debe liberarse en una llamada a [xlFree](xlfree.md) una vez que ya no sea necesaria, o mediante la configuración **xlbitXLFree** si devolver a Excel.</span><span class="sxs-lookup"><span data-stu-id="a5926-120">Any memory pointed to in the result will have been allocated by Excel and should be freed in a call to [xlFree](xlfree.md) once it is no longer needed, or by setting **xlbitXLFree** if returning it to Excel.</span></span> 
  
 <span data-ttu-id="a5926-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="a5926-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="a5926-122">El número de argumentos que se pasan a la función.</span><span class="sxs-lookup"><span data-stu-id="a5926-122">The number of arguments that will be passed to the function.</span></span> <span data-ttu-id="a5926-123">Iniciar en Excel 2007, el límite es 255 argumentos.</span><span class="sxs-lookup"><span data-stu-id="a5926-123">Starting in Excel 2007, the limit is 255 arguments.</span></span> <span data-ttu-id="a5926-124">En versiones anteriores, el límite es 30.</span><span class="sxs-lookup"><span data-stu-id="a5926-124">In earlier versions, the limit is 30.</span></span>
  
 <span data-ttu-id="a5926-125">_argumento1..._</span><span class="sxs-lookup"><span data-stu-id="a5926-125">_argument1, ..._</span></span>
  
<span data-ttu-id="a5926-126">Los argumentos opcionales a la función.</span><span class="sxs-lookup"><span data-stu-id="a5926-126">The optional arguments to the function.</span></span> <span data-ttu-id="a5926-127">Todos los argumentos deben ser punteros a s **XLOPER**en el caso de **Excel**, o s **XLOPER12**en el caso de **Excel12f**.</span><span class="sxs-lookup"><span data-stu-id="a5926-127">All arguments must be pointers to **XLOPER**s in the case of **Excel**, or **XLOPER12**s in the case of **Excel12f**.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="a5926-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5926-128">Return value</span></span>

<span data-ttu-id="a5926-129">Ambas funciones devuelven el mismo error y los códigos de éxito como **Excel4**, **Excel4v**, **Excel12**y **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="a5926-129">Both functions return the same error and success codes as **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**.</span></span> <span data-ttu-id="a5926-130">Para obtener una descripción completa de estos códigos, vea [Excel4/Excel12](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="a5926-130">See [Excel4/Excel12](excel4-excel12.md) for a full description of these codes.</span></span> <span data-ttu-id="a5926-131">Además, estas funciones de Framework devuelven **xlretFailed** sin llamar a la API de C si un puntero NULL a un parámetro se detecta.</span><span class="sxs-lookup"><span data-stu-id="a5926-131">In addition, these Framework functions return **xlretFailed** without calling the C API if a NULL pointer to a parameter is detected.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a5926-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5926-132">Example</span></span>

<span data-ttu-id="a5926-133">En este ejemplo se pasa un argumento no válido para la función **Excel12f** , que envía un mensaje para el depurador.</span><span class="sxs-lookup"><span data-stu-id="a5926-133">This example passes a bad argument to the **Excel12f** function, which sends a message to the debugger.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="a5926-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="a5926-134">See also</span></span>



[<span data-ttu-id="a5926-135">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="a5926-135">Excel4/Excel12</span></span>](excel4-excel12.md)


[<span data-ttu-id="a5926-136">Funciones de la biblioteca de Framework</span><span class="sxs-lookup"><span data-stu-id="a5926-136">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

