---
title: Celda ReplaceLockFormat (sección de comportamiento de cambio forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma reemplazada durante una operación de reemplazo de la forma. Si la celda ReplaceLockFormat de una forma de patrón se establece en TRUE (1), los valores de formato del patrón sobrescriben todos los valores correspondientes de una forma que se reemplaza por el patrón.
ms.openlocfilehash: bf1e28353cc1e2d737a7d7a6dcd90caf14e19dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822956"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a><span data-ttu-id="08a92-104">Celda ReplaceLockFormat (sección de comportamiento de cambio forma)</span><span class="sxs-lookup"><span data-stu-id="08a92-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="08a92-105">Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma reemplazada durante una operación de reemplazo de la forma.</span><span class="sxs-lookup"><span data-stu-id="08a92-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="08a92-106">Si la celda **ReplaceLockFormat** de una forma de patrón se establece en TRUE (1), los valores de formato del patrón sobrescriben todos los valores correspondientes de una forma que se reemplaza por el patrón.</span><span class="sxs-lookup"><span data-stu-id="08a92-106">If the **ReplaceLockFormat** cell of a master shape is set to TRUE (1), the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span> 
  
|<span data-ttu-id="08a92-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="08a92-107">**Value**</span></span>|<span data-ttu-id="08a92-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="08a92-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="08a92-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="08a92-109">TRUE</span></span>  <br/> |<span data-ttu-id="08a92-110">Si la celda **ReplaceLockFormat** de una forma de patrón está establecida en TRUE, los valores de formato del patrón sobrescriben todos los valores correspondientes de una forma que se reemplaza por el patrón.</span><span class="sxs-lookup"><span data-stu-id="08a92-110">If the **ReplaceLockFormat** cell of a master shape is set to TRUE, the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span>  <br/> |
|<span data-ttu-id="08a92-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="08a92-111">FALSE</span></span>  <br/> |<span data-ttu-id="08a92-112">Si la celda **ReplaceLockFormat** de una forma de patrón se establece en FALSE, la forma de reemplazo contiene los valores de formato locales de la forma antigua después de la operación de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="08a92-112">If the **ReplaceLockFormat** cell of a master shape is set to FALSE, the replacement shape contains the local formatting values from the old shape after the replacement operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08a92-113">Notas</span><span class="sxs-lookup"><span data-stu-id="08a92-113">Remarks</span></span>

<span data-ttu-id="08a92-114">La celda **ReplaceLockFormat** determina si la forma de patrón sobrescribe los valores de formato locales de las celdas en las secciones siguientes durante una operación de reemplazo de forma:</span><span class="sxs-lookup"><span data-stu-id="08a92-114">The **ReplaceLockFormat** cell determines whether the master shape overwrites the local formatting values of the cells in the following sections during a shape replacement operation:</span></span> 
  
- <span data-ttu-id="08a92-115">Sección de **Formato de relleno**</span><span class="sxs-lookup"><span data-stu-id="08a92-115">**Fill Format** section</span></span> 
    
- <span data-ttu-id="08a92-116">Sección de **Formato de línea**</span><span class="sxs-lookup"><span data-stu-id="08a92-116">**Line Format** section</span></span> 
    
- <span data-ttu-id="08a92-117">Sección de **Estilos rápidos**</span><span class="sxs-lookup"><span data-stu-id="08a92-117">**Quick Style** section</span></span> 
    
- <span data-ttu-id="08a92-118">Sección de **Propiedades del tema**</span><span class="sxs-lookup"><span data-stu-id="08a92-118">**Theme Properties** section</span></span> 
    
- <span data-ttu-id="08a92-119">Sección de **Propiedades de degradado**</span><span class="sxs-lookup"><span data-stu-id="08a92-119">**Gradient Properties** section</span></span> 
    
- <span data-ttu-id="08a92-120">Sección de **Propiedades de bisel**</span><span class="sxs-lookup"><span data-stu-id="08a92-120">**Bevel Properties** section</span></span> 
    
- <span data-ttu-id="08a92-121">Sección de **Propiedades de efecto adicionales**</span><span class="sxs-lookup"><span data-stu-id="08a92-121">**Additional Effect Properties** section</span></span> 
    
- <span data-ttu-id="08a92-122">Sección de **Puntos de degradado en línea**</span><span class="sxs-lookup"><span data-stu-id="08a92-122">**Line Gradient Stops** section</span></span> 
    
- <span data-ttu-id="08a92-123">Sección de **Puntos de degradado de relleno**</span><span class="sxs-lookup"><span data-stu-id="08a92-123">**Fill Gradient Stops** section</span></span> 
    
<span data-ttu-id="08a92-124">Para obtener una referencia a la celda **ReplaceLockFormat** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="08a92-124">To get a reference to the **ReplaceLockFormat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="08a92-125">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="08a92-125">Cell name:</span></span>  <br/> | <span data-ttu-id="08a92-126">ReplaceLockFormat</span><span class="sxs-lookup"><span data-stu-id="08a92-126">ReplaceLockFormat</span></span>  <br/> |
   
<span data-ttu-id="08a92-127">Para obtener una referencia a la celda **ReplaceLockFormat** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="08a92-127">To get a reference to the **ReplaceLockFormat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="08a92-128">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="08a92-128">Section index:</span></span>  <br/> |<span data-ttu-id="08a92-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="08a92-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="08a92-130">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="08a92-130">Row index:</span></span>  <br/> |<span data-ttu-id="08a92-131">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="08a92-131">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="08a92-132">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="08a92-132">Cell index:</span></span>  <br/> |<span data-ttu-id="08a92-133">**visReplaceLockFormat**</span><span class="sxs-lookup"><span data-stu-id="08a92-133">**visReplaceLockFormat**</span></span> <br/> |
   

