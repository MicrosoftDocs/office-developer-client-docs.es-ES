---
title: Celda DynamicsOff (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251641
localization_priority: Normal
ms.assetid: 055764aa-9681-ffb0-83ce-fdd612fe37af
description: Determina si las formas colocables se mueven y los conectores cambian sus recorridos para evitar a las restantes formas y conectores de la página de dibujo.
ms.openlocfilehash: 72d65860d1a2ee37efd5287ae3f4baf54bd3addb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822042"
---
# <a name="dynamicsoff-cell-page-layout-section"></a><span data-ttu-id="1ec9e-103">Celda DynamicsOff (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="1ec9e-103">DynamicsOff Cell (Page Layout Section)</span></span>

<span data-ttu-id="1ec9e-104">Determina si las formas colocables se mueven y los conectores cambian sus recorridos para evitar a las restantes formas y conectores de la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-104">Determines whether placeable shapes move and connectors reroute around other shapes and connectors on the drawing page.</span></span>
  
|<span data-ttu-id="1ec9e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1ec9e-105">**Value**</span></span>|<span data-ttu-id="1ec9e-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ec9e-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1ec9e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="1ec9e-107">TRUE</span></span>  <br/> | <span data-ttu-id="1ec9e-108">Deshabilitar propiedades dinámicas.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-108">Disable dynamics.</span></span>  <br/> |
| <span data-ttu-id="1ec9e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="1ec9e-109">FALSE</span></span>  <br/> | <span data-ttu-id="1ec9e-110">Habilitar propiedades dinámicas.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-110">Enable dynamics.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ec9e-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ec9e-111">Remarks</span></span>

<span data-ttu-id="1ec9e-p101">Puede deshabilitar las propiedades dinámicas para mejorar el rendimiento de la solución. Por ejemplo, si una solución agrega formas colocables a un dibujo y no desea que la aplicación cambie las rutas de los conectores y las posiciones de las formas cada vez que se agregue una, puede deshabilitar las propiedades dinámicas. Vuelva a habilitarlas cuando la solución haya agregado las formas.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-p101">You can disable dynamics to increase your solution's performance. For example, if your solution adds placeable shapes to a drawing and you don't want the application to reroute connectors and reposition shapes each time you add a shape, you can disable dynamics. After your solution adds the shapes, re-enable dynamics.</span></span>
  
<span data-ttu-id="1ec9e-115">Para obtener una referencia a la celda DynamicsOff por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="1ec9e-115">To get a reference to the DynamicsOff cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1ec9e-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="1ec9e-116">Cell name:</span></span>  <br/> | <span data-ttu-id="1ec9e-117">DynamicsOff</span><span class="sxs-lookup"><span data-stu-id="1ec9e-117">DynamicsOff</span></span>  <br/> |
   
<span data-ttu-id="1ec9e-118">Para obtener una referencia a la celda DynamicsOff por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1ec9e-118">To get a reference to the DynamicsOff cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1ec9e-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="1ec9e-119">Section index:</span></span>  <br/> |<span data-ttu-id="1ec9e-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1ec9e-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1ec9e-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="1ec9e-121">Row index:</span></span>  <br/> |<span data-ttu-id="1ec9e-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="1ec9e-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="1ec9e-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="1ec9e-123">Cell index:</span></span>  <br/> |<span data-ttu-id="1ec9e-124">**visPLODynamicsOff**</span><span class="sxs-lookup"><span data-stu-id="1ec9e-124">**visPLODynamicsOff**</span></span> <br/> |
   

