---
title: Celda Invisible (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
localization_priority: Normal
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: Indica si un hipervínculo aparece o no en el menú contextual de una forma o página.
ms.openlocfilehash: e269c5e907afa0d49f1fc6115b7a031835467c2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822356"
---
# <a name="invisible-cell-hyperlinks-section"></a><span data-ttu-id="22770-103">Celda Invisible (sección Hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="22770-103">Invisible Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="22770-104">Indica si un hipervínculo aparece o no en el menú contextual de una forma o página.</span><span class="sxs-lookup"><span data-stu-id="22770-104">Indicates whether a hyperlink appears on the shortcut menu for a shape or page.</span></span> 
  
|<span data-ttu-id="22770-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="22770-105">**Value**</span></span>|<span data-ttu-id="22770-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="22770-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="22770-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="22770-107">TRUE</span></span>  <br/> |<span data-ttu-id="22770-108">El hipervínculo no aparece como elemento de menú en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="22770-108">The hyperlink does not appear as a menu item on the shortcut menu.</span></span>  <br/> |
|<span data-ttu-id="22770-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="22770-109">FALSE</span></span>  <br/> |<span data-ttu-id="22770-110">El hipervínculo sí aparece como elemento de menú en el menú contextual (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="22770-110">The hyperlink does appear as a menu item on the shortcut menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22770-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22770-111">Remarks</span></span>

<span data-ttu-id="22770-112">Para obtener una referencia a la celda Invisible por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="22770-112">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="22770-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="22770-113">Cell name:</span></span>  <br/> |<span data-ttu-id="22770-114">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="22770-114">Hyperlink.</span></span> <span data-ttu-id="22770-115">*nombre* . Invisible donde hipervínculo *.name* es el nombre de fila</span><span class="sxs-lookup"><span data-stu-id="22770-115">*name*  .Invisible where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="22770-116">Para obtener una referencia desde un programa a la celda Invisible por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="22770-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="22770-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="22770-117">Section index:</span></span>  <br/> |<span data-ttu-id="22770-118">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="22770-118">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="22770-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="22770-119">Row index:</span></span>  <br/> |<span data-ttu-id="22770-120">**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="22770-120">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="22770-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="22770-121">Cell index:</span></span>  <br/> |<span data-ttu-id="22770-122">**visHLinkInvisible**</span><span class="sxs-lookup"><span data-stu-id="22770-122">**visHLinkInvisible**</span></span> <br/> |
   

