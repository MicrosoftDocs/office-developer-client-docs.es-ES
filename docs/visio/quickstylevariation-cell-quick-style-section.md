---
title: Celda QuickStyleVariation (sección de estilos rápidos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Determina si se deben reemplazar las fórmulas y los valores de texto, línea y relleno color (o una combinación de esas propiedades) mediante el uso de los colores que contraste con el fondo de diagrama. El valor es una operación OR bit a bit de 0, 1, 2, 4 y 8.
ms.openlocfilehash: fe6462798b61a0713f98196974876144cf4606e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822894"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="1c2b4-104">Celda QuickStyleVariation (sección de estilos rápidos)</span><span class="sxs-lookup"><span data-stu-id="1c2b4-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="1c2b4-105">Determina si se deben reemplazar las fórmulas y los valores de texto, línea y relleno color (o una combinación de esas propiedades) mediante el uso de los colores que contraste con el fondo de diagrama.</span><span class="sxs-lookup"><span data-stu-id="1c2b4-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="1c2b4-106">El valor es una operación OR bit a bit de 0, 1, 2, 4 y 8.</span><span class="sxs-lookup"><span data-stu-id="1c2b4-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="1c2b4-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1c2b4-107">**Value**</span></span>|<span data-ttu-id="1c2b4-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1c2b4-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1c2b4-109">0</span><span class="sxs-lookup"><span data-stu-id="1c2b4-109">0</span></span>  <br/> |<span data-ttu-id="1c2b4-110">No modifique el texto de una forma, línea, o relleno color (o cualquier combinación de esas propiedades) para permanecer visibles contra el color de fondo especificado de un tema.</span><span class="sxs-lookup"><span data-stu-id="1c2b4-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="1c2b4-111">1</span><span class="sxs-lookup"><span data-stu-id="1c2b4-111">1</span></span>  <br/> |<span data-ttu-id="1c2b4-112">No modifique el texto de una forma, línea, o relleno color (o cualquier combinación de esas propiedades) para permanecer visibles contra el color de fondo especificado de un tema.</span><span class="sxs-lookup"><span data-stu-id="1c2b4-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="1c2b4-113">2</span><span class="sxs-lookup"><span data-stu-id="1c2b4-113">2</span></span>  <br/> |<span data-ttu-id="1c2b4-114">Modificar el color del texto de una forma, si es necesario, se mantienen visibles contra un tema al indicar el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="1c2b4-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="1c2b4-115">4</span><span class="sxs-lookup"><span data-stu-id="1c2b4-115">4</span></span>  <br/> |<span data-ttu-id="1c2b4-116">Modificar el color de línea de una forma, si es necesario, se mantienen visibles contra un tema al indicar el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="1c2b4-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="1c2b4-117">8</span><span class="sxs-lookup"><span data-stu-id="1c2b4-117">8</span></span>  <br/> |<span data-ttu-id="1c2b4-118">Modificar el color de relleno de una forma, si es necesario, se mantienen visibles contra un tema al indicar el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="1c2b4-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c2b4-119">Notas</span><span class="sxs-lookup"><span data-stu-id="1c2b4-119">Remarks</span></span>

<span data-ttu-id="1c2b4-120">Utilice la celda QuickStyleVariation para garantizar la visibilidad en texto o líneas cuando están fuera de cualquier geometría de forma visible (por ejemplo, en una forma cuyo textbox está por debajo de la parte inferior de la forma, como las de diagramas de red).</span><span class="sxs-lookup"><span data-stu-id="1c2b4-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="1c2b4-121">Valor predeterminado de la celda es 0, lo que significa que su comportamiento está inactivo.</span><span class="sxs-lookup"><span data-stu-id="1c2b4-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="1c2b4-122">Cualquier otro valor, desencadena el comportamiento de la celda.</span><span class="sxs-lookup"><span data-stu-id="1c2b4-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="1c2b4-123">El valor de QuickStyleVariation invalida el valor generado por la función THEMEVAL cuando reside en el Color (sección de caracteres), FillForegnd o LineColor celdas (o producidos por referencias directas a estas tres propiedades por medio de THEMEVAL (" CharacterColor"), THEMEVAL("FillColor") y THEMEVAL("LineColor")).</span><span class="sxs-lookup"><span data-stu-id="1c2b4-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="1c2b4-124">Para obtener una referencia a la celda **QuickStyleVariation** por su nombre desde otra fórmula, mediante la obtención del valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="1c2b4-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c2b4-125">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="1c2b4-125">Cell name:</span></span>  <br/> |<span data-ttu-id="1c2b4-126">QuickStyleVariation</span><span class="sxs-lookup"><span data-stu-id="1c2b4-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="1c2b4-127">Para obtener una referencia a la celda **QuickStyleVariation** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1c2b4-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c2b4-128">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="1c2b4-128">Section index:</span></span>  <br/> |<span data-ttu-id="1c2b4-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1c2b4-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1c2b4-130">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="1c2b4-130">Row index:</span></span>  <br/> |<span data-ttu-id="1c2b4-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="1c2b4-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="1c2b4-132">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="1c2b4-132">Cell index:</span></span>  <br/> |<span data-ttu-id="1c2b4-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="1c2b4-133">**visQuickStyleVariation**</span></span> <br/> |
   

