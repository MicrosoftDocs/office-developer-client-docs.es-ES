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
- tempactiveref (función) [excel 2007], TempActiveRef12 (función) [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5c2e82dcaf9bf562048b5d2582ece1bd262b47eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815698"
---
# <a name="tempactivereftempactiveref12"></a><span data-ttu-id="23369-104">TempActiveRef/TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="23369-104">TempActiveRef/TempActiveRef12</span></span>

 <span data-ttu-id="23369-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="23369-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="23369-106">Función de la biblioteca de Framework que crea un temporal **XLOPER**/ **XLOPER12** que contiene una referencia externa a un bloque rectangular de celdas en la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="23369-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing an external reference to rectangular block of cells on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a><span data-ttu-id="23369-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23369-107">Parameters</span></span>

 <span data-ttu-id="23369-108">_rwFirst_</span><span class="sxs-lookup"><span data-stu-id="23369-108">_rwFirst_</span></span>
  
<span data-ttu-id="23369-109">La fila inicial de la referencia.</span><span class="sxs-lookup"><span data-stu-id="23369-109">The starting row of the reference.</span></span>
  
 <span data-ttu-id="23369-110">_rwLast_</span><span class="sxs-lookup"><span data-stu-id="23369-110">_rwLast_</span></span>
  
<span data-ttu-id="23369-111">La fila final de la referencia.</span><span class="sxs-lookup"><span data-stu-id="23369-111">The ending row of the reference.</span></span>
  
<span data-ttu-id="23369-112">Argumentos de fila son de base ceros para que esa fila 1 se pasa como 0.</span><span class="sxs-lookup"><span data-stu-id="23369-112">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="23369-113">En Microsoft Office Excel 2003 y anteriores versiones y a partir de Excel 2007 que se ejecuta un libro en modo de compatibilidad, el valor máximo es 65.535 = 2 ^ 16-1 y es el valor máximo que puede consultarse por un número entero de WORD.</span><span class="sxs-lookup"><span data-stu-id="23369-113">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="23369-114">A partir de que ejecuta un libro de Excel 2007, el valor máximo es 1.048.575 = 2 ^ 1 a 20.</span><span class="sxs-lookup"><span data-stu-id="23369-114">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="23369-115">RW se define como un entero con signo de 32 bits en XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="23369-115">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="23369-116">_colFirst_</span><span class="sxs-lookup"><span data-stu-id="23369-116">_colFirst_</span></span>
  
<span data-ttu-id="23369-117">El número de columna inicial de la referencia.</span><span class="sxs-lookup"><span data-stu-id="23369-117">The starting column number of the reference.</span></span>
  
 <span data-ttu-id="23369-118">_colLast_</span><span class="sxs-lookup"><span data-stu-id="23369-118">_colLast_</span></span>
  
<span data-ttu-id="23369-119">El número de columna final de la referencia.</span><span class="sxs-lookup"><span data-stu-id="23369-119">The ending column number of the reference.</span></span>
  
<span data-ttu-id="23369-120">Argumentos de la columna son de base ceros para que esa columna A se pasa como 0.</span><span class="sxs-lookup"><span data-stu-id="23369-120">Column arguments are zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="23369-121">En Excel 2003 y anteriores versiones y a partir de Excel 2007 que se ejecuta un libro en modo de compatibilidad, el valor máximo es 255 = 2 ^ 8-1 y es el valor máximo que se puede adoptar un entero de BYTE.</span><span class="sxs-lookup"><span data-stu-id="23369-121">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="23369-122">A partir de que ejecuta un libro de Excel 2007, el valor máximo es 16.383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="23369-122">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="23369-123">COL se define como un entero con signo de 32 bits en XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="23369-123">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="23369-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23369-124">Return value</span></span>

<span data-ttu-id="23369-125">Devuelve una referencia externa de **xltypeRef** a un bloque rectangular de celdas que se pasó.</span><span class="sxs-lookup"><span data-stu-id="23369-125">Returns an **xltypeRef** external reference to rectangular block of cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="23369-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="23369-126">Example</span></span>

<span data-ttu-id="23369-127">En este ejemplo se usa la función **TempActiveRef12** para seleccionar las celdas A105:C110.</span><span class="sxs-lookup"><span data-stu-id="23369-127">This example uses the **TempActiveRef12** function to select cells A105:C110.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="23369-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="23369-128">See also</span></span>



[<span data-ttu-id="23369-129">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="23369-129">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

