---
title: Funciones de la DLL genérica
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- DLL genérica [Excel 2007], funciones, funciones [Excel 2007], DLL genérica
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
# <a name="functions-in-the-generic-dll"></a><span data-ttu-id="9c9a3-104">Funciones de la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="9c9a3-104">Functions in the Generic DLL</span></span>

 <span data-ttu-id="9c9a3-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9c9a3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9c9a3-106">La carpeta `\EXAMPLES\GENERIC\` contiene los archivos de proyecto de Microsoft Visual Studio y los archivos de código fuente necesarios para compilar la dll genérica de ejemplo. XLL.</span><span class="sxs-lookup"><span data-stu-id="9c9a3-106">The folder  `\EXAMPLES\GENERIC\` contains Microsoft Visual Studio project files and source code files that are needed to compile the example DLL GENERIC.xll.</span></span> <span data-ttu-id="9c9a3-107">Puede usar este proyecto como una plantilla para escribir sus propios XLL de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="9c9a3-107">You can use this project as a template for writing your own Microsoft Excel XLLs.</span></span> <span data-ttu-id="9c9a3-108">El código fuente de este proyecto muestra muchas de las características de la API de C de Excel.</span><span class="sxs-lookup"><span data-stu-id="9c9a3-108">The source code in this project demonstrates many of the features of the Excel C API.</span></span> 
  
<span data-ttu-id="9c9a3-109">Cuando se carga GENERIC. XLL, se crea un nuevo menú **genérico** con cuatro comandos:</span><span class="sxs-lookup"><span data-stu-id="9c9a3-109">When you load GENERIC.xll, it creates a new **Generic** menu with four commands:</span></span> 
  
- <span data-ttu-id="9c9a3-110">**Dialog** -muestra un cuadro de diálogo de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="9c9a3-110">**Dialog** - Displays a Microsoft Excel dialog box.</span></span> 
    
- <span data-ttu-id="9c9a3-111">**Baile** : mueve la selección hasta que presione la tecla **ESC** .</span><span class="sxs-lookup"><span data-stu-id="9c9a3-111">**Dance** - Moves the selection around until you press the **ESC** key.</span></span> 
    
- <span data-ttu-id="9c9a3-112">Cuadro de diálogo **nativo** : muestra un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="9c9a3-112">**Native Dialog** - Displays a Windows dialog box.</span></span> 
    
- <span data-ttu-id="9c9a3-113">**Exit** -descarga Generic. XLL y quita el menú **genérico** .</span><span class="sxs-lookup"><span data-stu-id="9c9a3-113">**Exit** - Unloads GENERIC.xll and removes the **Generic** menu.</span></span> 
    
<span data-ttu-id="9c9a3-114">GENERIC. XLL también proporciona tres funciones de hoja de cálculo, Func1, FuncSum y FuncFib, que se pueden usar siempre que se cargue GENERIC. XLL.</span><span class="sxs-lookup"><span data-stu-id="9c9a3-114">GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded.</span></span> <span data-ttu-id="9c9a3-115">GENERIC. XLL se puede cargar mediante el administrador de complementos o se carga si estaba activo en el final normal de la última sesión de Excel.</span><span class="sxs-lookup"><span data-stu-id="9c9a3-115">GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.</span></span>
  
<span data-ttu-id="9c9a3-116">Este proyecto usa la biblioteca de marcos (FRMWRK32. lib).</span><span class="sxs-lookup"><span data-stu-id="9c9a3-116">This project uses the framework library (FRMWRK32.lib).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="9c9a3-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9c9a3-117">In this section</span></span>

[<span data-ttu-id="9c9a3-118">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="9c9a3-118">DIALOGMsgProc</span></span>](dialogmsgproc.md)
  
[<span data-ttu-id="9c9a3-119">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="9c9a3-119">ExcelCursorProc</span></span>](excelcursorproc.md)
  
[<span data-ttu-id="9c9a3-120">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="9c9a3-120">HookExcelWindow</span></span>](hookexcelwindow.md)
  
[<span data-ttu-id="9c9a3-121">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="9c9a3-121">UnhookExcelWindow</span></span>](unhookexcelwindow.md)
  
[<span data-ttu-id="9c9a3-122">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="9c9a3-122">fShowDialog</span></span>](fshowdialog.md)
  
[<span data-ttu-id="9c9a3-123">fDance</span><span class="sxs-lookup"><span data-stu-id="9c9a3-123">fDance</span></span>](fdance.md)
  
[<span data-ttu-id="9c9a3-124">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="9c9a3-124">fDialog/fDialog12</span></span>](fdialog-fdialog12.md)
  
[<span data-ttu-id="9c9a3-125">fExit</span><span class="sxs-lookup"><span data-stu-id="9c9a3-125">fExit</span></span>](fexit.md)
  
[<span data-ttu-id="9c9a3-126">Func1</span><span class="sxs-lookup"><span data-stu-id="9c9a3-126">Func1</span></span>](func1.md)
  
[<span data-ttu-id="9c9a3-127">FuncSum</span><span class="sxs-lookup"><span data-stu-id="9c9a3-127">FuncSum</span></span>](funcsum.md)
  
[<span data-ttu-id="9c9a3-128">FuncFib</span><span class="sxs-lookup"><span data-stu-id="9c9a3-128">FuncFib</span></span>](funcfib.md)
  
## <a name="see-also"></a><span data-ttu-id="9c9a3-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="9c9a3-129">See also</span></span>



[<span data-ttu-id="9c9a3-130">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="9c9a3-130">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

