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
- tempbool (función) [excel 2007], TempBool12 (función) [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 30874e7b918d8cd780bef60b4b02de1319f0f9ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815700"
---
# <a name="tempbooltempbool12"></a><span data-ttu-id="08b00-104">TempBool/TempBool12</span><span class="sxs-lookup"><span data-stu-id="08b00-104">TempBool/TempBool12</span></span>

 <span data-ttu-id="08b00-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="08b00-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="08b00-106">Función de la biblioteca de Framework que crea un temporal **XLOPER**/ **XLOPER12** que contiene **Boolean** **es TRUE** o **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="08b00-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing **Boolean** **TRUE** or **FALSE**.</span></span>
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a><span data-ttu-id="08b00-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08b00-107">Parameters</span></span>

 <span data-ttu-id="08b00-108">_b_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="08b00-108">_b_ (**int**)</span></span>
  
<span data-ttu-id="08b00-109">Use 0 para devolver **FALSE**; Use cualquier otro valor para devolver **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="08b00-109">Use 0 to return **FALSE**; use any other value to return **TRUE**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="08b00-110">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08b00-110">Property value/Return value</span></span>

<span data-ttu-id="08b00-111">Devuelve un **Boolean** que contiene el valor lógico que se pasó **xltypeBool** .</span><span class="sxs-lookup"><span data-stu-id="08b00-111">Returns an **xltypeBool** **Boolean** containing the logical value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="08b00-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="08b00-112">Example</span></span>

<span data-ttu-id="08b00-113">En el ejemplo siguiente se usa la función **TempBool12** para borrar la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="08b00-113">The following example uses the **TempBool12** function to clear the status bar.</span></span> <span data-ttu-id="08b00-114">Cuando se llama a la función de [Excel/Excel12f](excel-excel12f.md) , se libera memoria temporal.</span><span class="sxs-lookup"><span data-stu-id="08b00-114">Temporary memory is freed when the [Excel/Excel12f](excel-excel12f.md) function is called.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="08b00-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="08b00-115">See also</span></span>



[<span data-ttu-id="08b00-116">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="08b00-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

