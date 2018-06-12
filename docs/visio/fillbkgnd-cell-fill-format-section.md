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
ms.openlocfilehash: d1222026887313d7737a3a0ded9e798e9bf5ea30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822125"
---
# <a name="fillbkgnd-cell-fill-format-section"></a><span data-ttu-id="b86f7-103">Celda FillBkgnd (Sección de formato de relleno)</span><span class="sxs-lookup"><span data-stu-id="b86f7-103">FillBkgnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="b86f7-104">Determina el color utilizado para el fondo (relleno) de la trama de relleno de la forma.</span><span class="sxs-lookup"><span data-stu-id="b86f7-104">Determines the color used for the background (fill) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b86f7-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b86f7-105">Remarks</span></span>

<span data-ttu-id="b86f7-106">Para establecer el color, escriba un número entre el 0 y el 23.</span><span class="sxs-lookup"><span data-stu-id="b86f7-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="b86f7-107">Para especificar un color personalizado, utilice la función RGB o HSL.</span><span class="sxs-lookup"><span data-stu-id="b86f7-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="b86f7-108">El valor de un color personalizado es su color RGB y RGB (*r, g, b*), en lugar de un número, se mostrarán en la ventana ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="b86f7-108">The value of a custom color is its RGB color, and RGB(*r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="b86f7-109">Cuando se usa en operaciones numéricas, los colores personalizados tienen valores de 24 y superior.</span><span class="sxs-lookup"><span data-stu-id="b86f7-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="b86f7-110">Puede establecer la transparencia del relleno de fondo en la celda FillBkgndTrans.</span><span class="sxs-lookup"><span data-stu-id="b86f7-110">You can set the transparency of the background fill in the FillBkgndTrans cell.</span></span> 
  
<span data-ttu-id="b86f7-111">Para obtener una referencia a la celda FillBkgnd por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="b86f7-111">To get a reference to the FillBkgnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b86f7-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b86f7-112">Cell name:</span></span>  <br/> | <span data-ttu-id="b86f7-113">FillBkgnd</span><span class="sxs-lookup"><span data-stu-id="b86f7-113">FillBkgnd</span></span>  <br/> |
   
<span data-ttu-id="b86f7-114">Para obtener una referencia a la celda FillBkgnd por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b86f7-114">To get a reference to the FillBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b86f7-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b86f7-115">Section index:</span></span>  <br/> |<span data-ttu-id="b86f7-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b86f7-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b86f7-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b86f7-117">Row index:</span></span>  <br/> |<span data-ttu-id="b86f7-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="b86f7-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="b86f7-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b86f7-119">Cell index:</span></span>  <br/> |<span data-ttu-id="b86f7-120">**visFillBkgnd**</span><span class="sxs-lookup"><span data-stu-id="b86f7-120">**visFillBkgnd**</span></span> <br/> |
   

