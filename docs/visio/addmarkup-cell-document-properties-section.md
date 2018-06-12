---
title: Celda AddMarkup (Sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030801
localization_priority: Normal
ms.assetid: 46146424-b4c9-2240-36c0-19bb35ec51d1
description: Indica si el documento se está editando con marcas de revisión.
ms.openlocfilehash: 69430122b0a7665d7daa4a6b28f3a51745b74473
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821530"
---
# <a name="addmarkup-cell-document-properties-section"></a><span data-ttu-id="61062-103">Celda AddMarkup (Sección de propiedades del documento)</span><span class="sxs-lookup"><span data-stu-id="61062-103">AddMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="61062-104">Indica si el documento se está editando con marcas de revisión.</span><span class="sxs-lookup"><span data-stu-id="61062-104">Indicates whether the document is being reviewed for markup.</span></span>
  
|<span data-ttu-id="61062-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="61062-105">**Value**</span></span>|<span data-ttu-id="61062-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="61062-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="61062-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="61062-107">TRUE</span></span>  <br/> |<span data-ttu-id="61062-108">Se está revisando el documento.</span><span class="sxs-lookup"><span data-stu-id="61062-108">Document is being reviewed.</span></span>  <br/> |
|<span data-ttu-id="61062-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="61062-109">FALSE</span></span>  <br/> |<span data-ttu-id="61062-110">No se está revisando el documento (opción predeterminada).</span><span class="sxs-lookup"><span data-stu-id="61062-110">Document is not being reviewed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61062-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61062-111">Remarks</span></span>

<span data-ttu-id="61062-112">Cuando se establece la celda AddMarkup es true, el revisor agrega las marcas y los cambios se aplican a páginas de revisión superpuestas, no a las páginas de dibujo originales.</span><span class="sxs-lookup"><span data-stu-id="61062-112">When the AddMarkup cell is set to TRUE, the reviewer is adding markup and changes are applied to markup overlay pages, not to original drawing pages.</span></span> <span data-ttu-id="61062-113">Cuando la celda AddMarkup es FALSE, el seguimiento de revisiones está desactivado y los cambios se aplican a las páginas de dibujo originales.</span><span class="sxs-lookup"><span data-stu-id="61062-113">When the AddMarkup cell is FALSE, markup tracking is off and changes are applied to the original drawing pages.</span></span>
  
> [!NOTE]
> <span data-ttu-id="61062-114">Puede evitar marcado en los documentos mediante la función GUARD.</span><span class="sxs-lookup"><span data-stu-id="61062-114">You can prevent markup on your documents by using the GUARD function.</span></span> <span data-ttu-id="61062-115">Si la celda AddMarkup contiene la fórmula = GUARD (false), el comando **Seguimiento de revisiones** está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="61062-115">If the AddMarkup cell contains the formula =GUARD(FALSE), the **Track Markup** command is disabled.</span></span> 
  
<span data-ttu-id="61062-116">Esta configuración corresponde a la opción de comando **Seguimiento de revisiones** en el grupo de **marcado** en la ficha **Revisar** .</span><span class="sxs-lookup"><span data-stu-id="61062-116">This setting corresponds to the **Track Markup** command setting in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="61062-117">Para obtener una referencia a la celda AddMarkup por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="61062-117">To get a reference to the AddMarkup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61062-118">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="61062-118">Cell name:</span></span>  <br/> |<span data-ttu-id="61062-119">AddMarkup</span><span class="sxs-lookup"><span data-stu-id="61062-119">AddMarkup</span></span>  <br/> |
   
<span data-ttu-id="61062-120">Para obtener una referencia a la celda AddMarkup por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="61062-120">To get a reference to the AddMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61062-121">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="61062-121">Section index:</span></span>  <br/> |<span data-ttu-id="61062-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="61062-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="61062-123">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="61062-123">Row index:</span></span>  <br/> |<span data-ttu-id="61062-124">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="61062-124">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="61062-125">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="61062-125">Cell index:</span></span>  <br/> |<span data-ttu-id="61062-126">**visDocAddMarkup**</span><span class="sxs-lookup"><span data-stu-id="61062-126">**visDocAddMarkup**</span></span> <br/> |
   

