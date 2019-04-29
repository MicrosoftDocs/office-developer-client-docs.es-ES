---
title: Celda ShapeShdwShow (sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Determina si la forma muestra una sombra, como un entero entre 0 y 2.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422120"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a><span data-ttu-id="cf45f-103">Celda ShapeShdwShow (sección de formato de relleno)</span><span class="sxs-lookup"><span data-stu-id="cf45f-103">ShapeShdwShow Cell (Fill Format Section)</span></span>

<span data-ttu-id="cf45f-104">Determina si la forma muestra una sombra, como un entero entre 0 y 2.</span><span class="sxs-lookup"><span data-stu-id="cf45f-104">Determines whether the shape displays a shadow, as an integer from 0 to 2.</span></span>
  
|<span data-ttu-id="cf45f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cf45f-105">**Value**</span></span>|<span data-ttu-id="cf45f-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf45f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf45f-107">comprendi</span><span class="sxs-lookup"><span data-stu-id="cf45f-107">0</span></span>  <br/> |<span data-ttu-id="cf45f-108">Mostrar siempre la sombra si se especifica una sombra.</span><span class="sxs-lookup"><span data-stu-id="cf45f-108">Always display the shadow if a shadow is specified.</span></span> <span data-ttu-id="cf45f-109">No se muestran las sombras de las subformas.</span><span class="sxs-lookup"><span data-stu-id="cf45f-109">The shadows for sub-shapes are not displayed.</span></span>  <br/> |
|<span data-ttu-id="cf45f-110">1</span><span class="sxs-lookup"><span data-stu-id="cf45f-110">1</span></span>  <br/> |<span data-ttu-id="cf45f-111">No se representa una sombra a menos que la forma no tenga un elemento primario.</span><span class="sxs-lookup"><span data-stu-id="cf45f-111">Do not render a shadow unless the shape does not have a parent.</span></span> <span data-ttu-id="cf45f-112">Use sombras de subformas agrupadas.</span><span class="sxs-lookup"><span data-stu-id="cf45f-112">Use sub-shape shadows if grouped together.</span></span>  <br/> |
|<span data-ttu-id="cf45f-113">segundo</span><span class="sxs-lookup"><span data-stu-id="cf45f-113">2</span></span>  <br/> |<span data-ttu-id="cf45f-114">Mostrar siempre una sombra si se especifica una sombra.</span><span class="sxs-lookup"><span data-stu-id="cf45f-114">Always display a shadow if a shadow is specified.</span></span> <span data-ttu-id="cf45f-115">Se muestran las sombras de las subformas.</span><span class="sxs-lookup"><span data-stu-id="cf45f-115">The shadows for sub-shapes are displayed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf45f-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cf45f-116">Remarks</span></span>

<span data-ttu-id="cf45f-117">Para obtener una referencia a la celda **ShapeShdwShow** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="cf45f-117">To get a reference to the **ShapeShdwShow** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cf45f-118">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="cf45f-118">Cell name:</span></span>  <br/> | <span data-ttu-id="cf45f-119">ShapeShdwShow</span><span class="sxs-lookup"><span data-stu-id="cf45f-119">ShapeShdwShow</span></span>  <br/> |
   
<span data-ttu-id="cf45f-120">Para obtener una referencia desde un programa a la celda **ShapeShdwShow** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="cf45f-120">To get a reference to the **ShapeShdwShow** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cf45f-121">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="cf45f-121">Section index:</span></span>  <br/> |<span data-ttu-id="cf45f-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cf45f-122">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cf45f-123">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="cf45f-123">Row index:</span></span>  <br/> |<span data-ttu-id="cf45f-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="cf45f-124">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="cf45f-125">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="cf45f-125">Cell index:</span></span>  <br/> |<span data-ttu-id="cf45f-126">**visFillShdwShow**</span><span class="sxs-lookup"><span data-stu-id="cf45f-126">**visFillShdwShow**</span></span> <br/> |
   

