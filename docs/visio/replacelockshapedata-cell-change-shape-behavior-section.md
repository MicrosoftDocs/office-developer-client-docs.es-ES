---
title: Celda ReplaceLockShapeData (sección cambiar comportamiento de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de forma. ReplaceLockShapeData determina si los datos de formas de la forma de patrón sobrescribirán todos los datos de formas de la forma que se va a reemplazar.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348345"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a><span data-ttu-id="274eb-104">Celda ReplaceLockShapeData (sección cambiar comportamiento de forma)</span><span class="sxs-lookup"><span data-stu-id="274eb-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="274eb-105">Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de forma.</span><span class="sxs-lookup"><span data-stu-id="274eb-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="274eb-106">**ReplaceLockShapeData** determina si los datos de formas de la forma de patrón sobrescribirán todos los datos de formas de la forma que se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="274eb-106">The **ReplaceLockShapeData** determines whether the shape data of the master shape overwrites all of the shape data of the shape being replaced.</span></span> 
  
|<span data-ttu-id="274eb-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="274eb-107">**Value**</span></span>|<span data-ttu-id="274eb-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="274eb-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="274eb-109">1 (TRUE)</span><span class="sxs-lookup"><span data-stu-id="274eb-109">1 (TRUE)</span></span>  <br/> |<span data-ttu-id="274eb-110">Todas las filas y valores de la sección **datos de formas** de la forma de patrón se copian en la forma de reemplazo y se descartan todos los valores locales de la forma antigua que se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="274eb-110">All rows and values of the **Shape Data** section of the master shape are copied onto the replacement shape and any local values from the old shape being replaced are discarded.</span></span>  <br/> |
|<span data-ttu-id="274eb-111">0 (FALSO)</span><span class="sxs-lookup"><span data-stu-id="274eb-111">0 (FALSE)</span></span>  <br/> |<span data-ttu-id="274eb-112">Las filas y los valores de la sección **datos de formas** de la forma de patrón se copian a la nueva forma.</span><span class="sxs-lookup"><span data-stu-id="274eb-112">The rows and values of the **Shape Data** section of the master shape are copied to the replacement shape.</span></span> <span data-ttu-id="274eb-113">Las filas de la sección **datos de formas** de la forma antigua con valores locales se transfieren a la nueva forma.</span><span class="sxs-lookup"><span data-stu-id="274eb-113">Any rows in the **Shape Data** section of the old shape with local values are transferred to the replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="274eb-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="274eb-114">Remarks</span></span>

<span data-ttu-id="274eb-115">Para obtener una referencia a la celda **ReplaceLockShapeData** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="274eb-115">To get a reference to the **ReplaceLockShapeData** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="274eb-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="274eb-116">Cell name:</span></span>  <br/> | <span data-ttu-id="274eb-117">ReplaceLockShapeData</span><span class="sxs-lookup"><span data-stu-id="274eb-117">ReplaceLockShapeData</span></span>  <br/> |
   
<span data-ttu-id="274eb-118">Para obtener una referencia desde un programa a la celda **ReplaceLockShapeData** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="274eb-118">To get a reference to the **ReplaceLockShapeData** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="274eb-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="274eb-119">Section index:</span></span>  <br/> |<span data-ttu-id="274eb-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="274eb-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="274eb-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="274eb-121">Row index:</span></span>  <br/> |<span data-ttu-id="274eb-122">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="274eb-122">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="274eb-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="274eb-123">Cell index:</span></span>  <br/> |<span data-ttu-id="274eb-124">**visReplaceLockShapeData**</span><span class="sxs-lookup"><span data-stu-id="274eb-124">**visReplaceLockShapeData**</span></span> <br/> |
   

