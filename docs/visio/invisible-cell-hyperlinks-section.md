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
ms.openlocfilehash: b52da8244bf31e75bacbb6f24f73eba6ee8c6e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404634"
---
# <a name="invisible-cell-hyperlinks-section"></a><span data-ttu-id="3cdaf-103">Celda Invisible (Sección de hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="3cdaf-103">Invisible Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="3cdaf-104">Indica si un hipervínculo aparece o no en el menú contextual de una forma o página.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-104">Indicates whether a hyperlink appears on the shortcut menu for a shape or page.</span></span> 
  
|<span data-ttu-id="3cdaf-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3cdaf-105">**Value**</span></span>|<span data-ttu-id="3cdaf-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3cdaf-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3cdaf-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3cdaf-107">TRUE</span></span>  <br/> |<span data-ttu-id="3cdaf-108">El hipervínculo no aparece como elemento de menú en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-108">The hyperlink does not appear as a menu item on the shortcut menu.</span></span>  <br/> |
|<span data-ttu-id="3cdaf-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3cdaf-109">FALSE</span></span>  <br/> |<span data-ttu-id="3cdaf-110">El hipervínculo sí aparece como elemento de menú en el menú contextual (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="3cdaf-110">The hyperlink does appear as a menu item on the shortcut menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cdaf-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3cdaf-111">Remarks</span></span>

<span data-ttu-id="3cdaf-112">Para obtener una referencia a la celda Invisible por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="3cdaf-112">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3cdaf-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3cdaf-113">Cell name:</span></span>  <br/> |<span data-ttu-id="3cdaf-114">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-114">Hyperlink.</span></span> <span data-ttu-id="3cdaf-115">*nombre*  . Invisible donde Hyperlink  *.name*  es el nombre de fila</span><span class="sxs-lookup"><span data-stu-id="3cdaf-115">*name*  .Invisible where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="3cdaf-116">Para obtener una referencia desde un programa a la celda Invisible por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3cdaf-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3cdaf-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3cdaf-117">Section index:</span></span>  <br/> |<span data-ttu-id="3cdaf-118">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="3cdaf-118">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="3cdaf-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3cdaf-119">Row index:</span></span>  <br/> |<span data-ttu-id="3cdaf-120">**visRow1stHyperlink**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3cdaf-120">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="3cdaf-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3cdaf-121">Cell index:</span></span>  <br/> |<span data-ttu-id="3cdaf-122">**visHLinkInvisible**</span><span class="sxs-lookup"><span data-stu-id="3cdaf-122">**visHLinkInvisible**</span></span> <br/> |
   

