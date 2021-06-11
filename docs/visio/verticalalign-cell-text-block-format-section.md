---
title: Celda VerticalAlign (Sección de formato del bloque de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
localization_priority: Normal
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: Determina la alineación vertical del texto en el bloque de texto.
ms.openlocfilehash: 954a0cf0b80d6b675dcc016997f1923041069eac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425795"
---
# <a name="verticalalign-cell-text-block-format-section"></a><span data-ttu-id="6f0d3-103">Celda VerticalAlign (Sección de formato del bloque de texto)</span><span class="sxs-lookup"><span data-stu-id="6f0d3-103">VerticalAlign Cell (Text Block Format Section)</span></span>

<span data-ttu-id="6f0d3-104">Determina la alineación vertical del texto en el bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="6f0d3-104">Determines the vertical alignment of text within the text block.</span></span>
  
|<span data-ttu-id="6f0d3-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6f0d3-105">**Value**</span></span>|<span data-ttu-id="6f0d3-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f0d3-106">**Description**</span></span>|<span data-ttu-id="6f0d3-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="6f0d3-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="6f0d3-108">0</span><span class="sxs-lookup"><span data-stu-id="6f0d3-108">0</span></span>  <br/> | <span data-ttu-id="6f0d3-109">Top</span><span class="sxs-lookup"><span data-stu-id="6f0d3-109">Top</span></span>  <br/> |<span data-ttu-id="6f0d3-110">**visVertTop**</span><span class="sxs-lookup"><span data-stu-id="6f0d3-110">**visVertTop**</span></span> <br/> |
| <span data-ttu-id="6f0d3-111">1</span><span class="sxs-lookup"><span data-stu-id="6f0d3-111">1</span></span>  <br/> | <span data-ttu-id="6f0d3-112">Middle</span><span class="sxs-lookup"><span data-stu-id="6f0d3-112">Middle</span></span>  <br/> |<span data-ttu-id="6f0d3-113">**visVertMiddle**</span><span class="sxs-lookup"><span data-stu-id="6f0d3-113">**visVertMiddle**</span></span> <br/> |
| <span data-ttu-id="6f0d3-114">2</span><span class="sxs-lookup"><span data-stu-id="6f0d3-114">2</span></span>  <br/> | <span data-ttu-id="6f0d3-115">Hacia la parte inferior</span><span class="sxs-lookup"><span data-stu-id="6f0d3-115">Bottom</span></span>  <br/> |<span data-ttu-id="6f0d3-116">**visVertBottom**</span><span class="sxs-lookup"><span data-stu-id="6f0d3-116">**visVertBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f0d3-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6f0d3-117">Remarks</span></span>

<span data-ttu-id="6f0d3-118">Para obtener una referencia a la celda VerticalAlign por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="6f0d3-118">To get a reference to the VerticalAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6f0d3-119">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6f0d3-119">Cell name:</span></span>  <br/> | <span data-ttu-id="6f0d3-120">VerticalAlign</span><span class="sxs-lookup"><span data-stu-id="6f0d3-120">VerticalAlign</span></span>  <br/> |
   
<span data-ttu-id="6f0d3-121">Para obtener una referencia a la celda VerticalAlign por su índice
 desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6f0d3-121">To get a reference to the VerticalAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6f0d3-122">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6f0d3-122">Section index:</span></span>  <br/> |<span data-ttu-id="6f0d3-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6f0d3-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6f0d3-124">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6f0d3-124">Row index:</span></span>  <br/> |<span data-ttu-id="6f0d3-125">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="6f0d3-125">**visRowText**</span></span> <br/> |
| <span data-ttu-id="6f0d3-126">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6f0d3-126">Cell index:</span></span>  <br/> |<span data-ttu-id="6f0d3-127">**visTxtBlkVerticalAlign**</span><span class="sxs-lookup"><span data-stu-id="6f0d3-127">**visTxtBlkVerticalAlign**</span></span> <br/> |
   

