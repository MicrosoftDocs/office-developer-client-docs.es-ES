---
title: Funciones de la DLL genérica
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- dll genérico [excel 2007], funciones, funciones [Excel 2007], DLL genérica
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e78f276e58ca1c98786e28ed5167762cf0bfdf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815652"
---
# <a name="functions-in-the-generic-dll"></a><span data-ttu-id="fd54a-104">Funciones de la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="fd54a-104">Functions in the Generic DLL</span></span>

 <span data-ttu-id="fd54a-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fd54a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fd54a-106">La carpeta `\EXAMPLES\GENERIC\` contiene los archivos de proyecto de Microsoft Visual Studio y archivos de código fuente que se necesitan para compilar el ejemplo GENERIC.xll del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="fd54a-106">The folder  `\EXAMPLES\GENERIC\` contains Microsoft Visual Studio project files and source code files that are needed to compile the example DLL GENERIC.xll.</span></span> <span data-ttu-id="fd54a-107">Puede usar este proyecto como una plantilla para escribir su propia XLL de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="fd54a-107">You can use this project as a template for writing your own Microsoft Excel XLLs.</span></span> <span data-ttu-id="fd54a-108">El código de origen de este proyecto muestra muchas de las características de la API de C de Excel.</span><span class="sxs-lookup"><span data-stu-id="fd54a-108">The source code in this project demonstrates many of the features of the Excel C API.</span></span> 
  
<span data-ttu-id="fd54a-109">Cuando se carga GENERIC.xll, crea un nuevo menú **genérico** con cuatro comandos:</span><span class="sxs-lookup"><span data-stu-id="fd54a-109">When you load GENERIC.xll, it creates a new **Generic** menu with four commands:</span></span> 
  
- <span data-ttu-id="fd54a-110">**Cuadro de diálogo** - muestra un cuadro de diálogo de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="fd54a-110">**Dialog** - Displays a Microsoft Excel dialog box.</span></span> 
    
- <span data-ttu-id="fd54a-111">**Baile** - mueve la selección alrededor de hasta que se presione la tecla **ESC** .</span><span class="sxs-lookup"><span data-stu-id="fd54a-111">**Dance** - Moves the selection around until you press the **ESC** key.</span></span> 
    
- <span data-ttu-id="fd54a-112">**Cuadro de diálogo nativo** - muestra un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="fd54a-112">**Native Dialog** - Displays a Windows dialog box.</span></span> 
    
- <span data-ttu-id="fd54a-113">**Exit** - GENERIC.xll de descarga y se quita el menú **genérica** .</span><span class="sxs-lookup"><span data-stu-id="fd54a-113">**Exit** - Unloads GENERIC.xll and removes the **Generic** menu.</span></span> 
    
<span data-ttu-id="fd54a-114">GENERIC.xll también proporciona tres funciones de hoja de cálculo, Func1, FuncSum y FuncFib, que se puede utilizar siempre que se carga GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="fd54a-114">GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded.</span></span> <span data-ttu-id="fd54a-115">GENERIC.xll se pueden cargar con el Administrador de complementos, o se carga si estaba activo al final de la última sesión de Excel normal.</span><span class="sxs-lookup"><span data-stu-id="fd54a-115">GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.</span></span>
  
<span data-ttu-id="fd54a-116">Este proyecto usa la biblioteca de framework (FRMWRK32.lib).</span><span class="sxs-lookup"><span data-stu-id="fd54a-116">This project uses the framework library (FRMWRK32.lib).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="fd54a-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="fd54a-117">In this section</span></span>

[<span data-ttu-id="fd54a-118">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="fd54a-118">DIALOGMsgProc</span></span>](dialogmsgproc.md)
  
[<span data-ttu-id="fd54a-119">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="fd54a-119">ExcelCursorProc</span></span>](excelcursorproc.md)
  
[<span data-ttu-id="fd54a-120">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="fd54a-120">HookExcelWindow</span></span>](hookexcelwindow.md)
  
[<span data-ttu-id="fd54a-121">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="fd54a-121">UnhookExcelWindow</span></span>](unhookexcelwindow.md)
  
[<span data-ttu-id="fd54a-122">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="fd54a-122">fShowDialog</span></span>](fshowdialog.md)
  
[<span data-ttu-id="fd54a-123">fDance</span><span class="sxs-lookup"><span data-stu-id="fd54a-123">fDance</span></span>](fdance.md)
  
[<span data-ttu-id="fd54a-124">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="fd54a-124">fDialog/fDialog12</span></span>](fdialog-fdialog12.md)
  
[<span data-ttu-id="fd54a-125">fExit</span><span class="sxs-lookup"><span data-stu-id="fd54a-125">fExit</span></span>](fexit.md)
  
[<span data-ttu-id="fd54a-126">Func1</span><span class="sxs-lookup"><span data-stu-id="fd54a-126">Func1</span></span>](func1.md)
  
[<span data-ttu-id="fd54a-127">FuncSum</span><span class="sxs-lookup"><span data-stu-id="fd54a-127">FuncSum</span></span>](funcsum.md)
  
[<span data-ttu-id="fd54a-128">FuncFib</span><span class="sxs-lookup"><span data-stu-id="fd54a-128">FuncFib</span></span>](funcfib.md)
  
## <a name="see-also"></a><span data-ttu-id="fd54a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd54a-129">See also</span></span>



[<span data-ttu-id="fd54a-130">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="fd54a-130">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

