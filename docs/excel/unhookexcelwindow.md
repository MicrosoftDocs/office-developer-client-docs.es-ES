---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- función unhookexcelwindow
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: aef2734aeb4d9cf5df33e3d012cef309e8a1eb6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409450"
---
# <a name="unhookexcelwindow"></a><span data-ttu-id="b7276-104">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="b7276-104">UnhookExcelWindow</span></span>

 <span data-ttu-id="b7276-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b7276-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b7276-106">Quita el **ExcelCursorProc** instalado anteriormente por **HookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="b7276-106">Removes the **ExcelCursorProc** that was previously installed by **HookExcelWindow**.</span></span> <span data-ttu-id="b7276-107">Esto se habría hecho, de modo que se llamara a **ExcelCursorProc** antes que el **WndProc**principal de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="b7276-107">This would have been done so that **ExcelCursorProc** was called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="b7276-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="b7276-108">Parameters</span></span>

 <span data-ttu-id="b7276-109">_hWndExcel_ (**Controlador**)</span><span class="sxs-lookup"><span data-stu-id="b7276-109">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="b7276-110">El controlador principal de Windows de Excel.</span><span class="sxs-lookup"><span data-stu-id="b7276-110">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b7276-111">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7276-111">Property value/Return value</span></span>

<span data-ttu-id="b7276-112">La función no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="b7276-112">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b7276-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b7276-113">Remarks</span></span>

<span data-ttu-id="b7276-114">Esta función restaura el **WndProc** predeterminado de Excel mediante **SetWindowLong ()** para restaurar la dirección que guardó **HookExcelWindow ()**.</span><span class="sxs-lookup"><span data-stu-id="b7276-114">This function restores the Excel default **WndProc** using **SetWindowLong()** to restore the address that was saved by **HookExcelWindow()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="b7276-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b7276-115">Example</span></span>

<span data-ttu-id="b7276-116">Consulte `\SAMPLES\GENERIC\GENERIC.C` para obtener el código fuente de esta función.</span><span class="sxs-lookup"><span data-stu-id="b7276-116">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b7276-117">Ver también</span><span class="sxs-lookup"><span data-stu-id="b7276-117">See also</span></span>



[<span data-ttu-id="b7276-118">Funciones en la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="b7276-118">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

