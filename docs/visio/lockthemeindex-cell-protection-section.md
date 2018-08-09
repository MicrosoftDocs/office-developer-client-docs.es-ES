---
title: Celda LockThemeIndex (sección Protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Impide que ThemeIndex de celda en la fila de propiedades del tema que se modifiquen aplicar un tema nuevo o seleccionando una nueva combinación de conector. Impedir que los usuarios editen manualmente este valor en la hoja ShapeSheet.
ms.openlocfilehash: 4bef3eb799c943ff89027e69ae8580c9c0e51243
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822535"
---
# <a name="lockthemeindex-cell-protection-section"></a><span data-ttu-id="3165c-104">Celda LockThemeIndex (sección Protección)</span><span class="sxs-lookup"><span data-stu-id="3165c-104">LockThemeIndex Cell (Protection Section)</span></span>

<span data-ttu-id="3165c-105">Impide que **ThemeIndex** de celda en la fila de **Propiedades del tema** que se modifiquen aplicar un tema nuevo o seleccionando una nueva combinación de conector.</span><span class="sxs-lookup"><span data-stu-id="3165c-105">Prevents **ThemeIndex** cell in **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="3165c-106">Impedir que los usuarios editen manualmente este valor en la hoja ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="3165c-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="3165c-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3165c-107">**Value**</span></span>|<span data-ttu-id="3165c-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3165c-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3165c-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="3165c-109">TRUE</span></span>  <br/> |<span data-ttu-id="3165c-110">No se puede cambiar la celda **ThemeIndex** desde su valor actual a menos que cambie directamente en la hoja ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="3165c-110">The **ThemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="3165c-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="3165c-111">FALSE</span></span>  <br/> |<span data-ttu-id="3165c-112">Puede cambiar el valor actual de la celda **ThemeIndex** cuando se cambia el tema.</span><span class="sxs-lookup"><span data-stu-id="3165c-112">The **ThemeIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3165c-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3165c-113">Remarks</span></span>

<span data-ttu-id="3165c-114">Para obtener una referencia a la celda **LockThemeIndex** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="3165c-114">To get a reference to the **LockThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3165c-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3165c-115">Cell name:</span></span>  <br/> | <span data-ttu-id="3165c-116">LockThemeIndex</span><span class="sxs-lookup"><span data-stu-id="3165c-116">LockThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="3165c-117">Para obtener una referencia a la celda **LockThemeIndex** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3165c-117">To get a reference to the **LockThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3165c-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3165c-118">Section index:</span></span>  <br/> |<span data-ttu-id="3165c-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3165c-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3165c-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3165c-120">Row index:</span></span>  <br/> |<span data-ttu-id="3165c-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="3165c-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="3165c-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3165c-122">Cell index:</span></span>  <br/> |<span data-ttu-id="3165c-123">**visLockThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="3165c-123">**visLockThemeIndex**</span></span> <br/> |
   

