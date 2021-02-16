---
title: Celda Case (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251250
localization_priority: Normal
ms.assetid: cf063c05-5789-e037-700b-1e70df00e254
description: Determina el uso de mayúsculas y minúsculas en el texto de una forma. Las opciones de todas las letras en mayúsculas (1) y mayúsculas iniciales (2) no cambian la apariencia del texto escrito totalmente en mayúsculas. El texto debe estar en minúsculas para que estas opciones surtan efecto.
ms.openlocfilehash: 50ceaa1188caded40d36b8837c346fbbba2e14d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434350"
---
# <a name="case-cell-character-section"></a><span data-ttu-id="dab1b-105">Celda Case (Sección de caracteres)</span><span class="sxs-lookup"><span data-stu-id="dab1b-105">Case Cell (Character Section)</span></span>

<span data-ttu-id="dab1b-p102">Determina el uso de mayúsculas y minúsculas en el texto de una forma. Las opciones de todas las letras en mayúsculas (1) y mayúsculas iniciales (2) no cambian la apariencia del texto escrito totalmente en mayúsculas. El texto debe estar en minúsculas para que estas opciones surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="dab1b-p102">Determines the case of a shape's text. All capital (uppercase) letters (1) and initial capital letters (2) do not change the appearance of text that was entered in all capital letters. The text must be entered in lowercase letters for these options to show an effect.</span></span>
  
|<span data-ttu-id="dab1b-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="dab1b-109">**Value**</span></span>|<span data-ttu-id="dab1b-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dab1b-110">**Description**</span></span>|<span data-ttu-id="dab1b-111">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="dab1b-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="dab1b-112">0</span><span class="sxs-lookup"><span data-stu-id="dab1b-112">0</span></span>  <br/> | <span data-ttu-id="dab1b-113">Uso normal de mayúsculas y minúsculas</span><span class="sxs-lookup"><span data-stu-id="dab1b-113">Normal case</span></span>  <br/> |<span data-ttu-id="dab1b-114">**visCaseNormal**</span><span class="sxs-lookup"><span data-stu-id="dab1b-114">**visCaseNormal**</span></span> <br/> |
| <span data-ttu-id="dab1b-115">1 </span><span class="sxs-lookup"><span data-stu-id="dab1b-115">1</span></span>  <br/> | <span data-ttu-id="dab1b-116">Todo en mayúsculas</span><span class="sxs-lookup"><span data-stu-id="dab1b-116">All capital (uppercase) letters</span></span>  <br/> |<span data-ttu-id="dab1b-117">**visCaseAllCaps**</span><span class="sxs-lookup"><span data-stu-id="dab1b-117">**visCaseAllCaps**</span></span> <br/> |
| <span data-ttu-id="dab1b-118">2 </span><span class="sxs-lookup"><span data-stu-id="dab1b-118">2</span></span>  <br/> | <span data-ttu-id="dab1b-119">Sólo las letras iniciales en mayúsculas</span><span class="sxs-lookup"><span data-stu-id="dab1b-119">Initial capital letters only</span></span>  <br/> |<span data-ttu-id="dab1b-120">**visCaseInitialCaps**</span><span class="sxs-lookup"><span data-stu-id="dab1b-120">**visCaseInitialCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dab1b-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dab1b-121">Remarks</span></span>

<span data-ttu-id="dab1b-122">Para obtener una referencia a la celda Case por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="dab1b-122">To get a reference to the Case cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dab1b-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="dab1b-123">Cell name:</span></span>  <br/> | <span data-ttu-id="dab1b-124">Char.Case[  *i*  ] donde  *i*  = <1>, 2, 3, ...</span><span class="sxs-lookup"><span data-stu-id="dab1b-124">Char.Case[  *i*  ]            where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="dab1b-125">Para obtener una referencia desde un programa a la celda Case por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="dab1b-125">To get a reference to the Case cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dab1b-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="dab1b-126">Section index:</span></span>  <br/> |<span data-ttu-id="dab1b-127">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="dab1b-127">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="dab1b-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="dab1b-128">Row index:</span></span>  <br/> |<span data-ttu-id="dab1b-129">**visRowCharacter**  +   *i* donde *i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="dab1b-129">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="dab1b-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="dab1b-130">Cell index:</span></span>  <br/> |<span data-ttu-id="dab1b-131">**visCharacterCase**</span><span class="sxs-lookup"><span data-stu-id="dab1b-131">**visCharacterCase**</span></span> <br/> |
   

