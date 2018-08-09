---
title: Celda Strikethru (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm975
localization_priority: Normal
ms.assetid: b03b4415-0b1a-eb03-2b5e-373b39a0f07a
description: Determina si el texto tiene el formato tachado.
ms.openlocfilehash: 2b25d1d9b00d062214c02c3fc7b14569b43a5110
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823339"
---
# <a name="strikethru-cell-character-section"></a><span data-ttu-id="5ea5d-103">Celda Strikethru (sección Caracteres)</span><span class="sxs-lookup"><span data-stu-id="5ea5d-103">Strikethru Cell (Character Section)</span></span>

<span data-ttu-id="5ea5d-104">Determina si el texto tiene el formato tachado.</span><span class="sxs-lookup"><span data-stu-id="5ea5d-104">Determines whether the text is formatted as strikethrough.</span></span>
  
|<span data-ttu-id="5ea5d-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5ea5d-105">**Value**</span></span>|<span data-ttu-id="5ea5d-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5ea5d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5ea5d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5ea5d-107">TRUE</span></span>  <br/> |<span data-ttu-id="5ea5d-108">El texto tiene el formato tachado.</span><span class="sxs-lookup"><span data-stu-id="5ea5d-108">Text is formatted as strikethrough.</span></span>  <br/> |
|<span data-ttu-id="5ea5d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5ea5d-109">FALSE</span></span>  <br/> |<span data-ttu-id="5ea5d-110">El texto no tiene el formato tachado.</span><span class="sxs-lookup"><span data-stu-id="5ea5d-110">Text is not formatted as strikethrough.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ea5d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ea5d-111">Remarks</span></span>

<span data-ttu-id="5ea5d-112">También puede usar el cuadro de diálogo **Texto** para establecer el valor de esta celda (en la ficha **Inicio**, haga clic en la flecha de **Fuente**).</span><span class="sxs-lookup"><span data-stu-id="5ea5d-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="5ea5d-113">Para obtener una referencia a la celda Strikethru por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="5ea5d-113">To get a reference to the Strikethru cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5ea5d-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5ea5d-114">Cell name:</span></span>  <br/> |<span data-ttu-id="5ea5d-115">Char.Strikethru [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5ea5d-115">Char.Strikethru[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5ea5d-116">Para obtener una referencia desde un programa a la celda Strikethru por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5ea5d-116">To get a reference to the Strikethru cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5ea5d-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5ea5d-117">Section index:</span></span>  <br/> |<span data-ttu-id="5ea5d-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="5ea5d-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="5ea5d-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5ea5d-119">Row index:</span></span>  <br/> |<span data-ttu-id="5ea5d-120">**visRowCharacter** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5ea5d-120">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="5ea5d-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5ea5d-121">Cell index:</span></span>  <br/> |<span data-ttu-id="5ea5d-122">**visCharacterStrikethru**</span><span class="sxs-lookup"><span data-stu-id="5ea5d-122">**visCharacterStrikethru**</span></span> <br/> |
   

