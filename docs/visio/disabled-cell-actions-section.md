---
title: Celda Disabled (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251337
localization_priority: Normal
ms.assetid: ebf66729-d794-a398-268a-84d761bf06b6
description: Indica si está deshabilitado un elemento de un menú contextual o de etiquetas de acción.
ms.openlocfilehash: ddf55f40056d7df7a2403e500bb4bae335930433
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431354"
---
# <a name="disabled-cell-actions-section"></a><span data-ttu-id="195a4-103">Celda Disabled (sección de acciones)</span><span class="sxs-lookup"><span data-stu-id="195a4-103">Disabled Cell (Actions Section)</span></span>

<span data-ttu-id="195a4-104">Indica si está deshabilitado un elemento de un menú contextual o de etiquetas de acción.</span><span class="sxs-lookup"><span data-stu-id="195a4-104">Indicates whether an item on a shortcut or action tag menu is disabled.</span></span>
  
> [!NOTE]
> <span data-ttu-id="195a4-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="195a4-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="195a4-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="195a4-106">**Value**</span></span>|<span data-ttu-id="195a4-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="195a4-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="195a4-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="195a4-108">TRUE</span></span>  <br/> |<span data-ttu-id="195a4-109">Se deshabilita (atenúa) el nombre del comando.</span><span class="sxs-lookup"><span data-stu-id="195a4-109">Disable (dim) command name.</span></span>  <br/> |
|<span data-ttu-id="195a4-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="195a4-110">FALSE</span></span>  <br/> |<span data-ttu-id="195a4-111">Se habilita el nombre del comando (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="195a4-111">Enable the command name (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="195a4-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="195a4-112">Remarks</span></span>

<span data-ttu-id="195a4-113">Para obtener una referencia a la celda Disabled por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="195a4-113">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="195a4-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="195a4-114">Cell name:</span></span>  <br/> |<span data-ttu-id="195a4-115">Acciones.</span><span class="sxs-lookup"><span data-stu-id="195a4-115">Actions.</span></span> <span data-ttu-id="195a4-116">*nombre*  . Deshabilitado donde Actions.</span><span class="sxs-lookup"><span data-stu-id="195a4-116">*name*  .Disabled           where Actions.</span></span> <span data-ttu-id="195a4-117">*es*  el nombre de la fila Actions</span><span class="sxs-lookup"><span data-stu-id="195a4-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="195a4-118">Para obtener una referencia desde un programa a la celda Disabled por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="195a4-118">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="195a4-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="195a4-119">Section index:</span></span>  <br/> |<span data-ttu-id="195a4-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="195a4-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="195a4-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="195a4-121">Row index:</span></span>  <br/> |<span data-ttu-id="195a4-122">**visRowAction**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="195a4-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="195a4-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="195a4-123">Cell index:</span></span>  <br/> |<span data-ttu-id="195a4-124">**visActionDisabled**</span><span class="sxs-lookup"><span data-stu-id="195a4-124">**visActionDisabled**</span></span> <br/> |
   

