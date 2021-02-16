---
title: Celda Overline (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
localization_priority: Normal
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: Determina si el texto tiene una línea encima.
ms.openlocfilehash: d5df39c2f12890d5fb4881346516abdb4f2b8099
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431648"
---
# <a name="overline-cell-character-section"></a><span data-ttu-id="29cf1-103">Celda Overline (Sección de caracteres)</span><span class="sxs-lookup"><span data-stu-id="29cf1-103">Overline Cell (Character Section)</span></span>

<span data-ttu-id="29cf1-104">Determina si el texto tiene una línea encima.</span><span class="sxs-lookup"><span data-stu-id="29cf1-104">Determines whether the text has a line above it.</span></span>
  
|<span data-ttu-id="29cf1-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="29cf1-105">**Value**</span></span>|<span data-ttu-id="29cf1-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="29cf1-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="29cf1-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="29cf1-107">TRUE</span></span>  <br/> |<span data-ttu-id="29cf1-108">El texto tiene una línea encima.</span><span class="sxs-lookup"><span data-stu-id="29cf1-108">Text has a line above it.</span></span>  <br/> |
|<span data-ttu-id="29cf1-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="29cf1-109">FALSE</span></span>  <br/> |<span data-ttu-id="29cf1-110">El texto no tiene una línea encima.</span><span class="sxs-lookup"><span data-stu-id="29cf1-110">Text does not have a line above it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29cf1-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="29cf1-111">Remarks</span></span>

<span data-ttu-id="29cf1-112">También puede usar el cuadro de diálogo **Texto** para establecer el valor de esta celda (en la ficha **Inicio**, haga clic en la flecha de **Fuente**).</span><span class="sxs-lookup"><span data-stu-id="29cf1-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="29cf1-113">Para obtener una referencia a la celda Overline por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="29cf1-113">To get a reference to the Overline cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29cf1-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="29cf1-114">Cell name:</span></span>  <br/> |<span data-ttu-id="29cf1-115">Char.Overline[ *i*  ] donde  *i*  = <1>, 2.</span><span class="sxs-lookup"><span data-stu-id="29cf1-115">Char.Overline[ *i*  ] where  *i*  = <1>, 2.</span></span> <span data-ttu-id="29cf1-116">3...</span><span class="sxs-lookup"><span data-stu-id="29cf1-116">3...</span></span>  <br/> |
   
<span data-ttu-id="29cf1-117">Para obtener una referencia desde un programa a la celda Overline por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="29cf1-117">To get a reference to the Overline cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29cf1-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="29cf1-118">Section index:</span></span>  <br/> |<span data-ttu-id="29cf1-119">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="29cf1-119">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="29cf1-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="29cf1-120">Row index:</span></span>  <br/> |<span data-ttu-id="29cf1-121">**visRowCharacter**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="29cf1-121">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="29cf1-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="29cf1-122">Cell index:</span></span>  <br/> |<span data-ttu-id="29cf1-123">**visCharacterOverline**</span><span class="sxs-lookup"><span data-stu-id="29cf1-123">**visCharacterOverline**</span></span> <br/> |
   

