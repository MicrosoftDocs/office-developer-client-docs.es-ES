---
title: Celda HAlign (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
localization_priority: Normal
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: Determina la alineación horizontal de los caracteres del bloque de texto de una forma.
ms.openlocfilehash: a48619e2531c0a69ad63af3b88ae9f019019b1fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360182"
---
# <a name="halign-cell-paragraph-section"></a><span data-ttu-id="8e4bd-103">Celda HAlign (Sección de párrafo)</span><span class="sxs-lookup"><span data-stu-id="8e4bd-103">HAlign Cell (Paragraph Section)</span></span>

<span data-ttu-id="8e4bd-104">Determina la alineación horizontal de los caracteres del bloque de texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="8e4bd-104">Determines the horizontal alignment of text in the shape's text block.</span></span>
  
|<span data-ttu-id="8e4bd-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="8e4bd-105">**Value**</span></span>|<span data-ttu-id="8e4bd-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e4bd-106">**Description**</span></span>|<span data-ttu-id="8e4bd-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="8e4bd-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8e4bd-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="8e4bd-108">0</span></span>  <br/> | <span data-ttu-id="8e4bd-109">Alinear a la izquierda</span><span class="sxs-lookup"><span data-stu-id="8e4bd-109">Left align</span></span>  <br/> |<span data-ttu-id="8e4bd-110">**visHorzLeft**</span><span class="sxs-lookup"><span data-stu-id="8e4bd-110">**visHorzLeft**</span></span> <br/> |
| <span data-ttu-id="8e4bd-111">1</span><span class="sxs-lookup"><span data-stu-id="8e4bd-111">1</span></span>  <br/> | <span data-ttu-id="8e4bd-112">Hacia el centro</span><span class="sxs-lookup"><span data-stu-id="8e4bd-112">Center</span></span>  <br/> |<span data-ttu-id="8e4bd-113">**visHorzCenter**</span><span class="sxs-lookup"><span data-stu-id="8e4bd-113">**visHorzCenter**</span></span> <br/> |
| <span data-ttu-id="8e4bd-114">segundo</span><span class="sxs-lookup"><span data-stu-id="8e4bd-114">2</span></span>  <br/> | <span data-ttu-id="8e4bd-115">Alinear a la derecha</span><span class="sxs-lookup"><span data-stu-id="8e4bd-115">Right align</span></span>  <br/> |<span data-ttu-id="8e4bd-116">**visHorzRight**</span><span class="sxs-lookup"><span data-stu-id="8e4bd-116">**visHorzRight**</span></span> <br/> |
| <span data-ttu-id="8e4bd-117">3</span><span class="sxs-lookup"><span data-stu-id="8e4bd-117">3</span></span>  <br/> | <span data-ttu-id="8e4bd-118">Justify</span><span class="sxs-lookup"><span data-stu-id="8e4bd-118">Justify</span></span>  <br/> |<span data-ttu-id="8e4bd-119">**visHorzJustify**</span><span class="sxs-lookup"><span data-stu-id="8e4bd-119">**visHorzJustify**</span></span> <br/> |
| <span data-ttu-id="8e4bd-120">4</span><span class="sxs-lookup"><span data-stu-id="8e4bd-120">4</span></span>  <br/> | <span data-ttu-id="8e4bd-121">Forzar justificar</span><span class="sxs-lookup"><span data-stu-id="8e4bd-121">Force justify</span></span>  <br/> |<span data-ttu-id="8e4bd-122">**visHorzForce**</span><span class="sxs-lookup"><span data-stu-id="8e4bd-122">**visHorzForce**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e4bd-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8e4bd-123">Remarks</span></span>

<span data-ttu-id="8e4bd-124">La justificación agrega espacios entre palabras en todas las líneas excepto en la última del párrafo para alinear el lado izquierdo y derecho del texto con los márgenes.</span><span class="sxs-lookup"><span data-stu-id="8e4bd-124">Justify adds space between words in every line except the last line of the paragraph to align both the left and right sides of text with the margins.</span></span>
  
<span data-ttu-id="8e4bd-125">La opción Forzar justificación justifica todas las líneas del párrafo, incluso la última.</span><span class="sxs-lookup"><span data-stu-id="8e4bd-125">Force justify justifies every line in the paragraph, including the last.</span></span>
  
<span data-ttu-id="8e4bd-126">Para obtener una referencia a la celda HAlign por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="8e4bd-126">To get a reference to the HAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8e4bd-127">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="8e4bd-127">Cell name:</span></span>  <br/> | <span data-ttu-id="8e4bd-128">Para. HorzAlign [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8e4bd-128">Para.HorzAlign[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8e4bd-129">Para obtener una referencia desde un programa a la celda HAlign por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8e4bd-129">To get a reference to the HAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8e4bd-130">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="8e4bd-130">Section index:</span></span>  <br/> |<span data-ttu-id="8e4bd-131">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="8e4bd-131">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="8e4bd-132">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="8e4bd-132">Row index:</span></span>  <br/> |<span data-ttu-id="8e4bd-133">**visRowParagraph** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8e4bd-133">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8e4bd-134">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="8e4bd-134">Cell index:</span></span>  <br/> |<span data-ttu-id="8e4bd-135">**visHorzAlign**</span><span class="sxs-lookup"><span data-stu-id="8e4bd-135">**visHorzAlign**</span></span> <br/> |
   

