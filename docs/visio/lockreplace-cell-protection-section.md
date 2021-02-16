---
title: Celda LockReplace (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Indica si una forma puede participar en una operación de reemplazo (como una forma de destino o de reemplazo).
ms.openlocfilehash: 8b0e3175cacd9b906d91a4185dcd98fad604d8bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404144"
---
# <a name="lockreplace-cell-protection-section"></a><span data-ttu-id="edbe2-103">Celda LockReplace (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="edbe2-103">LockReplace Cell (Protection Section)</span></span>

<span data-ttu-id="edbe2-104">Indica si una forma puede participar en una operación de reemplazo (como una forma de destino o de reemplazo).</span><span class="sxs-lookup"><span data-stu-id="edbe2-104">Indicates whether a shape can participate in a replacement operation (as either a target or a replacement shape).</span></span> 
  
|<span data-ttu-id="edbe2-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="edbe2-105">**Value**</span></span>|<span data-ttu-id="edbe2-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="edbe2-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="edbe2-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="edbe2-107">TRUE</span></span>  <br/> |<span data-ttu-id="edbe2-108">La forma no se puede reemplazar ni usar como forma de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="edbe2-108">The shape cannot be replaced or be used as a replacement shape.</span></span>  <br/> <span data-ttu-id="edbe2-109">Para una forma del lienzo, el botón Cambiar **forma** se deshabilita cuando se selecciona la forma.</span><span class="sxs-lookup"><span data-stu-id="edbe2-109">For a shape on the canvas, the **Change Shape** button is disabled when the shape is selected.</span></span>  <br/> <span data-ttu-id="edbe2-110">Para una forma de una galería de símbolos, la forma  no aparece como forma de reemplazo cuando se hace clic en el botón Cambiar forma.</span><span class="sxs-lookup"><span data-stu-id="edbe2-110">For a shape on a stencil, the shape does not appear as a replacement shape when the **Change Shape** button is clicked.</span></span>  <br/> |
|<span data-ttu-id="edbe2-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="edbe2-111">FALSE</span></span>  <br/> |<span data-ttu-id="edbe2-112">La forma se puede reemplazar o usar como forma de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="edbe2-112">The shape can be replaced or used as a replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edbe2-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edbe2-113">Remarks</span></span>

<span data-ttu-id="edbe2-114">Para obtener una referencia a la celda **LockReplace** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** o desde un programa mediante la propiedad **CellsU,** utilice:</span><span class="sxs-lookup"><span data-stu-id="edbe2-114">To get a reference to the **LockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="edbe2-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="edbe2-115">Cell name:</span></span>  <br/> | <span data-ttu-id="edbe2-116">LockReplace</span><span class="sxs-lookup"><span data-stu-id="edbe2-116">LockReplace</span></span>  <br/> |
   
<span data-ttu-id="edbe2-117">Para obtener una referencia desde un programa a **la celda LockReplace** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="edbe2-117">To get a reference to the **LockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="edbe2-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="edbe2-118">Section index:</span></span>  <br/> |<span data-ttu-id="edbe2-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="edbe2-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="edbe2-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="edbe2-120">Row index:</span></span>  <br/> |<span data-ttu-id="edbe2-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="edbe2-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="edbe2-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="edbe2-122">Cell index:</span></span>  <br/> |<span data-ttu-id="edbe2-123">**visLockReplace**</span><span class="sxs-lookup"><span data-stu-id="edbe2-123">**visLockReplace**</span></span> <br/> |
   

