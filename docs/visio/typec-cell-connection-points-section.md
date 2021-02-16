---
title: Celda Type / C (Sección de puntos de conexión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
localization_priority: Normal
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: Determina el tipo de punto de conexión.
ms.openlocfilehash: a73554d9f3a3bce6a039689d2c0b192a1c5b69aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415239"
---
# <a name="type--c-cell-connection-points-section"></a><span data-ttu-id="c86d1-103">Celda Type / C (Sección de puntos de conexión)</span><span class="sxs-lookup"><span data-stu-id="c86d1-103">Type / C Cell (Connection Points Section)</span></span>

<span data-ttu-id="c86d1-104">Determina el tipo de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="c86d1-104">Determines the connection point type.</span></span>
  
|<span data-ttu-id="c86d1-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c86d1-105">**Value**</span></span>|<span data-ttu-id="c86d1-106">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c86d1-106">**Type**</span></span>|<span data-ttu-id="c86d1-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="c86d1-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c86d1-108">0</span><span class="sxs-lookup"><span data-stu-id="c86d1-108">0</span></span>  <br/> |<span data-ttu-id="c86d1-109">Hacia dentro</span><span class="sxs-lookup"><span data-stu-id="c86d1-109">Inward</span></span>  <br/> |<span data-ttu-id="c86d1-110">**visCnnctTypeInward**</span><span class="sxs-lookup"><span data-stu-id="c86d1-110">**visCnnctTypeInward**</span></span> <br/> |
|<span data-ttu-id="c86d1-111">1 </span><span class="sxs-lookup"><span data-stu-id="c86d1-111">1</span></span>  <br/> |<span data-ttu-id="c86d1-112">Salida</span><span class="sxs-lookup"><span data-stu-id="c86d1-112">Outward</span></span>  <br/> |<span data-ttu-id="c86d1-113">**visCnnctTypeOutward**</span><span class="sxs-lookup"><span data-stu-id="c86d1-113">**visCnnctTypeOutward**</span></span> <br/> |
|<span data-ttu-id="c86d1-114">2 </span><span class="sxs-lookup"><span data-stu-id="c86d1-114">2</span></span>  <br/> |<span data-ttu-id="c86d1-115">Hacia dentro &amp; hacia afuera</span><span class="sxs-lookup"><span data-stu-id="c86d1-115">Inward &amp; Outward</span></span>  <br/> |<span data-ttu-id="c86d1-116">**visCnnctTypeInwardOutward**</span><span class="sxs-lookup"><span data-stu-id="c86d1-116">**visCnnctTypeInwardOutward**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c86d1-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c86d1-117">Remarks</span></span>

<span data-ttu-id="c86d1-p101">Para establecer el tipo de punto de conexión también puede elegir la herramienta **Conector**, seleccionar una forma y, a continuación, hacer clic con el botón secundario en un punto de conexión. Para ello debe ejecutar en el modo para [programadores](run-in-developer-mode-display-the-developer-tab.md).</span><span class="sxs-lookup"><span data-stu-id="c86d1-p101">You can also set the connection point type by choosing the **Connector** tool, selecting a shape, and then right-clicking a connection point. To do this, you need to run in [developer](run-in-developer-mode-display-the-developer-tab.md) mode.</span></span> 
  
<span data-ttu-id="c86d1-120">Para obtener una referencia a la celda Type / C por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="c86d1-120">To get a reference to the Type / C cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c86d1-121">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c86d1-121">Cell name:</span></span>  <br/> |<span data-ttu-id="c86d1-122">Connections.Type[  *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c86d1-122">Connections.Type[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c86d1-123">Para obtener una referencia desde un programa a la celda Type / C por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c86d1-123">To get a reference to the Type / C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c86d1-124">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c86d1-124">Section index:</span></span>  <br/> |<span data-ttu-id="c86d1-125">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="c86d1-125">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="c86d1-126">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c86d1-126">Row index:</span></span>  <br/> |<span data-ttu-id="c86d1-127">**visRowConnectionPts**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c86d1-127">**visRowConnectionPts** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="c86d1-128">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c86d1-128">Cell index:</span></span>  <br/> |<span data-ttu-id="c86d1-129">**visCnnctType** (filas no extendidas) **visCnnctC** (filas extendidas)</span><span class="sxs-lookup"><span data-stu-id="c86d1-129">**visCnnctType** (non-extended rows) **visCnnctC** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="c86d1-130">Para obtener información sobre las filas extensibles y no extensibles, vea la fila de puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="c86d1-130">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

