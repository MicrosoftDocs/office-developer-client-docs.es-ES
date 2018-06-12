---
title: Celda LineColor (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
localization_priority: Normal
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: Determina el color de línea de la forma.
ms.openlocfilehash: 6086a45108b88475e250c4d833ab4b740f33b8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822459"
---
# <a name="linecolor-cell-line-format-section"></a><span data-ttu-id="a725e-103">Celda LineColor (Sección de formato de línea)</span><span class="sxs-lookup"><span data-stu-id="a725e-103">LineColor Cell (Line Format Section)</span></span>

<span data-ttu-id="a725e-104">Determina el color de línea de la forma.</span><span class="sxs-lookup"><span data-stu-id="a725e-104">Determines the line color of the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a725e-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a725e-105">Remarks</span></span>

<span data-ttu-id="a725e-106">Para establecer el color de línea, escriba un número entre 0 y 23, que es un índice en una colección de colores de línea.</span><span class="sxs-lookup"><span data-stu-id="a725e-106">To set the line color, enter a number from 0 to 23, which is an index into a collection of line colors.</span></span> <span data-ttu-id="a725e-107">Puede ver la colección de color de línea en el cuadro de diálogo **línea** (en la ficha **Inicio** , en el grupo **forma** , haga clic en **línea**, elija **grosor**y, a continuación, haga clic en **Más líneas**).</span><span class="sxs-lookup"><span data-stu-id="a725e-107">You can view the line color collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span> <span data-ttu-id="a725e-108">También puede establecer el valor de LineColor en el cuadro de diálogo **línea** .</span><span class="sxs-lookup"><span data-stu-id="a725e-108">You can also set the value of LineColor in the **Line** dialog box.</span></span> 
  
<span data-ttu-id="a725e-109">Para especificar un color personalizado, utilice la función RGB o HSL.</span><span class="sxs-lookup"><span data-stu-id="a725e-109">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="a725e-110">El valor de un color personalizado es su color RGB y RGB ( *r, g, b*), en lugar de un número, se mostrarán en la ventana ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="a725e-110">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="a725e-111">Cuando se usa en operaciones numéricas, los colores personalizados tienen valores de 24 y superior.</span><span class="sxs-lookup"><span data-stu-id="a725e-111">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="a725e-112">Puede establecer la transparencia del color de línea en la celda LineColorTrans.</span><span class="sxs-lookup"><span data-stu-id="a725e-112">You can set the transparency of the line color in the LineColorTrans cell.</span></span>
  
<span data-ttu-id="a725e-113">Para obtener una referencia a la celda LineColor por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="a725e-113">To get a reference to the LineColor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a725e-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a725e-114">Cell name:</span></span>  <br/> |<span data-ttu-id="a725e-115">LineColor</span><span class="sxs-lookup"><span data-stu-id="a725e-115">LineColor</span></span>  <br/> |
   
<span data-ttu-id="a725e-116">Para obtener una referencia a la celda LineColor por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a725e-116">To get a reference to the LineColor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a725e-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a725e-117">Section index:</span></span>  <br/> |<span data-ttu-id="a725e-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a725e-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a725e-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a725e-119">Row index:</span></span>  <br/> |<span data-ttu-id="a725e-120">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="a725e-120">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="a725e-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a725e-121">Cell index:</span></span>  <br/> |<span data-ttu-id="a725e-122">**visLineColor**</span><span class="sxs-lookup"><span data-stu-id="a725e-122">**visLineColor**</span></span> <br/> |
   

