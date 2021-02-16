---
title: Celda DoubleStrikethrough (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033762
localization_priority: Normal
ms.assetid: c48a77e1-ea3c-7a6d-8c05-f9e0cb434cda
description: Determina si el texto tiene formato de doble tachado.
ms.openlocfilehash: d8ef5bdb6e086be9657f51c66c10d578414e1deb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360595"
---
# <a name="doublestrikethrough-cell-character-section"></a><span data-ttu-id="b5681-103">Celda DoubleStrikethrough (Sección de caracteres)</span><span class="sxs-lookup"><span data-stu-id="b5681-103">DoubleStrikethrough Cell (Character Section)</span></span>

<span data-ttu-id="b5681-104">Determina si el texto tiene formato de doble tachado.</span><span class="sxs-lookup"><span data-stu-id="b5681-104">Determines whether text is formatted as double strikethrough.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5681-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b5681-105">Remarks</span></span>

<span data-ttu-id="b5681-106">Para obtener una referencia a la celda DoubleStrikethrough por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b5681-106">To get a reference to the DoubleStrikethrough cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b5681-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b5681-107">Cell name:</span></span>  <br/> | <span data-ttu-id="b5681-108">Char.DoubleStrikethrough[  *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b5681-108">Char.DoubleStrikethrough[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b5681-109">Para obtener una referencia desde un programa a la celda DoubleStrikethrough por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b5681-109">To get a reference to the DoubleStrikethrough cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b5681-110">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b5681-110">Section index:</span></span>  <br/> |<span data-ttu-id="b5681-111">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="b5681-111">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="b5681-112">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b5681-112">Row index:</span></span>  <br/> |<span data-ttu-id="b5681-113">**visRowCharacter**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b5681-113">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b5681-114">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b5681-114">Cell index:</span></span>  <br/> |<span data-ttu-id="b5681-115">**visCharacterDoubleStrikethrough**</span><span class="sxs-lookup"><span data-stu-id="b5681-115">**visCharacterDoubleStrikethrough**</span></span> <br/> |
   

