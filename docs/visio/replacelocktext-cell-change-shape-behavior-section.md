---
title: Celda ReplaceLockText (sección de comportamiento de cambio forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma reemplazada durante una operación de reemplazo de la forma. El ReplaceLockText determina si el texto que aparece en el maestro de sobrescribe el texto de la forma reemplazada.
ms.openlocfilehash: 75fb0831e7361345f04d7912eb0a55959d9417cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822989"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a><span data-ttu-id="d4793-104">Celda ReplaceLockText (sección de comportamiento de cambio forma)</span><span class="sxs-lookup"><span data-stu-id="d4793-104">ReplaceLockText Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="d4793-105">Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma reemplazada durante una operación de reemplazo de la forma.</span><span class="sxs-lookup"><span data-stu-id="d4793-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="d4793-106">El **ReplaceLockText** determina si el texto que aparece en el maestro de sobrescribe el texto de la forma reemplazada.</span><span class="sxs-lookup"><span data-stu-id="d4793-106">The **ReplaceLockText** determines whether the text displayed on the Master overwrites the text of the shape being replaced.</span></span> 
  
|<span data-ttu-id="d4793-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d4793-107">**Value**</span></span>|<span data-ttu-id="d4793-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d4793-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d4793-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="d4793-109">TRUE</span></span>  <br/> | <span data-ttu-id="d4793-110">El texto en la forma de patrón sobrescribe el texto de la forma anterior.</span><span class="sxs-lookup"><span data-stu-id="d4793-110">The text on the master shape overwrites the text on the old shape.</span></span> <span data-ttu-id="d4793-111">Además, la forma de patrón sobrescribe los valores de las celdas en las secciones siguientes durante una operación de reemplazo de forma:</span><span class="sxs-lookup"><span data-stu-id="d4793-111">In addition, the master shape overwrites the values of the cells in the following sections during a shape replacement operation:</span></span>  <br/> <span data-ttu-id="d4793-112">Sección de **Campos de texto**</span><span class="sxs-lookup"><span data-stu-id="d4793-112">**Text Fields** section</span></span>  <br/> <span data-ttu-id="d4793-113">Sección **Text Block Format**</span><span class="sxs-lookup"><span data-stu-id="d4793-113">**Text Block Format** section</span></span>  <br/> |
|<span data-ttu-id="d4793-114">FALSE</span><span class="sxs-lookup"><span data-stu-id="d4793-114">FALSE</span></span>  <br/> |<span data-ttu-id="d4793-115">La forma de reemplazo contiene cualquier texto, los campos de texto u otras propiedades de texto de la forma anterior que se han agregado a la forma.</span><span class="sxs-lookup"><span data-stu-id="d4793-115">The replacement shape contains any text, text fields, or other text properties from the old shape that have been added to the shape.</span></span>  <br/> <span data-ttu-id="d4793-116">Cuando la forma de reemplazo contiene las propiedades de texto de la forma anterior, la forma de reemplazo tiene también los valores de las secciones de **carácter** y de **párrafo** de la forma antigua si tienen más de una fila.</span><span class="sxs-lookup"><span data-stu-id="d4793-116">When the replacement shape contains text properties from the old shape, the replacement shape also has the values from the **Character** and **Paragraph** sections of the old shape if they have more than one row.</span></span>  <br/> |
   
<span data-ttu-id="d4793-117">Si se establece en TRUE (1), los valores de la forma patrón reemplaza los valores de las siguientes opciones en la forma reemplazada:</span><span class="sxs-lookup"><span data-stu-id="d4793-117">If set to TRUE (1), the values of the shape Master replaces the values of the following on the shape being replaced:</span></span>
  
- [<span data-ttu-id="d4793-118">Celda TheText (Sección de eventos)</span><span class="sxs-lookup"><span data-stu-id="d4793-118">TheText Cell (Events Section)</span></span>](thetext-cell-events-section.md)
    
- <span data-ttu-id="d4793-119">Celdas en la [sección de caracteres](character-section.md)</span><span class="sxs-lookup"><span data-stu-id="d4793-119">Cells in the [Character Section](character-section.md)</span></span>
    
- <span data-ttu-id="d4793-120">Celdas en la [sección de párrafo](paragraph-section.md)</span><span class="sxs-lookup"><span data-stu-id="d4793-120">Cells in the [Paragraph Section](paragraph-section.md)</span></span>
    
- <span data-ttu-id="d4793-121">Celdas en la [sección de tabulaciones](tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="d4793-121">Cells in the [Tabs Section](tabs-section.md)</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d4793-122">Notas</span><span class="sxs-lookup"><span data-stu-id="d4793-122">Remarks</span></span>

<span data-ttu-id="d4793-123">Para obtener una referencia a la celda **ReplaceLockText** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="d4793-123">To get a reference to the **ReplaceLockText** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4793-124">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d4793-124">Cell name:</span></span>  <br/> | <span data-ttu-id="d4793-125">ReplaceLockText</span><span class="sxs-lookup"><span data-stu-id="d4793-125">ReplaceLockText</span></span>  <br/> |
   
<span data-ttu-id="d4793-126">Para obtener una referencia a la celda **ReplaceLockText** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d4793-126">To get a reference to the **ReplaceLockText** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4793-127">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d4793-127">Section index:</span></span>  <br/> |<span data-ttu-id="d4793-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d4793-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d4793-129">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d4793-129">Row index:</span></span>  <br/> |<span data-ttu-id="d4793-130">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="d4793-130">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="d4793-131">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d4793-131">Cell index:</span></span>  <br/> |<span data-ttu-id="d4793-132">**visReplaceLockText**</span><span class="sxs-lookup"><span data-stu-id="d4793-132">**visReplaceLockText**</span></span> <br/> |
   

