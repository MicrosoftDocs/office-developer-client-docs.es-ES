---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- función funcfib [Excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb8f0c12c27fb2c95007eb5006c1d8b90970f3ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310839"
---
# <a name="funcfib"></a><span data-ttu-id="17566-104">FuncFib</span><span class="sxs-lookup"><span data-stu-id="17566-104">FuncFib</span></span>

 <span data-ttu-id="17566-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="17566-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="17566-106">Ejemplo de función de hoja de cálculo definida por el usuario que calcula el número de Fibonacci n.</span><span class="sxs-lookup"><span data-stu-id="17566-106">Example user-defined worksheet function that computes the Nth Fibonacci number.</span></span> <span data-ttu-id="17566-107">Cuando se carga GENERIC. XLL, se registra esta función para que se pueda llamar desde la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="17566-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a><span data-ttu-id="17566-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="17566-108">Parameters</span></span>

 <span data-ttu-id="17566-109">_pxN_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="17566-109">_pxN_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="17566-110">Valor de N para el que se requiere el número de Fibonacci n.</span><span class="sxs-lookup"><span data-stu-id="17566-110">The value of N for which the Nth Fibonacci number is required.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="17566-111">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17566-111">Property value/Return value</span></span>

<span data-ttu-id="17566-112">(**XLTYPENUM LPXLOPER12** si se realiza correctamente o **xltypeErr** de lo contrario)</span><span class="sxs-lookup"><span data-stu-id="17566-112">(**xltypeNum LPXLOPER12** if successful or **xltypeErr** otherwise)</span></span> 
  
<span data-ttu-id="17566-113">Número de Fibonacci n.</span><span class="sxs-lookup"><span data-stu-id="17566-113">The Nth Fibonacci number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="17566-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17566-114">Remarks</span></span>

<span data-ttu-id="17566-115">La función usa una variable estática definida en el bloque Function como el valor devuelto **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="17566-115">The function uses a static variable defined within the function block as the return value **XLOPER12**.</span></span> <span data-ttu-id="17566-116">Esto no es seguro para subprocesos, por lo que esta función y cualquier función de hoja de cálculo que use esta estrategia para devolver **XLOPER**s o **XLOPER12**, no deben registrarse como seguros para subprocesos a partir de Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="17566-116">This is not thread safe, and so this function, and any worksheet function that uses this strategy for returning **XLOPER**s or **XLOPER12**s, should not be registered as thread safe starting in Excel 2007.</span></span>
  
### <a name="example"></a><span data-ttu-id="17566-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="17566-117">Example</span></span>

<span data-ttu-id="17566-118">Consulte `\SAMPLES\GENERIC\GENERIC.C` para obtener el código fuente de esta función.</span><span class="sxs-lookup"><span data-stu-id="17566-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="17566-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="17566-119">See also</span></span>



[<span data-ttu-id="17566-120">Funciones en la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="17566-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

