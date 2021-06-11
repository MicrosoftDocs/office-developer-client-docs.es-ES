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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345335"
---
# <a name="about-the-formula-tracing-window"></a><span data-ttu-id="e7244-103">Acerca de la ventana Rastreo de fórmulas</span><span class="sxs-lookup"><span data-stu-id="e7244-103">About the Formula Tracing Window</span></span>

<span data-ttu-id="e7244-104">La ventana **Rastreo de fórmulas** se ha diseñado para ofrecer a los programadores de formas información sobre las interdependencias entre celdas, tanto las dependientes (celdas que dependen de otra celda determinada) como las precedentes (celdas de las cuales depende una celda determinada).</span><span class="sxs-lookup"><span data-stu-id="e7244-104">The **Formula Tracing** window is designed to provide shape developers with information about cell interdependencies—both dependent cells (cells that have a dependency on a given cell), and precedent cells (cells that a given cell depends on).</span></span> 
  
<span data-ttu-id="e7244-105">Las celdas de ShapeSheet de Microsoft Visio contienen valores y fórmulas.</span><span class="sxs-lookup"><span data-stu-id="e7244-105">The cells in a Microsoft Visio ShapeSheet contain values and formulas.</span></span> <span data-ttu-id="e7244-106">Las fórmulas, a su vez, pueden tener referencias a otras celdas, lo que le da la capacidad de calcular un valor en una celda en función del valor de otra celda.</span><span class="sxs-lookup"><span data-stu-id="e7244-106">Formulas can, in turn, have references to other cells, giving you the power to calculate a value in one cell based on another cell's value.</span></span> <span data-ttu-id="e7244-107">Sin embargo, al crear o mantener formas complejas, puede resultar difícil identificar todas estas interdependencias, dado que una fórmula puede hacer referencia a cualquier celda del dibujo, sea una celda de la misma ShapeSheet o de otro objeto del dibujo (por ejemplo, una página, un estilo, un patrón u otra forma).</span><span class="sxs-lookup"><span data-stu-id="e7244-107">When creating or maintaining complex shapes, however, it can be difficult to identify all these interdependencies because a formula can reference any cell in the drawing, whether it's a cell in the same ShapeSheet, or a cell belonging to another object in the drawing, for example, a page, style, master, or another shape.</span></span> 
  
<span data-ttu-id="e7244-108">La **ventana Seguimiento de** fórmulas proporciona información que le ayudará a comprender las implicaciones de los cambios realizados en las celdas.</span><span class="sxs-lookup"><span data-stu-id="e7244-108">The **Formula Tracing** window provides information to help you understand the implications of changes you make to cells.</span></span> 
  
## <a name="displaying-the-formula-tracing-window"></a><span data-ttu-id="e7244-109">Visualización de la ventana de seguimiento de fórmulas</span><span class="sxs-lookup"><span data-stu-id="e7244-109">Displaying the Formula Tracing Window</span></span>

<span data-ttu-id="e7244-110">Para ver la ventana **Seguimiento** de fórmulas, con la ventana **ShapeSheet** activa, en Herramientas de ShapeSheet en la ficha \*\* Diseño \*\*, en el grupo **Seguimiento** de fórmulas, haga clic en **Mostrar ventana**.</span><span class="sxs-lookup"><span data-stu-id="e7244-110">To view the **Formula Tracing** window, with the ShapeSheet window active, under **ShapeSheet Tools** on the \*\* Design \*\* tab, in the **Formula Tracing** group, click **Show Window**.</span></span> <span data-ttu-id="e7244-111">La  ventana Seguimiento de fórmulas aparece acoplada en la ventana ShapeSheet de forma predeterminada, pero es una ventana delimitada que  se puede acoplar, flotar o combinar con otras ventanas ShapeSheet ancladas disponibles, por ejemplo, la ventana Explorador de estilos.</span><span class="sxs-lookup"><span data-stu-id="e7244-111">The **Formula Tracing** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated or merged with other available anchored ShapeSheet windows, for example, the **Style Explorer** window.</span></span> 
  
## <a name="tracing-dependent-cells"></a><span data-ttu-id="e7244-112">Rastreo de celdas dependientes</span><span class="sxs-lookup"><span data-stu-id="e7244-112">Tracing dependent cells</span></span>

<span data-ttu-id="e7244-p103">Para ver una lista de las celdas dependientes de una celda determinada, seleccione dicha celda en la ventana ShapeSheet. En este ejemplo, está seleccionada la celda Width.</span><span class="sxs-lookup"><span data-stu-id="e7244-p103">To see a list of cells that are dependent on a particular cell, select that cell in the ShapeSheet window. In this example, the Width cell is selected.</span></span> 
  
![Celda Width seleccionada](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
<span data-ttu-id="e7244-116">Para ver sus celdas dependientes, en el grupo **Seguimiento de** fórmulas, haga clic en **Seguimiento dependientes**.</span><span class="sxs-lookup"><span data-stu-id="e7244-116">To view its dependent cells, in the **Formula Tracing** group, click **Trace Dependents**.</span></span>
  
<span data-ttu-id="e7244-p104">Aparecerá una lista de todas las celdas que dependan de Width en la ventana **Rastreo de fórmulas**. Puede explorar cualquiera de ellas haciendo doble clic en la ventana **Rastreo de fórmulas**.</span><span class="sxs-lookup"><span data-stu-id="e7244-p104">A list of all the cells with a dependency on the Width cell appears in the **Formula Tracing** window. You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![Todas las celdas con una dependencia en la celda Width aparecen en la ventana Seguimiento de fórmulas](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a><span data-ttu-id="e7244-120">Seguimiento de celdas precendentes</span><span class="sxs-lookup"><span data-stu-id="e7244-120">Tracing precendent cells</span></span>

<span data-ttu-id="e7244-p105">Para ver una lista de las celdas de las cuales depende una celda determinada, seleccione primero dicha celda en la ventana ShapeSheet. En este ejemplo, está seleccionada la celda Geometry1.X2.</span><span class="sxs-lookup"><span data-stu-id="e7244-p105">To see a list of cells that a particular cell is dependent upon, first select the cell in the ShapeSheet window. In this example, the Geometry1.X2 cell is selected.</span></span> 
  
![La celda Geometry1.X2 está seleccionada](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
<span data-ttu-id="e7244-124">Para ver sus celdas precedentes, en el grupo **Seguimiento de** fórmulas, haga clic en **Seguir precedentes**.</span><span class="sxs-lookup"><span data-stu-id="e7244-124">To view its precedent cells, in the **Formula Tracing** group, click **Trace Precedents**.</span></span>
  
<span data-ttu-id="e7244-125">En la ventana Seguimiento de fórmulas aparece una lista de  todas las celdas de las que depende la celda Geometry1.X2.</span><span class="sxs-lookup"><span data-stu-id="e7244-125">A list of all the cells that the Geometry1.X2 cell is dependent upon appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="e7244-126">Puede explorar cualquiera de ellas haciendo doble clic en la ventana **Rastreo de fórmulas**.</span><span class="sxs-lookup"><span data-stu-id="e7244-126">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![Todas las celdas de las que depende la celda Geometry1.X2 aparecen en la ventana Seguimiento de fórmulas](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

