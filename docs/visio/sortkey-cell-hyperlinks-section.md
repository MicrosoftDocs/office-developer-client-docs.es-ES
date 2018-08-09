---
title: Celda SortKey (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
localization_priority: Normal
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: Un número que determina el orden de los hipervínculos que aparecen en un menú contextual.
ms.openlocfilehash: 03596918924b04a776eb7ffd2f16db1c57de8194
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823301"
---
# <a name="sortkey-cell-hyperlinks-section"></a><span data-ttu-id="07878-103">Celda SortKey (sección Hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="07878-103">SortKey Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="07878-104">Un número que determina el orden de los hipervínculos que aparecen en un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="07878-104">A number that determines the order of hyperlinks that appear on a shortcut menu.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="07878-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07878-105">Remarks</span></span>

<span data-ttu-id="07878-p101">Los hipervínculos aparecen en un menú contextual ordenadas de menor a mayor, con los números más bajos en la parte superior del menú. Si dos filas de hipervínculos tienen el mismo valor para la celda SortKey, el orden queda determinado por el orden físico de la fila. El valor predeterminado es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="07878-p101">The hyperlinks on a shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu. If two hyperlink rows have the same SortKey cell value, the order is determined by physical row order. The default is 0 (zero).</span></span> 
  
<span data-ttu-id="07878-109">Para obtener una referencia a la celda SortKey por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="07878-109">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07878-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="07878-110">Cell name:</span></span>  <br/> |<span data-ttu-id="07878-111">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="07878-111">Hyperlink.</span></span> <span data-ttu-id="07878-112">*nombre* . SortKey donde hipervínculo *.name* es el nombre de fila</span><span class="sxs-lookup"><span data-stu-id="07878-112">*name*  .SortKey where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="07878-113">Para obtener una referencia desde un programa a la celda SortKey por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="07878-113">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07878-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="07878-114">Section index:</span></span>  <br/> |<span data-ttu-id="07878-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="07878-115">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="07878-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="07878-116">Row index:</span></span>  <br/> |<span data-ttu-id="07878-117">**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="07878-117">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="07878-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="07878-118">Cell index:</span></span>  <br/> |<span data-ttu-id="07878-119">**visHLinkSortKey**</span><span class="sxs-lookup"><span data-stu-id="07878-119">**visHLinkSortKey**</span></span> <br/> |
   

