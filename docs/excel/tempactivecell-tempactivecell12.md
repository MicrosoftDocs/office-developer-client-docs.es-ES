---
title: TempActiveCell/TempActiveCell12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveCell
- TempActiveCell12
keywords:
- tempactivecell12 (función) [excel 2007], TempActiveCell (función) [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8ad409a76195d67fa61e7991ce6527c40e0a3265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815695"
---
# <a name="tempactivecelltempactivecell12"></a><span data-ttu-id="86a1f-104">TempActiveCell/TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="86a1f-104">TempActiveCell/TempActiveCell12</span></span>

 <span data-ttu-id="86a1f-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="86a1f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="86a1f-106">Funciones de la biblioteca de Framework que creación un temporal **XLOPER**/ **XLOPER12** que contiene una referencia externa a una celda de la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="86a1f-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to a cell on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a><span data-ttu-id="86a1f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86a1f-107">Parameters</span></span>

 <span data-ttu-id="86a1f-108">_row_</span><span class="sxs-lookup"><span data-stu-id="86a1f-108">_row_</span></span>
  
<span data-ttu-id="86a1f-109">Para hacer referencia a la fila.</span><span class="sxs-lookup"><span data-stu-id="86a1f-109">The row to be referenced.</span></span> <span data-ttu-id="86a1f-110">Argumentos de fila son de base ceros para que esa fila 1 se pasa como 0.</span><span class="sxs-lookup"><span data-stu-id="86a1f-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="86a1f-111">En Microsoft Office Excel 2003 y anteriores versiones y a partir de Excel 2007 que se ejecuta un libro en modo de compatibilidad, el valor máximo es 65.535 = 2 ^ 16-1 y es el valor máximo que puede consultarse por un número entero de WORD.</span><span class="sxs-lookup"><span data-stu-id="86a1f-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="86a1f-112">A partir de que ejecuta un libro de Excel 2007, el valor máximo es 1.048.575 = 2 ^ 1 a 20.</span><span class="sxs-lookup"><span data-stu-id="86a1f-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="86a1f-113">RW se define como un entero con signo de 32 bits en XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="86a1f-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="86a1f-114">_Col_</span><span class="sxs-lookup"><span data-stu-id="86a1f-114">_col_</span></span>
  
<span data-ttu-id="86a1f-115">Para hacer referencia a la columna.</span><span class="sxs-lookup"><span data-stu-id="86a1f-115">The column to be referenced.</span></span> <span data-ttu-id="86a1f-116">Esto es basado en cero, por lo que una columna se pasa como 0.</span><span class="sxs-lookup"><span data-stu-id="86a1f-116">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="86a1f-117">En Excel 2003 y anteriores versiones y a partir de Excel 2007 que se ejecuta un libro en modo de compatibilidad, el valor máximo es 255 = 2 ^ 8-1 y es el valor máximo que se puede adoptar un entero de BYTE.</span><span class="sxs-lookup"><span data-stu-id="86a1f-117">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="86a1f-118">A partir de que ejecuta un libro de Excel 2007, el valor máximo es 16.383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="86a1f-118">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="86a1f-119">COL se define como un entero con signo de 32 bits en XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="86a1f-119">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="86a1f-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86a1f-120">Return value</span></span>

<span data-ttu-id="86a1f-121">Devuelve una referencia externa de **xltypeRef** a la celda que se pasó.</span><span class="sxs-lookup"><span data-stu-id="86a1f-121">Returns an **xltypeRef** external reference to the cell passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="86a1f-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="86a1f-122">Example</span></span>

<span data-ttu-id="86a1f-123">El siguiente ejemplo utiliza **TempActiveCell12** para mostrar el contenido de B94 en la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="86a1f-123">The following example uses **TempActiveCell12** to display the contents of B94 on the active sheet.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="86a1f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="86a1f-124">See also</span></span>



[<span data-ttu-id="86a1f-125">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="86a1f-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

