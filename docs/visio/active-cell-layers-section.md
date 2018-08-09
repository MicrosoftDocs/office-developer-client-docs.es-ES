---
title: Celda Active (Sección de capas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm10
localization_priority: Normal
ms.assetid: 4c8e366f-9e9b-30ea-a89f-57c8d7a1168e
description: Especifica si la capa está activa. Las formas sin capas preasignadas se asignan a las capas activas cuando se colocan en la página de dibujo.
ms.openlocfilehash: 81d3ec083e207a927c46dda99e2b7f42c0a7bd8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821512"
---
# <a name="active-cell-layers-section"></a><span data-ttu-id="16202-104">Celda Active (sección Capas)</span><span class="sxs-lookup"><span data-stu-id="16202-104">Active Cell (Layers Section)</span></span>

<span data-ttu-id="16202-p102">Especifica si la capa está activa. Las formas sin capas preasignadas se asignan a las capas activas cuando se colocan en la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="16202-p102">Specifies whether the layer is active. Shapes without pre-assigned layers are assigned to the active layer(s) when you drag them onto the drawing page.</span></span>
  
|<span data-ttu-id="16202-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="16202-107">**Value**</span></span>|<span data-ttu-id="16202-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="16202-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="16202-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="16202-109">TRUE</span></span>  <br/> |<span data-ttu-id="16202-110">
          La capa está activa.
</span><span class="sxs-lookup"><span data-stu-id="16202-110">Layer is active.</span></span>  <br/> |
|<span data-ttu-id="16202-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="16202-111">FALSE</span></span>  <br/> |<span data-ttu-id="16202-112">
          La capa no está activa.
</span><span class="sxs-lookup"><span data-stu-id="16202-112">Layer is not active.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16202-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="16202-113">Remarks</span></span>

<span data-ttu-id="16202-114">El valor de esta celda corresponde a la opción **Activar** del cuadro de diálogo **Propiedades de las capas** (en el grupo **Edición**, en la ficha **Inicio**, haga clic en **Capas** y, a continuación, en **Propiedades de las capas**).</span><span class="sxs-lookup"><span data-stu-id="16202-114">The value in this cell corresponds to the **Active** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="16202-115">Para obtener una referencia a la celda Active por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="16202-115">To get a reference to the Active cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16202-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="16202-116">Cell name:</span></span>  <br/> |<span data-ttu-id="16202-117">Layers.Active [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="16202-117">Layers.Active[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="16202-118">Para obtener una referencia a la celda Active por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="16202-118">To get a reference to the Active cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16202-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="16202-119">Section index:</span></span>  <br/> |<span data-ttu-id="16202-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="16202-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="16202-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="16202-121">Row index:</span></span>  <br/> |<span data-ttu-id="16202-122">**visRowLayer** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="16202-122">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="16202-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="16202-123">Cell index:</span></span>  <br/> |<span data-ttu-id="16202-124">**visLayerActive**</span><span class="sxs-lookup"><span data-stu-id="16202-124">**visLayerActive**</span></span> <br/> |
   

