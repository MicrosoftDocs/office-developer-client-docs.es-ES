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
ms.openlocfilehash: e4fb32c0fcb488173324ea597edc2c9d13f6bfca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414028"
---
# <a name="lineadjustto-cell-page-layout-section"></a><span data-ttu-id="9652e-103">Celda LineAdjustTo (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="9652e-103">LineAdjustTo Cell (Page Layout Section)</span></span>

<span data-ttu-id="9652e-104">Determina qué conectores dinámicos se alinean uno encima de otro.</span><span class="sxs-lookup"><span data-stu-id="9652e-104">Determines which dynamic connectors line up on top of one another.</span></span>
  
|<span data-ttu-id="9652e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9652e-105">**Value**</span></span>|<span data-ttu-id="9652e-106">**Cód**</span><span class="sxs-lookup"><span data-stu-id="9652e-106">**Adjustment**</span></span>|<span data-ttu-id="9652e-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="9652e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9652e-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="9652e-108">0</span></span>  <br/> |<span data-ttu-id="9652e-109">Predeterminado para el estilo de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="9652e-109">Routing style default</span></span>  <br/> |<span data-ttu-id="9652e-110">**visPLOLineAdjustToDefault**</span><span class="sxs-lookup"><span data-stu-id="9652e-110">**visPLOLineAdjustToDefault**</span></span> <br/> |
|<span data-ttu-id="9652e-111">1</span><span class="sxs-lookup"><span data-stu-id="9652e-111">1</span></span>  <br/> |<span data-ttu-id="9652e-112">Líneas cercanas entre sí</span><span class="sxs-lookup"><span data-stu-id="9652e-112">Lines that are close to each other</span></span>  <br/> |<span data-ttu-id="9652e-113">**visPLOLineAdjustToAll**</span><span class="sxs-lookup"><span data-stu-id="9652e-113">**visPLOLineAdjustToAll**</span></span> <br/> |
|<span data-ttu-id="9652e-114">segundo</span><span class="sxs-lookup"><span data-stu-id="9652e-114">2</span></span>  <br/> |<span data-ttu-id="9652e-115">Sin líneas</span><span class="sxs-lookup"><span data-stu-id="9652e-115">No lines</span></span>  <br/> |<span data-ttu-id="9652e-116">**visPLOLineAdjustToNone**</span><span class="sxs-lookup"><span data-stu-id="9652e-116">**visPLOLineAdjustToNone**</span></span> <br/> |
|<span data-ttu-id="9652e-117">3</span><span class="sxs-lookup"><span data-stu-id="9652e-117">3</span></span>  <br/> |<span data-ttu-id="9652e-118">Líneas relacionadas</span><span class="sxs-lookup"><span data-stu-id="9652e-118">Related lines</span></span>  <br/> |<span data-ttu-id="9652e-119">**visPLOLineAdjustToRelated**</span><span class="sxs-lookup"><span data-stu-id="9652e-119">**visPLOLineAdjustToRelated**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9652e-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9652e-120">Remarks</span></span>

<span data-ttu-id="9652e-121">También puede establecer el valor de esta celda en la ficha **Diseño y enrutamiento** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página** y, a continuación, haga clic en **Diseño y enrutamiento**).</span><span class="sxs-lookup"><span data-stu-id="9652e-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="9652e-122">Para obtener una referencia a la celda LineAdjustTo por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="9652e-122">To get a reference to the LineAdjustTo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9652e-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="9652e-123">Cell name:</span></span>  <br/> |<span data-ttu-id="9652e-124">LineAdjustTo</span><span class="sxs-lookup"><span data-stu-id="9652e-124">LineAdjustTo</span></span>  <br/> |
   
<span data-ttu-id="9652e-125">Para obtener una referencia desde un programa a la celda LineAdjustTo por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9652e-125">To get a reference to the LineAdjustTo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9652e-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="9652e-126">Section index:</span></span>  <br/> |<span data-ttu-id="9652e-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9652e-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9652e-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="9652e-128">Row index:</span></span>  <br/> |<span data-ttu-id="9652e-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="9652e-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="9652e-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="9652e-130">Cell index:</span></span>  <br/> |<span data-ttu-id="9652e-131">**visPLOLineAdjustTo**</span><span class="sxs-lookup"><span data-stu-id="9652e-131">**visPLOLineAdjustTo**</span></span> <br/> |
   

