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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406230"
---
# <a name="textdirection-cell-text-block-format-section"></a><span data-ttu-id="08dba-103">Celda TextDirection (Sección de formato del bloque de texto)</span><span class="sxs-lookup"><span data-stu-id="08dba-103">TextDirection Cell (Text Block Format Section)</span></span>

<span data-ttu-id="08dba-104">Determina la dirección de los caracteres de un bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="08dba-104">Determines the direction of the characters in a text block.</span></span>
  
|<span data-ttu-id="08dba-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="08dba-105">**Value**</span></span>|<span data-ttu-id="08dba-106">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="08dba-106">**Direction**</span></span>|<span data-ttu-id="08dba-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="08dba-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="08dba-108">0</span><span class="sxs-lookup"><span data-stu-id="08dba-108">0</span></span>  <br/> | <span data-ttu-id="08dba-109">Horizontal.</span><span class="sxs-lookup"><span data-stu-id="08dba-109">Horizontal</span></span>  <br/> |<span data-ttu-id="08dba-110">**visTxtBlkLeftToRight**</span><span class="sxs-lookup"><span data-stu-id="08dba-110">**visTxtBlkLeftToRight**</span></span> <br/> |
| <span data-ttu-id="08dba-111">1 </span><span class="sxs-lookup"><span data-stu-id="08dba-111">1</span></span>  <br/> | <span data-ttu-id="08dba-112">Vertical</span><span class="sxs-lookup"><span data-stu-id="08dba-112">Vertical</span></span>  <br/> |<span data-ttu-id="08dba-113">**visTxtBlkTopToBottom**</span><span class="sxs-lookup"><span data-stu-id="08dba-113">**visTxtBlkTopToBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08dba-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="08dba-114">Remarks</span></span>

<span data-ttu-id="08dba-115">En los productos Visio versión 5.0 en japonés, el valor de esta celda se almacenaba en la celda VerticalText de la sección de varios.</span><span class="sxs-lookup"><span data-stu-id="08dba-115">In Visio version 5.0 Japanese products, the value of this cell was stored in the VerticalText cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="08dba-116">Para obtener una referencia a la celda TextDirection por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="08dba-116">To get a reference to the TextDirection cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="08dba-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="08dba-117">Cell name:</span></span>  <br/> | <span data-ttu-id="08dba-118">TextDirection</span><span class="sxs-lookup"><span data-stu-id="08dba-118">TextDirection</span></span>  <br/> |
   
<span data-ttu-id="08dba-119">Para obtener una referencia desde un programa a la celda TextDirection por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="08dba-119">To get a reference to the TextDirection cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="08dba-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="08dba-120">Section index:</span></span>  <br/> |<span data-ttu-id="08dba-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="08dba-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="08dba-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="08dba-122">Row index:</span></span>  <br/> |<span data-ttu-id="08dba-123">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="08dba-123">**visRowText**</span></span> <br/> |
| <span data-ttu-id="08dba-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="08dba-124">Cell index:</span></span>  <br/> |<span data-ttu-id="08dba-125">**visTxtBlkDirection**</span><span class="sxs-lookup"><span data-stu-id="08dba-125">**visTxtBlkDirection**</span></span> <br/> |
   

