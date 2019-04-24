---
title: Celda QuickStyleVariation (sección estilos rápidos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Determina si se invalidan las fórmulas y los valores de texto, línea y color de relleno (o una combinación de estas propiedades) mediante colores que contrastan con el fondo del diagrama. El valor es una operación OR bit a bit de 0, 1, 2, 4 y 8.
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360022"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="fe328-104">Celda QuickStyleVariation (sección estilos rápidos)</span><span class="sxs-lookup"><span data-stu-id="fe328-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="fe328-105">Determina si se invalidan las fórmulas y los valores de texto, línea y color de relleno (o una combinación de estas propiedades) mediante colores que contrastan con el fondo del diagrama.</span><span class="sxs-lookup"><span data-stu-id="fe328-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="fe328-106">El valor es una operación OR bit a bit de 0, 1, 2, 4 y 8.</span><span class="sxs-lookup"><span data-stu-id="fe328-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="fe328-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="fe328-107">**Value**</span></span>|<span data-ttu-id="fe328-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fe328-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe328-109">comprendi</span><span class="sxs-lookup"><span data-stu-id="fe328-109">0</span></span>  <br/> |<span data-ttu-id="fe328-110">No modifique el color de relleno, línea o texto de una forma (o cualquier combinación de esas propiedades) para que permanezca visible en el color de fondo especificado de un tema.</span><span class="sxs-lookup"><span data-stu-id="fe328-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="fe328-111">1</span><span class="sxs-lookup"><span data-stu-id="fe328-111">1</span></span>  <br/> |<span data-ttu-id="fe328-112">No modifique el color de relleno, línea o texto de una forma (o cualquier combinación de esas propiedades) para que permanezca visible en el color de fondo especificado de un tema.</span><span class="sxs-lookup"><span data-stu-id="fe328-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="fe328-113">segundo</span><span class="sxs-lookup"><span data-stu-id="fe328-113">2</span></span>  <br/> |<span data-ttu-id="fe328-114">Alterar el color del texto de una forma, si es necesario, que permanezca visible en el color de fondo especificado de un tema.</span><span class="sxs-lookup"><span data-stu-id="fe328-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="fe328-115">4</span><span class="sxs-lookup"><span data-stu-id="fe328-115">4</span></span>  <br/> |<span data-ttu-id="fe328-116">Alterar el color de línea de una forma, si es necesario, para permanecer visible en el color de fondo especificado de un tema.</span><span class="sxs-lookup"><span data-stu-id="fe328-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="fe328-117">8,5</span><span class="sxs-lookup"><span data-stu-id="fe328-117">8</span></span>  <br/> |<span data-ttu-id="fe328-118">Altera el color de relleno de una forma, si es necesario, que permanezca visible en el color de fondo especificado de un tema.</span><span class="sxs-lookup"><span data-stu-id="fe328-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe328-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fe328-119">Remarks</span></span>

<span data-ttu-id="fe328-120">Utilice la celda QuickStyleVariation para garantizar la visibilidad en texto o líneas cuando están fuera de cualquier geometría de forma visible (por ejemplo, en una forma cuyo cuadro de texto está por debajo de la parte inferior de la forma, como los de diagramas de red).</span><span class="sxs-lookup"><span data-stu-id="fe328-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="fe328-121">El valor predeterminado de la celda es 0, lo que significa que su comportamiento es inactivo.</span><span class="sxs-lookup"><span data-stu-id="fe328-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="fe328-122">Cualquier otro valor desencadena el comportamiento de la celda.</span><span class="sxs-lookup"><span data-stu-id="fe328-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="fe328-123">El valor QuickStyleVariation reemplaza el valor producido por la función THEMEVAL cuando reside en las celdas color (sección de caracteres), FillForegnd o LineColor (o producidas por referencias directas a estas tres propiedades por medio de THEMEVAL) (" CharacterColor "), THEMEVAL (" FillColor ") y THEMEVAL (" LineColor ")).</span><span class="sxs-lookup"><span data-stu-id="fe328-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="fe328-124">Para obtener una referencia a la celda **QuickStyleVariation** por su nombre desde otra fórmula, obtenga el valor del atributo **N** de un elemento **Cell** , o de un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="fe328-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe328-125">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="fe328-125">Cell name:</span></span>  <br/> |<span data-ttu-id="fe328-126">QuickStyleVariation</span><span class="sxs-lookup"><span data-stu-id="fe328-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="fe328-127">Para obtener una referencia desde un programa a la celda **QuickStyleVariation** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="fe328-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe328-128">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="fe328-128">Section index:</span></span>  <br/> |<span data-ttu-id="fe328-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fe328-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fe328-130">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="fe328-130">Row index:</span></span>  <br/> |<span data-ttu-id="fe328-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="fe328-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="fe328-132">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="fe328-132">Cell index:</span></span>  <br/> |<span data-ttu-id="fe328-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="fe328-133">**visQuickStyleVariation**</span></span> <br/> |
   

