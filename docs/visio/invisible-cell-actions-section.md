---
title: Celda Invisible (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
localization_priority: Normal
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: Indica si la acción está visible en el menú contextual o de etiqueta de acción.
ms.openlocfilehash: 8749b7d6db4a932b97c68ab5cf30b879a57d28f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822347"
---
# <a name="invisible-cell-actions-section"></a><span data-ttu-id="4ecb8-103">Celda Invisible (sección Acciones)</span><span class="sxs-lookup"><span data-stu-id="4ecb8-103">Invisible Cell (Actions Section)</span></span>

<span data-ttu-id="4ecb8-104">Indica si la acción está visible en el menú contextual o de etiqueta de acción.</span><span class="sxs-lookup"><span data-stu-id="4ecb8-104">Indicates whether the action is visible on the action tag or shortcut menu.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4ecb8-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="4ecb8-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="4ecb8-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4ecb8-106">**Value**</span></span>|<span data-ttu-id="4ecb8-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4ecb8-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4ecb8-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="4ecb8-108">TRUE</span></span>  <br/> |<span data-ttu-id="4ecb8-109">La acción no está visible en el menú.</span><span class="sxs-lookup"><span data-stu-id="4ecb8-109">The action is not visible on the menu.</span></span>  <br/> |
|<span data-ttu-id="4ecb8-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="4ecb8-110">FALSE</span></span>  <br/> |<span data-ttu-id="4ecb8-111">La acción está visible en el menú (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="4ecb8-111">The action is visible on the menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ecb8-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ecb8-112">Remarks</span></span>

<span data-ttu-id="4ecb8-113">Para obtener una referencia a la celda Invisible por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="4ecb8-113">To get a reference to the Invisible cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ecb8-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4ecb8-114">Cell name:</span></span>  <br/> |<span data-ttu-id="4ecb8-115">Acciones.</span><span class="sxs-lookup"><span data-stu-id="4ecb8-115">Actions.</span></span> <span data-ttu-id="4ecb8-116">*nombre* . Acciones de Invisiblewhere.</span><span class="sxs-lookup"><span data-stu-id="4ecb8-116">*name*  .Invisiblewhere Actions.</span></span>  <span data-ttu-id="4ecb8-117">*nombre* es el nombre de la fila de acciones</span><span class="sxs-lookup"><span data-stu-id="4ecb8-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="4ecb8-118">Para obtener una referencia desde un programa a la celda Invisible por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4ecb8-118">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ecb8-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4ecb8-119">Section index:</span></span>  <br/> |<span data-ttu-id="4ecb8-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="4ecb8-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="4ecb8-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4ecb8-121">Row index:</span></span>  <br/> |<span data-ttu-id="4ecb8-122">**visRowAction** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4ecb8-122">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="4ecb8-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4ecb8-123">Cell index:</span></span>  <br/> |<span data-ttu-id="4ecb8-124">**visActionInvisible**</span><span class="sxs-lookup"><span data-stu-id="4ecb8-124">**visActionInvisible**</span></span> <br/> |
   

