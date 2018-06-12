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
ms.openlocfilehash: 12c953a160ab99aad007e9b2bb9089d651aee553
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823462"
---
# <a name="type--c-cell-connection-points-section"></a><span data-ttu-id="7b96e-103">Celda Type / C (Sección de puntos de conexión)</span><span class="sxs-lookup"><span data-stu-id="7b96e-103">Type / C Cell (Connection Points Section)</span></span>

<span data-ttu-id="7b96e-104">Determina el tipo de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="7b96e-104">Determines the connection point type.</span></span>
  
|<span data-ttu-id="7b96e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7b96e-105">**Value**</span></span>|<span data-ttu-id="7b96e-106">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7b96e-106">**Type**</span></span>|<span data-ttu-id="7b96e-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="7b96e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7b96e-108">0</span><span class="sxs-lookup"><span data-stu-id="7b96e-108">0</span></span>  <br/> |<span data-ttu-id="7b96e-109">Entrante</span><span class="sxs-lookup"><span data-stu-id="7b96e-109">Inward</span></span>  <br/> |<span data-ttu-id="7b96e-110">**visCnnctTypeInward**</span><span class="sxs-lookup"><span data-stu-id="7b96e-110">**visCnnctTypeInward**</span></span> <br/> |
|<span data-ttu-id="7b96e-111">1</span><span class="sxs-lookup"><span data-stu-id="7b96e-111">1</span></span>  <br/> |<span data-ttu-id="7b96e-112">Saliente</span><span class="sxs-lookup"><span data-stu-id="7b96e-112">Outward</span></span>  <br/> |<span data-ttu-id="7b96e-113">**visCnnctTypeOutward**</span><span class="sxs-lookup"><span data-stu-id="7b96e-113">**visCnnctTypeOutward**</span></span> <br/> |
|<span data-ttu-id="7b96e-114">2</span><span class="sxs-lookup"><span data-stu-id="7b96e-114">2</span></span>  <br/> |<span data-ttu-id="7b96e-115">Llamada &amp; hacia fuera</span><span class="sxs-lookup"><span data-stu-id="7b96e-115">Inward &amp; Outward</span></span>  <br/> |<span data-ttu-id="7b96e-116">**visCnnctTypeInwardOutward**</span><span class="sxs-lookup"><span data-stu-id="7b96e-116">**visCnnctTypeInwardOutward**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b96e-117">Notas</span><span class="sxs-lookup"><span data-stu-id="7b96e-117">Remarks</span></span>

<span data-ttu-id="7b96e-118">También puede establecer el tipo de punto de conexión por elegir la herramienta **conector** , seleccionar una forma y, a continuación, hace doble clic en un punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="7b96e-118">You can also set the connection point type by choosing the **Connector** tool, selecting a shape, and then right-clicking a connection point.</span></span> <span data-ttu-id="7b96e-119">Para ello, debe ejecutar en modo [para programadores](run-in-developer-mode-display-the-developer-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="7b96e-119">To do this, you need to run in [developer](run-in-developer-mode-display-the-developer-tab.md) mode.</span></span> 
  
<span data-ttu-id="7b96e-120">Para obtener una referencia al tipo / celda C por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="7b96e-120">To get a reference to the Type / C cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b96e-121">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="7b96e-121">Cell name:</span></span>  <br/> |<span data-ttu-id="7b96e-122">Connections.Type [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7b96e-122">Connections.Type[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7b96e-123">Para obtener una referencia al tipo / celda C por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7b96e-123">To get a reference to the Type / C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b96e-124">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="7b96e-124">Section index:</span></span>  <br/> |<span data-ttu-id="7b96e-125">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="7b96e-125">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="7b96e-126">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="7b96e-126">Row index:</span></span>  <br/> |<span data-ttu-id="7b96e-127">**visRowConnectionPts** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7b96e-127">**visRowConnectionPts** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7b96e-128">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="7b96e-128">Cell index:</span></span>  <br/> |<span data-ttu-id="7b96e-129">**visCnnctType** (filas no extensibles) **visCnnctC** (filas extensibles)</span><span class="sxs-lookup"><span data-stu-id="7b96e-129">**visCnnctType** (non-extended rows) **visCnnctC** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="7b96e-130">Para obtener información sobre las filas extensibles y no extensibles, vea la fila de puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="7b96e-130">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

