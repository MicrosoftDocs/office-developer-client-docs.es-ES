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
ms.openlocfilehash: 0624ec42978292e84965c978d25e4052fc41613f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823017"
---
# <a name="rounding-cell-line-format-section"></a><span data-ttu-id="ff7f6-105">Celda Rounding (sección Formato de línea)</span><span class="sxs-lookup"><span data-stu-id="ff7f6-105">Rounding Cell (Line Format Section)</span></span>

<span data-ttu-id="ff7f6-p102">Indica el radio del arco de redondeo aplicado donde se unen dos segmentos contiguos de un trazado. Por ejemplo, el redondeo puede utilizarse para aplicar esquinas redondeadas a un rectángulo. Para establecer el redondeo, escriba un valor con unidades de medida (un par número-unidad).</span><span class="sxs-lookup"><span data-stu-id="ff7f6-p102">Indicates the radius of the rounding arc applied where two contiguous segments of a path meet. For example, rounding can be used to give a rectangle rounded corners. To set rounding, enter a value with units of measure (a number-unit pair).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ff7f6-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff7f6-109">Remarks</span></span>

<span data-ttu-id="ff7f6-110">También puede establecer este valor en el cuadro de diálogo **línea** (en la ficha **Inicio** , en el grupo **forma** , haga clic en **línea**, elija **grosor**y, a continuación, haga clic en **Más líneas**).</span><span class="sxs-lookup"><span data-stu-id="ff7f6-110">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="ff7f6-111">Para obtener una referencia a la celda Rounding por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="ff7f6-111">To get a reference to the Rounding cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff7f6-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="ff7f6-112">Cell name:</span></span>  <br/> |<span data-ttu-id="ff7f6-113">Rounding</span><span class="sxs-lookup"><span data-stu-id="ff7f6-113">Rounding</span></span>  <br/> |
   
<span data-ttu-id="ff7f6-114">Para obtener una referencia desde un programa a la celda Rounding por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ff7f6-114">To get a reference to the Rounding cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff7f6-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="ff7f6-115">Section index:</span></span>  <br/> |<span data-ttu-id="ff7f6-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ff7f6-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ff7f6-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="ff7f6-117">Row index:</span></span>  <br/> |<span data-ttu-id="ff7f6-118">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="ff7f6-118">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="ff7f6-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="ff7f6-119">Cell index:</span></span>  <br/> |<span data-ttu-id="ff7f6-120">**visLineRounding**</span><span class="sxs-lookup"><span data-stu-id="ff7f6-120">**visLineRounding**</span></span> <br/> |
   

