---
title: Celda LockVariation (sección Protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Determina si se puede cambiar la variación de tema aplicada a la página o forma, como un valor Boolean.
ms.openlocfilehash: 69c991e3da7a96d6c59dc825dfb78fdad3d432e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427930"
---
# <a name="lockvariation-cell-protection-section"></a><span data-ttu-id="08b39-103">Celda LockVariation (sección Protección)</span><span class="sxs-lookup"><span data-stu-id="08b39-103">LockVariation Cell (Protection Section)</span></span>

<span data-ttu-id="08b39-104">Determina si se puede cambiar la variación de tema aplicada a la página o forma, como un valor Boolean.</span><span class="sxs-lookup"><span data-stu-id="08b39-104">Determines whether the theme variation applied to the page or shape can be changed, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08b39-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="08b39-105">TRUE</span></span>  <br/> |<span data-ttu-id="08b39-106">La variación actual aplicada a la página o forma no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="08b39-106">The current variation applied to the page or shape cannot be changed.</span></span>  <br/> |
|<span data-ttu-id="08b39-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="08b39-107">FALSE</span></span>  <br/> |<span data-ttu-id="08b39-108">Se puede cambiar la variación de la página o la forma.</span><span class="sxs-lookup"><span data-stu-id="08b39-108">The variation of the page or shape can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08b39-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="08b39-109">Remarks</span></span>

<span data-ttu-id="08b39-110">Para obtener una referencia a la **celda LockVariation** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la **propiedad CellsU,** use:</span><span class="sxs-lookup"><span data-stu-id="08b39-110">To get a reference to the **LockVariation** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="08b39-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="08b39-111">Cell name:</span></span>  <br/> | <span data-ttu-id="08b39-112">LockVariation</span><span class="sxs-lookup"><span data-stu-id="08b39-112">LockVariation</span></span>  <br/> |
   
<span data-ttu-id="08b39-113">Para obtener una referencia desde un programa a la **celda LockVariation** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="08b39-113">To get a reference to the **LockVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="08b39-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="08b39-114">Section index:</span></span>  <br/> |<span data-ttu-id="08b39-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="08b39-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="08b39-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="08b39-116">Row index:</span></span>  <br/> |<span data-ttu-id="08b39-117">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="08b39-117">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="08b39-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="08b39-118">Cell index:</span></span>  <br/> |<span data-ttu-id="08b39-119">**visLockVariation**</span><span class="sxs-lookup"><span data-stu-id="08b39-119">**visLockVariation**</span></span> <br/> |
   

