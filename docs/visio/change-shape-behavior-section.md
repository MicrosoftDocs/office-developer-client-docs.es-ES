---
title: Cambiar sección de comportamiento de forma
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Determina las propiedades que se transfieren de la forma antigua a la forma de reemplazo durante una operación de reemplazo. Los valores de las celdas de la sección Cambiar comportamiento de forma de la forma maestra del reemplazo se leen durante la operación de reemplazo de la forma.
ms.openlocfilehash: 74519b27ab5b2b5bafc7c00010a65769061bf691
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418669"
---
# <a name="change-shape-behavior-section"></a><span data-ttu-id="e0c24-104">Cambiar sección de comportamiento de forma</span><span class="sxs-lookup"><span data-stu-id="e0c24-104">Change Shape Behavior Section</span></span>

<span data-ttu-id="e0c24-105">Determina las propiedades que se transfieren de la forma antigua a la forma de reemplazo durante una operación de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="e0c24-105">Determines the properties that are transferred from the old shape to the replacement shape during a replacement operation.</span></span> <span data-ttu-id="e0c24-106">Los valores de las celdas de la sección **Cambiar** comportamiento de forma de la forma maestra del reemplazo se leen durante la operación de reemplazo de la forma.</span><span class="sxs-lookup"><span data-stu-id="e0c24-106">The values of the cells in the **Change Shape Behavior** section of the Master shape of the replacement are read during the shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e0c24-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0c24-107">Remarks</span></span>

<span data-ttu-id="e0c24-108">Al establecer las  celdas en la sección Cambiar comportamiento de la forma, puede asegurarse de que determinadas propiedades de la forma de reemplazo no se modifiquen durante la operación de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="e0c24-108">By setting the cells in the **Change Shape Behavior** section, you can ensure that certain properties of the replacement shape remain unchanged during the replacement operation.</span></span> <span data-ttu-id="e0c24-109">Las propiedades que no están protegidas se actualizan con los valores de forma local de la forma antigua durante la operación.</span><span class="sxs-lookup"><span data-stu-id="e0c24-109">Properties that are not protected are updated with the local shape values from the old shape during the operation.</span></span> 
  
<span data-ttu-id="e0c24-110">Puede cambiar la configuración del comportamiento de reemplazo de una  forma Maestra editando la forma Patrón (en la ventana Formas, haga clic con el botón secundario en la forma, elija Editar patrón y, a continuación, haga clic en Editar forma **maestra)** y cambiando los valores de las [celdas ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)y [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) en la ShapeSheet del patrón.</span><span class="sxs-lookup"><span data-stu-id="e0c24-110">You can change the replacement behavior settings of a Master shape by editing the Master shape (in the **Shapes** window, right-click the shape, point to **Edit Master**, and then click **Edit Master Shape**) and changing the values of the [ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md), and [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) cells in the Master's ShapeSheet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e0c24-111">No puede cambiar los comportamientos de reemplazo de formas de las formas que se incluyen en las galerías de símbolos integradas en Microsoft Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="e0c24-111">You cannot change the shape replacement behaviors of the shapes that are included with the built-in stencils in Microsoft Visio 2013.</span></span> <span data-ttu-id="e0c24-112">Para modificar los comportamientos de reemplazo de formas de las formas integradas de Visio, cree una nueva galería de símbolos y agregue la forma que desea modificar a la nueva galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="e0c24-112">To modify the shape replacement behaviors of the built-in Visio shapes, create a new stencil and add the shape that you want to modify to the new stencil.</span></span> 
  

