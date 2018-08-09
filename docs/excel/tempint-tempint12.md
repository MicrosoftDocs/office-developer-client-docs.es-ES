---
title: TempInt/TempInt12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempInt
- TempInt12
keywords:
- tempint12 (función) [excel 2007], TempInt (función) [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: eb1dd9be0c0b20e533d9cd8202f8878c43b997be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815706"
---
# <a name="tempinttempint12"></a><span data-ttu-id="fb926-104">TempInt/TempInt12</span><span class="sxs-lookup"><span data-stu-id="fb926-104">TempInt/TempInt12</span></span>

 <span data-ttu-id="fb926-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fb926-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fb926-106">Función de la biblioteca de Framework que crea un temporal **XLOPER**/ **XLOPER12** que contiene un número entero.</span><span class="sxs-lookup"><span data-stu-id="fb926-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** that contains an integer.</span></span> 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a><span data-ttu-id="fb926-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb926-107">Parameters</span></span>

 <span data-ttu-id="fb926-108">_i_</span><span class="sxs-lookup"><span data-stu-id="fb926-108">_i_</span></span>
  
<span data-ttu-id="fb926-109">El valor entero previsto.</span><span class="sxs-lookup"><span data-stu-id="fb926-109">The intended integer value.</span></span> <span data-ttu-id="fb926-110">Tenga en cuenta que el entero **XLOPER** es un entero de 16 bits (short int), mientras que el entero **XLOPER12** es un entero de 32 bits con signo (int [largo]).</span><span class="sxs-lookup"><span data-stu-id="fb926-110">Note that the **XLOPER** integer is a signed 16-bit integer (short int), whereas the **XLOPER12** integer is a signed 32-bit integer ([long] int).</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="fb926-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb926-111">Return value</span></span>

<span data-ttu-id="fb926-112">Devuelve un entero **xltypeInt** que contiene el valor que se pasó.</span><span class="sxs-lookup"><span data-stu-id="fb926-112">Returns an **xltypeInt** integer containing the value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="fb926-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb926-113">Example</span></span>

<span data-ttu-id="fb926-114">En este ejemplo se usa la función **TempInt12** para pasar un argumento a **xlfGetWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="fb926-114">This example uses the **TempInt12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempIntExample(void)
{
    XLOPER12 xRes;
    Excel12f(xlfGetWorkspace, (LPXLOPER12)&xRes, 1, TempInt12(44));
    Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="fb926-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb926-115">See also</span></span>



[<span data-ttu-id="fb926-116">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="fb926-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

