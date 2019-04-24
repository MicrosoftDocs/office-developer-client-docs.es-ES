---
title: Celda LockThemeIndex (sección protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Impide que se modifique la celda ThemeIndex de las propiedades del tema aplicando un nuevo tema o seleccionando un nuevo esquema de conector. No impide que los usuarios editen manualmente este valor en la ShapeSheet.
ms.openlocfilehash: 519c17f6e00c9aad2b5522bc66b41c0ceb75911b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358082"
---
# <a name="lockthemeindex-cell-protection-section"></a><span data-ttu-id="c4fab-104">Celda LockThemeIndex (sección protección)</span><span class="sxs-lookup"><span data-stu-id="c4fab-104">LockThemeIndex Cell (Protection Section)</span></span>

<span data-ttu-id="c4fab-105">Impide que se modifique la celda **ThemeIndex** de **las propiedades del tema** aplicando un nuevo tema o seleccionando un nuevo esquema de conector.</span><span class="sxs-lookup"><span data-stu-id="c4fab-105">Prevents **ThemeIndex** cell in **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="c4fab-106">No impide que los usuarios editen manualmente este valor en la ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c4fab-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="c4fab-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="c4fab-107">**Value**</span></span>|<span data-ttu-id="c4fab-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c4fab-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c4fab-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="c4fab-109">TRUE</span></span>  <br/> |<span data-ttu-id="c4fab-110">No se puede cambiar el valor actual de la celda **ThemeIndex** a no ser que se cambie directamente en la ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c4fab-110">The **ThemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="c4fab-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="c4fab-111">FALSE</span></span>  <br/> |<span data-ttu-id="c4fab-112">La celda **ThemeIndex** puede cambiarse de su valor actual cuando se cambia el tema.</span><span class="sxs-lookup"><span data-stu-id="c4fab-112">The **ThemeIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4fab-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c4fab-113">Remarks</span></span>

<span data-ttu-id="c4fab-114">Para obtener una referencia a la celda **LockThemeIndex** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="c4fab-114">To get a reference to the **LockThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c4fab-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c4fab-115">Cell name:</span></span>  <br/> | <span data-ttu-id="c4fab-116">LockThemeIndex</span><span class="sxs-lookup"><span data-stu-id="c4fab-116">LockThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="c4fab-117">Para obtener una referencia desde un programa a la celda **LockThemeIndex** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c4fab-117">To get a reference to the **LockThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c4fab-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c4fab-118">Section index:</span></span>  <br/> |<span data-ttu-id="c4fab-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c4fab-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c4fab-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c4fab-120">Row index:</span></span>  <br/> |<span data-ttu-id="c4fab-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="c4fab-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="c4fab-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c4fab-122">Cell index:</span></span>  <br/> |<span data-ttu-id="c4fab-123">**visLockThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="c4fab-123">**visLockThemeIndex**</span></span> <br/> |
   

