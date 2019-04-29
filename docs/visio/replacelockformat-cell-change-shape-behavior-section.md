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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427237"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a><span data-ttu-id="09dee-104">Celda ReplaceLockFormat (sección cambiar comportamiento de forma)</span><span class="sxs-lookup"><span data-stu-id="09dee-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="09dee-105">Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de forma.</span><span class="sxs-lookup"><span data-stu-id="09dee-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="09dee-106">Si la celda **ReplaceLockFormat** de una forma de patrón se establece en true (1), los valores de formato del patrón sobrescribirán todos los valores correspondientes de una forma que sea reemplazado por el patrón.</span><span class="sxs-lookup"><span data-stu-id="09dee-106">If the **ReplaceLockFormat** cell of a master shape is set to TRUE (1), the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span> 
  
|<span data-ttu-id="09dee-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="09dee-107">**Value**</span></span>|<span data-ttu-id="09dee-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="09dee-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="09dee-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="09dee-109">TRUE</span></span>  <br/> |<span data-ttu-id="09dee-110">Si la celda **ReplaceLockFormat** de una forma de patrón está establecida en true, los valores de formato del patrón sobrescribirán todos los valores correspondientes de una forma que sea reemplazado por el patrón.</span><span class="sxs-lookup"><span data-stu-id="09dee-110">If the **ReplaceLockFormat** cell of a master shape is set to TRUE, the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span>  <br/> |
|<span data-ttu-id="09dee-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="09dee-111">FALSE</span></span>  <br/> |<span data-ttu-id="09dee-112">Si la celda **ReplaceLockFormat** de una forma de patrón está establecida en false, la nueva forma de reemplazo contiene los valores de formato local de la forma antigua después de la operación de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="09dee-112">If the **ReplaceLockFormat** cell of a master shape is set to FALSE, the replacement shape contains the local formatting values from the old shape after the replacement operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="09dee-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09dee-113">Remarks</span></span>

<span data-ttu-id="09dee-114">La celda **ReplaceLockFormat** determina si la forma de patrón sobrescribirá los valores de formato local de las celdas de las siguientes secciones durante una operación de reemplazo de formas:</span><span class="sxs-lookup"><span data-stu-id="09dee-114">The **ReplaceLockFormat** cell determines whether the master shape overwrites the local formatting values of the cells in the following sections during a shape replacement operation:</span></span> 
  
- <span data-ttu-id="09dee-115">Sección de **formato de relleno**</span><span class="sxs-lookup"><span data-stu-id="09dee-115">**Fill Format** section</span></span> 
    
- <span data-ttu-id="09dee-116">Sección de **formato de línea**</span><span class="sxs-lookup"><span data-stu-id="09dee-116">**Line Format** section</span></span> 
    
- <span data-ttu-id="09dee-117">Sección de **estilo rápido**</span><span class="sxs-lookup"><span data-stu-id="09dee-117">**Quick Style** section</span></span> 
    
- <span data-ttu-id="09dee-118">Sección **propiedades del tema**</span><span class="sxs-lookup"><span data-stu-id="09dee-118">**Theme Properties** section</span></span> 
    
- <span data-ttu-id="09dee-119">Sección **propiedades** de degradado</span><span class="sxs-lookup"><span data-stu-id="09dee-119">**Gradient Properties** section</span></span> 
    
- <span data-ttu-id="09dee-120">Sección **propiedades de bisel**</span><span class="sxs-lookup"><span data-stu-id="09dee-120">**Bevel Properties** section</span></span> 
    
- <span data-ttu-id="09dee-121">Sección **propiedades del efecto adicional**</span><span class="sxs-lookup"><span data-stu-id="09dee-121">**Additional Effect Properties** section</span></span> 
    
- <span data-ttu-id="09dee-122">Sección degradado de **línea en puntos**</span><span class="sxs-lookup"><span data-stu-id="09dee-122">**Line Gradient Stops** section</span></span> 
    
- <span data-ttu-id="09dee-123">Sección de delimitadores de **relleno**</span><span class="sxs-lookup"><span data-stu-id="09dee-123">**Fill Gradient Stops** section</span></span> 
    
<span data-ttu-id="09dee-124">Para obtener una referencia a la celda **ReplaceLockFormat** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="09dee-124">To get a reference to the **ReplaceLockFormat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="09dee-125">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="09dee-125">Cell name:</span></span>  <br/> | <span data-ttu-id="09dee-126">ReplaceLockFormat</span><span class="sxs-lookup"><span data-stu-id="09dee-126">ReplaceLockFormat</span></span>  <br/> |
   
<span data-ttu-id="09dee-127">Para obtener una referencia desde un programa a la celda **ReplaceLockFormat** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="09dee-127">To get a reference to the **ReplaceLockFormat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="09dee-128">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="09dee-128">Section index:</span></span>  <br/> |<span data-ttu-id="09dee-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="09dee-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="09dee-130">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="09dee-130">Row index:</span></span>  <br/> |<span data-ttu-id="09dee-131">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="09dee-131">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="09dee-132">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="09dee-132">Cell index:</span></span>  <br/> |<span data-ttu-id="09dee-133">**visReplaceLockFormat**</span><span class="sxs-lookup"><span data-stu-id="09dee-133">**visReplaceLockFormat**</span></span> <br/> |
   

