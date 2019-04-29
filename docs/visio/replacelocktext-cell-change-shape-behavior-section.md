---
title: Celda ReplaceLockText (sección cambiar comportamiento de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de forma. ReplaceLockText determina si el texto que se muestra en el patrón sobrescribe el texto de la forma que se va a reemplazar.
ms.openlocfilehash: 299bd571ad935886879abb11108c3d0bd28e3183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411921"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a><span data-ttu-id="47247-104">Celda ReplaceLockText (sección cambiar comportamiento de forma)</span><span class="sxs-lookup"><span data-stu-id="47247-104">ReplaceLockText Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="47247-105">Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de forma.</span><span class="sxs-lookup"><span data-stu-id="47247-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="47247-106">**ReplaceLockText** determina si el texto que se muestra en el patrón sobrescribe el texto de la forma que se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="47247-106">The **ReplaceLockText** determines whether the text displayed on the Master overwrites the text of the shape being replaced.</span></span> 
  
|<span data-ttu-id="47247-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="47247-107">**Value**</span></span>|<span data-ttu-id="47247-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="47247-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="47247-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="47247-109">TRUE</span></span>  <br/> | <span data-ttu-id="47247-110">El texto de la forma patrón sobrescribirá el texto de la forma antigua.</span><span class="sxs-lookup"><span data-stu-id="47247-110">The text on the master shape overwrites the text on the old shape.</span></span> <span data-ttu-id="47247-111">Además, la forma de patrón sobrescribe los valores de las celdas de las siguientes secciones durante una operación de reemplazo de formas:</span><span class="sxs-lookup"><span data-stu-id="47247-111">In addition, the master shape overwrites the values of the cells in the following sections during a shape replacement operation:</span></span>  <br/> <span data-ttu-id="47247-112">Sección de **campos de texto**</span><span class="sxs-lookup"><span data-stu-id="47247-112">**Text Fields** section</span></span>  <br/> <span data-ttu-id="47247-113">Sección **formato del bloque de texto**</span><span class="sxs-lookup"><span data-stu-id="47247-113">**Text Block Format** section</span></span>  <br/> |
|<span data-ttu-id="47247-114">FALSE</span><span class="sxs-lookup"><span data-stu-id="47247-114">FALSE</span></span>  <br/> |<span data-ttu-id="47247-115">La forma de reemplazo contiene cualquier texto, campos de texto u otras propiedades de texto de la forma antigua que se hayan agregado a la forma.</span><span class="sxs-lookup"><span data-stu-id="47247-115">The replacement shape contains any text, text fields, or other text properties from the old shape that have been added to the shape.</span></span>  <br/> <span data-ttu-id="47247-116">Cuando la forma de reemplazo contiene propiedades de texto de la forma antigua, la nueva forma de reemplazo también tiene los valores de las secciones de **carácter** y de **párrafo** de la forma antigua si tienen más de una fila.</span><span class="sxs-lookup"><span data-stu-id="47247-116">When the replacement shape contains text properties from the old shape, the replacement shape also has the values from the **Character** and **Paragraph** sections of the old shape if they have more than one row.</span></span>  <br/> |
   
<span data-ttu-id="47247-117">Si se establece en TRUE (1), los valores de la forma principal reemplazan los valores de los siguientes en la forma que se está reemplazando:</span><span class="sxs-lookup"><span data-stu-id="47247-117">If set to TRUE (1), the values of the shape Master replaces the values of the following on the shape being replaced:</span></span>
  
- [<span data-ttu-id="47247-118">Celda TheText (Sección de eventos)</span><span class="sxs-lookup"><span data-stu-id="47247-118">TheText Cell (Events Section)</span></span>](thetext-cell-events-section.md)
    
- <span data-ttu-id="47247-119">Celdas de la [sección de caracteres](character-section.md)</span><span class="sxs-lookup"><span data-stu-id="47247-119">Cells in the [Character Section](character-section.md)</span></span>
    
- <span data-ttu-id="47247-120">Celdas de la [sección de párrafo](paragraph-section.md)</span><span class="sxs-lookup"><span data-stu-id="47247-120">Cells in the [Paragraph Section](paragraph-section.md)</span></span>
    
- <span data-ttu-id="47247-121">Celdas de la [sección](tabs-section.md) de tabulaciones</span><span class="sxs-lookup"><span data-stu-id="47247-121">Cells in the [Tabs Section](tabs-section.md)</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47247-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="47247-122">Remarks</span></span>

<span data-ttu-id="47247-123">Para obtener una referencia a la celda **ReplaceLockText** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="47247-123">To get a reference to the **ReplaceLockText** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="47247-124">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="47247-124">Cell name:</span></span>  <br/> | <span data-ttu-id="47247-125">ReplaceLockText</span><span class="sxs-lookup"><span data-stu-id="47247-125">ReplaceLockText</span></span>  <br/> |
   
<span data-ttu-id="47247-126">Para obtener una referencia desde un programa a la celda **ReplaceLockText** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="47247-126">To get a reference to the **ReplaceLockText** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="47247-127">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="47247-127">Section index:</span></span>  <br/> |<span data-ttu-id="47247-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="47247-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="47247-129">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="47247-129">Row index:</span></span>  <br/> |<span data-ttu-id="47247-130">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="47247-130">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="47247-131">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="47247-131">Cell index:</span></span>  <br/> |<span data-ttu-id="47247-132">**visReplaceLockText**</span><span class="sxs-lookup"><span data-stu-id="47247-132">**visReplaceLockText**</span></span> <br/> |
   

