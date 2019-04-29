---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- función FUNC1 [Excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a3d3c6bbd529f43bd75b31b9348498928390a8f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408918"
---
# <a name="func1"></a><span data-ttu-id="af5f1-104">Func1</span><span class="sxs-lookup"><span data-stu-id="af5f1-104">Func1</span></span>

 <span data-ttu-id="af5f1-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="af5f1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="af5f1-106">Ejemplo de función de hoja de cálculo definida por el usuario muestra la devolución de un valor de cadena estática.</span><span class="sxs-lookup"><span data-stu-id="af5f1-106">Example user-defined worksheet function demonstrates the return of a static string value.</span></span> <span data-ttu-id="af5f1-107">Cuando se carga GENERIC. XLL, se registra esta función para que se pueda llamar desde la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="af5f1-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a><span data-ttu-id="af5f1-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="af5f1-108">Parameters</span></span>

 <span data-ttu-id="af5f1-109">_PX_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="af5f1-109">_px_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="af5f1-110">Este argumento se omite y solo sirve para desencadenar a Microsoft Excel para llamar a la función.</span><span class="sxs-lookup"><span data-stu-id="af5f1-110">This argument is ignored, and serves only to trigger Microsoft Excel to call the function.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="af5f1-111">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af5f1-111">Property value/Return value</span></span>

 <span data-ttu-id="af5f1-112">**LPXLOPER12**: siempre es la cadena "Func1"</span><span class="sxs-lookup"><span data-stu-id="af5f1-112">**LPXLOPER12**: Always the string "Func1"</span></span>
  
### <a name="example"></a><span data-ttu-id="af5f1-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="af5f1-113">Example</span></span>

<span data-ttu-id="af5f1-114">Consulte `\SAMPLES\GENERIC\GENERIC.C` para obtener el código fuente de esta función.</span><span class="sxs-lookup"><span data-stu-id="af5f1-114">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="af5f1-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="af5f1-115">See also</span></span>



[<span data-ttu-id="af5f1-116">Funciones en la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="af5f1-116">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

