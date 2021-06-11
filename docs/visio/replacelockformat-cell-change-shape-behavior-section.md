---
title: Celda ReplaceLockFormat (sección Cambiar comportamiento de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Indica si los valores de las celdas especificadas en una forma maestra sobrescriben los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de formas. Si la celda ReplaceLockFormat de una forma maestra está establecida en TRUE (1), los valores de formato del patrón sobrescriben todos los valores correspondientes de una forma que va a reemplazar el patrón.
ms.openlocfilehash: 88af22accb7a80640e7553338dae1af48934f246
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427237"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a><span data-ttu-id="c3521-104">Celda ReplaceLockFormat (sección Cambiar comportamiento de forma)</span><span class="sxs-lookup"><span data-stu-id="c3521-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="c3521-105">Indica si los valores de las celdas especificadas en una forma maestra sobrescriben los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de formas.</span><span class="sxs-lookup"><span data-stu-id="c3521-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="c3521-106">Si la **celda ReplaceLockFormat** de una forma maestra está establecida en TRUE (1), los valores de formato del patrón sobrescriben todos los valores correspondientes de una forma que va a reemplazar el patrón.</span><span class="sxs-lookup"><span data-stu-id="c3521-106">If the **ReplaceLockFormat** cell of a master shape is set to TRUE (1), the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span> 
  
|<span data-ttu-id="c3521-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c3521-107">**Value**</span></span>|<span data-ttu-id="c3521-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c3521-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c3521-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="c3521-109">TRUE</span></span>  <br/> |<span data-ttu-id="c3521-110">Si la **celda ReplaceLockFormat** de una forma maestra se establece en TRUE, los valores de formato del patrón sobrescriben todos los valores correspondientes de una forma que va a reemplazar el patrón.</span><span class="sxs-lookup"><span data-stu-id="c3521-110">If the **ReplaceLockFormat** cell of a master shape is set to TRUE, the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span>  <br/> |
|<span data-ttu-id="c3521-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="c3521-111">FALSE</span></span>  <br/> |<span data-ttu-id="c3521-112">Si la **celda ReplaceLockFormat** de una forma maestra está establecida en FALSE, la forma de reemplazo contiene los valores de formato locales de la forma antigua después de la operación de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="c3521-112">If the **ReplaceLockFormat** cell of a master shape is set to FALSE, the replacement shape contains the local formatting values from the old shape after the replacement operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3521-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c3521-113">Remarks</span></span>

<span data-ttu-id="c3521-114">La **celda ReplaceLockFormat** determina si la forma maestra sobrescribe los valores de formato locales de las celdas de las secciones siguientes durante una operación de reemplazo de formas:</span><span class="sxs-lookup"><span data-stu-id="c3521-114">The **ReplaceLockFormat** cell determines whether the master shape overwrites the local formatting values of the cells in the following sections during a shape replacement operation:</span></span> 
  
- <span data-ttu-id="c3521-115">**Sección Formato de** relleno</span><span class="sxs-lookup"><span data-stu-id="c3521-115">**Fill Format** section</span></span> 
    
- <span data-ttu-id="c3521-116">**Sección Formato de** línea</span><span class="sxs-lookup"><span data-stu-id="c3521-116">**Line Format** section</span></span> 
    
- <span data-ttu-id="c3521-117">**Sección Estilo** rápido</span><span class="sxs-lookup"><span data-stu-id="c3521-117">**Quick Style** section</span></span> 
    
- <span data-ttu-id="c3521-118">**Sección Propiedades del** tema</span><span class="sxs-lookup"><span data-stu-id="c3521-118">**Theme Properties** section</span></span> 
    
- <span data-ttu-id="c3521-119">**Sección Propiedades de** degradado</span><span class="sxs-lookup"><span data-stu-id="c3521-119">**Gradient Properties** section</span></span> 
    
- <span data-ttu-id="c3521-120">**Sección Propiedades de biselado**</span><span class="sxs-lookup"><span data-stu-id="c3521-120">**Bevel Properties** section</span></span> 
    
- <span data-ttu-id="c3521-121">**Sección Propiedades de efecto adicionales**</span><span class="sxs-lookup"><span data-stu-id="c3521-121">**Additional Effect Properties** section</span></span> 
    
- <span data-ttu-id="c3521-122">**Sección De paradas de degradado de** línea</span><span class="sxs-lookup"><span data-stu-id="c3521-122">**Line Gradient Stops** section</span></span> 
    
- <span data-ttu-id="c3521-123">**Sección Fill Gradient Stops**</span><span class="sxs-lookup"><span data-stu-id="c3521-123">**Fill Gradient Stops** section</span></span> 
    
<span data-ttu-id="c3521-124">Para obtener una referencia a la celda **ReplaceLockFormat** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la propiedad **CellsU,** use:</span><span class="sxs-lookup"><span data-stu-id="c3521-124">To get a reference to the **ReplaceLockFormat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c3521-125">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c3521-125">Cell name:</span></span>  <br/> | <span data-ttu-id="c3521-126">ReplaceLockFormat</span><span class="sxs-lookup"><span data-stu-id="c3521-126">ReplaceLockFormat</span></span>  <br/> |
   
<span data-ttu-id="c3521-127">Para obtener una referencia desde un programa a la celda **ReplaceLockFormat** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c3521-127">To get a reference to the **ReplaceLockFormat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c3521-128">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c3521-128">Section index:</span></span>  <br/> |<span data-ttu-id="c3521-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c3521-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c3521-130">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c3521-130">Row index:</span></span>  <br/> |<span data-ttu-id="c3521-131">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="c3521-131">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="c3521-132">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c3521-132">Cell index:</span></span>  <br/> |<span data-ttu-id="c3521-133">**visReplaceLockFormat**</span><span class="sxs-lookup"><span data-stu-id="c3521-133">**visReplaceLockFormat**</span></span> <br/> |
   

