---
title: Celda ShapePermeableY (Sección de diseño de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
localization_priority: Normal
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: Determina si un conector puede enrutar verticalmente a través de una forma.
ms.openlocfilehash: 62f8bfa0fdfb5c483836f344e8b784dc9092fded
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417521"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a><span data-ttu-id="33d33-103">Celda ShapePermeableY (Sección de diseño de forma)</span><span class="sxs-lookup"><span data-stu-id="33d33-103">ShapePermeableY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="33d33-104">Determina si un conector puede enrutar verticalmente a través de una forma.</span><span class="sxs-lookup"><span data-stu-id="33d33-104">Determines whether a connector can route vertically through a shape.</span></span>
  
|<span data-ttu-id="33d33-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="33d33-105">**Value**</span></span>|<span data-ttu-id="33d33-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="33d33-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33d33-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="33d33-107">TRUE</span></span>  <br/> |<span data-ttu-id="33d33-108">Se permite que los conectores enruten verticalmente a través de una forma.</span><span class="sxs-lookup"><span data-stu-id="33d33-108">Enable connectors to route vertically through a shape.</span></span>  <br/> |
|<span data-ttu-id="33d33-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="33d33-109">FALSE</span></span>  <br/> |<span data-ttu-id="33d33-110">No se permite que los conectores enruten verticalmente a través de una forma.</span><span class="sxs-lookup"><span data-stu-id="33d33-110">Do not let connectors route vertically through a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33d33-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="33d33-111">Remarks</span></span>

<span data-ttu-id="33d33-112">También puede establecer el valor de esta celda  en la ficha Colocación del [](run-in-developer-mode-display-the-developer-tab.md) cuadro de  diálogo Comportamiento (con una forma  seleccionada, en la ficha Programador, en el grupo Diseño de formas, haga clic en Comportamiento y, a continuación, haga clic en la ficha Colocación).  </span><span class="sxs-lookup"><span data-stu-id="33d33-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="33d33-113">En las versiones anteriores a Visio 2000, este comportamiento se establece mediante la celda ObjInteract, en la sección de varios.</span><span class="sxs-lookup"><span data-stu-id="33d33-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="33d33-114">Para obtener una referencia a la celda ShapePermeableY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="33d33-114">To get a reference to the ShapePermeableY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="33d33-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="33d33-115">Cell name:</span></span>  <br/> |<span data-ttu-id="33d33-116">ShapePermeableY</span><span class="sxs-lookup"><span data-stu-id="33d33-116">ShapePermeableY</span></span>  <br/> |
   
<span data-ttu-id="33d33-117">Para obtener una referencia desde un programa a la celda ShapePermeableY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="33d33-117">To get a reference to the ShapePermeableY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="33d33-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="33d33-118">Section index:</span></span>  <br/> |<span data-ttu-id="33d33-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="33d33-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="33d33-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="33d33-120">Row index:</span></span>  <br/> |<span data-ttu-id="33d33-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="33d33-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="33d33-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="33d33-122">Cell index:</span></span>  <br/> |<span data-ttu-id="33d33-123">**visSLOPermY**</span><span class="sxs-lookup"><span data-stu-id="33d33-123">**visSLOPermY**</span></span> <br/> |
   

