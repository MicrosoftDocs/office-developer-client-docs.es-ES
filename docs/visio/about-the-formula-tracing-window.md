---
title: Ventana Rastreo de fórmulas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60118
localization_priority: Normal
ms.assetid: 0cdacd4e-74dc-32c3-2eb2-219bf7fcb532
description: La ventana Rastreo de fórmulas se ha diseñado para ofrecer a los programadores de formas información sobre las interdependencias entre celdas, tanto las dependientes (celdas que dependen de otra celda determinada) como las precedentes (celdas de las cuales depende una celda determinada).
ms.openlocfilehash: f5f9d6a7ba3ab7049715d31342cfe7aa68ea053f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385329"
---
# <a name="about-the-formula-tracing-window"></a><span data-ttu-id="91e87-103">Información sobre la ventana Rastreo de fórmulas</span><span class="sxs-lookup"><span data-stu-id="91e87-103">About the Formula Tracing Window</span></span>

<span data-ttu-id="91e87-104">La ventana **Rastreo de fórmulas** se ha diseñado para ofrecer a los programadores de formas información sobre las interdependencias entre celdas, tanto las dependientes (celdas que dependen de otra celda determinada) como las precedentes (celdas de las cuales depende una celda determinada).</span><span class="sxs-lookup"><span data-stu-id="91e87-104">The **Formula Tracing** window is designed to provide shape developers with information about cell interdependencies—both dependent cells (cells that have a dependency on a given cell), and precedent cells (cells that a given cell depends on).</span></span> 
  
<span data-ttu-id="91e87-105">Las celdas de ShapeSheet de Microsoft Visio contienen valores y fórmulas.</span><span class="sxs-lookup"><span data-stu-id="91e87-105">The cells in a Microsoft Visio ShapeSheet contain values and formulas.</span></span> <span data-ttu-id="91e87-106">Fórmulas a su vez, pueden hacer que las referencias a otras celdas, que ofrece la potencia para calcular un valor en una celda basándose en el valor de otra celda.</span><span class="sxs-lookup"><span data-stu-id="91e87-106">Formulas can, in turn, have references to other cells, giving you the power to calculate a value in one cell based on another cell's value.</span></span> <span data-ttu-id="91e87-107">Al crear o mantener formas complejas, sin embargo, puede resultar difícil identificar todas estas interdependencias debido a que una fórmula puede hacer referencia a cualquier celda del dibujo, ya sea una celda de la misma ShapeSheet o una celda perteneciente a otro objeto en el dibujo, Por ejemplo, una página, estilo, patrón u otra forma.</span><span class="sxs-lookup"><span data-stu-id="91e87-107">When creating or maintaining complex shapes, however, it can be difficult to identify all these interdependencies because a formula can reference any cell in the drawing, whether it's a cell in the same ShapeSheet, or a cell belonging to another object in the drawing, for example, a page, style, master, or another shape.</span></span> 
  
<span data-ttu-id="91e87-108">La ventana **Rastreo de fórmulas** ofrece información para ayudarle a comprender las consecuencias de los cambios realizados a las celdas.</span><span class="sxs-lookup"><span data-stu-id="91e87-108">The **Formula Tracing** window provides information to help you understand the implications of changes you make to cells.</span></span> 
  
## <a name="displaying-the-formula-tracing-window"></a><span data-ttu-id="91e87-109">Mostrar la ventana Rastreo de fórmulas</span><span class="sxs-lookup"><span data-stu-id="91e87-109">Displaying the Formula Tracing Window</span></span>

