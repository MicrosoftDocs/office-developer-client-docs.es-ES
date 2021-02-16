---
title: Celda ReplaceLockText (Sección de comportamiento de cambio de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Indica si los valores de las celdas especificadas en una forma maestra sobrescriben los valores (incluidos los valores locales) de una forma que se va a reemplazar durante una operación de reemplazo de forma. ReplaceLockText determina si el texto que se muestra en el Patrón sobrescribe el texto de la forma que se va a reemplazar.
ms.openlocfilehash: 299bd571ad935886879abb11108c3d0bd28e3183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411921"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a><span data-ttu-id="2b4e8-104">Celda ReplaceLockText (Sección de comportamiento de cambio de forma)</span><span class="sxs-lookup"><span data-stu-id="2b4e8-104">ReplaceLockText Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="2b4e8-105">Indica si los valores de las celdas especificadas en una forma maestra sobrescriben los valores (incluidos los valores locales) de una forma que se va a reemplazar durante una operación de reemplazo de forma.</span><span class="sxs-lookup"><span data-stu-id="2b4e8-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="2b4e8-106">**ReplaceLockText determina** si el texto que se muestra en el Patrón sobrescribe el texto de la forma que se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="2b4e8-106">The **ReplaceLockText** determines whether the text displayed on the Master overwrites the text of the shape being replaced.</span></span> 
  
|<span data-ttu-id="2b4e8-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2b4e8-107">**Value**</span></span>|<span data-ttu-id="2b4e8-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b4e8-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2b4e8-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="2b4e8-109">TRUE</span></span>  <br/> | <span data-ttu-id="2b4e8-110">El texto de la forma maestra sobrescribe el texto de la forma antigua.</span><span class="sxs-lookup"><span data-stu-id="2b4e8-110">The text on the master shape overwrites the text on the old shape.</span></span> <span data-ttu-id="2b4e8-111">Además, la forma maestra sobrescribe los valores de las celdas de las secciones siguientes durante una operación de reemplazo de forma:</span><span class="sxs-lookup"><span data-stu-id="2b4e8-111">In addition, the master shape overwrites the values of the cells in the following sections during a shape replacement operation:</span></span>  <br/> <span data-ttu-id="2b4e8-112">**Sección Campos de** texto</span><span class="sxs-lookup"><span data-stu-id="2b4e8-112">**Text Fields** section</span></span>  <br/> <span data-ttu-id="2b4e8-113">**Sección Formato de bloque de** texto</span><span class="sxs-lookup"><span data-stu-id="2b4e8-113">**Text Block Format** section</span></span>  <br/> |
|<span data-ttu-id="2b4e8-114">FALSE</span><span class="sxs-lookup"><span data-stu-id="2b4e8-114">FALSE</span></span>  <br/> |<span data-ttu-id="2b4e8-115">La forma de reemplazo contiene cualquier texto, campos de texto u otras propiedades de texto de la forma antigua que se han agregado a la forma.</span><span class="sxs-lookup"><span data-stu-id="2b4e8-115">The replacement shape contains any text, text fields, or other text properties from the old shape that have been added to the shape.</span></span>  <br/> <span data-ttu-id="2b4e8-116">Cuando la forma de reemplazo contiene propiedades de texto de la  forma  antigua, la forma de reemplazo también tiene los valores de las secciones Carácter y Párrafo de la forma antigua si tienen más de una fila.</span><span class="sxs-lookup"><span data-stu-id="2b4e8-116">When the replacement shape contains text properties from the old shape, the replacement shape also has the values from the **Character** and **Paragraph** sections of the old shape if they have more than one row.</span></span>  <br/> |
   
<span data-ttu-id="2b4e8-117">Si se establece en TRUE (1), los valores de la forma Master reemplazan los valores de lo siguiente en la forma que se va a reemplazar:</span><span class="sxs-lookup"><span data-stu-id="2b4e8-117">If set to TRUE (1), the values of the shape Master replaces the values of the following on the shape being replaced:</span></span>
  
- [<span data-ttu-id="2b4e8-118">Celda TheText (Sección de eventos)</span><span class="sxs-lookup"><span data-stu-id="2b4e8-118">TheText Cell (Events Section)</span></span>](thetext-cell-events-section.md)
    
- <span data-ttu-id="2b4e8-119">Celdas de la [sección de caracteres](character-section.md)</span><span class="sxs-lookup"><span data-stu-id="2b4e8-119">Cells in the [Character Section](character-section.md)</span></span>
    
- <span data-ttu-id="2b4e8-120">Celdas de la [sección de párrafo](paragraph-section.md)</span><span class="sxs-lookup"><span data-stu-id="2b4e8-120">Cells in the [Paragraph Section](paragraph-section.md)</span></span>
    
- <span data-ttu-id="2b4e8-121">Celdas de la [sección de pestañas](tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="2b4e8-121">Cells in the [Tabs Section](tabs-section.md)</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2b4e8-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2b4e8-122">Remarks</span></span>

<span data-ttu-id="2b4e8-123">Para obtener una referencia a la celda **ReplaceLockText** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** o desde un programa mediante la propiedad **CellsU,** utilice:</span><span class="sxs-lookup"><span data-stu-id="2b4e8-123">To get a reference to the **ReplaceLockText** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2b4e8-124">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="2b4e8-124">Cell name:</span></span>  <br/> | <span data-ttu-id="2b4e8-125">ReplaceLockText</span><span class="sxs-lookup"><span data-stu-id="2b4e8-125">ReplaceLockText</span></span>  <br/> |
   
<span data-ttu-id="2b4e8-126">Para obtener una referencia desde un programa a la celda **ReplaceLockText** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2b4e8-126">To get a reference to the **ReplaceLockText** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2b4e8-127">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="2b4e8-127">Section index:</span></span>  <br/> |<span data-ttu-id="2b4e8-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2b4e8-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2b4e8-129">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="2b4e8-129">Row index:</span></span>  <br/> |<span data-ttu-id="2b4e8-130">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="2b4e8-130">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="2b4e8-131">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="2b4e8-131">Cell index:</span></span>  <br/> |<span data-ttu-id="2b4e8-132">**visReplaceLockText**</span><span class="sxs-lookup"><span data-stu-id="2b4e8-132">**visReplaceLockText**</span></span> <br/> |
   

