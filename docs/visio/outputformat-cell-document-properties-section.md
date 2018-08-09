---
title: Celda OutputFormat (Sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251617
localization_priority: Normal
ms.assetid: 17238019-c800-5d3a-32f6-fb0008d4e25f
description: Determina el formato de salida de un dibujo. Las páginas de dibujo suelen tener formato para imprimirse (valor predeterminado); no obstante, el usuario puede elegir otros formatos de salida.
ms.openlocfilehash: 7103fa5c2bc721add3496b7a497989d6632d58f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822698"
---
# <a name="outputformat-cell-document-properties-section"></a><span data-ttu-id="6c1c1-104">Celda OutputFormat (sección Propiedades del documento)</span><span class="sxs-lookup"><span data-stu-id="6c1c1-104">OutputFormat Cell (Document Properties Section)</span></span>

<span data-ttu-id="6c1c1-p102">Determina el formato de salida de un dibujo. Las páginas de dibujo suelen tener formato para imprimirse (valor predeterminado); no obstante, el usuario puede elegir otros formatos de salida.</span><span class="sxs-lookup"><span data-stu-id="6c1c1-p102">Determines the output format for a drawing. Drawing pages are usually formatted for printing (default); however, you can choose other output formats.</span></span>
  
|<span data-ttu-id="6c1c1-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6c1c1-107">**Value**</span></span>|<span data-ttu-id="6c1c1-108">**Formato de salida**</span><span class="sxs-lookup"><span data-stu-id="6c1c1-108">**Output format**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6c1c1-109">0</span><span class="sxs-lookup"><span data-stu-id="6c1c1-109">0</span></span>  <br/> | <span data-ttu-id="6c1c1-110">Impresión (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="6c1c1-110">Printing (default)</span></span>  <br/> |
| <span data-ttu-id="6c1c1-111">1</span><span class="sxs-lookup"><span data-stu-id="6c1c1-111">1</span></span>  <br/> | <span data-ttu-id="6c1c1-112">Presentación de diapositivas de PowerPoint</span><span class="sxs-lookup"><span data-stu-id="6c1c1-112">PowerPoint slide show</span></span>  <br/> |
| <span data-ttu-id="6c1c1-113">2</span><span class="sxs-lookup"><span data-stu-id="6c1c1-113">2</span></span>  <br/> | <span data-ttu-id="6c1c1-114">Salida HTML o GIF</span><span class="sxs-lookup"><span data-stu-id="6c1c1-114">HTML or GIF output</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c1c1-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6c1c1-115">Remarks</span></span>

<span data-ttu-id="6c1c1-116">Para obtener una referencia a la celda OutputFormat por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="6c1c1-116">To get a reference to the OutputFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c1c1-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6c1c1-117">Cell name:</span></span>  <br/> | <span data-ttu-id="6c1c1-118">OutputFormat</span><span class="sxs-lookup"><span data-stu-id="6c1c1-118">OutputFormat</span></span>  <br/> |
   
<span data-ttu-id="6c1c1-119">Para obtener una referencia desde un programa a la celda OutputFormat por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6c1c1-119">To get a reference to the OutputFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c1c1-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6c1c1-120">Section index:</span></span>  <br/> |<span data-ttu-id="6c1c1-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6c1c1-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6c1c1-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6c1c1-122">Row index:</span></span>  <br/> |<span data-ttu-id="6c1c1-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="6c1c1-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="6c1c1-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6c1c1-124">Cell index:</span></span>  <br/> |<span data-ttu-id="6c1c1-125">**visDocOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="6c1c1-125">**visDocOutputFormat**</span></span> <br/> |
   

