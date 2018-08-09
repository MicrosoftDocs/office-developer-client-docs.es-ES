---
title: Celda LineAdjustFrom (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251887
localization_priority: Normal
ms.assetid: 6949c717-dc69-1d17-5215-eb6efce56fcb
description: Determina qué conectores dinámicos separa la aplicación si se enrutan de manera superpuesta.
ms.openlocfilehash: ee3a107f7e19b53017c2ea24c94babceb49620d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822444"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a><span data-ttu-id="4b12d-103">Celda LineAdjustFrom (sección Diseño de página)</span><span class="sxs-lookup"><span data-stu-id="4b12d-103">LineAdjustFrom Cell (Page Layout Section)</span></span>

<span data-ttu-id="4b12d-104">Determina qué conectores dinámicos separa la aplicación si se enrutan de manera superpuesta.</span><span class="sxs-lookup"><span data-stu-id="4b12d-104">Determines which dynamic connectors the application spaces apart if they route on top of each other.</span></span>
  
|<span data-ttu-id="4b12d-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4b12d-105">**Value**</span></span>|<span data-ttu-id="4b12d-106">**Ajuste**</span><span class="sxs-lookup"><span data-stu-id="4b12d-106">**Adjustment**</span></span>|<span data-ttu-id="4b12d-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="4b12d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4b12d-108">0</span><span class="sxs-lookup"><span data-stu-id="4b12d-108">0</span></span>  <br/> |<span data-ttu-id="4b12d-109">Líneas no relacionadas</span><span class="sxs-lookup"><span data-stu-id="4b12d-109">Unrelated lines</span></span>  <br/> |<span data-ttu-id="4b12d-110">**visPLOLineAdjustFromNotRelated**</span><span class="sxs-lookup"><span data-stu-id="4b12d-110">**visPLOLineAdjustFromNotRelated**</span></span> <br/> |
|<span data-ttu-id="4b12d-111">1</span><span class="sxs-lookup"><span data-stu-id="4b12d-111">1</span></span>  <br/> |<span data-ttu-id="4b12d-112">Todas las líneas</span><span class="sxs-lookup"><span data-stu-id="4b12d-112">All lines</span></span>  <br/> |<span data-ttu-id="4b12d-113">**visPLOLineAdjustFromAll**</span><span class="sxs-lookup"><span data-stu-id="4b12d-113">**visPLOLineAdjustFromAll**</span></span> <br/> |
|<span data-ttu-id="4b12d-114">2</span><span class="sxs-lookup"><span data-stu-id="4b12d-114">2</span></span>  <br/> |<span data-ttu-id="4b12d-115">Sin líneas</span><span class="sxs-lookup"><span data-stu-id="4b12d-115">No lines</span></span>  <br/> |<span data-ttu-id="4b12d-116">**visPLOLineAdjustFromNone**</span><span class="sxs-lookup"><span data-stu-id="4b12d-116">**visPLOLineAdjustFromNone**</span></span> <br/> |
|<span data-ttu-id="4b12d-117">3</span><span class="sxs-lookup"><span data-stu-id="4b12d-117">3</span></span>  <br/> |<span data-ttu-id="4b12d-118">Predeterminado para el estilo de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="4b12d-118">Routing style default</span></span>  <br/> |<span data-ttu-id="4b12d-119">**visPLOLineAdjustFromRoutingDefault**</span><span class="sxs-lookup"><span data-stu-id="4b12d-119">**visPLOLineAdjustFromRoutingDefault**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b12d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b12d-120">Remarks</span></span>

<span data-ttu-id="4b12d-121">También puede establecer el valor de esta celda en la ficha **Diseño y enrutamiento** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página** y, a continuación, haga clic en **Diseño y enrutamiento**).</span><span class="sxs-lookup"><span data-stu-id="4b12d-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="4b12d-122">Para obtener una referencia a la celda LineAdjustFrom por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="4b12d-122">To get a reference to the LineAdjustFrom cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4b12d-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4b12d-123">Cell name:</span></span>  <br/> |<span data-ttu-id="4b12d-124">LineAdjustFrom</span><span class="sxs-lookup"><span data-stu-id="4b12d-124">LineAdjustFrom</span></span>  <br/> |
   
<span data-ttu-id="4b12d-125">Para obtener una referencia desde un programa a la celda LineAdjustFrom por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4b12d-125">To get a reference to the LineAdjustFrom cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4b12d-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4b12d-126">Section index:</span></span>  <br/> |<span data-ttu-id="4b12d-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4b12d-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4b12d-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4b12d-128">Row index:</span></span>  <br/> |<span data-ttu-id="4b12d-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="4b12d-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="4b12d-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4b12d-130">Cell index:</span></span>  <br/> |<span data-ttu-id="4b12d-131">**visPLOLineAdjustFrom**</span><span class="sxs-lookup"><span data-stu-id="4b12d-131">**visPLOLineAdjustFrom**</span></span> <br/> |
   

