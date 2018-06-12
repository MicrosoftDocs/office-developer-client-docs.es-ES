---
title: Celda KeepTextFlat (sección de propiedades de rotación 3D)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Indica si el texto de una forma pasará por alto la rotación de la forma en 3D. No se aplica a la rotación 2D.
ms.openlocfilehash: cf8b964360e602b81a2a7b7ca79961921eeeb8b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822398"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a><span data-ttu-id="c9f76-104">Celda KeepTextFlat (sección de propiedades de rotación 3D)</span><span class="sxs-lookup"><span data-stu-id="c9f76-104">KeepTextFlat Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="c9f76-105">Indica si el texto de una forma pasará por alto la rotación de la forma en 3D.</span><span class="sxs-lookup"><span data-stu-id="c9f76-105">Indicates whether a shape's text will ignore the shape's rotation in 3-D.</span></span> <span data-ttu-id="c9f76-106">No se aplica a la rotación 2D.</span><span class="sxs-lookup"><span data-stu-id="c9f76-106">Does not apply to 2-D rotation.</span></span> 
  
****

|<span data-ttu-id="c9f76-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c9f76-107">**Value**</span></span>|<span data-ttu-id="c9f76-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9f76-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c9f76-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="c9f76-109">TRUE</span></span>  <br/> |<span data-ttu-id="c9f76-110">Texto de la forma no gira con la geometría de la forma.</span><span class="sxs-lookup"><span data-stu-id="c9f76-110">Shape text does not rotate with the shape's geometry.</span></span>  <br/> |
|<span data-ttu-id="c9f76-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="c9f76-111">FALSE</span></span>  <br/> |<span data-ttu-id="c9f76-112">Texto de la forma se transforma para gira con la geometría de la forma.</span><span class="sxs-lookup"><span data-stu-id="c9f76-112">Shape text is transformed to rotate with the shape's geometry.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9f76-113">Notas</span><span class="sxs-lookup"><span data-stu-id="c9f76-113">Remarks</span></span>

<span data-ttu-id="c9f76-114">Para obtener una referencia a la celda **KeepTextFlat** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="c9f76-114">To get a reference to the **KeepTextFlat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9f76-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c9f76-115">Cell name:</span></span>  <br/> |<span data-ttu-id="c9f76-116">KeepTextFlat</span><span class="sxs-lookup"><span data-stu-id="c9f76-116">KeepTextFlat</span></span>  <br/> |
   
<span data-ttu-id="c9f76-117">Para obtener una referencia a la celda **KeepTextFlat** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c9f76-117">To get a reference to the **KeepTextFlat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9f76-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c9f76-118">Section index:</span></span>  <br/> |<span data-ttu-id="c9f76-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c9f76-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c9f76-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c9f76-120">Row index:</span></span>  <br/> |<span data-ttu-id="c9f76-121">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="c9f76-121">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="c9f76-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c9f76-122">Cell index:</span></span>  <br/> |<span data-ttu-id="c9f76-123">**visKeepTextFlat**</span><span class="sxs-lookup"><span data-stu-id="c9f76-123">**visKeepTextFlat**</span></span> <br/> |
   

