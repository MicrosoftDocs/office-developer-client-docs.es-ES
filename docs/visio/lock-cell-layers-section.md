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
ms.openlocfilehash: d548a6f0fe0cac10d80d73c904739b2979ecf27f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438830"
---
# <a name="lock-cell-layers-section"></a><span data-ttu-id="bc95d-103">Celda Lock (Sección de capas)</span><span class="sxs-lookup"><span data-stu-id="bc95d-103">Lock Cell (Layers Section)</span></span>

<span data-ttu-id="bc95d-104">Determina si las formas que pertenecen a la capa están bloqueadas de modo que no puedan seleccionarse o modificarse.</span><span class="sxs-lookup"><span data-stu-id="bc95d-104">Specifies whether shapes belonging to the layer are locked against being selected or edited.</span></span>
  
|<span data-ttu-id="bc95d-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="bc95d-105">**Value**</span></span>|<span data-ttu-id="bc95d-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bc95d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bc95d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="bc95d-107">TRUE</span></span>  <br/> |<span data-ttu-id="bc95d-108">Las formas están bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="bc95d-108">Shapes are locked.</span></span>  <br/> |
|<span data-ttu-id="bc95d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="bc95d-109">FALSE</span></span>  <br/> |<span data-ttu-id="bc95d-110">Las formas no están bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="bc95d-110">Shapes are not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc95d-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bc95d-111">Remarks</span></span>

<span data-ttu-id="bc95d-112">También puede establecer este valor si selecciona **Bloquear** en el cuadro de diálogo **Propiedades de las capas** (en la ficha **Inicio**, en el grupo **Edición**, haga clic en **Capas** y, a continuación, en **Propiedades de las capas**).</span><span class="sxs-lookup"><span data-stu-id="bc95d-112">You can also set this value by selecting **Lock** in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="bc95d-113">Para obtener una referencia a la celda Lock por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="bc95d-113">To get a reference to the Lock cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc95d-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="bc95d-114">Cell name:</span></span>  <br/> |<span data-ttu-id="bc95d-115">Layers. Locked [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="bc95d-115">Layers.Locked[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bc95d-116">Para obtener una referencia desde un programa a la celda Lock por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="bc95d-116">To get a reference to the Lock cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc95d-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="bc95d-117">Section index:</span></span>  <br/> |<span data-ttu-id="bc95d-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="bc95d-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="bc95d-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="bc95d-119">Row index:</span></span>  <br/> |<span data-ttu-id="bc95d-120">**visRowLayer** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bc95d-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="bc95d-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="bc95d-121">Cell index:</span></span>  <br/> |<span data-ttu-id="bc95d-122">**visLayerLock**</span><span class="sxs-lookup"><span data-stu-id="bc95d-122">**visLayerLock**</span></span> <br/> |
   

