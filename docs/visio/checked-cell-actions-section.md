---
title: Celda Checked (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm155
localization_priority: Normal
ms.assetid: 50937e29-eaa1-0cd0-53cc-dc17e7793e55
description: Indica si un elemento aparece activado en el menú contextual o de etiquetas de acción.
ms.openlocfilehash: 870823f28d802e7cafa81efbe5617f27b6714885
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438333"
---
# <a name="checked-cell-actions-section"></a><span data-ttu-id="dad76-103">Celda Checked (sección de acciones)</span><span class="sxs-lookup"><span data-stu-id="dad76-103">Checked Cell (Actions Section)</span></span>

<span data-ttu-id="dad76-104">Indica si un elemento aparece activado en el menú contextual o de etiquetas de acción.</span><span class="sxs-lookup"><span data-stu-id="dad76-104">Indicates whether an item is checked on the shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dad76-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="dad76-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="dad76-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="dad76-106">**Value**</span></span>|<span data-ttu-id="dad76-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dad76-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dad76-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="dad76-108">TRUE</span></span>  <br/> |<span data-ttu-id="dad76-109">Se muestra una marca de verificación.</span><span class="sxs-lookup"><span data-stu-id="dad76-109">Check mark is displayed.</span></span>  <br/> |
|<span data-ttu-id="dad76-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="dad76-110">FALSE</span></span>  <br/> |<span data-ttu-id="dad76-111">No se muestra marca de verificación (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="dad76-111">Check mark is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dad76-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dad76-112">Remarks</span></span>

<span data-ttu-id="dad76-113">Para obtener una referencia a la celda Checked por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="dad76-113">To get a reference to the Checked cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dad76-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="dad76-114">Cell name:</span></span>  <br/> |<span data-ttu-id="dad76-115">Actividades.</span><span class="sxs-lookup"><span data-stu-id="dad76-115">Actions.</span></span> <span data-ttu-id="dad76-116">*nombre* . Comprobando las acciones.</span><span class="sxs-lookup"><span data-stu-id="dad76-116">*name*  .Checked           where Actions.</span></span> <span data-ttu-id="dad76-117">*nombre* es el nombre de la fila de acciones.</span><span class="sxs-lookup"><span data-stu-id="dad76-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="dad76-118">Para obtener una referencia desde un programa a la celda Checked por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="dad76-118">To get a reference to the Checked cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dad76-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="dad76-119">Section index:</span></span>  <br/> |<span data-ttu-id="dad76-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="dad76-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="dad76-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="dad76-121">Row index:</span></span>  <br/> |<span data-ttu-id="dad76-122">**visRowAction** +  *i* donde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="dad76-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="dad76-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="dad76-123">Cell index:</span></span>  <br/> |<span data-ttu-id="dad76-124">**visActionChecked**</span><span class="sxs-lookup"><span data-stu-id="dad76-124">**visActionChecked**</span></span> <br/> |
   

