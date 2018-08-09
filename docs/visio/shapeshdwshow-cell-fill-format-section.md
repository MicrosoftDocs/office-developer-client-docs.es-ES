---
title: Celda ShapeShdwShow (sección Formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Determina si la forma muestra una sombra, como un número entero de 0 a 2.
ms.openlocfilehash: 72077e60089acd3cd3f8a9349691e1468f6b1f9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823175"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a><span data-ttu-id="751c2-103">Celda ShapeShdwShow (sección Formato de relleno)</span><span class="sxs-lookup"><span data-stu-id="751c2-103">ShapeShdwShow Cell (Fill Format Section)</span></span>

<span data-ttu-id="751c2-104">Determina si la forma muestra una sombra, como un número entero de 0 a 2.</span><span class="sxs-lookup"><span data-stu-id="751c2-104">Determines whether the shape displays a shadow, as an integer from 0 to 2.</span></span>
  
|<span data-ttu-id="751c2-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="751c2-105">**Value**</span></span>|<span data-ttu-id="751c2-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="751c2-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="751c2-107">0</span><span class="sxs-lookup"><span data-stu-id="751c2-107">0</span></span>  <br/> |<span data-ttu-id="751c2-108">Mostrar siempre la sombra si se especifica una sombra.</span><span class="sxs-lookup"><span data-stu-id="751c2-108">Always display the shadow if a shadow is specified.</span></span> <span data-ttu-id="751c2-109">No se muestran las sombras para las subformas.</span><span class="sxs-lookup"><span data-stu-id="751c2-109">The shadows for sub-shapes are not displayed.</span></span>  <br/> |
|<span data-ttu-id="751c2-110">1</span><span class="sxs-lookup"><span data-stu-id="751c2-110">1</span></span>  <br/> |<span data-ttu-id="751c2-111">No se representará una sombra a menos que la forma no tiene un elemento primario.</span><span class="sxs-lookup"><span data-stu-id="751c2-111">Do not render a shadow unless the shape does not have a parent.</span></span> <span data-ttu-id="751c2-112">Usar sombras de forma subcaracterística si se agrupan juntos.</span><span class="sxs-lookup"><span data-stu-id="751c2-112">Use sub-shape shadows if grouped together.</span></span>  <br/> |
|<span data-ttu-id="751c2-113">2</span><span class="sxs-lookup"><span data-stu-id="751c2-113">2</span></span>  <br/> |<span data-ttu-id="751c2-114">Mostrar siempre una sombra si se especifica una sombra.</span><span class="sxs-lookup"><span data-stu-id="751c2-114">Always display a shadow if a shadow is specified.</span></span> <span data-ttu-id="751c2-115">Se muestran las sombras para las subformas.</span><span class="sxs-lookup"><span data-stu-id="751c2-115">The shadows for sub-shapes are displayed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="751c2-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="751c2-116">Remarks</span></span>

<span data-ttu-id="751c2-117">Para obtener una referencia a la celda **ShapeShdwShow** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="751c2-117">To get a reference to the **ShapeShdwShow** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="751c2-118">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="751c2-118">Cell name:</span></span>  <br/> | <span data-ttu-id="751c2-119">ShapeShdwShow</span><span class="sxs-lookup"><span data-stu-id="751c2-119">ShapeShdwShow</span></span>  <br/> |
   
<span data-ttu-id="751c2-120">Para obtener una referencia a la celda **ShapeShdwShow** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="751c2-120">To get a reference to the **ShapeShdwShow** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="751c2-121">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="751c2-121">Section index:</span></span>  <br/> |<span data-ttu-id="751c2-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="751c2-122">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="751c2-123">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="751c2-123">Row index:</span></span>  <br/> |<span data-ttu-id="751c2-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="751c2-124">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="751c2-125">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="751c2-125">Cell index:</span></span>  <br/> |<span data-ttu-id="751c2-126">**visFillShdwShow**</span><span class="sxs-lookup"><span data-stu-id="751c2-126">**visFillShdwShow**</span></span> <br/> |
   

