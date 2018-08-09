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
ms.openlocfilehash: 0b6392030e7efc8ea36c8d728b99c9b82482840b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823192"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a><span data-ttu-id="f3b93-103">Celda ShapeShdwScaleFactor (sección Formato de relleno)</span><span class="sxs-lookup"><span data-stu-id="f3b93-103">ShapeShdwScaleFactor Cell (Fill Format Section)</span></span>

<span data-ttu-id="f3b93-104">Especifica el porcentaje en que se puede aumentar o reducir la sombra de una forma.</span><span class="sxs-lookup"><span data-stu-id="f3b93-104">Specifies the percentage by which the shadow of a shape can be enlarged or reduced.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f3b93-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3b93-105">Remarks</span></span>

<span data-ttu-id="f3b93-106">Cada sombra tiene una ubicación de eje sombreada, que es un punto de la sombra que corresponde al eje de la forma.</span><span class="sxs-lookup"><span data-stu-id="f3b93-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="f3b93-107">Por ejemplo, si el eje de una forma se encuentra en el centro de la forma, la ubicación de eje sombreada sería el punto en el centro de la sombra.</span><span class="sxs-lookup"><span data-stu-id="f3b93-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="f3b93-108">Cuando se aplica la escala a sombras simples, ampliación se centra en la ubicación de eje sombreada; Cuando se aplica la escala a sombras oblicuas, ampliación se aplica en la dirección oblicua.</span><span class="sxs-lookup"><span data-stu-id="f3b93-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
<span data-ttu-id="f3b93-109">Para establecer este valor para todas las formas de una página, utilice la celda ShdwScaleFactor de la sección de propiedades de página.</span><span class="sxs-lookup"><span data-stu-id="f3b93-109">To set this value for all the shapes on a page, use the ShdwScaleFactor cell in the Page Properties section.</span></span>
  
<span data-ttu-id="f3b93-110">Este valor corresponde al valor del parámetro **Ampliación** del cuadro de diálogo **Sombra** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Sombra** y, a continuación, en **Opciones de sombra**).</span><span class="sxs-lookup"><span data-stu-id="f3b93-110">This value corresponds to the value of the **Magnification** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="f3b93-111">Para obtener una referencia a la celda ShapeShdwScaleFactor por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="f3b93-111">To get a reference to the ShapeShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3b93-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f3b93-112">Cell name:</span></span>  <br/> |<span data-ttu-id="f3b93-113">ShapeShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="f3b93-113">ShapeShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="f3b93-114">Para obtener una referencia desde un programa a la celda ShapeShdwScaleFactor por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f3b93-114">To get a reference to the ShapeShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3b93-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f3b93-115">Section index:</span></span>  <br/> |<span data-ttu-id="f3b93-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f3b93-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f3b93-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f3b93-117">Row index:</span></span>  <br/> |<span data-ttu-id="f3b93-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="f3b93-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="f3b93-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f3b93-119">Cell index:</span></span>  <br/> |<span data-ttu-id="f3b93-120">**visFillShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="f3b93-120">**visFillShdwScaleFactor**</span></span> <br/> |
   

