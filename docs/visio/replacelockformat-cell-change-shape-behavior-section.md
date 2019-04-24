---
title: Celda ReplaceLockFormat (sección cambiar comportamiento de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de forma. Si la celda ReplaceLockFormat de una forma de patrón se establece en TRUE (1), los valores de formato del patrón sobrescribirán todos los valores correspondientes de una forma que sea reemplazado por el patrón.
ms.openlocfilehash: 88af22accb7a80640e7553338dae1af48934f246
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329893"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a><span data-ttu-id="28c21-104">Celda ReplaceLockFormat (sección cambiar comportamiento de forma)</span><span class="sxs-lookup"><span data-stu-id="28c21-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="28c21-105">Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de forma.</span><span class="sxs-lookup"><span data-stu-id="28c21-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="28c21-106">Si la celda **ReplaceLockFormat** de una forma de patrón se establece en true (1), los valores de formato del patrón sobrescribirán todos los valores correspondientes de una forma que sea reemplazado por el patrón.</span><span class="sxs-lookup"><span data-stu-id="28c21-106">If the **ReplaceLockFormat** cell of a master shape is set to TRUE (1), the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span> 
  
|<span data-ttu-id="28c21-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="28c21-107">**Value**</span></span>|<span data-ttu-id="28c21-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28c21-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="28c21-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="28c21-109">TRUE</span></span>  <br/> |<span data-ttu-id="28c21-110">Si la celda **ReplaceLockFormat** de una forma de patrón está establecida en true, los valores de formato del patrón sobrescribirán todos los valores correspondientes de una forma que sea reemplazado por el patrón.</span><span class="sxs-lookup"><span data-stu-id="28c21-110">If the **ReplaceLockFormat** cell of a master shape is set to TRUE, the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span>  <br/> |
|<span data-ttu-id="28c21-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="28c21-111">FALSE</span></span>  <br/> |<span data-ttu-id="28c21-112">Si la celda **ReplaceLockFormat** de una forma de patrón está establecida en false, la nueva forma de reemplazo contiene los valores de formato local de la forma antigua después de la operación de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="28c21-112">If the **ReplaceLockFormat** cell of a master shape is set to FALSE, the replacement shape contains the local formatting values from the old shape after the replacement operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28c21-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="28c21-113">Remarks</span></span>

<span data-ttu-id="28c21-114">La celda **ReplaceLockFormat** determina si la forma de patrón sobrescribirá los valores de formato local de las celdas de las siguientes secciones durante una operación de reemplazo de formas:</span><span class="sxs-lookup"><span data-stu-id="28c21-114">The **ReplaceLockFormat** cell determines whether the master shape overwrites the local formatting values of the cells in the following sections during a shape replacement operation:</span></span> 
  
- <span data-ttu-id="28c21-115">Sección de **formato de relleno**</span><span class="sxs-lookup"><span data-stu-id="28c21-115">**Fill Format** section</span></span> 
    
- <span data-ttu-id="28c21-116">Sección de **formato de línea**</span><span class="sxs-lookup"><span data-stu-id="28c21-116">**Line Format** section</span></span> 
    
- <span data-ttu-id="28c21-117">Sección de **estilo rápido**</span><span class="sxs-lookup"><span data-stu-id="28c21-117">**Quick Style** section</span></span> 
    
- <span data-ttu-id="28c21-118">Sección **propiedades del tema**</span><span class="sxs-lookup"><span data-stu-id="28c21-118">**Theme Properties** section</span></span> 
    
- <span data-ttu-id="28c21-119">Sección **propiedades** de degradado</span><span class="sxs-lookup"><span data-stu-id="28c21-119">**Gradient Properties** section</span></span> 
    
- <span data-ttu-id="28c21-120">Sección **propiedades de bisel**</span><span class="sxs-lookup"><span data-stu-id="28c21-120">**Bevel Properties** section</span></span> 
    
- <span data-ttu-id="28c21-121">Sección **propiedades del efecto adicional**</span><span class="sxs-lookup"><span data-stu-id="28c21-121">**Additional Effect Properties** section</span></span> 
    
- <span data-ttu-id="28c21-122">Sección degradado de **línea en puntos**</span><span class="sxs-lookup"><span data-stu-id="28c21-122">**Line Gradient Stops** section</span></span> 
    
- <span data-ttu-id="28c21-123">Sección de delimitadores de **relleno**</span><span class="sxs-lookup"><span data-stu-id="28c21-123">**Fill Gradient Stops** section</span></span> 
    
<span data-ttu-id="28c21-124">Para obtener una referencia a la celda **ReplaceLockFormat** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="28c21-124">To get a reference to the **ReplaceLockFormat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="28c21-125">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="28c21-125">Cell name:</span></span>  <br/> | <span data-ttu-id="28c21-126">ReplaceLockFormat</span><span class="sxs-lookup"><span data-stu-id="28c21-126">ReplaceLockFormat</span></span>  <br/> |
   
<span data-ttu-id="28c21-127">Para obtener una referencia desde un programa a la celda **ReplaceLockFormat** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="28c21-127">To get a reference to the **ReplaceLockFormat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="28c21-128">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="28c21-128">Section index:</span></span>  <br/> |<span data-ttu-id="28c21-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="28c21-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="28c21-130">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="28c21-130">Row index:</span></span>  <br/> |<span data-ttu-id="28c21-131">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="28c21-131">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="28c21-132">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="28c21-132">Cell index:</span></span>  <br/> |<span data-ttu-id="28c21-133">**visReplaceLockFormat**</span><span class="sxs-lookup"><span data-stu-id="28c21-133">**visReplaceLockFormat**</span></span> <br/> |
   

