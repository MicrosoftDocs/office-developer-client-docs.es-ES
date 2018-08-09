---
title: Celda ShdwObliqueAngle (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
localization_priority: Normal
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: Contiene un número que especifica el ángulo de dirección oblicua cuando se aplica el tipo de sombra predeterminado de la página.
ms.openlocfilehash: 4549ce7b5202b4649a925b04ea54c0d5df569599
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823228"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a><span data-ttu-id="e2f68-103">Celda ShdwObliqueAngle (sección Propiedades de la página)</span><span class="sxs-lookup"><span data-stu-id="e2f68-103">ShdwObliqueAngle Cell (Page Properties Section)</span></span>

<span data-ttu-id="e2f68-104">Contiene un número que especifica el ángulo de dirección oblicua cuando se aplica el tipo de sombra predeterminado de la página.</span><span class="sxs-lookup"><span data-stu-id="e2f68-104">Contains a number specifying the angle of oblique direction when applying the default page shadow type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e2f68-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2f68-105">Remarks</span></span>

<span data-ttu-id="e2f68-106">Un valor de cero (0) en esta celda indica que la dirección del ángulo es vertical hacia arriba y que se mide moviéndose en el sentido de las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="e2f68-106">A value of zero (0) in this cell indicates that the angle direction is straight up and is measured moving clockwise.</span></span>
  
 <span data-ttu-id="e2f68-107">El ángulo que se describe en esta celda se utiliza cuando la celda ShapeShdwType (tipo de sombra para una forma en la página) se establece en el valor predeterminado de página (**visFSTPageDefault** ), y el tipo de sombra es oblicuo.</span><span class="sxs-lookup"><span data-stu-id="e2f68-107">The angle described in this cell is used whenever the ShapeShdwType Cell (the shadow type for a shape on the page) is set to Page Default (**visFSTPageDefault** ), and the shadow type is oblique.</span></span> <span data-ttu-id="e2f68-108">El tipo de sombra de página predeterminado se define en la celda ShdwType.</span><span class="sxs-lookup"><span data-stu-id="e2f68-108">The default page shadow type is defined in the ShdwType cell.</span></span> 
  
<span data-ttu-id="e2f68-109">Para establecer este comportamiento para una forma individual, utilice la celda ShapeShdwObliqueAngle de la sección de formato de relleno.</span><span class="sxs-lookup"><span data-stu-id="e2f68-109">To set this behavior for an individual shape, use the ShapeShdwObliqueAngle cell in the Fill Format section.</span></span>
  
<span data-ttu-id="e2f68-110">Para obtener una referencia a la celda ShdwObliqueAngle por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e2f68-110">To get a reference to the ShdwObliqueAngle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e2f68-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e2f68-111">Cell name:</span></span>  <br/> | <span data-ttu-id="e2f68-112">ShdwObliqueAngle</span><span class="sxs-lookup"><span data-stu-id="e2f68-112">ShdwObliqueAngle</span></span>  <br/> |
   
<span data-ttu-id="e2f68-113">Para obtener una referencia desde un programa a la celda ShdwObliqueAngle por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e2f68-113">To get a reference to the ShdwObliqueAngle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e2f68-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e2f68-114">Section index:</span></span>  <br/> |<span data-ttu-id="e2f68-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e2f68-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e2f68-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e2f68-116">Row index:</span></span>  <br/> |<span data-ttu-id="e2f68-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="e2f68-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="e2f68-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e2f68-118">Cell index:</span></span>  <br/> |<span data-ttu-id="e2f68-119">**visPageShdwObliqueAngle**</span><span class="sxs-lookup"><span data-stu-id="e2f68-119">**visPageShdwObliqueAngle**</span></span> <br/> |
   

