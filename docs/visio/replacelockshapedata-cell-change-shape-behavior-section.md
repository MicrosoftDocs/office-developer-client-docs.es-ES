---
title: Celda ReplaceLockShapeData (sección Cambiar comportamiento de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma reemplazada durante una operación de reemplazo de la forma. El ReplaceLockShapeData determina si los datos de formas de la forma de patrón sobrescriben todos los datos de la forma de la forma reemplazada.
ms.openlocfilehash: 07547140c7c96e49663270e51a90fd559afedf29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822978"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a><span data-ttu-id="78082-104">Celda ReplaceLockShapeData (sección Cambiar comportamiento de forma)</span><span class="sxs-lookup"><span data-stu-id="78082-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="78082-105">Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma reemplazada durante una operación de reemplazo de la forma.</span><span class="sxs-lookup"><span data-stu-id="78082-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="78082-106">El **ReplaceLockShapeData** determina si los datos de formas de la forma de patrón sobrescriben todos los datos de la forma de la forma reemplazada.</span><span class="sxs-lookup"><span data-stu-id="78082-106">The **ReplaceLockShapeData** determines whether the shape data of the master shape overwrites all of the shape data of the shape being replaced.</span></span> 
  
|<span data-ttu-id="78082-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="78082-107">**Value**</span></span>|<span data-ttu-id="78082-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="78082-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="78082-109">1 (TRUE)</span><span class="sxs-lookup"><span data-stu-id="78082-109">1 (TRUE)</span></span>  <br/> |<span data-ttu-id="78082-110">Todas las filas y valores de la sección **Datos de formas** de la forma de patrón se copian en la forma de reemplazo y los valores locales de la forma antigua reemplazada se descartan.</span><span class="sxs-lookup"><span data-stu-id="78082-110">All rows and values of the **Shape Data** section of the master shape are copied onto the replacement shape and any local values from the old shape being replaced are discarded.</span></span>  <br/> |
|<span data-ttu-id="78082-111">0 (FALSO)</span><span class="sxs-lookup"><span data-stu-id="78082-111">0 (FALSE)</span></span>  <br/> |<span data-ttu-id="78082-112">Las filas y valores de la sección **Datos de formas** de la forma de patrón se copian en la nueva forma.</span><span class="sxs-lookup"><span data-stu-id="78082-112">The rows and values of the **Shape Data** section of the master shape are copied to the replacement shape.</span></span> <span data-ttu-id="78082-113">Todas las filas en la sección **Datos de formas** de la forma antigua con valores locales se transfieren a la nueva forma.</span><span class="sxs-lookup"><span data-stu-id="78082-113">Any rows in the **Shape Data** section of the old shape with local values are transferred to the replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78082-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="78082-114">Remarks</span></span>

<span data-ttu-id="78082-115">Para obtener una referencia a la celda **ReplaceLockShapeData** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="78082-115">To get a reference to the **ReplaceLockShapeData** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="78082-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="78082-116">Cell name:</span></span>  <br/> | <span data-ttu-id="78082-117">ReplaceLockShapeData</span><span class="sxs-lookup"><span data-stu-id="78082-117">ReplaceLockShapeData</span></span>  <br/> |
   
<span data-ttu-id="78082-118">Para obtener una referencia a la celda **ReplaceLockShapeData** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="78082-118">To get a reference to the **ReplaceLockShapeData** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="78082-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="78082-119">Section index:</span></span>  <br/> |<span data-ttu-id="78082-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="78082-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="78082-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="78082-121">Row index:</span></span>  <br/> |<span data-ttu-id="78082-122">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="78082-122">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="78082-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="78082-123">Cell index:</span></span>  <br/> |<span data-ttu-id="78082-124">**visReplaceLockShapeData**</span><span class="sxs-lookup"><span data-stu-id="78082-124">**visReplaceLockShapeData**</span></span> <br/> |
   

