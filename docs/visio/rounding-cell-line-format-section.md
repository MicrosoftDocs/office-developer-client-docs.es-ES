---
title: Celda Rounding (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm860
localization_priority: Normal
ms.assetid: c44457ca-997a-5315-44dd-4218e4203550
description: Indica el radio del arco de redondeo aplicado donde se unen dos segmentos contiguos de un trazado. Por ejemplo, el redondeo puede utilizarse para aplicar esquinas redondeadas a un rectángulo. Para establecer el redondeo, escriba un valor con unidades de medida (un par número-unidad).
ms.openlocfilehash: d64d3266e3dd2b0a3998955efe271aab04905fbf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427013"
---
# <a name="rounding-cell-line-format-section"></a><span data-ttu-id="27539-105">Celda Rounding (Sección de formato de línea)</span><span class="sxs-lookup"><span data-stu-id="27539-105">Rounding Cell (Line Format Section)</span></span>

<span data-ttu-id="27539-p102">Indica el radio del arco de redondeo aplicado donde se unen dos segmentos contiguos de un trazado. Por ejemplo, el redondeo puede utilizarse para aplicar esquinas redondeadas a un rectángulo. Para establecer el redondeo, escriba un valor con unidades de medida (un par número-unidad).</span><span class="sxs-lookup"><span data-stu-id="27539-p102">Indicates the radius of the rounding arc applied where two contiguous segments of a path meet. For example, rounding can be used to give a rectangle rounded corners. To set rounding, enter a value with units of measure (a number-unit pair).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="27539-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="27539-109">Remarks</span></span>

<span data-ttu-id="27539-110">También puede establecer este  valor en el  cuadro de diálogo  Línea (en la ficha Inicio, en el grupo Formas, haga clic en Línea **,** elija Grosor **y,** a continuación, haga clic en **Más líneas).**</span><span class="sxs-lookup"><span data-stu-id="27539-110">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="27539-111">Para obtener una referencia a la celda Rounding por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="27539-111">To get a reference to the Rounding cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27539-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="27539-112">Cell name:</span></span>  <br/> |<span data-ttu-id="27539-113">Redondeo</span><span class="sxs-lookup"><span data-stu-id="27539-113">Rounding</span></span>  <br/> |
   
<span data-ttu-id="27539-114">Para obtener una referencia desde un programa a la celda Rounding por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="27539-114">To get a reference to the Rounding cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27539-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="27539-115">Section index:</span></span>  <br/> |<span data-ttu-id="27539-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="27539-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="27539-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="27539-117">Row index:</span></span>  <br/> |<span data-ttu-id="27539-118">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="27539-118">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="27539-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="27539-119">Cell index:</span></span>  <br/> |<span data-ttu-id="27539-120">**visLineRounding**</span><span class="sxs-lookup"><span data-stu-id="27539-120">**visLineRounding**</span></span> <br/> |
   

