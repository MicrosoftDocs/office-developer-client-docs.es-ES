---
title: Celda ShdwScaleFactor (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
localization_priority: Normal
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: Especifica el porcentaje para aumentar o reducir la forma de una sombra.
ms.openlocfilehash: 9175e9a1148779524fdce96ff18eac22fe8dd421
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342885"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a><span data-ttu-id="50c54-103">Celda ShdwScaleFactor (Sección de propiedades de página)</span><span class="sxs-lookup"><span data-stu-id="50c54-103">ShdwScaleFactor Cell (Page Properties Section)</span></span>

<span data-ttu-id="50c54-104">Especifica el porcentaje para aumentar o reducir la forma de una sombra.</span><span class="sxs-lookup"><span data-stu-id="50c54-104">Specifies the percentage to enlarge or reduce a shape's shadow.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="50c54-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="50c54-105">Remarks</span></span>

<span data-ttu-id="50c54-106">Cada sombra tiene una ubicación de eje sombreada, que es un punto en la sombra que corresponde al eje de la forma.</span><span class="sxs-lookup"><span data-stu-id="50c54-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="50c54-107">Por ejemplo, si el eje de una forma se encuentra en el centro de ésta, la ubicación de eje sombreada sería el punto que se encuentra en el centro de la sombra.</span><span class="sxs-lookup"><span data-stu-id="50c54-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="50c54-108">Cuando se aplica la escala a sombras sencillas, la ampliación se centra en la ubicación del PIN sombreado; al aplicar la escala a sombras oblicuas, la ampliación se aplica en la dirección oblicuo.</span><span class="sxs-lookup"><span data-stu-id="50c54-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
 <span data-ttu-id="50c54-109">Este porcentaje se usa cuando el tipo de sombra de una forma se establece como predeterminado para la página (la celda ShapeShdwType es igual a \* \* visFSTPageDefault \* \*).</span><span class="sxs-lookup"><span data-stu-id="50c54-109">This percentage is used when the shadow type for a shape is set to Page Default (ShapeShdwType cell equals \*\* visFSTPageDefault \*\* ).</span></span> 
  
<span data-ttu-id="50c54-110">Para establecer este comportamiento para una forma individual, utilice la celda ShapeShdwScaleFactor de la sección de formato de relleno.</span><span class="sxs-lookup"><span data-stu-id="50c54-110">To set this behavior for an individual shape, use the ShapeShdwScaleFactor cell in the Fill Format section.</span></span>
  
<span data-ttu-id="50c54-111">Este valor corresponde al del cuadro **Ampliación** de la ficha **Sombras** en el cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página**).</span><span class="sxs-lookup"><span data-stu-id="50c54-111">This value corresponds to the value in the **Magnification** box on the **Shadows** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="50c54-112">Para obtener una referencia a la celda ShdwScaleFactor por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="50c54-112">To get a reference to the ShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="50c54-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="50c54-113">Cell name:</span></span>  <br/> | <span data-ttu-id="50c54-114">ShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="50c54-114">ShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="50c54-115">Para obtener una referencia desde un programa a la celda ShdwScaleFactor por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="50c54-115">To get a reference to the ShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="50c54-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="50c54-116">Section index:</span></span>  <br/> |<span data-ttu-id="50c54-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="50c54-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="50c54-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="50c54-118">Row index:</span></span>  <br/> |<span data-ttu-id="50c54-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="50c54-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="50c54-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="50c54-120">Cell index:</span></span>  <br/> |<span data-ttu-id="50c54-121">**visPageShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="50c54-121">**visPageShdwScaleFactor**</span></span> <br/> |
   

