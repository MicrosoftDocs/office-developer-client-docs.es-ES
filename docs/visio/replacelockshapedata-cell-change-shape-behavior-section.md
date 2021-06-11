---
title: Celda ReplaceLockShapeData (sección Cambiar comportamiento de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Indica si los valores de las celdas especificadas en una forma maestra sobrescriben los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de formas. ReplaceLockShapeData determina si los datos de formas de la forma maestra sobrescriben todos los datos de formas de la forma que se va a reemplazar.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408876"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a><span data-ttu-id="7e15a-104">Celda ReplaceLockShapeData (sección Cambiar comportamiento de forma)</span><span class="sxs-lookup"><span data-stu-id="7e15a-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="7e15a-105">Indica si los valores de las celdas especificadas en una forma maestra sobrescriben los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de formas.</span><span class="sxs-lookup"><span data-stu-id="7e15a-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="7e15a-106">**ReplaceLockShapeData determina** si los datos de formas de la forma maestra sobrescriben todos los datos de formas de la forma que se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="7e15a-106">The **ReplaceLockShapeData** determines whether the shape data of the master shape overwrites all of the shape data of the shape being replaced.</span></span> 
  
|<span data-ttu-id="7e15a-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7e15a-107">**Value**</span></span>|<span data-ttu-id="7e15a-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7e15a-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e15a-109">1 (TRUE)</span><span class="sxs-lookup"><span data-stu-id="7e15a-109">1 (TRUE)</span></span>  <br/> |<span data-ttu-id="7e15a-110">Todas las filas y valores de la sección **Datos** de formas de la forma maestra se copian en la forma de reemplazo y se descartan los valores locales de la forma antigua que se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="7e15a-110">All rows and values of the **Shape Data** section of the master shape are copied onto the replacement shape and any local values from the old shape being replaced are discarded.</span></span>  <br/> |
|<span data-ttu-id="7e15a-111">0 (FALSE)</span><span class="sxs-lookup"><span data-stu-id="7e15a-111">0 (FALSE)</span></span>  <br/> |<span data-ttu-id="7e15a-112">Las filas y los valores de la **sección Datos de** formas de la forma maestra se copian en la forma de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="7e15a-112">The rows and values of the **Shape Data** section of the master shape are copied to the replacement shape.</span></span> <span data-ttu-id="7e15a-113">Las filas de la **sección Datos de** formas de la forma antigua con valores locales se transfieren a la forma de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="7e15a-113">Any rows in the **Shape Data** section of the old shape with local values are transferred to the replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e15a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e15a-114">Remarks</span></span>

<span data-ttu-id="7e15a-115">Para obtener una referencia a la celda **ReplaceLockShapeData** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la propiedad **CellsU,** use:</span><span class="sxs-lookup"><span data-stu-id="7e15a-115">To get a reference to the **ReplaceLockShapeData** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7e15a-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="7e15a-116">Cell name:</span></span>  <br/> | <span data-ttu-id="7e15a-117">ReplaceLockShapeData</span><span class="sxs-lookup"><span data-stu-id="7e15a-117">ReplaceLockShapeData</span></span>  <br/> |
   
<span data-ttu-id="7e15a-118">Para obtener una referencia desde un programa a la celda **ReplaceLockShapeData** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7e15a-118">To get a reference to the **ReplaceLockShapeData** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7e15a-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="7e15a-119">Section index:</span></span>  <br/> |<span data-ttu-id="7e15a-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7e15a-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7e15a-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="7e15a-121">Row index:</span></span>  <br/> |<span data-ttu-id="7e15a-122">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="7e15a-122">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="7e15a-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="7e15a-123">Cell index:</span></span>  <br/> |<span data-ttu-id="7e15a-124">**visReplaceLockShapeData**</span><span class="sxs-lookup"><span data-stu-id="7e15a-124">**visReplaceLockShapeData**</span></span> <br/> |
   

