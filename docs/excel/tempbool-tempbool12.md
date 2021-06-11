---
title: TempBool/TempBool12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempBool
- TempBool12
keywords:
- función tempbool [excel 2007],Función TempBool12 [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c8c917f0004fe091413ea670f1cc562f1d701fa0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433720"
---
# <a name="tempbooltempbool12"></a><span data-ttu-id="9b920-104">TempBool/TempBool12</span><span class="sxs-lookup"><span data-stu-id="9b920-104">TempBool/TempBool12</span></span>

 <span data-ttu-id="9b920-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9b920-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9b920-106">Función de biblioteca de marcos que crea un /  **XLOPER XLOPER12** temporal que contiene **booleanos** **TRUE** o **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9b920-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing **Boolean** **TRUE** or **FALSE**.</span></span>
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a><span data-ttu-id="9b920-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="9b920-107">Parameters</span></span>

 <span data-ttu-id="9b920-108">_b_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="9b920-108">_b_ (**int**)</span></span>
  
<span data-ttu-id="9b920-109">Use 0 para devolver **FALSE**; use cualquier otro valor para devolver **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="9b920-109">Use 0 to return **FALSE**; use any other value to return **TRUE**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9b920-110">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b920-110">Property value/Return value</span></span>

<span data-ttu-id="9b920-111">Devuelve un **valor booleano xltypeBool** **que** contiene el valor lógico pasado.</span><span class="sxs-lookup"><span data-stu-id="9b920-111">Returns an **xltypeBool** **Boolean** containing the logical value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9b920-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b920-112">Example</span></span>

<span data-ttu-id="9b920-113">En el ejemplo siguiente se usa **la función TempBool12** para borrar la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="9b920-113">The following example uses the **TempBool12** function to clear the status bar.</span></span> <span data-ttu-id="9b920-114">La memoria temporal se libera [cuando se llama a la función Excel/Excel12f.](excel-excel12f.md)</span><span class="sxs-lookup"><span data-stu-id="9b920-114">Temporary memory is freed when the [Excel/Excel12f](excel-excel12f.md) function is called.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="9b920-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b920-115">See also</span></span>



[<span data-ttu-id="9b920-116">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="9b920-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

