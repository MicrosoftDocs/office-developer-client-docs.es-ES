---
title: Celda Pos (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm805
localization_priority: Normal
ms.assetid: c02186ce-6a20-fbe7-588d-d64c3ea4dec4
description: Determina la posición del texto de la forma con respecto a la línea base.
ms.openlocfilehash: d5f6823d6f55493095d29054745f62b579a47893
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414021"
---
# <a name="pos-cell-character-section"></a><span data-ttu-id="35b38-103">Celda Pos (Sección de caracteres)</span><span class="sxs-lookup"><span data-stu-id="35b38-103">Pos Cell (Character Section)</span></span>

<span data-ttu-id="35b38-104">Determina la posición del texto de la forma con respecto a la línea base.</span><span class="sxs-lookup"><span data-stu-id="35b38-104">Determines the position of the shape's text relative to the baseline.</span></span>
  
|<span data-ttu-id="35b38-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="35b38-105">**Value**</span></span>|<span data-ttu-id="35b38-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="35b38-106">**Description**</span></span>|<span data-ttu-id="35b38-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="35b38-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="35b38-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="35b38-108">0</span></span>  <br/> | <span data-ttu-id="35b38-109">Posición normal</span><span class="sxs-lookup"><span data-stu-id="35b38-109">Normal position</span></span>  <br/> |<span data-ttu-id="35b38-110">**visPosNormal**</span><span class="sxs-lookup"><span data-stu-id="35b38-110">**visPosNormal**</span></span> <br/> |
| <span data-ttu-id="35b38-111">1</span><span class="sxs-lookup"><span data-stu-id="35b38-111">1</span></span>  <br/> | <span data-ttu-id="35b38-112">Superíndice</span><span class="sxs-lookup"><span data-stu-id="35b38-112">Superscript</span></span>  <br/> |<span data-ttu-id="35b38-113">**visPosSuper**</span><span class="sxs-lookup"><span data-stu-id="35b38-113">**visPosSuper**</span></span> <br/> |
| <span data-ttu-id="35b38-114">segundo</span><span class="sxs-lookup"><span data-stu-id="35b38-114">2</span></span>  <br/> | <span data-ttu-id="35b38-115">Subíndice</span><span class="sxs-lookup"><span data-stu-id="35b38-115">Subscript</span></span>  <br/> |<span data-ttu-id="35b38-116">**visPosSub**</span><span class="sxs-lookup"><span data-stu-id="35b38-116">**visPosSub**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35b38-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="35b38-117">Remarks</span></span>

<span data-ttu-id="35b38-118">Para obtener una referencia a la celda Pos por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="35b38-118">To get a reference to the Pos cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="35b38-119">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="35b38-119">Cell name:</span></span>  <br/> | <span data-ttu-id="35b38-120">Char. pos [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="35b38-120">Char.Pos[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="35b38-121">Para obtener una referencia desde un programa a la celda Pos por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="35b38-121">To get a reference to the Pos cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="35b38-122">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="35b38-122">Section index:</span></span>  <br/> |<span data-ttu-id="35b38-123">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="35b38-123">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="35b38-124">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="35b38-124">Row index:</span></span>  <br/> |<span data-ttu-id="35b38-125">**visRowCharacter** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="35b38-125">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="35b38-126">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="35b38-126">Cell index:</span></span>  <br/> |<span data-ttu-id="35b38-127">**visCharacterPos**</span><span class="sxs-lookup"><span data-stu-id="35b38-127">**visCharacterPos**</span></span> <br/> |
   

