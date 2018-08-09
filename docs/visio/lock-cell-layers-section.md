---
title: Celda Lock (Sección de capas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm590
localization_priority: Normal
ms.assetid: 47bb268f-acdd-7369-716c-bd51a32b8a49
description: Determina si las formas que pertenecen a la capa están bloqueadas de modo que no puedan seleccionarse o modificarse.
ms.openlocfilehash: f404fe15814de802f4f6bfcebfd2558cf10cc7eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822489"
---
# <a name="lock-cell-layers-section"></a><span data-ttu-id="e8e0f-103">Celda Lock (sección Capas)</span><span class="sxs-lookup"><span data-stu-id="e8e0f-103">Lock Cell (Layers Section)</span></span>

<span data-ttu-id="e8e0f-104">Determina si las formas que pertenecen a la capa están bloqueadas de modo que no puedan seleccionarse o modificarse.</span><span class="sxs-lookup"><span data-stu-id="e8e0f-104">Specifies whether shapes belonging to the layer are locked against being selected or edited.</span></span>
  
|<span data-ttu-id="e8e0f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e8e0f-105">**Value**</span></span>|<span data-ttu-id="e8e0f-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8e0f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8e0f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e8e0f-107">TRUE</span></span>  <br/> |<span data-ttu-id="e8e0f-108">Las formas están bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="e8e0f-108">Shapes are locked.</span></span>  <br/> |
|<span data-ttu-id="e8e0f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e8e0f-109">FALSE</span></span>  <br/> |<span data-ttu-id="e8e0f-110">Las formas no están bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="e8e0f-110">Shapes are not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8e0f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8e0f-111">Remarks</span></span>

<span data-ttu-id="e8e0f-112">También puede establecer este valor si selecciona **Bloquear** en el cuadro de diálogo **Propiedades de las capas** (en la ficha **Inicio**, en el grupo **Edición**, haga clic en **Capas** y, a continuación, en **Propiedades de las capas**).</span><span class="sxs-lookup"><span data-stu-id="e8e0f-112">You can also set this value by selecting **Lock** in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="e8e0f-113">Para obtener una referencia a la celda Lock por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e8e0f-113">To get a reference to the Lock cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8e0f-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e8e0f-114">Cell name:</span></span>  <br/> |<span data-ttu-id="e8e0f-115">Layers.Locked [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e8e0f-115">Layers.Locked[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e8e0f-116">Para obtener una referencia desde un programa a la celda Lock por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e8e0f-116">To get a reference to the Lock cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8e0f-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e8e0f-117">Section index:</span></span>  <br/> |<span data-ttu-id="e8e0f-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="e8e0f-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="e8e0f-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e8e0f-119">Row index:</span></span>  <br/> |<span data-ttu-id="e8e0f-120">**visRowLayer** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e8e0f-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="e8e0f-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e8e0f-121">Cell index:</span></span>  <br/> |<span data-ttu-id="e8e0f-122">**visLayerLock**</span><span class="sxs-lookup"><span data-stu-id="e8e0f-122">**visLayerLock**</span></span> <br/> |
   

