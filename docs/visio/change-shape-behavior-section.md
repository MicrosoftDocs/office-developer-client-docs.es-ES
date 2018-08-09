---
title: Sección Cambiar comportamiento de forma
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Determina las propiedades que se transfieren durante una operación de reemplazo de la forma anterior a la forma de reemplazo. Los valores de las celdas en la sección cambiar el comportamiento de forma de patrón de la forma de la sustitución se leen durante la operación de reemplazo de forma.
ms.openlocfilehash: 3b4b3cac37b8415309a2433c19c2b420fd652df7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821738"
---
# <a name="change-shape-behavior-section"></a><span data-ttu-id="7f0e5-104">Sección Cambiar comportamiento de forma</span><span class="sxs-lookup"><span data-stu-id="7f0e5-104">Change Shape Behavior Section</span></span>

<span data-ttu-id="7f0e5-105">Determina las propiedades que se transfieren durante una operación de reemplazo de la forma anterior a la forma de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="7f0e5-105">Determines the properties that are transferred from the old shape to the replacement shape during a replacement operation.</span></span> <span data-ttu-id="7f0e5-106">Los valores de las celdas en la sección **Comportamiento de cambio de forma** de patrón de la forma de la sustitución se leen durante la operación de reemplazo de forma.</span><span class="sxs-lookup"><span data-stu-id="7f0e5-106">The values of the cells in the **Change Shape Behavior** section of the Master shape of the replacement are read during the shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7f0e5-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7f0e5-107">Remarks</span></span>

<span data-ttu-id="7f0e5-108">Mediante la configuración de las celdas en la sección **Comportamiento de cambio de forma** , puede asegurarse de que determinadas propiedades de la forma de sustitución no se modifican durante la operación de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="7f0e5-108">By setting the cells in the **Change Shape Behavior** section, you can ensure that certain properties of the replacement shape remain unchanged during the replacement operation.</span></span> <span data-ttu-id="7f0e5-109">Las propiedades que no están protegidas se actualizan con los valores de forma local desde la antigua forma durante la operación.</span><span class="sxs-lookup"><span data-stu-id="7f0e5-109">Properties that are not protected are updated with the local shape values from the old shape during the operation.</span></span> 
  
<span data-ttu-id="7f0e5-110">Puede cambiar la sustitución configuración del comportamiento de un patrón de forma mediante la edición el patrón de forma (en la ventana **formas** , haga clic en la forma, elija **Modificar patrón**y, a continuación, haga clic en **Modificar forma de patrón**) y cambiar los valores de la [ ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)y [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) las celdas de ShapeSheet del patrón.</span><span class="sxs-lookup"><span data-stu-id="7f0e5-110">You can change the replacement behavior settings of a Master shape by editing the Master shape (in the **Shapes** window, right-click the shape, point to **Edit Master**, and then click **Edit Master Shape**) and changing the values of the [ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md), and [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) cells in the Master's ShapeSheet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7f0e5-111">No se puede cambiar los comportamientos de sustitución de forma de las formas que se incluyen con las galerías de símbolos integrados en Microsoft Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="7f0e5-111">You cannot change the shape replacement behaviors of the shapes that are included with the built-in stencils in Microsoft Visio 2013.</span></span> <span data-ttu-id="7f0e5-112">Para modificar los comportamientos de sustitución de forma de las formas de Visio integradas, cree una nueva galería de símbolos y agregue la forma que desee modificar la nueva galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="7f0e5-112">To modify the shape replacement behaviors of the built-in Visio shapes, create a new stencil and add the shape that you want to modify to the new stencil.</span></span> 
  

