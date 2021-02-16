---
title: Celda LockThemeFonts (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Impide que se altere la celda FontIndex de la fila Propiedades del tema aplicando un tema nuevo. No impide que los usuarios editen manualmente este valor en ShapeSheet.
ms.openlocfilehash: b3bd21c1dcd8c8c13d843c50cb29edcc5b8c4999
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421231"
---
# <a name="lockthemefonts-cell-protection-section"></a><span data-ttu-id="8d4b3-104">Celda LockThemeFonts (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="8d4b3-104">LockThemeFonts Cell (Protection Section)</span></span>

<span data-ttu-id="8d4b3-105">Impide que **se altere** la celda FontIndex de la **fila Propiedades** del tema aplicando un tema nuevo.</span><span class="sxs-lookup"><span data-stu-id="8d4b3-105">Prevents the **FontIndex** cell in the **Theme Properties** row from being altered by applying a new theme.</span></span> <span data-ttu-id="8d4b3-106">No impide que los usuarios editen manualmente este valor en ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8d4b3-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="8d4b3-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8d4b3-107">**Value**</span></span>|<span data-ttu-id="8d4b3-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8d4b3-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8d4b3-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="8d4b3-109">TRUE</span></span>  <br/> |<span data-ttu-id="8d4b3-110">La **celda FontIndex** no se puede cambiar desde su valor actual a menos que se cambie directamente en la ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8d4b3-110">The **FontIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="8d4b3-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="8d4b3-111">FALSE</span></span>  <br/> |<span data-ttu-id="8d4b3-112">La **celda FontIndex** se puede cambiar desde su valor actual cuando se cambia el tema.</span><span class="sxs-lookup"><span data-stu-id="8d4b3-112">The **FontIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d4b3-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8d4b3-113">Remarks</span></span>

<span data-ttu-id="8d4b3-114">Para obtener una referencia a la celda **LockThemeFonts** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** o desde un programa mediante la propiedad **CellsU,** utilice:</span><span class="sxs-lookup"><span data-stu-id="8d4b3-114">To get a reference to the **LockThemeFonts** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8d4b3-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="8d4b3-115">Cell name:</span></span>  <br/> | <span data-ttu-id="8d4b3-116">LockThemeFonts</span><span class="sxs-lookup"><span data-stu-id="8d4b3-116">LockThemeFonts</span></span>  <br/> |
   
<span data-ttu-id="8d4b3-117">Para obtener una referencia desde un programa a la celda **LockThemeFonts** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8d4b3-117">To get a reference to the **LockThemeFonts** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8d4b3-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="8d4b3-118">Section index:</span></span>  <br/> |<span data-ttu-id="8d4b3-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8d4b3-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8d4b3-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="8d4b3-120">Row index:</span></span>  <br/> |<span data-ttu-id="8d4b3-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="8d4b3-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="8d4b3-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="8d4b3-122">Cell index:</span></span>  <br/> |<span data-ttu-id="8d4b3-123">**visLockThemeFonts**</span><span class="sxs-lookup"><span data-stu-id="8d4b3-123">**visLockThemeFonts**</span></span> <br/> |
   

