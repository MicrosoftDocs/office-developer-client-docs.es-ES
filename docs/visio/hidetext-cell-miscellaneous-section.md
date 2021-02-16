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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425487"
---
# <a name="hidetext-cell-miscellaneous-section"></a><span data-ttu-id="0a5b3-104">Celda HideText (Sección de varios)</span><span class="sxs-lookup"><span data-stu-id="0a5b3-104">HideText Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="0a5b3-p102">Oculta el texto en una forma. Puede ver el texto, editar las propiedades y aplicar diversos estilos al texto en el bloque de texto, aunque los cambios no aparezcan hasta que restablezca HideText a FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="0a5b3-p102">Hides the text for a shape. You can view text, edit properties, and apply styles to the text in the text block, although the changes will not appear until you reset HideText to FALSE (0).</span></span>
  
|<span data-ttu-id="0a5b3-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0a5b3-107">**Value**</span></span>|<span data-ttu-id="0a5b3-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0a5b3-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0a5b3-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="0a5b3-109">TRUE</span></span>  <br/> | <span data-ttu-id="0a5b3-110">El texto se encuentra oculto y no se imprime.</span><span class="sxs-lookup"><span data-stu-id="0a5b3-110">Text is hidden and does not print.</span></span>  <br/> |
| <span data-ttu-id="0a5b3-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="0a5b3-111">FALSE</span></span>  <br/> | <span data-ttu-id="0a5b3-112">El texto no se encuentra oculto.</span><span class="sxs-lookup"><span data-stu-id="0a5b3-112">Text is not hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a5b3-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0a5b3-113">Remarks</span></span>

<span data-ttu-id="0a5b3-114">Para obtener una referencia a la celda HideText por su nombre desde otra fórmula, o desde un programa mediante la **propiedad CellsU,** utilice:</span><span class="sxs-lookup"><span data-stu-id="0a5b3-114">To get a reference to the HideText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0a5b3-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="0a5b3-115">Cell name:</span></span>  <br/> | <span data-ttu-id="0a5b3-116">HideText</span><span class="sxs-lookup"><span data-stu-id="0a5b3-116">HideText</span></span>  <br/> |
   
<span data-ttu-id="0a5b3-117">Para obtener una referencia desde un programa a la celda HideText por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0a5b3-117">To get a reference to the HideText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0a5b3-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="0a5b3-118">Section index:</span></span>  <br/> |<span data-ttu-id="0a5b3-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0a5b3-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0a5b3-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="0a5b3-120">Row index:</span></span>  <br/> |<span data-ttu-id="0a5b3-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="0a5b3-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="0a5b3-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="0a5b3-122">Cell index:</span></span>  <br/> |<span data-ttu-id="0a5b3-123">**visHideText**</span><span class="sxs-lookup"><span data-stu-id="0a5b3-123">**visHideText**</span></span> <br/> |
   

