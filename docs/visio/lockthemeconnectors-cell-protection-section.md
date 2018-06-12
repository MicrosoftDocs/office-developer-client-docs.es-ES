---
title: Celda LockThemeConnectors (sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Impide que la celda ConnectorsSchemeIndex en la fila de propiedades del tema que se modifiquen aplicar un tema nuevo o seleccionando una nueva combinación de conector. Impedir que los usuarios editen manualmente este valor en la hoja ShapeSheet.
ms.openlocfilehash: c74bcf554f0f14de47480397a96680469826d2c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822532"
---
# <a name="lockthemeconnectors-cell-protection-section"></a><span data-ttu-id="671cb-104">Celda LockThemeConnectors (sección de protección)</span><span class="sxs-lookup"><span data-stu-id="671cb-104">LockThemeConnectors Cell (Protection Section)</span></span>

<span data-ttu-id="671cb-105">Impide que la celda **ConnectorsSchemeIndex** en la fila de **Propiedades del tema** que se modifiquen aplicar un tema nuevo o seleccionando una nueva combinación de conector.</span><span class="sxs-lookup"><span data-stu-id="671cb-105">Prevents the **ConnectorsSchemeIndex** cell in the **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="671cb-106">Impedir que los usuarios editen manualmente este valor en la hoja ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="671cb-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="671cb-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="671cb-107">**Value**</span></span>|<span data-ttu-id="671cb-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="671cb-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="671cb-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="671cb-109">TRUE</span></span>  <br/> |<span data-ttu-id="671cb-110">No se puede cambiar la celda **ConnectorsSchemeIndex** desde su valor actual a menos que cambie directamente en la hoja ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="671cb-110">The **ConnectorsSchemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="671cb-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="671cb-111">FALSE</span></span>  <br/> |<span data-ttu-id="671cb-112">Puede cambiar la celda **ConnectorsSchemeIndex** desde su valor actual a través de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="671cb-112">The **ConnectorsSchemeIndex** cell can be changed from its current value through the UI.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="671cb-113">Notas</span><span class="sxs-lookup"><span data-stu-id="671cb-113">Remarks</span></span>

<span data-ttu-id="671cb-114">Para obtener una referencia a la celda **LockThemeConnectors** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="671cb-114">To get a reference to the **LockThemeConnectors** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="671cb-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="671cb-115">Cell name:</span></span>  <br/> | <span data-ttu-id="671cb-116">LockThemeConnectors</span><span class="sxs-lookup"><span data-stu-id="671cb-116">LockThemeConnectors</span></span>  <br/> |
   
<span data-ttu-id="671cb-117">Para obtener una referencia a la celda **LockThemeConnectors** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="671cb-117">To get a reference to the **LockThemeConnectors** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="671cb-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="671cb-118">Section index:</span></span>  <br/> |<span data-ttu-id="671cb-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="671cb-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="671cb-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="671cb-120">Row index:</span></span>  <br/> |<span data-ttu-id="671cb-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="671cb-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="671cb-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="671cb-122">Cell index:</span></span>  <br/> |<span data-ttu-id="671cb-123">**visLockThemeConnectors**</span><span class="sxs-lookup"><span data-stu-id="671cb-123">**visLockThemeConnectors**</span></span> <br/> |
   

