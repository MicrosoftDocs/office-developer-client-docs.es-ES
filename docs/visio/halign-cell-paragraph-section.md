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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414742"
---
# <a name="halign-cell-paragraph-section"></a><span data-ttu-id="c0ba1-103">Celda HAlign (Sección de párrafo)</span><span class="sxs-lookup"><span data-stu-id="c0ba1-103">HAlign Cell (Paragraph Section)</span></span>

<span data-ttu-id="c0ba1-104">Determina la alineación horizontal de los caracteres del bloque de texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="c0ba1-104">Determines the horizontal alignment of text in the shape's text block.</span></span>
  
|<span data-ttu-id="c0ba1-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c0ba1-105">**Value**</span></span>|<span data-ttu-id="c0ba1-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c0ba1-106">**Description**</span></span>|<span data-ttu-id="c0ba1-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="c0ba1-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c0ba1-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="c0ba1-108">0</span></span>  <br/> | <span data-ttu-id="c0ba1-109">Alinear a la izquierda</span><span class="sxs-lookup"><span data-stu-id="c0ba1-109">Left align</span></span>  <br/> |<span data-ttu-id="c0ba1-110">**visHorzLeft**</span><span class="sxs-lookup"><span data-stu-id="c0ba1-110">**visHorzLeft**</span></span> <br/> |
| <span data-ttu-id="c0ba1-111">1</span><span class="sxs-lookup"><span data-stu-id="c0ba1-111">1</span></span>  <br/> | <span data-ttu-id="c0ba1-112">Hacia el centro</span><span class="sxs-lookup"><span data-stu-id="c0ba1-112">Center</span></span>  <br/> |<span data-ttu-id="c0ba1-113">**visHorzCenter**</span><span class="sxs-lookup"><span data-stu-id="c0ba1-113">**visHorzCenter**</span></span> <br/> |
| <span data-ttu-id="c0ba1-114">segundo</span><span class="sxs-lookup"><span data-stu-id="c0ba1-114">2</span></span>  <br/> | <span data-ttu-id="c0ba1-115">Alinear a la derecha</span><span class="sxs-lookup"><span data-stu-id="c0ba1-115">Right align</span></span>  <br/> |<span data-ttu-id="c0ba1-116">**visHorzRight**</span><span class="sxs-lookup"><span data-stu-id="c0ba1-116">**visHorzRight**</span></span> <br/> |
| <span data-ttu-id="c0ba1-117">3</span><span class="sxs-lookup"><span data-stu-id="c0ba1-117">3</span></span>  <br/> | <span data-ttu-id="c0ba1-118">Justify</span><span class="sxs-lookup"><span data-stu-id="c0ba1-118">Justify</span></span>  <br/> |<span data-ttu-id="c0ba1-119">**visHorzJustify**</span><span class="sxs-lookup"><span data-stu-id="c0ba1-119">**visHorzJustify**</span></span> <br/> |
| <span data-ttu-id="c0ba1-120">4 </span><span class="sxs-lookup"><span data-stu-id="c0ba1-120">4</span></span>  <br/> | <span data-ttu-id="c0ba1-121">Forzar justificar</span><span class="sxs-lookup"><span data-stu-id="c0ba1-121">Force justify</span></span>  <br/> |<span data-ttu-id="c0ba1-122">**visHorzForce**</span><span class="sxs-lookup"><span data-stu-id="c0ba1-122">**visHorzForce**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0ba1-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c0ba1-123">Remarks</span></span>

<span data-ttu-id="c0ba1-124">La justificación agrega espacios entre palabras en todas las líneas excepto en la última del párrafo para alinear el lado izquierdo y derecho del texto con los márgenes.</span><span class="sxs-lookup"><span data-stu-id="c0ba1-124">Justify adds space between words in every line except the last line of the paragraph to align both the left and right sides of text with the margins.</span></span>
  
<span data-ttu-id="c0ba1-125">La opción Forzar justificación justifica todas las líneas del párrafo, incluso la última.</span><span class="sxs-lookup"><span data-stu-id="c0ba1-125">Force justify justifies every line in the paragraph, including the last.</span></span>
  
<span data-ttu-id="c0ba1-126">Para obtener una referencia a la celda HAlign por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="c0ba1-126">To get a reference to the HAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0ba1-127">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c0ba1-127">Cell name:</span></span>  <br/> | <span data-ttu-id="c0ba1-128">Para. HorzAlign [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c0ba1-128">Para.HorzAlign[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c0ba1-129">Para obtener una referencia desde un programa a la celda HAlign por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c0ba1-129">To get a reference to the HAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0ba1-130">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c0ba1-130">Section index:</span></span>  <br/> |<span data-ttu-id="c0ba1-131">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="c0ba1-131">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="c0ba1-132">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c0ba1-132">Row index:</span></span>  <br/> |<span data-ttu-id="c0ba1-133">**visRowParagraph** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c0ba1-133">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c0ba1-134">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c0ba1-134">Cell index:</span></span>  <br/> |<span data-ttu-id="c0ba1-135">**visHorzAlign**</span><span class="sxs-lookup"><span data-stu-id="c0ba1-135">**visHorzAlign**</span></span> <br/> |
   

