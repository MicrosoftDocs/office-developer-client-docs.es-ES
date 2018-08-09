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
ms.openlocfilehash: 9acd786b6fa38aec42990f1fd942174367f1135e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821701"
---
# <a name="case-cell-character-section"></a><span data-ttu-id="cc23e-105">Celda Case (sección Caracteres)</span><span class="sxs-lookup"><span data-stu-id="cc23e-105">Case Cell (Character Section)</span></span>

<span data-ttu-id="cc23e-p102">Determina el uso de mayúsculas y minúsculas en el texto de una forma. Las opciones de todas las letras en mayúsculas (1) y mayúsculas iniciales (2) no cambian la apariencia del texto escrito totalmente en mayúsculas. El texto debe estar en minúsculas para que estas opciones surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="cc23e-p102">Determines the case of a shape's text. All capital (uppercase) letters (1) and initial capital letters (2) do not change the appearance of text that was entered in all capital letters. The text must be entered in lowercase letters for these options to show an effect.</span></span>
  
|<span data-ttu-id="cc23e-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cc23e-109">**Value**</span></span>|<span data-ttu-id="cc23e-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc23e-110">**Description**</span></span>|<span data-ttu-id="cc23e-111">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="cc23e-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="cc23e-112">0</span><span class="sxs-lookup"><span data-stu-id="cc23e-112">0</span></span>  <br/> | <span data-ttu-id="cc23e-113">Uso normal de mayúsculas y minúsculas</span><span class="sxs-lookup"><span data-stu-id="cc23e-113">Normal case</span></span>  <br/> |<span data-ttu-id="cc23e-114">**visCaseNormal**</span><span class="sxs-lookup"><span data-stu-id="cc23e-114">**visCaseNormal**</span></span> <br/> |
| <span data-ttu-id="cc23e-115">1</span><span class="sxs-lookup"><span data-stu-id="cc23e-115">1</span></span>  <br/> | <span data-ttu-id="cc23e-116">Todo en mayúsculas</span><span class="sxs-lookup"><span data-stu-id="cc23e-116">All capital (uppercase) letters</span></span>  <br/> |<span data-ttu-id="cc23e-117">**visCaseAllCaps**</span><span class="sxs-lookup"><span data-stu-id="cc23e-117">**visCaseAllCaps**</span></span> <br/> |
| <span data-ttu-id="cc23e-118">2</span><span class="sxs-lookup"><span data-stu-id="cc23e-118">2</span></span>  <br/> | <span data-ttu-id="cc23e-119">Sólo las letras iniciales en mayúsculas</span><span class="sxs-lookup"><span data-stu-id="cc23e-119">Initial capital letters only</span></span>  <br/> |<span data-ttu-id="cc23e-120">**visCaseInitialCaps**</span><span class="sxs-lookup"><span data-stu-id="cc23e-120">**visCaseInitialCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc23e-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc23e-121">Remarks</span></span>

<span data-ttu-id="cc23e-122">Para obtener una referencia a la celda Case por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="cc23e-122">To get a reference to the Case cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cc23e-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="cc23e-123">Cell name:</span></span>  <br/> | <span data-ttu-id="cc23e-124">Char.Case [ *i* ] donde *i* = < 1 >, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="cc23e-124">Char.Case[  *i*  ]            where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="cc23e-125">Para obtener una referencia desde un programa a la celda Case por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="cc23e-125">To get a reference to the Case cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cc23e-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="cc23e-126">Section index:</span></span>  <br/> |<span data-ttu-id="cc23e-127">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="cc23e-127">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="cc23e-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="cc23e-128">Row index:</span></span>  <br/> |<span data-ttu-id="cc23e-129">**visRowCharacter** +  *i* donde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="cc23e-129">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="cc23e-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="cc23e-130">Cell index:</span></span>  <br/> |<span data-ttu-id="cc23e-131">**visCharacterCase**</span><span class="sxs-lookup"><span data-stu-id="cc23e-131">**visCharacterCase**</span></span> <br/> |
   

