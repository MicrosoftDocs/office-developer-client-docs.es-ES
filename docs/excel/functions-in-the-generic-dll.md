---
title: Funciones de la DLL genérica
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- dll genérica [excel 2007], functions,functions [Excel 2007], DLL genérica
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3064e1a09ad8850e121da678f3702a6236574599
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420601"
---
# <a name="functions-in-the-generic-dll"></a><span data-ttu-id="c7477-104">Funciones de la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="c7477-104">Functions in the Generic DLL</span></span>

 <span data-ttu-id="c7477-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c7477-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c7477-106">La carpeta contiene Microsoft Visual Studio archivos de proyecto y archivos de código fuente necesarios para `\EXAMPLES\GENERIC\` compilar el ejemplo DLL GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="c7477-106">The folder  `\EXAMPLES\GENERIC\` contains Microsoft Visual Studio project files and source code files that are needed to compile the example DLL GENERIC.xll.</span></span> <span data-ttu-id="c7477-107">Puede usar este proyecto como plantilla para escribir sus propios Microsoft Excel XLLs.</span><span class="sxs-lookup"><span data-stu-id="c7477-107">You can use this project as a template for writing your own Microsoft Excel XLLs.</span></span> <span data-ttu-id="c7477-108">El código fuente de este proyecto muestra muchas de las características de la API Excel C.</span><span class="sxs-lookup"><span data-stu-id="c7477-108">The source code in this project demonstrates many of the features of the Excel C API.</span></span> 
  
<span data-ttu-id="c7477-109">Al cargar GENERIC.xll, se crea un nuevo **menú Genérico** con cuatro comandos:</span><span class="sxs-lookup"><span data-stu-id="c7477-109">When you load GENERIC.xll, it creates a new **Generic** menu with four commands:</span></span> 
  
- <span data-ttu-id="c7477-110">**Cuadro** de diálogo: muestra Microsoft Excel cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7477-110">**Dialog** - Displays a Microsoft Excel dialog box.</span></span> 
    
- <span data-ttu-id="c7477-111">**Baile:** mueve la selección hasta que presiona la **tecla ESC.**</span><span class="sxs-lookup"><span data-stu-id="c7477-111">**Dance** - Moves the selection around until you press the **ESC** key.</span></span> 
    
- <span data-ttu-id="c7477-112">**Cuadro de diálogo** nativo: muestra Windows cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7477-112">**Native Dialog** - Displays a Windows dialog box.</span></span> 
    
- <span data-ttu-id="c7477-113">**Exit:** descarga GENERIC.xll y quita el **menú Genérico.**</span><span class="sxs-lookup"><span data-stu-id="c7477-113">**Exit** - Unloads GENERIC.xll and removes the **Generic** menu.</span></span> 
    
<span data-ttu-id="c7477-114">GENERIC.xll también proporciona tres funciones de hoja de cálculo, Func1, FuncSum y FuncFib, que se pueden usar siempre que se cargue GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="c7477-114">GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded.</span></span> <span data-ttu-id="c7477-115">GENERIC.xll se puede cargar con el Administrador de complementos o se carga si estaba activo al final normal de la última Excel sesión.</span><span class="sxs-lookup"><span data-stu-id="c7477-115">GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.</span></span>
  
<span data-ttu-id="c7477-116">Este proyecto usa la biblioteca de marcos (FRMWRK32.lib).</span><span class="sxs-lookup"><span data-stu-id="c7477-116">This project uses the framework library (FRMWRK32.lib).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="c7477-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c7477-117">In this section</span></span>

[<span data-ttu-id="c7477-118">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="c7477-118">DIALOGMsgProc</span></span>](dialogmsgproc.md)
  
[<span data-ttu-id="c7477-119">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="c7477-119">ExcelCursorProc</span></span>](excelcursorproc.md)
  
[<span data-ttu-id="c7477-120">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="c7477-120">HookExcelWindow</span></span>](hookexcelwindow.md)
  
[<span data-ttu-id="c7477-121">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="c7477-121">UnhookExcelWindow</span></span>](unhookexcelwindow.md)
  
[<span data-ttu-id="c7477-122">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="c7477-122">fShowDialog</span></span>](fshowdialog.md)
  
[<span data-ttu-id="c7477-123">fDance</span><span class="sxs-lookup"><span data-stu-id="c7477-123">fDance</span></span>](fdance.md)
  
[<span data-ttu-id="c7477-124">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="c7477-124">fDialog/fDialog12</span></span>](fdialog-fdialog12.md)
  
[<span data-ttu-id="c7477-125">fExit</span><span class="sxs-lookup"><span data-stu-id="c7477-125">fExit</span></span>](fexit.md)
  
[<span data-ttu-id="c7477-126">Func1</span><span class="sxs-lookup"><span data-stu-id="c7477-126">Func1</span></span>](func1.md)
  
[<span data-ttu-id="c7477-127">FuncSum</span><span class="sxs-lookup"><span data-stu-id="c7477-127">FuncSum</span></span>](funcsum.md)
  
[<span data-ttu-id="c7477-128">FuncFib</span><span class="sxs-lookup"><span data-stu-id="c7477-128">FuncFib</span></span>](funcfib.md)
  
## <a name="see-also"></a><span data-ttu-id="c7477-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7477-129">See also</span></span>



[<span data-ttu-id="c7477-130">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="c7477-130">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

