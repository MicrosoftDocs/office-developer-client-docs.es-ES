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
ms.openlocfilehash: 7c5bcdbfe5b7d8e796af49c8da6ef0fc233e3d62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821779"
---
# <a name="checked-cell-actions-section"></a><span data-ttu-id="da1e5-103">Celda Checked (sección Acciones)</span><span class="sxs-lookup"><span data-stu-id="da1e5-103">Checked Cell (Actions Section)</span></span>

<span data-ttu-id="da1e5-104">Indica si un elemento aparece activado en el menú contextual o de etiquetas de acción.</span><span class="sxs-lookup"><span data-stu-id="da1e5-104">Indicates whether an item is checked on the shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="da1e5-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="da1e5-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="da1e5-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="da1e5-106">**Value**</span></span>|<span data-ttu-id="da1e5-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="da1e5-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="da1e5-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="da1e5-108">TRUE</span></span>  <br/> |<span data-ttu-id="da1e5-109">
          Se muestra una marca de verificación.
</span><span class="sxs-lookup"><span data-stu-id="da1e5-109">Check mark is displayed.</span></span>  <br/> |
|<span data-ttu-id="da1e5-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="da1e5-110">FALSE</span></span>  <br/> |<span data-ttu-id="da1e5-111">
          No se muestra marca de verificación (valor predeterminado).
</span><span class="sxs-lookup"><span data-stu-id="da1e5-111">Check mark is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da1e5-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="da1e5-112">Remarks</span></span>

<span data-ttu-id="da1e5-113">Para obtener una referencia a la celda Checked por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="da1e5-113">To get a reference to the Checked cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da1e5-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="da1e5-114">Cell name:</span></span>  <br/> |<span data-ttu-id="da1e5-115">Acciones.</span><span class="sxs-lookup"><span data-stu-id="da1e5-115">Actions.</span></span> <span data-ttu-id="da1e5-116">*nombre* . Comprueba que las acciones.</span><span class="sxs-lookup"><span data-stu-id="da1e5-116">*name*  .Checked           where Actions.</span></span> <span data-ttu-id="da1e5-117">*nombre* es el nombre de la fila de acciones</span><span class="sxs-lookup"><span data-stu-id="da1e5-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="da1e5-118">Para obtener una referencia desde un programa a la celda Checked por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="da1e5-118">To get a reference to the Checked cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da1e5-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="da1e5-119">Section index:</span></span>  <br/> |<span data-ttu-id="da1e5-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="da1e5-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="da1e5-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="da1e5-121">Row index:</span></span>  <br/> |<span data-ttu-id="da1e5-122">**visRowAction** +  *i* donde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="da1e5-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="da1e5-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="da1e5-123">Cell index:</span></span>  <br/> |<span data-ttu-id="da1e5-124">**visActionChecked**</span><span class="sxs-lookup"><span data-stu-id="da1e5-124">**visActionChecked**</span></span> <br/> |
   

