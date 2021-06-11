---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- función funcfib [excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb8f0c12c27fb2c95007eb5006c1d8b90970f3ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423674"
---
# <a name="funcfib"></a><span data-ttu-id="49b8b-104">FuncFib</span><span class="sxs-lookup"><span data-stu-id="49b8b-104">FuncFib</span></span>

 <span data-ttu-id="49b8b-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="49b8b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="49b8b-106">Función de hoja de cálculo definida por el usuario que calcula el número Nésima de Fibonacci.</span><span class="sxs-lookup"><span data-stu-id="49b8b-106">Example user-defined worksheet function that computes the Nth Fibonacci number.</span></span> <span data-ttu-id="49b8b-107">Cuando se carga GENERIC.xll, registra esta función para que se pueda llamar desde la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="49b8b-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a><span data-ttu-id="49b8b-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="49b8b-108">Parameters</span></span>

 <span data-ttu-id="49b8b-109">_pxN_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="49b8b-109">_pxN_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="49b8b-110">Valor de N para el que se requiere el número Nésima fibonacci.</span><span class="sxs-lookup"><span data-stu-id="49b8b-110">The value of N for which the Nth Fibonacci number is required.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="49b8b-111">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49b8b-111">Property value/Return value</span></span>

<span data-ttu-id="49b8b-112">(**xltypeNum LPXLOPER12** si se realiza correctamente **o xltypeErr de lo** contrario)</span><span class="sxs-lookup"><span data-stu-id="49b8b-112">(**xltypeNum LPXLOPER12** if successful or **xltypeErr** otherwise)</span></span> 
  
<span data-ttu-id="49b8b-113">Número Nésima fibonacci.</span><span class="sxs-lookup"><span data-stu-id="49b8b-113">The Nth Fibonacci number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="49b8b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="49b8b-114">Remarks</span></span>

<span data-ttu-id="49b8b-115">La función usa una variable estática definida dentro del bloque de funciones como el valor devuelto **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="49b8b-115">The function uses a static variable defined within the function block as the return value **XLOPER12**.</span></span> <span data-ttu-id="49b8b-116">Esto no es seguro para subprocesos, por lo que esta función y cualquier función de hoja de cálculo que use esta estrategia para devolver **XLOPER** s o **XLOPER12** s, no deben registrarse como seguros para subprocesos a partir de Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="49b8b-116">This is not thread safe, and so this function, and any worksheet function that uses this strategy for returning **XLOPER** s or **XLOPER12** s, should not be registered as thread safe starting in Excel 2007.</span></span>
  
### <a name="example"></a><span data-ttu-id="49b8b-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="49b8b-117">Example</span></span>

<span data-ttu-id="49b8b-118">Vea  `\SAMPLES\GENERIC\GENERIC.C` el código fuente de esta función.</span><span class="sxs-lookup"><span data-stu-id="49b8b-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="49b8b-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="49b8b-119">See also</span></span>



[<span data-ttu-id="49b8b-120">Funciones en la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="49b8b-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

