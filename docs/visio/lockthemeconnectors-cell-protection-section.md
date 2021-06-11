---
title: Celda LockThemeConnectors (sección Protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Impide que la celda ConnectorsSchemeIndex de la fila Propiedades del tema se altere aplicando un nuevo tema o seleccionando un nuevo esquema de conector. No impide que los usuarios editen manualmente este valor en ShapeSheet.
ms.openlocfilehash: 8097e50646fd59f4ac0212cbe9ca2ecfaadab7a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438410"
---
# <a name="lockthemeconnectors-cell-protection-section"></a><span data-ttu-id="6c3b4-104">Celda LockThemeConnectors (sección Protección)</span><span class="sxs-lookup"><span data-stu-id="6c3b4-104">LockThemeConnectors Cell (Protection Section)</span></span>

<span data-ttu-id="6c3b4-105">Impide que **la celda ConnectorsSchemeIndex** de la fila **Propiedades** del tema se altere aplicando un nuevo tema o seleccionando un nuevo esquema de conector.</span><span class="sxs-lookup"><span data-stu-id="6c3b4-105">Prevents the **ConnectorsSchemeIndex** cell in the **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="6c3b4-106">No impide que los usuarios editen manualmente este valor en ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="6c3b4-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="6c3b4-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6c3b4-107">**Value**</span></span>|<span data-ttu-id="6c3b4-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6c3b4-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6c3b4-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="6c3b4-109">TRUE</span></span>  <br/> |<span data-ttu-id="6c3b4-110">La **celda ConnectorsSchemeIndex** no se puede cambiar de su valor actual a menos que se cambie directamente en ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="6c3b4-110">The **ConnectorsSchemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="6c3b4-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="6c3b4-111">FALSE</span></span>  <br/> |<span data-ttu-id="6c3b4-112">La **celda ConnectorsSchemeIndex** se puede cambiar desde su valor actual a través de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="6c3b4-112">The **ConnectorsSchemeIndex** cell can be changed from its current value through the UI.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c3b4-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6c3b4-113">Remarks</span></span>

<span data-ttu-id="6c3b4-114">Para obtener una referencia a la celda **LockThemeConnectors** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la propiedad **CellsU,** use:</span><span class="sxs-lookup"><span data-stu-id="6c3b4-114">To get a reference to the **LockThemeConnectors** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c3b4-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6c3b4-115">Cell name:</span></span>  <br/> | <span data-ttu-id="6c3b4-116">LockThemeConnectors</span><span class="sxs-lookup"><span data-stu-id="6c3b4-116">LockThemeConnectors</span></span>  <br/> |
   
<span data-ttu-id="6c3b4-117">Para obtener una referencia desde un programa a la celda **LockThemeConnectors** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6c3b4-117">To get a reference to the **LockThemeConnectors** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c3b4-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6c3b4-118">Section index:</span></span>  <br/> |<span data-ttu-id="6c3b4-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6c3b4-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6c3b4-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6c3b4-120">Row index:</span></span>  <br/> |<span data-ttu-id="6c3b4-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="6c3b4-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="6c3b4-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6c3b4-122">Cell index:</span></span>  <br/> |<span data-ttu-id="6c3b4-123">**visLockThemeConnectors**</span><span class="sxs-lookup"><span data-stu-id="6c3b4-123">**visLockThemeConnectors**</span></span> <br/> |
   

