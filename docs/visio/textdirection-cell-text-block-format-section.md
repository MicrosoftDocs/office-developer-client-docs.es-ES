---
title: Celda TextDirection (Sección de formato del bloque de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
localization_priority: Normal
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: Determina la dirección de los caracteres de un bloque de texto.
ms.openlocfilehash: 559a2930d9ef62612cabab79ccf55ca2c30e877b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332378"
---
# <a name="textdirection-cell-text-block-format-section"></a><span data-ttu-id="16fcb-103">Celda TextDirection (Sección de formato del bloque de texto)</span><span class="sxs-lookup"><span data-stu-id="16fcb-103">TextDirection Cell (Text Block Format Section)</span></span>

<span data-ttu-id="16fcb-104">Determina la dirección de los caracteres de un bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="16fcb-104">Determines the direction of the characters in a text block.</span></span>
  
|<span data-ttu-id="16fcb-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="16fcb-105">**Value**</span></span>|<span data-ttu-id="16fcb-106">**Direction**</span><span class="sxs-lookup"><span data-stu-id="16fcb-106">**Direction**</span></span>|<span data-ttu-id="16fcb-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="16fcb-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="16fcb-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="16fcb-108">0</span></span>  <br/> | <span data-ttu-id="16fcb-109">Horizontal.</span><span class="sxs-lookup"><span data-stu-id="16fcb-109">Horizontal</span></span>  <br/> |<span data-ttu-id="16fcb-110">**visTxtBlkLeftToRight**</span><span class="sxs-lookup"><span data-stu-id="16fcb-110">**visTxtBlkLeftToRight**</span></span> <br/> |
| <span data-ttu-id="16fcb-111">1</span><span class="sxs-lookup"><span data-stu-id="16fcb-111">1</span></span>  <br/> | <span data-ttu-id="16fcb-112">Vertical</span><span class="sxs-lookup"><span data-stu-id="16fcb-112">Vertical</span></span>  <br/> |<span data-ttu-id="16fcb-113">**visTxtBlkTopToBottom**</span><span class="sxs-lookup"><span data-stu-id="16fcb-113">**visTxtBlkTopToBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16fcb-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="16fcb-114">Remarks</span></span>

<span data-ttu-id="16fcb-115">En los productos Visio versión 5.0 en japonés, el valor de esta celda se almacenaba en la celda VerticalText de la sección de varios.</span><span class="sxs-lookup"><span data-stu-id="16fcb-115">In Visio version 5.0 Japanese products, the value of this cell was stored in the VerticalText cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="16fcb-116">Para obtener una referencia a la celda TextDirection por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="16fcb-116">To get a reference to the TextDirection cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16fcb-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="16fcb-117">Cell name:</span></span>  <br/> | <span data-ttu-id="16fcb-118">TextDirection</span><span class="sxs-lookup"><span data-stu-id="16fcb-118">TextDirection</span></span>  <br/> |
   
<span data-ttu-id="16fcb-119">Para obtener una referencia desde un programa a la celda TextDirection por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="16fcb-119">To get a reference to the TextDirection cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16fcb-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="16fcb-120">Section index:</span></span>  <br/> |<span data-ttu-id="16fcb-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="16fcb-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="16fcb-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="16fcb-122">Row index:</span></span>  <br/> |<span data-ttu-id="16fcb-123">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="16fcb-123">**visRowText**</span></span> <br/> |
| <span data-ttu-id="16fcb-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="16fcb-124">Cell index:</span></span>  <br/> |<span data-ttu-id="16fcb-125">**visTxtBlkDirection**</span><span class="sxs-lookup"><span data-stu-id="16fcb-125">**visTxtBlkDirection**</span></span> <br/> |
   

