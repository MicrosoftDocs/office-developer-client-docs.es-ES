---
title: TempActiveColumn/TempActiveColumn12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveColumn
- TempActiveColumn12
keywords:
- función tempactivecolumn12 [Excel 2007], TempActiveColumn [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d1399a407e3e269b78c7afbde8ff32c126b4b1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417878"
---
# <a name="tempactivecolumntempactivecolumn12"></a><span data-ttu-id="6643e-104">TempActiveColumn/TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="6643e-104">TempActiveColumn/TempActiveColumn12</span></span>

 <span data-ttu-id="6643e-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6643e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6643e-106">Funciones de biblioteca de .NET Framework que crean una**XLOPER12** de **XLOPER**/ temporal que contiene una referencia externa a una columna completa de la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="6643e-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire column on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a><span data-ttu-id="6643e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="6643e-107">Parameters</span></span>

 <span data-ttu-id="6643e-108">_col_ (**Byte**)</span><span class="sxs-lookup"><span data-stu-id="6643e-108">_col_ (**BYTE**)</span></span>
  
<span data-ttu-id="6643e-109">Columna a la que se va a hacer referencia.</span><span class="sxs-lookup"><span data-stu-id="6643e-109">The column to be referenced.</span></span> <span data-ttu-id="6643e-110">Se basa en cero para que la columna A se pase como 0.</span><span class="sxs-lookup"><span data-stu-id="6643e-110">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="6643e-111">En Microsoft Office Excel 2003 y versiones anteriores, y a partir de Excel 2007 ejecutar un libro en modo de compatibilidad, el valor máximo es 255 = 2 ^ 8-1 y es el valor máximo que puede tomar un entero de BYTEs.</span><span class="sxs-lookup"><span data-stu-id="6643e-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="6643e-112">A partir de Excel 2007, al ejecutar un libro, el valor máximo es 16.383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="6643e-112">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="6643e-113">COL se define como un entero con signo de 32 bits en XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="6643e-113">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="6643e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6643e-114">Return value</span></span>

<span data-ttu-id="6643e-115">Devuelve una referencia externa **xltypeRef** a la columna que se ha pasado.</span><span class="sxs-lookup"><span data-stu-id="6643e-115">Returns an **xltypeRef** external reference to the column passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6643e-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6643e-116">Example</span></span>

<span data-ttu-id="6643e-117">En el siguiente ejemplo, se usa **TempActiveColumn12** para seleccionar toda la columna B.</span><span class="sxs-lookup"><span data-stu-id="6643e-117">The following example uses **TempActiveColumn12** to select the entire column B.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="6643e-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="6643e-118">See also</span></span>



[<span data-ttu-id="6643e-119">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="6643e-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

