---
title: Celda LockFormat (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
localization_priority: Normal
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: Bloquea el formato de una forma para no se pueda cambiar.
ms.openlocfilehash: e0d1bb8a65b8087136e57bb46ad9f5363da30030
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409681"
---
# <a name="lockformat-cell-protection-section"></a><span data-ttu-id="bbf14-103">Celda LockFormat (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="bbf14-103">LockFormat Cell (Protection Section)</span></span>

<span data-ttu-id="bbf14-104">Bloquea el formato de una forma para no se pueda cambiar.</span><span class="sxs-lookup"><span data-stu-id="bbf14-104">Locks the formatting of a shape so it cannot be changed.</span></span>
  
|<span data-ttu-id="bbf14-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="bbf14-105">**Value**</span></span>|<span data-ttu-id="bbf14-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bbf14-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bbf14-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="bbf14-107">TRUE</span></span>  <br/> | <span data-ttu-id="bbf14-108">El formato no puede cambiarse.</span><span class="sxs-lookup"><span data-stu-id="bbf14-108">Formatting cannot be changed.</span></span>  <br/> |
| <span data-ttu-id="bbf14-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="bbf14-109">FALSE</span></span>  <br/> | <span data-ttu-id="bbf14-110">El formato puede cambiarse.</span><span class="sxs-lookup"><span data-stu-id="bbf14-110">Formatting can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bbf14-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bbf14-111">Remarks</span></span>

<span data-ttu-id="bbf14-112">Para obtener una referencia a la celda LockFormat por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="bbf14-112">To get a reference to the LockFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bbf14-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="bbf14-113">Cell name:</span></span>  <br/> | <span data-ttu-id="bbf14-114">LockFormat</span><span class="sxs-lookup"><span data-stu-id="bbf14-114">LockFormat</span></span>  <br/> |
   
<span data-ttu-id="bbf14-115">Para obtener una referencia desde un programa a la celda LockFormat por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="bbf14-115">To get a reference to the LockFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bbf14-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="bbf14-116">Section index:</span></span>  <br/> |<span data-ttu-id="bbf14-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bbf14-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bbf14-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="bbf14-118">Row index:</span></span>  <br/> |<span data-ttu-id="bbf14-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="bbf14-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="bbf14-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="bbf14-120">Cell index:</span></span>  <br/> |<span data-ttu-id="bbf14-121">**visLockFormat**</span><span class="sxs-lookup"><span data-stu-id="bbf14-121">**visLockFormat**</span></span> <br/> |
   