<span data-ttu-id="91e87-110">Para ver la ventana **Rastreo de fórmulas** , con la ventana ShapeSheet activa, en **Herramientas de ShapeSheet** en la \*\* diseño \*\* ficha, en el grupo **Rastreo de fórmulas** , haga clic en **Mostrar ventana**.</span><span class="sxs-lookup"><span data-stu-id="91e87-110">To view the **Formula Tracing** window, with the ShapeSheet window active, under **ShapeSheet Tools** on the \*\* Design \*\* tab, in the **Formula Tracing** group, click **Show Window**.</span></span> <span data-ttu-id="91e87-111">La ventana **Rastreo de fórmulas** aparece acoplada en la ventana ShapeSheet de forma predeterminada, pero es una ventana anclada que puede acoplar, flotar o combinada con otras ventanas de ShapeSheet disponibles, por ejemplo, la ventana **Explorador de estilos** .</span><span class="sxs-lookup"><span data-stu-id="91e87-111">The **Formula Tracing** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated or merged with other available anchored ShapeSheet windows, for example, the **Style Explorer** window.</span></span> 
  
## <a name="tracing-dependent-cells"></a><span data-ttu-id="91e87-112">Rastreo de celdas dependientes</span><span class="sxs-lookup"><span data-stu-id="91e87-112">Tracing dependent cells</span></span>

<span data-ttu-id="91e87-p103">Para ver una lista de las celdas dependientes de una celda determinada, seleccione dicha celda en la ventana ShapeSheet. En este ejemplo, está seleccionada la celda Width.</span><span class="sxs-lookup"><span data-stu-id="91e87-p103">To see a list of cells that are dependent on a particular cell, select that cell in the ShapeSheet window. In this example, the Width cell is selected.</span></span> 
  
![Se selecciona la celda Width](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
<span data-ttu-id="91e87-116">Para ver sus celdas dependientes, en el grupo **Rastreo de fórmulas**, haga clic en **Rastrear dependientes**.</span><span class="sxs-lookup"><span data-stu-id="91e87-116">To view its dependent cells, in the **Formula Tracing**group, click **Trace Dependents**.</span></span>
  
<span data-ttu-id="91e87-p104">Aparecerá una lista de todas las celdas que dependan de Width en la ventana **Rastreo de fórmulas**. Puede explorar cualquiera de ellas haciendo doble clic en la ventana **Rastreo de fórmulas**.</span><span class="sxs-lookup"><span data-stu-id="91e87-p104">A list of all the cells with a dependency on the Width cell appears in the **Formula Tracing** window. You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![Todas las celdas con una dependencia en la celda Width aparecen en la ventana Rastreo de fórmulas](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a><span data-ttu-id="91e87-120">Rastreo de celdas precendent</span><span class="sxs-lookup"><span data-stu-id="91e87-120">Tracing precendent cells</span></span>

<span data-ttu-id="91e87-p105">Para ver una lista de las celdas de las cuales depende una celda determinada, seleccione primero dicha celda en la ventana ShapeSheet. En este ejemplo, está seleccionada la celda Geometry1.X2.</span><span class="sxs-lookup"><span data-stu-id="91e87-p105">To see a list of cells that a particular cell is dependent upon, first select the cell in the ShapeSheet window. In this example, the Geometry1.X2 cell is selected.</span></span> 
  
![Se selecciona la celda Geometry1.X2](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
<span data-ttu-id="91e87-124">Para ver sus celdas precedentes, en el grupo **Rastreo de fórmulas**, haga clic en **Rastrear precedentes**.</span><span class="sxs-lookup"><span data-stu-id="91e87-124">To view its precedent cells, in the **Formula Tracing**group, click **Trace Precedents**.</span></span>
  
<span data-ttu-id="91e87-125">Aparece una lista de todas las celdas que depende la celda Geometry1.X2 en la ventana **Rastreo de fórmulas** .</span><span class="sxs-lookup"><span data-stu-id="91e87-125">A list of all the cells that the Geometry1.X2 cell is dependent upon appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="91e87-126">Puede navegar a cualquier celda de la lista haciendo doble clic en su entrada en la ventana **Rastreo de fórmulas** .</span><span class="sxs-lookup"><span data-stu-id="91e87-126">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![Todas las celdas que depende la celda Geometry1.X2 aparecen en la ventana Rastreo de fórmulas](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

