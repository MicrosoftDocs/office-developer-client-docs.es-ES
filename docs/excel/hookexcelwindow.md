---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- hookexcelwindow (función) [excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8965cc6b1e3d24001c42744f2ee7d447aa4c79b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815645"
---
# <a name="hookexcelwindow"></a><span data-ttu-id="c7efd-104">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="c7efd-104">HookExcelWindow</span></span>

 <span data-ttu-id="c7efd-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c7efd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c7efd-106">Instala **ExcelCursorProc** para que se le llama antes de la principal de Microsoft Excel **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="c7efd-106">Installs **ExcelCursorProc** so that it is called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="c7efd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7efd-107">Parameters</span></span>

 <span data-ttu-id="c7efd-108">_hWndExcel_ (**Controlar**)</span><span class="sxs-lookup"><span data-stu-id="c7efd-108">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="c7efd-109">El identificador de Windows principal de Excel.</span><span class="sxs-lookup"><span data-stu-id="c7efd-109">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c7efd-110">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7efd-110">Property value/Return value</span></span>

<span data-ttu-id="c7efd-111">La función no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="c7efd-111">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c7efd-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c7efd-112">Remarks</span></span>

<span data-ttu-id="c7efd-113">La función obtiene la dirección de Excel **WndProc** mediante el uso de **GetWindowLong()**.</span><span class="sxs-lookup"><span data-stu-id="c7efd-113">The function obtains the address of the Excel **WndProc** through the use of **GetWindowLong()**.</span></span> <span data-ttu-id="c7efd-114">Este valor almacena en global que se puede usar el valor predeterminado **WndProc** de llamadas y restaurarlo.</span><span class="sxs-lookup"><span data-stu-id="c7efd-114">It stores this value in a global that can be used to call the default **WndProc** and also to restore it.</span></span> <span data-ttu-id="c7efd-115">Por último, esta dirección reemplaza con la dirección de **ExcelCursorProc** con **SetWindowLong()**.</span><span class="sxs-lookup"><span data-stu-id="c7efd-115">Finally, it replaces this address with the address of **ExcelCursorProc** using **SetWindowLong()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="c7efd-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7efd-116">Example</span></span>

<span data-ttu-id="c7efd-117">Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función.</span><span class="sxs-lookup"><span data-stu-id="c7efd-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7efd-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7efd-118">See also</span></span>



[<span data-ttu-id="c7efd-119">Funciones de la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="c7efd-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

