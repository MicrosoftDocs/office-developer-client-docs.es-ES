---
title: Celda ViewMarkup (Sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
localization_priority: Normal
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: Determina si la marca de revisión aparece en la ventana de dibujo.
ms.openlocfilehash: eeccdd0d14bf28630937b0e480822abb6fb19da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416408"
---
# <a name="viewmarkup-cell-document-properties-section"></a><span data-ttu-id="fa18f-103">Celda ViewMarkup (Sección de propiedades del documento)</span><span class="sxs-lookup"><span data-stu-id="fa18f-103">ViewMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="fa18f-104">Determina si la marca de revisión aparece en la ventana de dibujo.</span><span class="sxs-lookup"><span data-stu-id="fa18f-104">Determines whether markup appears in the drawing window.</span></span> 
  
|<span data-ttu-id="fa18f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fa18f-105">**Value**</span></span>|<span data-ttu-id="fa18f-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa18f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fa18f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="fa18f-107">TRUE</span></span>  <br/> |<span data-ttu-id="fa18f-108">Aparece la marca de revisión en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="fa18f-108">Markup is displayed on the drawing.</span></span>  <br/> |
|<span data-ttu-id="fa18f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="fa18f-109">FALSE</span></span>  <br/> |<span data-ttu-id="fa18f-110">La marca de revisión no se muestra (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="fa18f-110">Markup is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa18f-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa18f-111">Remarks</span></span>

 <span data-ttu-id="fa18f-112">Cuando se activa el seguimiento de marcado (la celda AddMarkup es TRUE), la celda ViewMarkup se establece automáticamente en TRUE y permanece en TRUE incluso después de desactivar el seguimiento de marcado (la celda AddMarkup es FALSE).</span><span class="sxs-lookup"><span data-stu-id="fa18f-112">When markup tracking is turned on (AddMarkup cell is TRUE), the ViewMarkup cell is automatically set to TRUE and remains TRUE even after markup tracking has been turned off (AddMarkup cell is FALSE).</span></span> <span data-ttu-id="fa18f-113">Se omite el valor de la celda ViewMarkup cuando el valor de AddMarkup es TRUE.</span><span class="sxs-lookup"><span data-stu-id="fa18f-113">The value in the ViewMarkup cell is ignored when the AddMarkup cell is TRUE.</span></span> 
  
<span data-ttu-id="fa18f-114">La celda ViewMarkup también se establece en TRUE cuando se insertan comentarios en un dibujo (con independencia de que estén o no activadas las marcas de revisión), y es necesario que sea TRUE para ver los comentarios en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="fa18f-114">The ViewMarkup cell is also set to TRUE when comments are inserted in a drawing (whether or not markup tracking is turned on) and must be TRUE to see comments in the drawing.</span></span>
  
<span data-ttu-id="fa18f-115">Esta celda corresponde al comando **Mostrar marcas** en el grupo **Revisión** de la ficha **Revisar**.</span><span class="sxs-lookup"><span data-stu-id="fa18f-115">This cell corresponds to the **Show Markup** command in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="fa18f-116">Para obtener una referencia a la celda ViewMarkup por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="fa18f-116">To get a reference to the ViewMarkup cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa18f-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="fa18f-117">Cell name:</span></span>  <br/> |<span data-ttu-id="fa18f-118">ViewMarkup</span><span class="sxs-lookup"><span data-stu-id="fa18f-118">ViewMarkup</span></span>  <br/> |
   
<span data-ttu-id="fa18f-119">Para obtener una referencia desde un programa a la celda ViewMarkup por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="fa18f-119">To get a reference to the ViewMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa18f-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="fa18f-120">Section index:</span></span>  <br/> |<span data-ttu-id="fa18f-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fa18f-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fa18f-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="fa18f-122">Row index:</span></span>  <br/> |<span data-ttu-id="fa18f-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="fa18f-123">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="fa18f-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="fa18f-124">Cell index:</span></span>  <br/> |<span data-ttu-id="fa18f-125">**visDocViewMarkup**</span><span class="sxs-lookup"><span data-stu-id="fa18f-125">**visDocViewMarkup**</span></span> <br/> |
   

