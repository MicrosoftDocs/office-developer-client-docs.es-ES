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
- función tempbool [Excel 2007], TempBool12 [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c8c917f0004fe091413ea670f1cc562f1d701fa0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310356"
---
# <a name="tempbooltempbool12"></a><span data-ttu-id="d8ab7-104">TempBool/TempBool12</span><span class="sxs-lookup"><span data-stu-id="d8ab7-104">TempBool/TempBool12</span></span>

 <span data-ttu-id="d8ab7-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d8ab7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d8ab7-106">Función de biblioteca de Framework que crea un**XLOPER12** de **XLOPER**/ temporal que contiene **booleano** **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="d8ab7-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing **Boolean** **TRUE** or **FALSE**.</span></span>
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a><span data-ttu-id="d8ab7-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="d8ab7-107">Parameters</span></span>

 <span data-ttu-id="d8ab7-108">_b_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="d8ab7-108">_b_ (**int**)</span></span>
  
<span data-ttu-id="d8ab7-109">Use 0 para devolver **false**; use cualquier otro valor para devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="d8ab7-109">Use 0 to return **FALSE**; use any other value to return **TRUE**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d8ab7-110">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8ab7-110">Property value/Return value</span></span>

<span data-ttu-id="d8ab7-111">Devuelve un valor **booleano** **xltypeBool** que contiene el valor lógico pasado.</span><span class="sxs-lookup"><span data-stu-id="d8ab7-111">Returns an **xltypeBool** **Boolean** containing the logical value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d8ab7-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d8ab7-112">Example</span></span>

<span data-ttu-id="d8ab7-113">En el siguiente ejemplo, se usa la función **TempBool12** para borrar la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="d8ab7-113">The following example uses the **TempBool12** function to clear the status bar.</span></span> <span data-ttu-id="d8ab7-114">La memoria temporal se libera cuando se llama a la función [Excel/Excel12f](excel-excel12f.md) .</span><span class="sxs-lookup"><span data-stu-id="d8ab7-114">Temporary memory is freed when the [Excel/Excel12f](excel-excel12f.md) function is called.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="d8ab7-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8ab7-115">See also</span></span>



[<span data-ttu-id="d8ab7-116">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="d8ab7-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

