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
ms.openlocfilehash: a32f5dbc935e85a49ab585073ca6a31215fd102a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823015"
---
# <a name="resizemode-cell-shape-transform-section"></a><span data-ttu-id="4924e-103">Celda ResizeMode (sección Transformación de forma)</span><span class="sxs-lookup"><span data-stu-id="4924e-103">ResizeMode Cell (Shape Transform Section)</span></span>

<span data-ttu-id="4924e-104">Muestra la configuración actual del comportamiento de cambio de tamaño para la forma.</span><span class="sxs-lookup"><span data-stu-id="4924e-104">Shows the current resize behavior setting for the shape.</span></span>
  
|<span data-ttu-id="4924e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4924e-105">**Value**</span></span>|<span data-ttu-id="4924e-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4924e-106">**Description**</span></span>|<span data-ttu-id="4924e-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="4924e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4924e-108">0</span><span class="sxs-lookup"><span data-stu-id="4924e-108">0</span></span>  <br/> |<span data-ttu-id="4924e-109">Usar la configuración del grupo.</span><span class="sxs-lookup"><span data-stu-id="4924e-109">Use group's setting.</span></span>  <br/> |<span data-ttu-id="4924e-110">**visXFormResizeDontCare**</span><span class="sxs-lookup"><span data-stu-id="4924e-110">**visXFormResizeDontCare**</span></span> <br/> |
|<span data-ttu-id="4924e-111">1</span><span class="sxs-lookup"><span data-stu-id="4924e-111">1</span></span>  <br/> |<span data-ttu-id="4924e-112">Ajustar la posición únicamente.</span><span class="sxs-lookup"><span data-stu-id="4924e-112">Reposition only.</span></span>  <br/> |<span data-ttu-id="4924e-113">**visXFormResizeSpread**</span><span class="sxs-lookup"><span data-stu-id="4924e-113">**visXFormResizeSpread**</span></span> <br/> |
|<span data-ttu-id="4924e-114">2</span><span class="sxs-lookup"><span data-stu-id="4924e-114">2</span></span>  <br/> |<span data-ttu-id="4924e-115">Cambiar la escala con el grupo.</span><span class="sxs-lookup"><span data-stu-id="4924e-115">Scale with group.</span></span>  <br/> |<span data-ttu-id="4924e-116">**visXFormResizeScale**</span><span class="sxs-lookup"><span data-stu-id="4924e-116">**visXFormResizeScale**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4924e-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4924e-117">Remarks</span></span>

<span data-ttu-id="4924e-118">También puede establecer este valor en la ficha **comportamiento** en el cuadro de diálogo **comportamiento** (en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md), en el grupo **Diseño de formas** , haga clic en **comportamiento**).</span><span class="sxs-lookup"><span data-stu-id="4924e-118">You can also set this value on the **Behavior** tab in the **Behavior** dialog box (on the [Developer](run-in-developer-mode-display-the-developer-tab.md)tab, in the **Shape Design** group, click **Behavior**).</span></span> <span data-ttu-id="4924e-119">Para obtener una referencia a la celda ResizeMode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="4924e-119">To get a reference to the ResizeMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4924e-120">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4924e-120">Cell name:</span></span>  <br/> |<span data-ttu-id="4924e-121">ResizeMode</span><span class="sxs-lookup"><span data-stu-id="4924e-121">ResizeMode</span></span>  <br/> |
   
<span data-ttu-id="4924e-122">Para obtener una referencia desde un programa a la celda ResizeMode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4924e-122">To get a reference to the ResizeMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4924e-123">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4924e-123">Section index:</span></span>  <br/> |<span data-ttu-id="4924e-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4924e-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4924e-125">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4924e-125">Row index:</span></span>  <br/> |<span data-ttu-id="4924e-126">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="4924e-126">**visRowXFormOut**</span></span> <br/> |
|<span data-ttu-id="4924e-127">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4924e-127">Cell index:</span></span>  <br/> |<span data-ttu-id="4924e-128">**visXFormResizeMode**</span><span class="sxs-lookup"><span data-stu-id="4924e-128">**visXFormResizeMode**</span></span> <br/> |
   

