---
title: Celda ShapeShdwScaleFactor (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033175
localization_priority: Normal
ms.assetid: 94ec06c5-8d2f-dd27-1eed-1abaf93daba8
description: Especifica el porcentaje en que se puede aumentar o reducir la sombra de una forma.
ms.openlocfilehash: 5862b61ca1f5df25ca97bf8742b9e20bf45091a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436268"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a><span data-ttu-id="5fd80-103">Celda ShapeShdwScaleFactor (Sección de formato de relleno)</span><span class="sxs-lookup"><span data-stu-id="5fd80-103">ShapeShdwScaleFactor Cell (Fill Format Section)</span></span>

<span data-ttu-id="5fd80-104">Especifica el porcentaje en que se puede aumentar o reducir la sombra de una forma.</span><span class="sxs-lookup"><span data-stu-id="5fd80-104">Specifies the percentage by which the shadow of a shape can be enlarged or reduced.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5fd80-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5fd80-105">Remarks</span></span>

<span data-ttu-id="5fd80-106">Cada sombra tiene una ubicación de eje sombreada, que es un punto en la sombra que corresponde al eje de la forma.</span><span class="sxs-lookup"><span data-stu-id="5fd80-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="5fd80-107">Por ejemplo, si el eje de una forma se encuentra en el centro de ésta, la ubicación de eje sombreada sería el punto que se encuentra en el centro de la sombra.</span><span class="sxs-lookup"><span data-stu-id="5fd80-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="5fd80-108">Al aplicar la escala a sombras simples, la ampliación se centra en la ubicación de la patilla sombreada; al aplicar escala a sombras oblicuas, la ampliación se aplica en dirección oblicua.</span><span class="sxs-lookup"><span data-stu-id="5fd80-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
<span data-ttu-id="5fd80-109">Para establecer este valor para todas las formas de una página, utilice la celda ShdwScaleFactor de la sección de propiedades de página.</span><span class="sxs-lookup"><span data-stu-id="5fd80-109">To set this value for all the shapes on a page, use the ShdwScaleFactor cell in the Page Properties section.</span></span>
  
<span data-ttu-id="5fd80-110">Este valor corresponde al valor del parámetro **Ampliación** del cuadro de diálogo **Sombra** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Sombra** y, a continuación, en **Opciones de sombra**).</span><span class="sxs-lookup"><span data-stu-id="5fd80-110">This value corresponds to the value of the **Magnification** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="5fd80-111">Para obtener una referencia a la celda ShapeShdwScaleFactor por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="5fd80-111">To get a reference to the ShapeShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5fd80-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5fd80-112">Cell name:</span></span>  <br/> |<span data-ttu-id="5fd80-113">ShapeShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="5fd80-113">ShapeShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="5fd80-114">Para obtener una referencia desde un programa a la celda ShapeShdwScaleFactor por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5fd80-114">To get a reference to the ShapeShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5fd80-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5fd80-115">Section index:</span></span>  <br/> |<span data-ttu-id="5fd80-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5fd80-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5fd80-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5fd80-117">Row index:</span></span>  <br/> |<span data-ttu-id="5fd80-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="5fd80-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="5fd80-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5fd80-119">Cell index:</span></span>  <br/> |<span data-ttu-id="5fd80-120">**visFillShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="5fd80-120">**visFillShdwScaleFactor**</span></span> <br/> |
   

