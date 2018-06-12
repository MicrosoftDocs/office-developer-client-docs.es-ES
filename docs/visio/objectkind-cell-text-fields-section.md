---
title: Celda ObjectKind (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
localization_priority: Normal
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: Indica el tipo de campo de texto.
ms.openlocfilehash: d4b94b46e83935de14400468957adbdc8f6cb171
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822683"
---
# <a name="objectkind-cell-text-fields-section"></a><span data-ttu-id="d3924-103">Celda ObjectKind (Sección de campos de texto)</span><span class="sxs-lookup"><span data-stu-id="d3924-103">ObjectKind Cell (Text Fields Section)</span></span>

<span data-ttu-id="d3924-104">Indica el tipo de campo de texto.</span><span class="sxs-lookup"><span data-stu-id="d3924-104">Indicates the type of text field.</span></span>
  
|<span data-ttu-id="d3924-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d3924-105">**Value**</span></span>|<span data-ttu-id="d3924-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d3924-106">**Description**</span></span>|<span data-ttu-id="d3924-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="d3924-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="d3924-108">0</span><span class="sxs-lookup"><span data-stu-id="d3924-108">0</span></span>  <br/> | <span data-ttu-id="d3924-109">Estándar</span><span class="sxs-lookup"><span data-stu-id="d3924-109">Standard</span></span>  <br/> |<span data-ttu-id="d3924-110">**visTFOKStandard**</span><span class="sxs-lookup"><span data-stu-id="d3924-110">**visTFOKStandard**</span></span> <br/> |
| <span data-ttu-id="d3924-111">1</span><span class="sxs-lookup"><span data-stu-id="d3924-111">1</span></span>  <br/> |<span data-ttu-id="d3924-112">Horizontal en vertical</span><span class="sxs-lookup"><span data-stu-id="d3924-112">Horizontal in vertical</span></span>  <br/> |<span data-ttu-id="d3924-113">**visTFOKHorizontaInVertical**</span><span class="sxs-lookup"><span data-stu-id="d3924-113">**visTFOKHorizontaInVertical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3924-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d3924-114">Remarks</span></span>

<span data-ttu-id="d3924-115">Los campos de texto pueden ser de uno de los dos siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="d3924-115">Text fields can be one of the following types:</span></span>
  
- <span data-ttu-id="d3924-116">Estándar, que indica que el campo se insertó por su categoría.</span><span class="sxs-lookup"><span data-stu-id="d3924-116">Standard, indicating that the field was inserted by field category.</span></span>
    
- <span data-ttu-id="d3924-117">Horizontal en vertical, que indica que el campo es de texto horizontal sobre texto vertical.</span><span class="sxs-lookup"><span data-stu-id="d3924-117">Horizontal in vertical, indicating that the field is horizontal text set within vertical text.</span></span>
    
<span data-ttu-id="d3924-118">Para obtener una referencia a la celda ObjectKind por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="d3924-118">To get a reference to the ObjectKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3924-119">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d3924-119">Cell name:</span></span>  <br/> | <span data-ttu-id="d3924-120">Fields.ObjectKind [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d3924-120">Fields.ObjectKind[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d3924-121">Para obtener una referencia a la celda ObjectKind por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d3924-121">To get a reference to the ObjectKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3924-122">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d3924-122">Section index:</span></span>  <br/> |<span data-ttu-id="d3924-123">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="d3924-123">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="d3924-124">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d3924-124">Row index:</span></span>  <br/> |<span data-ttu-id="d3924-125">**visRowField** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d3924-125">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d3924-126">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d3924-126">Cell index:</span></span>  <br/> |<span data-ttu-id="d3924-127">**visFieldObjectKind**</span><span class="sxs-lookup"><span data-stu-id="d3924-127">**visFieldObjectKind**</span></span> <br/> |
   

