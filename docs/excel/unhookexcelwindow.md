---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- unhookexcelwindow (función)
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7b70bf4ed0ff45921df407605baa692c7621bca4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815713"
---
# <a name="unhookexcelwindow"></a><span data-ttu-id="9a6a3-104">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="9a6a3-104">UnhookExcelWindow</span></span>

 <span data-ttu-id="9a6a3-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9a6a3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9a6a3-106">Quita el **ExcelCursorProc** que se había instalado por **HookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-106">Removes the **ExcelCursorProc** that was previously installed by **HookExcelWindow**.</span></span> <span data-ttu-id="9a6a3-107">Esto habría se ha realizado el modo en que se llamó a **ExcelCursorProc** antes de la principal de Microsoft Excel **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-107">This would have been done so that **ExcelCursorProc** was called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="9a6a3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a6a3-108">Parameters</span></span>

 <span data-ttu-id="9a6a3-109">_hWndExcel_ (**Controlar**)</span><span class="sxs-lookup"><span data-stu-id="9a6a3-109">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="9a6a3-110">El identificador de Windows principal de Excel.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-110">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9a6a3-111">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a6a3-111">Property value/Return value</span></span>

<span data-ttu-id="9a6a3-112">La función no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-112">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9a6a3-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9a6a3-113">Remarks</span></span>

<span data-ttu-id="9a6a3-114">Esta función restaura el valor predeterminado de Excel **WndProc** con **SetWindowLong()** para restaurar la dirección que se guardó por **HookExcelWindow()**.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-114">This function restores the Excel default **WndProc** using **SetWindowLong()** to restore the address that was saved by **HookExcelWindow()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="9a6a3-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9a6a3-115">Example</span></span>

<span data-ttu-id="9a6a3-116">Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-116">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9a6a3-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a6a3-117">See also</span></span>



[<span data-ttu-id="9a6a3-118">Funciones de la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="9a6a3-118">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

