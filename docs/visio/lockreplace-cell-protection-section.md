---
title: Celda LockReplace (sección Protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Indica si una forma puede participar en una operación de reemplazo (como un destino o una forma de reemplazo).
ms.openlocfilehash: 6f3e41d6a6c5b28c55e21961de63d0cc20eeb129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822515"
---
# <a name="lockreplace-cell-protection-section"></a><span data-ttu-id="10e78-103">Celda LockReplace (sección Protección)</span><span class="sxs-lookup"><span data-stu-id="10e78-103">LockReplace Cell (Protection Section)</span></span>

<span data-ttu-id="10e78-104">Indica si una forma puede participar en una operación de reemplazo (como un destino o una forma de reemplazo).</span><span class="sxs-lookup"><span data-stu-id="10e78-104">Indicates whether a shape can participate in a replacement operation (as either a target or a replacement shape).</span></span> 
  
|<span data-ttu-id="10e78-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="10e78-105">**Value**</span></span>|<span data-ttu-id="10e78-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="10e78-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="10e78-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="10e78-107">TRUE</span></span>  <br/> |<span data-ttu-id="10e78-108">La forma no se puede reemplazar o se pueden usar como una forma de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="10e78-108">The shape cannot be replaced or be used as a replacement shape.</span></span>  <br/> <span data-ttu-id="10e78-109">Para una forma en el lienzo, se deshabilita el botón **Cambiar forma** cuando se selecciona la forma.</span><span class="sxs-lookup"><span data-stu-id="10e78-109">For a shape on the canvas, the **Change Shape** button is disabled when the shape is selected.</span></span>  <br/> <span data-ttu-id="10e78-110">Para una forma en una galería de símbolos, la forma no aparece como una forma de reemplazo cuando se hace clic en el botón **Cambiar forma** .</span><span class="sxs-lookup"><span data-stu-id="10e78-110">For a shape on a stencil, the shape does not appear as a replacement shape when the **Change Shape** button is clicked.</span></span>  <br/> |
|<span data-ttu-id="10e78-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="10e78-111">FALSE</span></span>  <br/> |<span data-ttu-id="10e78-112">La forma puede ser reemplazada o usar como una forma de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="10e78-112">The shape can be replaced or used as a replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10e78-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="10e78-113">Remarks</span></span>

<span data-ttu-id="10e78-114">Para obtener una referencia a la celda **LockReplace** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="10e78-114">To get a reference to the **LockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="10e78-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="10e78-115">Cell name:</span></span>  <br/> | <span data-ttu-id="10e78-116">LockReplace</span><span class="sxs-lookup"><span data-stu-id="10e78-116">LockReplace</span></span>  <br/> |
   
<span data-ttu-id="10e78-117">Para obtener una referencia a la celda **LockReplace** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="10e78-117">To get a reference to the **LockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="10e78-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="10e78-118">Section index:</span></span>  <br/> |<span data-ttu-id="10e78-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="10e78-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="10e78-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="10e78-120">Row index:</span></span>  <br/> |<span data-ttu-id="10e78-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="10e78-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="10e78-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="10e78-122">Cell index:</span></span>  <br/> |<span data-ttu-id="10e78-123">**visLockReplace**</span><span class="sxs-lookup"><span data-stu-id="10e78-123">**visLockReplace**</span></span> <br/> |
   

