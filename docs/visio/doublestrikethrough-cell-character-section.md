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
ms.openlocfilehash: dcd7c7769da8298c1f6ab474d2b63fc982f479b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822032"
---
# <a name="doublestrikethrough-cell-character-section"></a><span data-ttu-id="b5b17-103">Celda DoubleStrikethrough (sección Caracteres)</span><span class="sxs-lookup"><span data-stu-id="b5b17-103">DoubleStrikethrough Cell (Character Section)</span></span>

<span data-ttu-id="b5b17-104">Determina si el texto tiene formato de doble tachado.</span><span class="sxs-lookup"><span data-stu-id="b5b17-104">Determines whether text is formatted as double strikethrough.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5b17-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b5b17-105">Remarks</span></span>

<span data-ttu-id="b5b17-106">Para obtener una referencia a la celda DoubleStrikethrough por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b5b17-106">To get a reference to the DoubleStrikethrough cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b5b17-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b5b17-107">Cell name:</span></span>  <br/> | <span data-ttu-id="b5b17-108">Char.DoubleStrikethrough [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b5b17-108">Char.DoubleStrikethrough[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b5b17-109">Para obtener una referencia desde un programa a la celda DoubleStrikethrough por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b5b17-109">To get a reference to the DoubleStrikethrough cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b5b17-110">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b5b17-110">Section index:</span></span>  <br/> |<span data-ttu-id="b5b17-111">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="b5b17-111">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="b5b17-112">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b5b17-112">Row index:</span></span>  <br/> |<span data-ttu-id="b5b17-113">**visRowCharacter** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b5b17-113">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b5b17-114">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b5b17-114">Cell index:</span></span>  <br/> |<span data-ttu-id="b5b17-115">**visCharacterDoubleStrikethrough**</span><span class="sxs-lookup"><span data-stu-id="b5b17-115">**visCharacterDoubleStrikethrough**</span></span> <br/> |
   

