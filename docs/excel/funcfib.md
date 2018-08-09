---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- funcfib (función) [excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8d1c97ea57e968aaedffca6b37ded3d875e87413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815632"
---
# <a name="funcfib"></a><span data-ttu-id="cc4c0-104">FuncFib</span><span class="sxs-lookup"><span data-stu-id="cc4c0-104">FuncFib</span></span>

 <span data-ttu-id="cc4c0-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cc4c0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cc4c0-106">Función de hoja de cálculo definida por el usuario de ejemplo que calcula el número de Fibonacci n.</span><span class="sxs-lookup"><span data-stu-id="cc4c0-106">Example user-defined worksheet function that computes the Nth Fibonacci number.</span></span> <span data-ttu-id="cc4c0-107">Cuando se carga GENERIC.xll, registra esta función para que se pueda llamar desde la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="cc4c0-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a><span data-ttu-id="cc4c0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc4c0-108">Parameters</span></span>

 <span data-ttu-id="cc4c0-109">_pxN_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="cc4c0-109">_pxN_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="cc4c0-110">El valor de N para la que se requiere el número de Fibonacci n.</span><span class="sxs-lookup"><span data-stu-id="cc4c0-110">The value of N for which the Nth Fibonacci number is required.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="cc4c0-111">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc4c0-111">Property value/Return value</span></span>

<span data-ttu-id="cc4c0-112">(**xltypeNum LPXLOPER12** si se realiza correctamente o **xltypeErr** en caso contrario)</span><span class="sxs-lookup"><span data-stu-id="cc4c0-112">(**xltypeNum LPXLOPER12** if successful or **xltypeErr** otherwise)</span></span> 
  
<span data-ttu-id="cc4c0-113">El número de Fibonacci n.</span><span class="sxs-lookup"><span data-stu-id="cc4c0-113">The Nth Fibonacci number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cc4c0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc4c0-114">Remarks</span></span>

<span data-ttu-id="cc4c0-115">La función utiliza una variable estática definida dentro del bloque de función como el valor devuelto **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="cc4c0-115">The function uses a static variable defined within the function block as the return value **XLOPER12**.</span></span> <span data-ttu-id="cc4c0-116">Esto no es seguro para subprocesos y, por lo que esta función y cualquier función de hoja de cálculo que utiliza esta estrategia para devolver **XLOPER**s o s **XLOPER12**, no se deben registrar como subprocesos de inicio en Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="cc4c0-116">This is not thread safe, and so this function, and any worksheet function that uses this strategy for returning **XLOPER**s or **XLOPER12**s, should not be registered as thread safe starting in Excel 2007.</span></span>
  
### <a name="example"></a><span data-ttu-id="cc4c0-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cc4c0-117">Example</span></span>

<span data-ttu-id="cc4c0-118">Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función.</span><span class="sxs-lookup"><span data-stu-id="cc4c0-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cc4c0-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc4c0-119">See also</span></span>



[<span data-ttu-id="cc4c0-120">Funciones de la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="cc4c0-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

