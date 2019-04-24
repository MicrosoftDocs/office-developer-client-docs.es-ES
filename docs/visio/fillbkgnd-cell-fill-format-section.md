---
title: Celda FillBkgnd (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm365
localization_priority: Normal
ms.assetid: 603d698f-a025-538c-8767-18e7716a9a5f
description: Determina el color utilizado para el fondo (relleno) de la trama de relleno de la forma.
ms.openlocfilehash: f4df5d2b44a50380c996b9b2e0f7cda7d212093b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322515"
---
# <a name="fillbkgnd-cell-fill-format-section"></a><span data-ttu-id="e2831-103">Celda FillBkgnd (Sección de formato de relleno)</span><span class="sxs-lookup"><span data-stu-id="e2831-103">FillBkgnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="e2831-104">Determina el color utilizado para el fondo (relleno) de la trama de relleno de la forma.</span><span class="sxs-lookup"><span data-stu-id="e2831-104">Determines the color used for the background (fill) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e2831-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2831-105">Remarks</span></span>

<span data-ttu-id="e2831-106">Para establecer el color, escriba un número entre el 0 y el 23.</span><span class="sxs-lookup"><span data-stu-id="e2831-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="e2831-p101">Para especificar un color personalizado, utilice la función RGB o HSL. El valor de un color personalizado es su color RGB. En la ventana ShapeSheet se mostrará RGB(*r, g, b*) en lugar de un número. Cuando se utilizan en operaciones numéricas, los colores personalizados tienen un valor igual o mayor que 24.</span><span class="sxs-lookup"><span data-stu-id="e2831-p101">To enter a custom color, use the RGB or HSL function. The value of a custom color is its RGB color, and RGB(*r, g, b*), rather than a number, will be shown in the ShapeSheet window. When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="e2831-110">Puede establecer la transparencia del relleno de fondo en la celda FillBkgndTrans.</span><span class="sxs-lookup"><span data-stu-id="e2831-110">You can set the transparency of the background fill in the FillBkgndTrans cell.</span></span> 
  
<span data-ttu-id="e2831-111">Para obtener una referencia a la celda FillBkgnd por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e2831-111">To get a reference to the FillBkgnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e2831-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e2831-112">Cell name:</span></span>  <br/> | <span data-ttu-id="e2831-113">FillBkgnd</span><span class="sxs-lookup"><span data-stu-id="e2831-113">FillBkgnd</span></span>  <br/> |
   
<span data-ttu-id="e2831-114">Para obtener una referencia desde un programa a la celda FillBkgnd por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e2831-114">To get a reference to the FillBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e2831-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e2831-115">Section index:</span></span>  <br/> |<span data-ttu-id="e2831-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e2831-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e2831-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e2831-117">Row index:</span></span>  <br/> |<span data-ttu-id="e2831-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="e2831-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="e2831-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e2831-119">Cell index:</span></span>  <br/> |<span data-ttu-id="e2831-120">**visFillBkgnd**</span><span class="sxs-lookup"><span data-stu-id="e2831-120">**visFillBkgnd**</span></span> <br/> |
   

