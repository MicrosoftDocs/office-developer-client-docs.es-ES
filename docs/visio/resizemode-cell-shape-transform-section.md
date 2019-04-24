---
title: Celda ResizeMode (Sección de transformación de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Muestra la configuración actual del comportamiento de cambio de tamaño para la forma.
ms.openlocfilehash: 7e9080fcd4604e2dbdc1dae31992f05e5b512213
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326883"
---
# <a name="resizemode-cell-shape-transform-section"></a><span data-ttu-id="940f0-103">Celda ResizeMode (Sección de transformación de forma)</span><span class="sxs-lookup"><span data-stu-id="940f0-103">ResizeMode Cell (Shape Transform Section)</span></span>

<span data-ttu-id="940f0-104">Muestra la configuración actual del comportamiento de cambio de tamaño para la forma.</span><span class="sxs-lookup"><span data-stu-id="940f0-104">Shows the current resize behavior setting for the shape.</span></span>
  
|<span data-ttu-id="940f0-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="940f0-105">**Value**</span></span>|<span data-ttu-id="940f0-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="940f0-106">**Description**</span></span>|<span data-ttu-id="940f0-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="940f0-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="940f0-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="940f0-108">0</span></span>  <br/> |<span data-ttu-id="940f0-109">Usar la configuración del grupo.</span><span class="sxs-lookup"><span data-stu-id="940f0-109">Use group's setting.</span></span>  <br/> |<span data-ttu-id="940f0-110">**visXFormResizeDontCare**</span><span class="sxs-lookup"><span data-stu-id="940f0-110">**visXFormResizeDontCare**</span></span> <br/> |
|<span data-ttu-id="940f0-111">1</span><span class="sxs-lookup"><span data-stu-id="940f0-111">1</span></span>  <br/> |<span data-ttu-id="940f0-112">Ajustar la posición únicamente.</span><span class="sxs-lookup"><span data-stu-id="940f0-112">Reposition only.</span></span>  <br/> |<span data-ttu-id="940f0-113">**visXFormResizeSpread**</span><span class="sxs-lookup"><span data-stu-id="940f0-113">**visXFormResizeSpread**</span></span> <br/> |
|<span data-ttu-id="940f0-114">segundo</span><span class="sxs-lookup"><span data-stu-id="940f0-114">2</span></span>  <br/> |<span data-ttu-id="940f0-115">Cambiar la escala con el grupo.</span><span class="sxs-lookup"><span data-stu-id="940f0-115">Scale with group.</span></span>  <br/> |<span data-ttu-id="940f0-116">**visXFormResizeScale**</span><span class="sxs-lookup"><span data-stu-id="940f0-116">**visXFormResizeScale**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="940f0-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="940f0-117">Remarks</span></span>

<span data-ttu-id="940f0-118">También puede establecer este valor en la ficha **comportamiento** del cuadro de diálogo **comportamiento** (en la ficha [programador](run-in-developer-mode-display-the-developer-tab.md), en el grupo **diseño de formas** , haga clic en **comportamiento**).</span><span class="sxs-lookup"><span data-stu-id="940f0-118">You can also set this value on the **Behavior** tab in the **Behavior** dialog box (on the [Developer](run-in-developer-mode-display-the-developer-tab.md)tab, in the **Shape Design** group, click **Behavior**).</span></span> <span data-ttu-id="940f0-119">Para obtener una referencia a la celda ResizeMode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="940f0-119">To get a reference to the ResizeMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="940f0-120">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="940f0-120">Cell name:</span></span>  <br/> |<span data-ttu-id="940f0-121">ResizeMode</span><span class="sxs-lookup"><span data-stu-id="940f0-121">ResizeMode</span></span>  <br/> |
   
<span data-ttu-id="940f0-122">Para obtener una referencia desde un programa a la celda ResizeMode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="940f0-122">To get a reference to the ResizeMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="940f0-123">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="940f0-123">Section index:</span></span>  <br/> |<span data-ttu-id="940f0-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="940f0-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="940f0-125">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="940f0-125">Row index:</span></span>  <br/> |<span data-ttu-id="940f0-126">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="940f0-126">**visRowXFormOut**</span></span> <br/> |
|<span data-ttu-id="940f0-127">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="940f0-127">Cell index:</span></span>  <br/> |<span data-ttu-id="940f0-128">**visXFormResizeMode**</span><span class="sxs-lookup"><span data-stu-id="940f0-128">**visXFormResizeMode**</span></span> <br/> |
   

