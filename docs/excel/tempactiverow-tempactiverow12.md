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
- tempactiverow (función) [excel 2007], TempActiveRow12 (función) [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a406d6e5a8ffa91e103276cb39230058b4840614
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815696"
---
# <a name="tempactiverowtempactiverow12"></a><span data-ttu-id="01fe3-104">TempActiveRow/TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="01fe3-104">TempActiveRow/TempActiveRow12</span></span>

 <span data-ttu-id="01fe3-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="01fe3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="01fe3-106">Funciones de la biblioteca de Framework que creación un temporal **XLOPER**/ **XLOPER12** que contiene una referencia externa a una fila completa de la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="01fe3-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire row on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a><span data-ttu-id="01fe3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01fe3-107">Parameters</span></span>

 <span data-ttu-id="01fe3-108">_fila_</span><span class="sxs-lookup"><span data-stu-id="01fe3-108">_row_</span></span>
  
<span data-ttu-id="01fe3-109">Para hacer referencia a la fila.</span><span class="sxs-lookup"><span data-stu-id="01fe3-109">The row to be referenced.</span></span> <span data-ttu-id="01fe3-110">Argumentos de fila son de base ceros para que esa fila 1 se pasa como 0.</span><span class="sxs-lookup"><span data-stu-id="01fe3-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="01fe3-111">En Microsoft Office Excel 2003 y anteriores versiones y a partir de Excel 2007 que se ejecuta un libro en modo de compatibilidad, el valor máximo es 65.535 = 2 ^ 16-1 y es el valor máximo que puede consultarse por un número entero de WORD.</span><span class="sxs-lookup"><span data-stu-id="01fe3-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="01fe3-112">A partir de que ejecuta un libro de Excel 2007, el valor máximo es 1.048.575 = 2 ^ 1 a 20.</span><span class="sxs-lookup"><span data-stu-id="01fe3-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="01fe3-113">RW se define como un entero con signo de 32 bits en XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="01fe3-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="01fe3-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01fe3-114">Return value</span></span>

<span data-ttu-id="01fe3-115">Devuelve una referencia externa de **xltypeRef** a celdas de la fila que se pasó.</span><span class="sxs-lookup"><span data-stu-id="01fe3-115">Returns an **xltypeRef** external reference to row cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="01fe3-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01fe3-116">Example</span></span>

<span data-ttu-id="01fe3-117">En este ejemplo se usa la función **TempActiveRow12** para seleccionar fila 113.</span><span class="sxs-lookup"><span data-stu-id="01fe3-117">This example uses the **TempActiveRow12** function to select row 113.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="01fe3-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="01fe3-118">See also</span></span>



[<span data-ttu-id="01fe3-119">Funciones de la biblioteca de Framework</span><span class="sxs-lookup"><span data-stu-id="01fe3-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

