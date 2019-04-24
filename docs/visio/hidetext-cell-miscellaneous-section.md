---
title: Celda HideText (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
localization_priority: Normal
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: Oculta el texto en una forma. Puede ver el texto, editar las propiedades y aplicar diversos estilos al texto en el bloque de texto, aunque los cambios no aparezcan hasta que restablezca HideText a FALSE (0).
ms.openlocfilehash: 3e1be814984ed15247c451f5cd86d0f7a6dba71a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329963"
---
# <a name="hidetext-cell-miscellaneous-section"></a><span data-ttu-id="cddef-104">Celda HideText (Sección de varios)</span><span class="sxs-lookup"><span data-stu-id="cddef-104">HideText Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="cddef-p102">Oculta el texto en una forma. Puede ver el texto, editar las propiedades y aplicar diversos estilos al texto en el bloque de texto, aunque los cambios no aparezcan hasta que restablezca HideText a FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="cddef-p102">Hides the text for a shape. You can view text, edit properties, and apply styles to the text in the text block, although the changes will not appear until you reset HideText to FALSE (0).</span></span>
  
|<span data-ttu-id="cddef-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cddef-107">**Value**</span></span>|<span data-ttu-id="cddef-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cddef-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="cddef-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="cddef-109">TRUE</span></span>  <br/> | <span data-ttu-id="cddef-110">El texto se encuentra oculto y no se imprime.</span><span class="sxs-lookup"><span data-stu-id="cddef-110">Text is hidden and does not print.</span></span>  <br/> |
| <span data-ttu-id="cddef-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="cddef-111">FALSE</span></span>  <br/> | <span data-ttu-id="cddef-112">El texto no se encuentra oculto.</span><span class="sxs-lookup"><span data-stu-id="cddef-112">Text is not hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cddef-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cddef-113">Remarks</span></span>

<span data-ttu-id="cddef-114">Para obtener una referencia a la celda HideText por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="cddef-114">To get a reference to the HideText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cddef-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="cddef-115">Cell name:</span></span>  <br/> | <span data-ttu-id="cddef-116">HideText</span><span class="sxs-lookup"><span data-stu-id="cddef-116">HideText</span></span>  <br/> |
   
<span data-ttu-id="cddef-117">Para obtener una referencia desde un programa a la celda HideText por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="cddef-117">To get a reference to the HideText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cddef-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="cddef-118">Section index:</span></span>  <br/> |<span data-ttu-id="cddef-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cddef-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cddef-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="cddef-120">Row index:</span></span>  <br/> |<span data-ttu-id="cddef-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="cddef-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="cddef-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="cddef-122">Cell index:</span></span>  <br/> |<span data-ttu-id="cddef-123">**visHideText**</span><span class="sxs-lookup"><span data-stu-id="cddef-123">**visHideText**</span></span> <br/> |
   

