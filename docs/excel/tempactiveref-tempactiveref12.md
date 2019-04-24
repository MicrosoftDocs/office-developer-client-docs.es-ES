---
title: TempActiveRef/TempActiveRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRef
- TempActiveRef12
keywords:
- función tempactiveref [Excel 2007], TempActiveRef12 [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58feee8f43e0f90f710c9e4387684dcb6d173a7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301571"
---
# <a name="tempactivereftempactiveref12"></a><span data-ttu-id="7bf5b-104">TempActiveRef/TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="7bf5b-104">TempActiveRef/TempActiveRef12</span></span>

 <span data-ttu-id="7bf5b-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7bf5b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7bf5b-106">Función de biblioteca de .NET Framework que crea un**XLOPER12** de **XLOPER**/ temporal que contiene una referencia externa al bloque rectangular de celdas de la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="7bf5b-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing an external reference to rectangular block of cells on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a><span data-ttu-id="7bf5b-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="7bf5b-107">Parameters</span></span>

 <span data-ttu-id="7bf5b-108">_rwFirst_</span><span class="sxs-lookup"><span data-stu-id="7bf5b-108">_rwFirst_</span></span>
  
<span data-ttu-id="7bf5b-109">La fila inicial de la referencia.</span><span class="sxs-lookup"><span data-stu-id="7bf5b-109">The starting row of the reference.</span></span>
  
 <span data-ttu-id="7bf5b-110">_rwLast_</span><span class="sxs-lookup"><span data-stu-id="7bf5b-110">_rwLast_</span></span>
  
<span data-ttu-id="7bf5b-111">La fila final de la referencia.</span><span class="sxs-lookup"><span data-stu-id="7bf5b-111">The ending row of the reference.</span></span>
  
<span data-ttu-id="7bf5b-112">Los argumentos de fila están basados en cero, de modo que la fila 1 se pasa como 0.</span><span class="sxs-lookup"><span data-stu-id="7bf5b-112">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="7bf5b-113">En Microsoft Office Excel 2003 y versiones anteriores, y a partir de Excel 2007 ejecutar un libro en modo de compatibilidad, el valor máximo es 65.535 = 2 ^ 16-1 y es el valor máximo que puede tomar un entero de palabra.</span><span class="sxs-lookup"><span data-stu-id="7bf5b-113">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="7bf5b-114">A partir de Excel 2007, al ejecutar un libro, el valor máximo es 1.048.575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="7bf5b-114">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="7bf5b-115">RW se define como un entero con signo de 32 bits en XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="7bf5b-115">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="7bf5b-116">_colFirst_</span><span class="sxs-lookup"><span data-stu-id="7bf5b-116">_colFirst_</span></span>
  
<span data-ttu-id="7bf5b-117">Número de la columna inicial de la referencia.</span><span class="sxs-lookup"><span data-stu-id="7bf5b-117">The starting column number of the reference.</span></span>
  
 <span data-ttu-id="7bf5b-118">_colLast_</span><span class="sxs-lookup"><span data-stu-id="7bf5b-118">_colLast_</span></span>
  
<span data-ttu-id="7bf5b-119">Número de columna final de la referencia.</span><span class="sxs-lookup"><span data-stu-id="7bf5b-119">The ending column number of the reference.</span></span>
  
<span data-ttu-id="7bf5b-120">Los argumentos de columna están basados en cero, por lo que la columna A se pasa como 0.</span><span class="sxs-lookup"><span data-stu-id="7bf5b-120">Column arguments are zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="7bf5b-121">En Excel 2003 y versiones anteriores, y a partir de Excel 2007 ejecutar un libro en modo de compatibilidad, el valor máximo es 255 = 2 ^ 8-1 y es el valor máximo que puede tomar un entero de BYTEs.</span><span class="sxs-lookup"><span data-stu-id="7bf5b-121">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="7bf5b-122">A partir de Excel 2007, al ejecutar un libro, el valor máximo es 16.383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="7bf5b-122">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="7bf5b-123">COL se define como un entero con signo de 32 bits en XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="7bf5b-123">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="7bf5b-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7bf5b-124">Return value</span></span>

<span data-ttu-id="7bf5b-125">Devuelve una referencia externa **xltypeRef** al bloque de celdas rectangular que se ha pasado.</span><span class="sxs-lookup"><span data-stu-id="7bf5b-125">Returns an **xltypeRef** external reference to rectangular block of cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="7bf5b-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7bf5b-126">Example</span></span>

<span data-ttu-id="7bf5b-127">En este ejemplo, se usa la función **TempActiveRef12** para seleccionar las celdas A105: C110.</span><span class="sxs-lookup"><span data-stu-id="7bf5b-127">This example uses the **TempActiveRef12** function to select cells A105:C110.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="7bf5b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7bf5b-128">See also</span></span>



[<span data-ttu-id="7bf5b-129">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="7bf5b-129">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

