---
title: Celda LinePattern (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
localization_priority: Normal
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: Determina la trama de línea de la forma. El valor especificado en la celda LinePattern es un número que actúa como índice en una colección de tramas de línea.
ms.openlocfilehash: eec5bed18777f7822f9544d59dce7722f2f732bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416758"
---
# <a name="linepattern-cell-line-format-section"></a><span data-ttu-id="a0402-104">Celda LinePattern (Sección de formato de línea)</span><span class="sxs-lookup"><span data-stu-id="a0402-104">LinePattern Cell (Line Format Section)</span></span>

<span data-ttu-id="a0402-p102">Determina la trama de línea de la forma. El valor especificado en la celda LinePattern es un número que actúa como índice en una colección de tramas de línea.</span><span class="sxs-lookup"><span data-stu-id="a0402-p102">Determines the line pattern of the shape. The value entered in the LinePattern cell is a number that is an index into a collection of line patterns.</span></span>
  
|<span data-ttu-id="a0402-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a0402-107">**Value**</span></span>|<span data-ttu-id="a0402-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a0402-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0402-109">comprendi</span><span class="sxs-lookup"><span data-stu-id="a0402-109">0</span></span>  <br/> |<span data-ttu-id="a0402-110">Sin trama de línea</span><span class="sxs-lookup"><span data-stu-id="a0402-110">No line pattern</span></span>  <br/> |
|<span data-ttu-id="a0402-111">1</span><span class="sxs-lookup"><span data-stu-id="a0402-111">1</span></span>  <br/> |<span data-ttu-id="a0402-112">Sólido</span><span class="sxs-lookup"><span data-stu-id="a0402-112">Solid</span></span>  <br/> |
|<span data-ttu-id="a0402-113">2 -23</span><span class="sxs-lookup"><span data-stu-id="a0402-113">2 - 23</span></span>  <br/> |<span data-ttu-id="a0402-114">Varias tramas de línea</span><span class="sxs-lookup"><span data-stu-id="a0402-114">Assorted line patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0402-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a0402-115">Remarks</span></span>

<span data-ttu-id="a0402-116">Puede ver la colección de tramas de línea en el cuadro de diálogo **Línea** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Línea**, seleccione **Guiones** y, a continuación, haga clic en **Más líneas**).</span><span class="sxs-lookup"><span data-stu-id="a0402-116">You can view the line pattern collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Dashes**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="a0402-117">Puede especificar una trama de línea personalizada si utiliza la función USE en esta celda.</span><span class="sxs-lookup"><span data-stu-id="a0402-117">To specify a custom line pattern, use the USE function in this cell.</span></span>
  
<span data-ttu-id="a0402-118">Para obtener una referencia a la celda LinePattern por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="a0402-118">To get a reference to the LinePattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0402-119">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a0402-119">Cell name:</span></span>  <br/> |<span data-ttu-id="a0402-120">LinePattern</span><span class="sxs-lookup"><span data-stu-id="a0402-120">LinePattern</span></span>  <br/> |
   
<span data-ttu-id="a0402-121">Para obtener una referencia desde un programa a la celda LinePattern por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a0402-121">To get a reference to the LinePattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0402-122">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a0402-122">Section index:</span></span>  <br/> |<span data-ttu-id="a0402-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a0402-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a0402-124">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a0402-124">Row index:</span></span>  <br/> |<span data-ttu-id="a0402-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="a0402-125">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="a0402-126">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a0402-126">Cell index:</span></span>  <br/> |<span data-ttu-id="a0402-127">**visLinePattern**</span><span class="sxs-lookup"><span data-stu-id="a0402-127">**visLinePattern**</span></span> <br/> |
   

