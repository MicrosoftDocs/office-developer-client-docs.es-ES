---
title: ISTHEMED (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Devuelve un valor Boolean que indica si una forma tiene un tema que se ha aplicado.
ms.openlocfilehash: 4311780d8686b5792e999c204ec182d23efb723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822400"
---
# <a name="isthemed-function"></a><span data-ttu-id="0757a-103">ISTHEMED (función)</span><span class="sxs-lookup"><span data-stu-id="0757a-103">ISTHEMED Function</span></span>

<span data-ttu-id="0757a-104">Devuelve un valor Boolean que indica si una forma tiene un tema que se ha aplicado.</span><span class="sxs-lookup"><span data-stu-id="0757a-104">Returns a Boolean value indicating whether a shape has a theme applied to it.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="0757a-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="0757a-105">Version Information</span></span>

<span data-ttu-id="0757a-106">Versión agregada: Visio 2013</span><span class="sxs-lookup"><span data-stu-id="0757a-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0757a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0757a-107">Syntax</span></span>

 <span data-ttu-id="0757a-108">**ISTHEMED** ()</span><span class="sxs-lookup"><span data-stu-id="0757a-108">**ISTHEMED**()</span></span>
  
## <a name="return-value"></a><span data-ttu-id="0757a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0757a-109">Return value</span></span>

<span data-ttu-id="0757a-110">Boolean</span><span class="sxs-lookup"><span data-stu-id="0757a-110">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0757a-111">Notas</span><span class="sxs-lookup"><span data-stu-id="0757a-111">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="0757a-112">La función **ISTHEMED** en Visio 2013 reemplaza la función **CELLISTHEMED** desde versiones anteriores de Visio.</span><span class="sxs-lookup"><span data-stu-id="0757a-112">The **ISTHEMED** function in Visio 2013 replaces the **CELLISTHEMED** function from previous versions of Visio.</span></span> 
  
<span data-ttu-id="0757a-113">El **ISTHEMED** permite asignar las partes adecuadas del formato de un tema a una forma de funcionar pero conservar la posibilidad de reemplazar otras partes del tema formato con el formato aplicado manualmente.</span><span class="sxs-lookup"><span data-stu-id="0757a-113">The **ISTHEMED** function lets you assign appropriate parts of a theme's formatting to a shape but retain the ability to override other parts of the theme formatting with manually-applied formatting.</span></span> <span data-ttu-id="0757a-114">Si posteriormente se vuelve a aplicar el tema, cualquier formato manual se anula y la forma toma en todos los de formato del tema.</span><span class="sxs-lookup"><span data-stu-id="0757a-114">If you subsequently reapply the theme, any manual formatting is overridden and the shape takes on all of the theme's formatting.</span></span> 
  
 <span data-ttu-id="0757a-115">**ISTHEMED** se evalúa como TRUE si la celda [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) de la forma es mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="0757a-115">**ISTHEMED** evaluates to TRUE if the [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) cell in the shape is greater than 0.</span></span> <span data-ttu-id="0757a-116">Si esta celda es igual a 0, **ISTHEMED** se evalúa como FALSE.</span><span class="sxs-lookup"><span data-stu-id="0757a-116">If this cell is equal to 0, then **ISTHEMED** evaluates to FALSE.</span></span> <span data-ttu-id="0757a-117">El tema de la DocumentSheet y PageSheet no afecta al valor de la función **ISTHEMED** que se utiliza en una hoja ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="0757a-117">The theme of the DocumentSheet and PageSheet won't affect the value of the **ISTHEMED** function used in a ShapeSheet.</span></span> <span data-ttu-id="0757a-118">Sólo si la función **ISTHEMED** se muestra en el PageSheet lo hace asunto del tema de la página.</span><span class="sxs-lookup"><span data-stu-id="0757a-118">Only if the **ISTHEMED** function shows up in the PageSheet does the page's theme matter.</span></span> 
  
## <a name="example"></a><span data-ttu-id="0757a-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0757a-119">Example</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="0757a-120">Celda</span><span class="sxs-lookup"><span data-stu-id="0757a-120">Cell</span></span>  <br/> |<span data-ttu-id="0757a-121">Fórmula</span><span class="sxs-lookup"><span data-stu-id="0757a-121">Formula</span></span>  <br/> |<span data-ttu-id="0757a-122">Resultado</span><span class="sxs-lookup"><span data-stu-id="0757a-122">Result</span></span>  <br/> |
|<span data-ttu-id="0757a-123">Char.Font</span><span class="sxs-lookup"><span data-stu-id="0757a-123">Char.Font</span></span>  <br/> |<span data-ttu-id="0757a-124">If(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span><span class="sxs-lookup"><span data-stu-id="0757a-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span></span>  <br/> |<span data-ttu-id="0757a-125">Si la forma tiene un estilo con que se ha aplicado, el texto de la forma acepta el formato del tema de fuente.</span><span class="sxs-lookup"><span data-stu-id="0757a-125">If the shape has a themed applied to it, the shape text accepts the font formatting from the theme.</span></span> <span data-ttu-id="0757a-126">Si la forma no es con temas, el texto de la forma tiene formato de la fuente "Calibri".</span><span class="sxs-lookup"><span data-stu-id="0757a-126">If the shape is not themed, the shape text is formatted with the "Calibri" font.</span></span>  <br/> |
|<span data-ttu-id="0757a-127">LineColor</span><span class="sxs-lookup"><span data-stu-id="0757a-127">LineColor</span></span>  <br/> |<span data-ttu-id="0757a-128">IF (ISTHEMED, RGB (255, 0, 0), RGB (0, 255, 0))</span><span class="sxs-lookup"><span data-stu-id="0757a-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span></span>  <br/> |<span data-ttu-id="0757a-129">Si la forma tiene un estilo con que se ha aplicado, el color de línea de la forma es rojo.</span><span class="sxs-lookup"><span data-stu-id="0757a-129">If the shape has a themed applied to it, the shape's line color is red.</span></span> <span data-ttu-id="0757a-130">Si la forma no es con temas, el color de línea de la forma es de color verde.</span><span class="sxs-lookup"><span data-stu-id="0757a-130">If the shape is not themed, the shape's line color is green.</span></span>  <br/> |
   

