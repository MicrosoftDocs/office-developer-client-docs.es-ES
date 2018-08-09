---
title: Celda Font (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
localization_priority: Normal
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: Representa el número de la fuente empleada para dar formato al texto. Los números de fuente varían de acuerdo con las fuentes que tenga instaladas en el sistema. El número 0 representa la fuente predeterminada, que suele ser Arial.
ms.openlocfilehash: cbbf2a2400c995e0cbc217c1161fbd18f7459b28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822164"
---
# <a name="font-cell-character-section"></a><span data-ttu-id="1a049-105">Celda Font (sección Caracteres)</span><span class="sxs-lookup"><span data-stu-id="1a049-105">Font Cell (Character Section)</span></span>

<span data-ttu-id="1a049-p102">Representa el número de la fuente empleada para dar formato al texto. Los números de fuente varían de acuerdo con las fuentes que tenga instaladas en el sistema. El número 0 representa la fuente predeterminada, que suele ser Arial.</span><span class="sxs-lookup"><span data-stu-id="1a049-p102">Represents the number of the font used to format the text. Font numbers vary according to the fonts installed on your system. The number 0 represents the default font, which is typically Arial.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1a049-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1a049-109">Remarks</span></span>

<span data-ttu-id="1a049-110">Para obtener una referencia a la celda Font por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="1a049-110">To get a reference to the Font cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1a049-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="1a049-111">Cell name:</span></span>  <br/> | <span data-ttu-id="1a049-112">Char.Font [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1a049-112">Char.Font[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="1a049-113">Para obtener una referencia desde un programa a la celda Font por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1a049-113">To get a reference to the Font cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1a049-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="1a049-114">Section index:</span></span>  <br/> |<span data-ttu-id="1a049-115">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="1a049-115">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="1a049-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="1a049-116">Row index:</span></span>  <br/> |<span data-ttu-id="1a049-117">**visRowCharacter** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1a049-117">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1a049-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="1a049-118">Cell index:</span></span>  <br/> |<span data-ttu-id="1a049-119">**visCharacterFont**</span><span class="sxs-lookup"><span data-stu-id="1a049-119">**visCharacterFont**</span></span> <br/> |
   

