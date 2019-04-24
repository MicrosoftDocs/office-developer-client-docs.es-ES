---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- función hookexcelwindow [Excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4103bf3a95388d20efeb74fcd736aeb5520d0845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310832"
---
# <a name="hookexcelwindow"></a><span data-ttu-id="eee48-104">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="eee48-104">HookExcelWindow</span></span>

 <span data-ttu-id="eee48-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="eee48-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="eee48-106">Instala **ExcelCursorProc** de modo que se pueda llamar antes de la llamada **WndProc**principal de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="eee48-106">Installs **ExcelCursorProc** so that it is called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="eee48-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="eee48-107">Parameters</span></span>

 <span data-ttu-id="eee48-108">_hWndExcel_ (**Controlador**)</span><span class="sxs-lookup"><span data-stu-id="eee48-108">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="eee48-109">El controlador principal de Windows de Excel.</span><span class="sxs-lookup"><span data-stu-id="eee48-109">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="eee48-110">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eee48-110">Property value/Return value</span></span>

<span data-ttu-id="eee48-111">La función no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="eee48-111">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eee48-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eee48-112">Remarks</span></span>

<span data-ttu-id="eee48-113">La función obtiene la dirección del **WndProc** de Excel mediante el uso de **GetWindowLong ()**.</span><span class="sxs-lookup"><span data-stu-id="eee48-113">The function obtains the address of the Excel **WndProc** through the use of **GetWindowLong()**.</span></span> <span data-ttu-id="eee48-114">Almacena este valor en un global que se puede usar para llamar al **WndProc** predeterminado y también para restaurarlo.</span><span class="sxs-lookup"><span data-stu-id="eee48-114">It stores this value in a global that can be used to call the default **WndProc** and also to restore it.</span></span> <span data-ttu-id="eee48-115">Por último, reemplaza esta dirección con la dirección de **ExcelCursorProc** mediante **SetWindowLong ()**.</span><span class="sxs-lookup"><span data-stu-id="eee48-115">Finally, it replaces this address with the address of **ExcelCursorProc** using **SetWindowLong()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="eee48-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eee48-116">Example</span></span>

<span data-ttu-id="eee48-117">Consulte `\SAMPLES\GENERIC\GENERIC.C` para obtener el código fuente de esta función.</span><span class="sxs-lookup"><span data-stu-id="eee48-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eee48-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="eee48-118">See also</span></span>



[<span data-ttu-id="eee48-119">Funciones en la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="eee48-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

