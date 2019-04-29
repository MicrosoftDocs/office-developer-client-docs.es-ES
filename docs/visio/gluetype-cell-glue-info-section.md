---
title: Celda GlueType (Sección de información de pegado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm420
localization_priority: Normal
ms.assetid: fffbefd6-8b0b-0023-6b03-026d1c6e885e
description: Determina si la forma 1D utiliza un pegado estático (punto a punto) o dinámico (forma a forma) cuando se pega encima de otra.
ms.openlocfilehash: ae4eddf17c6e7b5e56cb3397f03d0721d965c9b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410675"
---
# <a name="gluetype-cell-glue-info-section"></a><span data-ttu-id="4773f-103">Celda GlueType (Sección de información de pegado)</span><span class="sxs-lookup"><span data-stu-id="4773f-103">GlueType Cell (Glue Info Section)</span></span>

<span data-ttu-id="4773f-104">Determina si la forma 1D utiliza un pegado estático (punto a punto) o dinámico (forma a forma) cuando se pega encima de otra.</span><span class="sxs-lookup"><span data-stu-id="4773f-104">Determines whether a 1-D shape uses static (point-to-point) or dynamic (shape-to-shape) glue when it is glued to another shape.</span></span>
  
|<span data-ttu-id="4773f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4773f-105">**Value**</span></span>|<span data-ttu-id="4773f-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4773f-106">**Description**</span></span>|<span data-ttu-id="4773f-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="4773f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="4773f-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="4773f-108">&amp;H0</span></span>  <br/> | <span data-ttu-id="4773f-109">Éste es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4773f-109">Default.</span></span> <span data-ttu-id="4773f-110">Permitir el pegado dinámico sólo para el conector dinámico y, si no es el caso, utilizar el pegado estático.</span><span class="sxs-lookup"><span data-stu-id="4773f-110">Allow dynamic glue for the dynamic connector only; otherwise, use static glue.</span></span>  <br/> |<span data-ttu-id="4773f-111">**visGlueTypeDefault**</span><span class="sxs-lookup"><span data-stu-id="4773f-111">**visGlueTypeDefault**</span></span> <br/> |
| <span data-ttu-id="4773f-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="4773f-112">&amp;H1</span></span>  <br/> | <span data-ttu-id="4773f-113">Permitir el pegado dinámico.</span><span class="sxs-lookup"><span data-stu-id="4773f-113">Allow dynamic glue.</span></span>  <br/> | <span data-ttu-id="4773f-114">Obsoleto en Visio 2002</span><span class="sxs-lookup"><span data-stu-id="4773f-114">Obsolete in Visio 2002</span></span>  <br/> |
| <span data-ttu-id="4773f-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="4773f-115">&amp;H2</span></span>  <br/> | <span data-ttu-id="4773f-116">Permitir el pegado dinámico.</span><span class="sxs-lookup"><span data-stu-id="4773f-116">Allow dynamic glue.</span></span>  <br/> |<span data-ttu-id="4773f-117">**visGlueTypeWalking**</span><span class="sxs-lookup"><span data-stu-id="4773f-117">**visGlueTypeWalking**</span></span> <br/> |
| <span data-ttu-id="4773f-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="4773f-118">&amp;H4</span></span>  <br/> | <span data-ttu-id="4773f-119">No permitir el pegado dinámico.</span><span class="sxs-lookup"><span data-stu-id="4773f-119">Do not allow dynamic glue.</span></span>  <br/> |<span data-ttu-id="4773f-120">**visGlueTypeNoWalking**</span><span class="sxs-lookup"><span data-stu-id="4773f-120">**visGlueTypeNoWalking**</span></span> <br/> |
| <span data-ttu-id="4773f-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="4773f-121">&amp;H8</span></span>  <br/> | <span data-ttu-id="4773f-122">No permitir a esta forma bidimensional estar conectada con pegado dinámico.</span><span class="sxs-lookup"><span data-stu-id="4773f-122">Do not allow this 2-D shape to be connected to with dynamic glue.</span></span>  <br/> |<span data-ttu-id="4773f-123">**visGlueTypeNoWalkingTo**</span><span class="sxs-lookup"><span data-stu-id="4773f-123">**visGlueTypeNoWalkingTo**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4773f-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4773f-124">Remarks</span></span>

<span data-ttu-id="4773f-125">Si la celda contiene un valor de 1, 2 o 3, el pegado dinámico determinará que acción de las siguientes acontecerá:</span><span class="sxs-lookup"><span data-stu-id="4773f-125">If this cell contains a value of 1, 2 or 3, dynamic glue will be established when either of the following occurs:</span></span>
  
- <span data-ttu-id="4773f-126">Las formas tendrán un pegado dinámico en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4773f-126">Shapes are dynamically glued in the user interface.</span></span>
    
- <span data-ttu-id="4773f-127">Las formas se pegarán en la celda PinX o PinY de otra forma de un programa.</span><span class="sxs-lookup"><span data-stu-id="4773f-127">Shapes are glued to the PinX or PinY cell of another shape from a program.</span></span>
    
<span data-ttu-id="4773f-128">El pegado estático se utilizará si las formas se pegan en otras celdas de la forma distintas de PinX y PinY en un programa.</span><span class="sxs-lookup"><span data-stu-id="4773f-128">If shapes are glued to shape cells other than PinX or PinY from a program, then static glue is used.</span></span>
  
<span data-ttu-id="4773f-p102">Cambiar el valor de permitir a no permitir el pegado dinámico no anula ni modifica el pegado dinámico actual. Los programas pueden establecer el pegado dinámico aunque se haya deshabilitado en la celda GlueType.</span><span class="sxs-lookup"><span data-stu-id="4773f-p102">Changing this value from allowing to not allowing dynamic glue does not sever or change existing dynamic glue. Programs can establish dynamic glue even if dynamic glue is disabled in the GlueType cell.</span></span>
  
<span data-ttu-id="4773f-131">Para obtener una referencia a la celda GlueType por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="4773f-131">To get a reference to the GlueType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4773f-132">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4773f-132">Cell name:</span></span>  <br/> | <span data-ttu-id="4773f-133">GlueType</span><span class="sxs-lookup"><span data-stu-id="4773f-133">GlueType</span></span>  <br/> |
   
<span data-ttu-id="4773f-134">Para obtener una referencia desde un programa a la celda GlueType por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4773f-134">To get a reference to the GlueType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4773f-135">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4773f-135">Section index:</span></span>  <br/> |<span data-ttu-id="4773f-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4773f-136">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4773f-137">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4773f-137">Row index:</span></span>  <br/> |<span data-ttu-id="4773f-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="4773f-138">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="4773f-139">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4773f-139">Cell index:</span></span>  <br/> |<span data-ttu-id="4773f-140">**visGlueType**</span><span class="sxs-lookup"><span data-stu-id="4773f-140">**visGlueType**</span></span> <br/> |
   

