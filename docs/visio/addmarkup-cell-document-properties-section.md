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
ms.openlocfilehash: 4e0860639b0d89fce2c35a8947bd5ac00fcc63e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427636"
---
# <a name="addmarkup-cell-document-properties-section"></a><span data-ttu-id="4888d-103">Celda AddMarkup (Sección de propiedades del documento)</span><span class="sxs-lookup"><span data-stu-id="4888d-103">AddMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="4888d-104">Indica si el documento se está editando con marcas de revisión.</span><span class="sxs-lookup"><span data-stu-id="4888d-104">Indicates whether the document is being reviewed for markup.</span></span>
  
|<span data-ttu-id="4888d-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4888d-105">**Value**</span></span>|<span data-ttu-id="4888d-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4888d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4888d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="4888d-107">TRUE</span></span>  <br/> |<span data-ttu-id="4888d-108">Se está revisando el documento.</span><span class="sxs-lookup"><span data-stu-id="4888d-108">Document is being reviewed.</span></span>  <br/> |
|<span data-ttu-id="4888d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="4888d-109">FALSE</span></span>  <br/> |<span data-ttu-id="4888d-110">No se está revisando el documento (opción predeterminada).</span><span class="sxs-lookup"><span data-stu-id="4888d-110">Document is not being reviewed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4888d-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4888d-111">Remarks</span></span>

<span data-ttu-id="4888d-112">Cuando se establece en TRUE la celda AddMarkup, el revisor agrega las marcas y los cambios se aplican a las páginas de superposición de revisiones, no a las páginas de dibujo originales.</span><span class="sxs-lookup"><span data-stu-id="4888d-112">When the AddMarkup cell is set to TRUE, the reviewer is adding markup and changes are applied to markup overlay pages, not to original drawing pages.</span></span> <span data-ttu-id="4888d-113">Cuando se establece en FALSE, se desactivan las marcas y los cambios se aplican a las páginas de dibujo originales.</span><span class="sxs-lookup"><span data-stu-id="4888d-113">When the AddMarkup cell is FALSE, markup tracking is off and changes are applied to the original drawing pages.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4888d-114">Puede evitar el marcado en los documentos mediante la función GUARD.</span><span class="sxs-lookup"><span data-stu-id="4888d-114">You can prevent markup on your documents by using the GUARD function.</span></span> <span data-ttu-id="4888d-115">Si la celda AddMarkup contiene la fórmula =GUARD(FALSE), el comando **Track Markup** está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="4888d-115">If the AddMarkup cell contains the formula =GUARD(FALSE), the **Track Markup** command is disabled.</span></span> 
  
<span data-ttu-id="4888d-116">Esta configuración corresponde al comando **Seguimiento de revisiones** del grupo **Revisión** de la ficha **Revisar**.</span><span class="sxs-lookup"><span data-stu-id="4888d-116">This setting corresponds to the **Track Markup** command setting in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="4888d-117">Para obtener una referencia a la celda AddMarkup por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="4888d-117">To get a reference to the AddMarkup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4888d-118">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4888d-118">Cell name:</span></span>  <br/> |<span data-ttu-id="4888d-119">AddMarkup</span><span class="sxs-lookup"><span data-stu-id="4888d-119">AddMarkup</span></span>  <br/> |
   
<span data-ttu-id="4888d-120">Para obtener una referencia a la celda AddMarkup por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4888d-120">To get a reference to the AddMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4888d-121">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4888d-121">Section index:</span></span>  <br/> |<span data-ttu-id="4888d-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4888d-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4888d-123">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4888d-123">Row index:</span></span>  <br/> |<span data-ttu-id="4888d-124">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="4888d-124">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="4888d-125">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4888d-125">Cell index:</span></span>  <br/> |<span data-ttu-id="4888d-126">**visDocAddMarkup**</span><span class="sxs-lookup"><span data-stu-id="4888d-126">**visDocAddMarkup**</span></span> <br/> |
   

