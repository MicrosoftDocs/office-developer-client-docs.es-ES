---
title: Celda LockThemeFonts (sección Protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Impide que la celda FontIndex en la fila de propiedades del tema que se modifica aplicando un tema nuevo. Impedir que los usuarios editen manualmente este valor en la hoja ShapeSheet.
ms.openlocfilehash: b90ffe4c5555df017bb0506a78351514c954ec39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822553"
---
# <a name="lockthemefonts-cell-protection-section"></a><span data-ttu-id="118c9-104">Celda LockThemeFonts (sección Protección)</span><span class="sxs-lookup"><span data-stu-id="118c9-104">LockThemeFonts Cell (Protection Section)</span></span>

<span data-ttu-id="118c9-105">Impide que la celda **FontIndex** en la fila de **Propiedades del tema** que se modifica aplicando un tema nuevo.</span><span class="sxs-lookup"><span data-stu-id="118c9-105">Prevents the **FontIndex** cell in the **Theme Properties** row from being altered by applying a new theme.</span></span> <span data-ttu-id="118c9-106">Impedir que los usuarios editen manualmente este valor en la hoja ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="118c9-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="118c9-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="118c9-107">**Value**</span></span>|<span data-ttu-id="118c9-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="118c9-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="118c9-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="118c9-109">TRUE</span></span>  <br/> |<span data-ttu-id="118c9-110">No se puede cambiar la celda **FontIndex** desde su valor actual a menos que cambie directamente en la hoja ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="118c9-110">The **FontIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="118c9-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="118c9-111">FALSE</span></span>  <br/> |<span data-ttu-id="118c9-112">Puede cambiar el valor actual de la celda **FontIndex** cuando se cambia el tema.</span><span class="sxs-lookup"><span data-stu-id="118c9-112">The **FontIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="118c9-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="118c9-113">Remarks</span></span>

<span data-ttu-id="118c9-114">Para obtener una referencia a la celda **LockThemeFonts** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="118c9-114">To get a reference to the **LockThemeFonts** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="118c9-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="118c9-115">Cell name:</span></span>  <br/> | <span data-ttu-id="118c9-116">LockThemeFonts</span><span class="sxs-lookup"><span data-stu-id="118c9-116">LockThemeFonts</span></span>  <br/> |
   
<span data-ttu-id="118c9-117">Para obtener una referencia a la celda **LockThemeFonts** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="118c9-117">To get a reference to the **LockThemeFonts** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="118c9-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="118c9-118">Section index:</span></span>  <br/> |<span data-ttu-id="118c9-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="118c9-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="118c9-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="118c9-120">Row index:</span></span>  <br/> |<span data-ttu-id="118c9-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="118c9-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="118c9-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="118c9-122">Cell index:</span></span>  <br/> |<span data-ttu-id="118c9-123">**visLockThemeFonts**</span><span class="sxs-lookup"><span data-stu-id="118c9-123">**visLockThemeFonts**</span></span> <br/> |
   

