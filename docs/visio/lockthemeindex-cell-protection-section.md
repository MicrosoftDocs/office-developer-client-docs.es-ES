---
title: Celda LockThemeIndex (sección Protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Impide que la celda ThemeIndex de la fila Propiedades del tema se altere aplicando un nuevo tema o seleccionando un nuevo esquema de conector. No impide que los usuarios editen manualmente este valor en ShapeSheet.
ms.openlocfilehash: 519c17f6e00c9aad2b5522bc66b41c0ceb75911b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411242"
---
# <a name="lockthemeindex-cell-protection-section"></a><span data-ttu-id="2339e-104">Celda LockThemeIndex (sección Protección)</span><span class="sxs-lookup"><span data-stu-id="2339e-104">LockThemeIndex Cell (Protection Section)</span></span>

<span data-ttu-id="2339e-105">Impide **que la celda ThemeIndex** de la fila **Propiedades** del tema se altere aplicando un nuevo tema o seleccionando un nuevo esquema de conector.</span><span class="sxs-lookup"><span data-stu-id="2339e-105">Prevents **ThemeIndex** cell in **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="2339e-106">No impide que los usuarios editen manualmente este valor en ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="2339e-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="2339e-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2339e-107">**Value**</span></span>|<span data-ttu-id="2339e-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2339e-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2339e-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="2339e-109">TRUE</span></span>  <br/> |<span data-ttu-id="2339e-110">La **celda ThemeIndex** no se puede cambiar desde su valor actual a menos que se cambie directamente en shapesheet.</span><span class="sxs-lookup"><span data-stu-id="2339e-110">The **ThemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="2339e-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="2339e-111">FALSE</span></span>  <br/> |<span data-ttu-id="2339e-112">La **celda ThemeIndex** se puede cambiar desde su valor actual cuando se cambia el tema.</span><span class="sxs-lookup"><span data-stu-id="2339e-112">The **ThemeIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2339e-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2339e-113">Remarks</span></span>

<span data-ttu-id="2339e-114">Para obtener una referencia a la celda **LockThemeIndex** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la **propiedad CellsU,** use:</span><span class="sxs-lookup"><span data-stu-id="2339e-114">To get a reference to the **LockThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2339e-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="2339e-115">Cell name:</span></span>  <br/> | <span data-ttu-id="2339e-116">LockThemeIndex</span><span class="sxs-lookup"><span data-stu-id="2339e-116">LockThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="2339e-117">Para obtener una referencia desde un programa a la celda **LockThemeIndex** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2339e-117">To get a reference to the **LockThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2339e-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="2339e-118">Section index:</span></span>  <br/> |<span data-ttu-id="2339e-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2339e-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2339e-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="2339e-120">Row index:</span></span>  <br/> |<span data-ttu-id="2339e-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="2339e-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="2339e-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="2339e-122">Cell index:</span></span>  <br/> |<span data-ttu-id="2339e-123">**visLockThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="2339e-123">**visLockThemeIndex**</span></span> <br/> |
   

