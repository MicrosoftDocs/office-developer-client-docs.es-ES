---
title: Celda KeepTextFlat (sección Propiedades de rotación 3D)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Indica si el texto de una forma omitirá el giro de la forma en 3D. No se aplica a la rotación 2D.
ms.openlocfilehash: fc8cf2fac431645876c7f81ed9864cb6c2036169
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422043"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a><span data-ttu-id="cd71e-104">Celda KeepTextFlat (sección Propiedades de rotación 3D)</span><span class="sxs-lookup"><span data-stu-id="cd71e-104">KeepTextFlat Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="cd71e-105">Indica si el texto de una forma omitirá el giro de la forma en 3D.</span><span class="sxs-lookup"><span data-stu-id="cd71e-105">Indicates whether a shape's text will ignore the shape's rotation in 3-D.</span></span> <span data-ttu-id="cd71e-106">No se aplica a la rotación 2D.</span><span class="sxs-lookup"><span data-stu-id="cd71e-106">Does not apply to 2-D rotation.</span></span> 
  
****

|<span data-ttu-id="cd71e-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cd71e-107">**Value**</span></span>|<span data-ttu-id="cd71e-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd71e-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd71e-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="cd71e-109">TRUE</span></span>  <br/> |<span data-ttu-id="cd71e-110">El texto de la forma no gira con la geometría de la forma.</span><span class="sxs-lookup"><span data-stu-id="cd71e-110">Shape text does not rotate with the shape's geometry.</span></span>  <br/> |
|<span data-ttu-id="cd71e-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="cd71e-111">FALSE</span></span>  <br/> |<span data-ttu-id="cd71e-112">El texto de la forma se transforma para girar con la geometría de la forma.</span><span class="sxs-lookup"><span data-stu-id="cd71e-112">Shape text is transformed to rotate with the shape's geometry.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd71e-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd71e-113">Remarks</span></span>

<span data-ttu-id="cd71e-114">Para obtener una referencia a la **celda KeepTextFlat** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la propiedad **CellsU,** use:</span><span class="sxs-lookup"><span data-stu-id="cd71e-114">To get a reference to the **KeepTextFlat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd71e-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="cd71e-115">Cell name:</span></span>  <br/> |<span data-ttu-id="cd71e-116">KeepTextFlat</span><span class="sxs-lookup"><span data-stu-id="cd71e-116">KeepTextFlat</span></span>  <br/> |
   
<span data-ttu-id="cd71e-117">Para obtener una referencia desde un programa a la **celda KeepTextFlat** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="cd71e-117">To get a reference to the **KeepTextFlat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd71e-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="cd71e-118">Section index:</span></span>  <br/> |<span data-ttu-id="cd71e-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cd71e-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cd71e-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="cd71e-120">Row index:</span></span>  <br/> |<span data-ttu-id="cd71e-121">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="cd71e-121">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="cd71e-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="cd71e-122">Cell index:</span></span>  <br/> |<span data-ttu-id="cd71e-123">**visKeepTextFlat**</span><span class="sxs-lookup"><span data-stu-id="cd71e-123">**visKeepTextFlat**</span></span> <br/> |
   

