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
- tempactivecolumn12 (función) [excel 2007], TempActiveColumn (función) [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ac3dbb0bb43527f790e6934d73bee30a33f8555f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815701"
---
# <a name="tempactivecolumntempactivecolumn12"></a><span data-ttu-id="538ba-104">TempActiveColumn/TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="538ba-104">TempActiveColumn/TempActiveColumn12</span></span>

 <span data-ttu-id="538ba-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="538ba-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="538ba-106">Funciones de la biblioteca de Framework que creación un temporal **XLOPER**/ **XLOPER12** que contiene una referencia externa a una columna completa en la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="538ba-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire column on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a><span data-ttu-id="538ba-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="538ba-107">Parameters</span></span>

 <span data-ttu-id="538ba-108">_col_ (**Bytes**)</span><span class="sxs-lookup"><span data-stu-id="538ba-108">_col_ (**BYTE**)</span></span>
  
<span data-ttu-id="538ba-109">Para hacer referencia a la columna.</span><span class="sxs-lookup"><span data-stu-id="538ba-109">The column to be referenced.</span></span> <span data-ttu-id="538ba-110">Esto es basado en cero, por lo que una columna se pasa como 0.</span><span class="sxs-lookup"><span data-stu-id="538ba-110">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="538ba-111">En Microsoft Office Excel 2003 y anteriores versiones y a partir de Excel 2007 que se ejecuta un libro en modo de compatibilidad, el valor máximo es 255 = 2 ^ 8-1 y es el valor máximo que se puede adoptar un entero de BYTE.</span><span class="sxs-lookup"><span data-stu-id="538ba-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="538ba-112">A partir de que ejecuta un libro de Excel 2007, el valor máximo es 16.383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="538ba-112">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="538ba-113">COL se define como un entero con signo de 32 bits en XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="538ba-113">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="538ba-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="538ba-114">Return value</span></span>

<span data-ttu-id="538ba-115">Devuelve una referencia externa de **xltypeRef** a la columna que se pasó.</span><span class="sxs-lookup"><span data-stu-id="538ba-115">Returns an **xltypeRef** external reference to the column passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="538ba-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="538ba-116">Example</span></span>

<span data-ttu-id="538ba-117">En el ejemplo siguiente, se utiliza **TempActiveColumn12** para seleccionar toda la columna B.</span><span class="sxs-lookup"><span data-stu-id="538ba-117">The following example uses **TempActiveColumn12** to select the entire column B.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="538ba-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="538ba-118">See also</span></span>



[<span data-ttu-id="538ba-119">Funciones de la biblioteca de Framework</span><span class="sxs-lookup"><span data-stu-id="538ba-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

