---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- función func1 [excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 26439f1fb05aae2077844ce19935d9ff99e4f701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815634"
---
# <a name="func1"></a><span data-ttu-id="6a48c-104">Func1</span><span class="sxs-lookup"><span data-stu-id="6a48c-104">Func1</span></span>

 <span data-ttu-id="6a48c-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6a48c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6a48c-106">Función de hoja de cálculo definida por el usuario de ejemplo muestra la devolución de un valor de cadena estática.</span><span class="sxs-lookup"><span data-stu-id="6a48c-106">Example user-defined worksheet function demonstrates the return of a static string value.</span></span> <span data-ttu-id="6a48c-107">Cuando se carga GENERIC.xll, registra esta función para que se pueda llamar desde la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="6a48c-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a><span data-ttu-id="6a48c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a48c-108">Parameters</span></span>

 <span data-ttu-id="6a48c-109">_px_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="6a48c-109">_px_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="6a48c-110">Este argumento se omite y sólo sirve para Microsoft Excel para llamar a la función de desencadenador.</span><span class="sxs-lookup"><span data-stu-id="6a48c-110">This argument is ignored, and serves only to trigger Microsoft Excel to call the function.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="6a48c-111">Propiedad valor y valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a48c-111">Property value/Return value</span></span>

 <span data-ttu-id="6a48c-112">**LPXLOPER12**: siempre la cadena "Func1"</span><span class="sxs-lookup"><span data-stu-id="6a48c-112">**LPXLOPER12**: Always the string "Func1"</span></span>
  
### <a name="example"></a><span data-ttu-id="6a48c-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6a48c-113">Example</span></span>

<span data-ttu-id="6a48c-114">Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función.</span><span class="sxs-lookup"><span data-stu-id="6a48c-114">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6a48c-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="6a48c-115">See also</span></span>



[<span data-ttu-id="6a48c-116">Funciones en el archivo DLL genérica</span><span class="sxs-lookup"><span data-stu-id="6a48c-116">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

