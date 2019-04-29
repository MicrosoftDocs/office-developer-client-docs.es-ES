---
title: TempActiveRow/TempActiveRow12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRow
- TempActiveRow12
keywords:
- función tempactiverow [Excel 2007], TempActiveRow12 [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1f89c458a521b41e4f172f8a6c53526440bb472b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413111"
---
# <a name="tempactiverowtempactiverow12"></a><span data-ttu-id="ef482-104">TempActiveRow/TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="ef482-104">TempActiveRow/TempActiveRow12</span></span>

 <span data-ttu-id="ef482-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ef482-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ef482-106">Funciones de biblioteca de .NET Framework que crean una**XLOPER12** de **XLOPER**/ temporal que contiene una referencia externa a una fila completa de la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="ef482-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire row on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a><span data-ttu-id="ef482-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="ef482-107">Parameters</span></span>

 <span data-ttu-id="ef482-108">_columna_</span><span class="sxs-lookup"><span data-stu-id="ef482-108">_row_</span></span>
  
<span data-ttu-id="ef482-109">La fila a la que se va a hacer referencia.</span><span class="sxs-lookup"><span data-stu-id="ef482-109">The row to be referenced.</span></span> <span data-ttu-id="ef482-110">Los argumentos de fila están basados en cero, de modo que la fila 1 se pasa como 0.</span><span class="sxs-lookup"><span data-stu-id="ef482-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="ef482-111">En Microsoft Office Excel 2003 y versiones anteriores, y a partir de Excel 2007 ejecutar un libro en modo de compatibilidad, el valor máximo es 65.535 = 2 ^ 16-1 y es el valor máximo que puede tomar un entero de palabra.</span><span class="sxs-lookup"><span data-stu-id="ef482-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="ef482-112">A partir de Excel 2007, al ejecutar un libro, el valor máximo es 1.048.575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="ef482-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="ef482-113">RW se define como un entero con signo de 32 bits en XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="ef482-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="ef482-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef482-114">Return value</span></span>

<span data-ttu-id="ef482-115">Devuelve una referencia externa **xltypeRef** a las celdas de fila que se han pasado.</span><span class="sxs-lookup"><span data-stu-id="ef482-115">Returns an **xltypeRef** external reference to row cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ef482-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ef482-116">Example</span></span>

<span data-ttu-id="ef482-117">En este ejemplo, se usa la función **TempActiveRow12** para seleccionar la fila 113.</span><span class="sxs-lookup"><span data-stu-id="ef482-117">This example uses the **TempActiveRow12** function to select row 113.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="ef482-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="ef482-118">See also</span></span>



[<span data-ttu-id="ef482-119">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="ef482-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

