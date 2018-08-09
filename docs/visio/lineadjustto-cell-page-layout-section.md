---
title: Celda LineAdjustTo (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
localization_priority: Normal
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: Determina qué conectores dinámicos se alinean uno encima de otro.
ms.openlocfilehash: 13540f9dc5e6e6861d3f3679bcf49204d553397a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822455"
---
# <a name="lineadjustto-cell-page-layout-section"></a><span data-ttu-id="dde7d-103">Celda LineAdjustTo (sección Diseño de página)</span><span class="sxs-lookup"><span data-stu-id="dde7d-103">LineAdjustTo Cell (Page Layout Section)</span></span>

<span data-ttu-id="dde7d-104">Determina qué conectores dinámicos se alinean uno encima de otro.</span><span class="sxs-lookup"><span data-stu-id="dde7d-104">Determines which dynamic connectors line up on top of one another.</span></span>
  
|<span data-ttu-id="dde7d-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="dde7d-105">**Value**</span></span>|<span data-ttu-id="dde7d-106">**Ajuste**</span><span class="sxs-lookup"><span data-stu-id="dde7d-106">**Adjustment**</span></span>|<span data-ttu-id="dde7d-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="dde7d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dde7d-108">0</span><span class="sxs-lookup"><span data-stu-id="dde7d-108">0</span></span>  <br/> |<span data-ttu-id="dde7d-109">Predeterminado para el estilo de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="dde7d-109">Routing style default</span></span>  <br/> |<span data-ttu-id="dde7d-110">**visPLOLineAdjustToDefault**</span><span class="sxs-lookup"><span data-stu-id="dde7d-110">**visPLOLineAdjustToDefault**</span></span> <br/> |
|<span data-ttu-id="dde7d-111">1</span><span class="sxs-lookup"><span data-stu-id="dde7d-111">1</span></span>  <br/> |<span data-ttu-id="dde7d-112">Líneas cercanas entre sí</span><span class="sxs-lookup"><span data-stu-id="dde7d-112">Lines that are close to each other</span></span>  <br/> |<span data-ttu-id="dde7d-113">**visPLOLineAdjustToAll**</span><span class="sxs-lookup"><span data-stu-id="dde7d-113">**visPLOLineAdjustToAll**</span></span> <br/> |
|<span data-ttu-id="dde7d-114">2</span><span class="sxs-lookup"><span data-stu-id="dde7d-114">2</span></span>  <br/> |<span data-ttu-id="dde7d-115">Sin líneas</span><span class="sxs-lookup"><span data-stu-id="dde7d-115">No lines</span></span>  <br/> |<span data-ttu-id="dde7d-116">**visPLOLineAdjustToNone**</span><span class="sxs-lookup"><span data-stu-id="dde7d-116">**visPLOLineAdjustToNone**</span></span> <br/> |
|<span data-ttu-id="dde7d-117">3</span><span class="sxs-lookup"><span data-stu-id="dde7d-117">3</span></span>  <br/> |<span data-ttu-id="dde7d-118">Líneas relacionadas</span><span class="sxs-lookup"><span data-stu-id="dde7d-118">Related lines</span></span>  <br/> |<span data-ttu-id="dde7d-119">**visPLOLineAdjustToRelated**</span><span class="sxs-lookup"><span data-stu-id="dde7d-119">**visPLOLineAdjustToRelated**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dde7d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dde7d-120">Remarks</span></span>

<span data-ttu-id="dde7d-121">También puede establecer el valor de esta celda en la ficha **Diseño y enrutamiento** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página** y, a continuación, haga clic en **Diseño y enrutamiento**).</span><span class="sxs-lookup"><span data-stu-id="dde7d-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="dde7d-122">Para obtener una referencia a la celda LineAdjustTo por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="dde7d-122">To get a reference to the LineAdjustTo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dde7d-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="dde7d-123">Cell name:</span></span>  <br/> |<span data-ttu-id="dde7d-124">LineAdjustTo</span><span class="sxs-lookup"><span data-stu-id="dde7d-124">LineAdjustTo</span></span>  <br/> |
   
<span data-ttu-id="dde7d-125">Para obtener una referencia desde un programa a la celda LineAdjustTo por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="dde7d-125">To get a reference to the LineAdjustTo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dde7d-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="dde7d-126">Section index:</span></span>  <br/> |<span data-ttu-id="dde7d-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dde7d-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dde7d-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="dde7d-128">Row index:</span></span>  <br/> |<span data-ttu-id="dde7d-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="dde7d-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="dde7d-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="dde7d-130">Cell index:</span></span>  <br/> |<span data-ttu-id="dde7d-131">**visPLOLineAdjustTo**</span><span class="sxs-lookup"><span data-stu-id="dde7d-131">**visPLOLineAdjustTo**</span></span> <br/> |
   

