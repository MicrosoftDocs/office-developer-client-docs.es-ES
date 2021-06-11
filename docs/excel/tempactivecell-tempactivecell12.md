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
- función tempactivecell12 [excel 2007], función TempActiveCell [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f9bdb4cd9919d0e52654a3996ede99c4d1b35cc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413195"
---
# <a name="tempactivecelltempactivecell12"></a><span data-ttu-id="d8820-104">TempActiveCell/TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="d8820-104">TempActiveCell/TempActiveCell12</span></span>

 <span data-ttu-id="d8820-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d8820-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d8820-106">Funciones de biblioteca de marcos que crean un /  **XLOPER XLOPER12** temporal que contiene una referencia externa a una celda de la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="d8820-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to a cell on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a><span data-ttu-id="d8820-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="d8820-107">Parameters</span></span>

 <span data-ttu-id="d8820-108">_fila_</span><span class="sxs-lookup"><span data-stu-id="d8820-108">_row_</span></span>
  
<span data-ttu-id="d8820-109">Fila a la que se va a hacer referencia.</span><span class="sxs-lookup"><span data-stu-id="d8820-109">The row to be referenced.</span></span> <span data-ttu-id="d8820-110">Los argumentos row están basados en cero para que la fila 1 se pase como 0.</span><span class="sxs-lookup"><span data-stu-id="d8820-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="d8820-111">En Microsoft Office Excel 2003 y versiones anteriores, y a partir de Excel 2007 ejecutando un libro en modo de compatibilidad, el valor máximo es 65.535 = 2^16 - 1 y es el valor máximo que puede tomar un entero de WORD.</span><span class="sxs-lookup"><span data-stu-id="d8820-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="d8820-112">A partir Excel 2007 que ejecuta un libro, el valor máximo es 1.048.575 = 2^20 - 1.</span><span class="sxs-lookup"><span data-stu-id="d8820-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="d8820-113">RW se define como un entero con signo de 32 bits en XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="d8820-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="d8820-114">_col_</span><span class="sxs-lookup"><span data-stu-id="d8820-114">_col_</span></span>
  
<span data-ttu-id="d8820-115">Columna a la que se debe hacer referencia.</span><span class="sxs-lookup"><span data-stu-id="d8820-115">The column to be referenced.</span></span> <span data-ttu-id="d8820-116">Se trata de una base cero para que la columna A se pase como 0.</span><span class="sxs-lookup"><span data-stu-id="d8820-116">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="d8820-117">En Excel 2003 y versiones anteriores, y a partir de Excel 2007 ejecutando un libro en modo de compatibilidad, el valor máximo es 255 = 2^8 - 1 y es el valor máximo que puede tomar un entero BYTE.</span><span class="sxs-lookup"><span data-stu-id="d8820-117">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="d8820-118">A partir Excel 2007 que ejecuta un libro, el valor máximo es 16.383 = 2^14 - 1.</span><span class="sxs-lookup"><span data-stu-id="d8820-118">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="d8820-119">COL se define como un entero con signo de 32 bits en XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="d8820-119">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="d8820-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8820-120">Return value</span></span>

<span data-ttu-id="d8820-121">Devuelve una **referencia externa xltypeRef** a la celda pasada.</span><span class="sxs-lookup"><span data-stu-id="d8820-121">Returns an **xltypeRef** external reference to the cell passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d8820-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d8820-122">Example</span></span>

<span data-ttu-id="d8820-123">En el ejemplo siguiente se **usa TempActiveCell12 para** mostrar el contenido de B94 en la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="d8820-123">The following example uses **TempActiveCell12** to display the contents of B94 on the active sheet.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="d8820-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8820-124">See also</span></span>



[<span data-ttu-id="d8820-125">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="d8820-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

