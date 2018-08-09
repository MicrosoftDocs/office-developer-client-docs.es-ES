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
ms.openlocfilehash: 3956b6cf5ccb870255d6943e74b4f02650952d09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821976"
---
# <a name="disabled-cell-actions-section"></a><span data-ttu-id="dbf26-103">Celda Disabled (sección Acciones)</span><span class="sxs-lookup"><span data-stu-id="dbf26-103">Disabled Cell (Actions Section)</span></span>

<span data-ttu-id="dbf26-104">Indica si está deshabilitado un elemento de un menú contextual o de etiquetas de acción.</span><span class="sxs-lookup"><span data-stu-id="dbf26-104">Indicates whether an item on a shortcut or action tag menu is disabled.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dbf26-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="dbf26-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="dbf26-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="dbf26-106">**Value**</span></span>|<span data-ttu-id="dbf26-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dbf26-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dbf26-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="dbf26-108">TRUE</span></span>  <br/> |<span data-ttu-id="dbf26-109">Se deshabilita (atenúa) el nombre del comando.</span><span class="sxs-lookup"><span data-stu-id="dbf26-109">Disable (dim) command name.</span></span>  <br/> |
|<span data-ttu-id="dbf26-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="dbf26-110">FALSE</span></span>  <br/> |<span data-ttu-id="dbf26-111">Se habilita el nombre del comando (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="dbf26-111">Enable the command name (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dbf26-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dbf26-112">Remarks</span></span>

<span data-ttu-id="dbf26-113">Para obtener una referencia a la celda Disabled por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="dbf26-113">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dbf26-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="dbf26-114">Cell name:</span></span>  <br/> |<span data-ttu-id="dbf26-115">Acciones.</span><span class="sxs-lookup"><span data-stu-id="dbf26-115">Actions.</span></span> <span data-ttu-id="dbf26-116">*nombre* . Deshabilitado donde acciones.</span><span class="sxs-lookup"><span data-stu-id="dbf26-116">*name*  .Disabled           where Actions.</span></span> <span data-ttu-id="dbf26-117">*nombre* es el nombre de la fila de acciones</span><span class="sxs-lookup"><span data-stu-id="dbf26-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="dbf26-118">Para obtener una referencia desde un programa a la celda Disabled por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="dbf26-118">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dbf26-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="dbf26-119">Section index:</span></span>  <br/> |<span data-ttu-id="dbf26-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="dbf26-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="dbf26-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="dbf26-121">Row index:</span></span>  <br/> |<span data-ttu-id="dbf26-122">**visRowAction** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dbf26-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="dbf26-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="dbf26-123">Cell index:</span></span>  <br/> |<span data-ttu-id="dbf26-124">**visActionDisabled**</span><span class="sxs-lookup"><span data-stu-id="dbf26-124">**visActionDisabled**</span></span> <br/> |
   

