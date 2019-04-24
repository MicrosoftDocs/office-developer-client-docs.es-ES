---
title: Función ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Devuelve un valor Boolean que indica si una forma tiene un tema aplicado.
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357515"
---
# <a name="isthemed-function"></a><span data-ttu-id="7058e-103">Función ISTHEMED</span><span class="sxs-lookup"><span data-stu-id="7058e-103">ISTHEMED Function</span></span>

<span data-ttu-id="7058e-104">Devuelve un valor Boolean que indica si una forma tiene un tema aplicado.</span><span class="sxs-lookup"><span data-stu-id="7058e-104">Returns a Boolean value indicating whether a shape has a theme applied to it.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="7058e-105">Información de versiones</span><span class="sxs-lookup"><span data-stu-id="7058e-105">Version Information</span></span>

<span data-ttu-id="7058e-106">Versión añadida: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="7058e-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7058e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7058e-107">Syntax</span></span>

 <span data-ttu-id="7058e-108">**ISTHEMED** ()</span><span class="sxs-lookup"><span data-stu-id="7058e-108">**ISTHEMED**()</span></span>
  
## <a name="return-value"></a><span data-ttu-id="7058e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7058e-109">Return value</span></span>

<span data-ttu-id="7058e-110">Booleano</span><span class="sxs-lookup"><span data-stu-id="7058e-110">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7058e-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7058e-111">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="7058e-112">La función **ISTHEMED** de Visio 2013 reemplaza la función **CELLISTHEMED** de versiones anteriores de Visio.</span><span class="sxs-lookup"><span data-stu-id="7058e-112">The **ISTHEMED** function in Visio 2013 replaces the **CELLISTHEMED** function from previous versions of Visio.</span></span> 
  
<span data-ttu-id="7058e-113">La función **ISTHEMED** permite asignar las partes adecuadas del formato de un tema a una forma, pero mantener la capacidad de invalidar otras partes del formato del tema con un formato aplicado manualmente.</span><span class="sxs-lookup"><span data-stu-id="7058e-113">The **ISTHEMED** function lets you assign appropriate parts of a theme's formatting to a shape but retain the ability to override other parts of the theme formatting with manually-applied formatting.</span></span> <span data-ttu-id="7058e-114">Si, a continuación, vuelve a aplicar el tema, se reemplaza cualquier formato manual y la forma adopta todo el formato del tema.</span><span class="sxs-lookup"><span data-stu-id="7058e-114">If you subsequently reapply the theme, any manual formatting is overridden and the shape takes on all of the theme's formatting.</span></span> 
  
 <span data-ttu-id="7058e-115">**ISTHEMED** se evalúa como true si la celda [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) de la forma es mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="7058e-115">**ISTHEMED** evaluates to TRUE if the [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) cell in the shape is greater than 0.</span></span> <span data-ttu-id="7058e-116">Si esta celda es igual a 0, **ISTHEMED** se evalúa como false.</span><span class="sxs-lookup"><span data-stu-id="7058e-116">If this cell is equal to 0, then **ISTHEMED** evaluates to FALSE.</span></span> <span data-ttu-id="7058e-117">El tema de DocumentSheet y PageSheet no afectará al valor de la función **ISTHEMED** que se usa en ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="7058e-117">The theme of the DocumentSheet and PageSheet won't affect the value of the **ISTHEMED** function used in a ShapeSheet.</span></span> <span data-ttu-id="7058e-118">Sólo si la función **ISTHEMED** se muestra en PageSheet es la cuestión del tema de la página.</span><span class="sxs-lookup"><span data-stu-id="7058e-118">Only if the **ISTHEMED** function shows up in the PageSheet does the page's theme matter.</span></span> 
  
## <a name="example"></a><span data-ttu-id="7058e-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7058e-119">Example</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="7058e-120">Cell</span><span class="sxs-lookup"><span data-stu-id="7058e-120">Cell</span></span>  <br/> |<span data-ttu-id="7058e-121">Formula</span><span class="sxs-lookup"><span data-stu-id="7058e-121">Formula</span></span>  <br/> |<span data-ttu-id="7058e-122">Resultado</span><span class="sxs-lookup"><span data-stu-id="7058e-122">Result</span></span>  <br/> |
|<span data-ttu-id="7058e-123">Char. Font</span><span class="sxs-lookup"><span data-stu-id="7058e-123">Char.Font</span></span>  <br/> |<span data-ttu-id="7058e-124">IF (ISTHEMED (), THEMEVAL (), FONT ("caLibri"))</span><span class="sxs-lookup"><span data-stu-id="7058e-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span></span>  <br/> |<span data-ttu-id="7058e-125">Si la forma tiene un tema aplicado, el texto de la forma acepta el formato de fuente del tema.</span><span class="sxs-lookup"><span data-stu-id="7058e-125">If the shape has a themed applied to it, the shape text accepts the font formatting from the theme.</span></span> <span data-ttu-id="7058e-126">Si la forma no tiene temas, el texto de la forma tiene el formato de la fuente "caLibri".</span><span class="sxs-lookup"><span data-stu-id="7058e-126">If the shape is not themed, the shape text is formatted with the "Calibri" font.</span></span>  <br/> |
|<span data-ttu-id="7058e-127">LineColor</span><span class="sxs-lookup"><span data-stu-id="7058e-127">LineColor</span></span>  <br/> |<span data-ttu-id="7058e-128">SI (ISTHEMED, RGB (255, 0, 0), RGB (0, 255, 0))</span><span class="sxs-lookup"><span data-stu-id="7058e-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span></span>  <br/> |<span data-ttu-id="7058e-129">Si la forma tiene un temas aplicados, el color de la línea de la forma es rojo.</span><span class="sxs-lookup"><span data-stu-id="7058e-129">If the shape has a themed applied to it, the shape's line color is red.</span></span> <span data-ttu-id="7058e-130">Si la forma no tiene temas, el color de la línea de la forma es verde.</span><span class="sxs-lookup"><span data-stu-id="7058e-130">If the shape is not themed, the shape's line color is green.</span></span>  <br/> |
   

