---
title: Celda LockVariation (sección Protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Determina si se puede cambiar la variación de tema aplicada a la forma o página, como un valor Boolean.
ms.openlocfilehash: c3c272a637f28aa4df43f6c23030d6676280138e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822549"
---
# <a name="lockvariation-cell-protection-section"></a><span data-ttu-id="6ba32-103">Celda LockVariation (sección Protección)</span><span class="sxs-lookup"><span data-stu-id="6ba32-103">LockVariation Cell (Protection Section)</span></span>

<span data-ttu-id="6ba32-104">Determina si se puede cambiar la variación de tema aplicada a la forma o página, como un valor Boolean.</span><span class="sxs-lookup"><span data-stu-id="6ba32-104">Determines whether the theme variation applied to the page or shape can be changed, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ba32-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="6ba32-105">TRUE</span></span>  <br/> |<span data-ttu-id="6ba32-106">No se puede cambiar la variante actual aplicada a la forma o página.</span><span class="sxs-lookup"><span data-stu-id="6ba32-106">The current variation applied to the page or shape cannot be changed.</span></span>  <br/> |
|<span data-ttu-id="6ba32-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="6ba32-107">FALSE</span></span>  <br/> |<span data-ttu-id="6ba32-108">La variación de la página o la forma se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="6ba32-108">The variation of the page or shape can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ba32-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ba32-109">Remarks</span></span>

<span data-ttu-id="6ba32-110">Para obtener una referencia a la celda **LockVariation** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="6ba32-110">To get a reference to the **LockVariation** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6ba32-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6ba32-111">Cell name:</span></span>  <br/> | <span data-ttu-id="6ba32-112">LockVariation</span><span class="sxs-lookup"><span data-stu-id="6ba32-112">LockVariation</span></span>  <br/> |
   
<span data-ttu-id="6ba32-113">Para obtener una referencia a la celda **LockVariation** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6ba32-113">To get a reference to the **LockVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6ba32-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6ba32-114">Section index:</span></span>  <br/> |<span data-ttu-id="6ba32-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6ba32-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6ba32-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6ba32-116">Row index:</span></span>  <br/> |<span data-ttu-id="6ba32-117">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="6ba32-117">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="6ba32-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6ba32-118">Cell index:</span></span>  <br/> |<span data-ttu-id="6ba32-119">**visLockVariation**</span><span class="sxs-lookup"><span data-stu-id="6ba32-119">**visLockVariation**</span></span> <br/> |
   

