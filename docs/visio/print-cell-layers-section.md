---
title: Celda Print (Sección de capas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
localization_priority: Normal
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: Determina si las formas que pertenecen a la capa pueden imprimirse.
ms.openlocfilehash: f9a1dca6d45b53c02ff0ed29f921c352fc947630
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435218"
---
# <a name="print-cell-layers-section"></a><span data-ttu-id="f2624-103">Celda Print (Sección de capas)</span><span class="sxs-lookup"><span data-stu-id="f2624-103">Print Cell (Layers Section)</span></span>

<span data-ttu-id="f2624-104">Determina si las formas que pertenecen a la capa pueden imprimirse.</span><span class="sxs-lookup"><span data-stu-id="f2624-104">Specifies whether shapes belonging to the layer can be printed.</span></span>
  
|<span data-ttu-id="f2624-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f2624-105">**Value**</span></span>|<span data-ttu-id="f2624-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f2624-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2624-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f2624-107">TRUE</span></span>  <br/> |<span data-ttu-id="f2624-108">Los formas pueden imprimirse.</span><span class="sxs-lookup"><span data-stu-id="f2624-108">Shapes can be printed.</span></span>  <br/> |
|<span data-ttu-id="f2624-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f2624-109">FALSE</span></span>  <br/> |<span data-ttu-id="f2624-110">Las formas no pueden imprimirse.</span><span class="sxs-lookup"><span data-stu-id="f2624-110">Shapes cannot be printed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2624-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f2624-111">Remarks</span></span>

<span data-ttu-id="f2624-112">También puede usar la opción **Imprimir** en el cuadro de diálogo **Propiedades de las capas** para establecer este valor (en la ficha **Inicio**, en el grupo **Edición**, haga clic en **Capas** y, a continuación, en **Propiedades de las capas**).</span><span class="sxs-lookup"><span data-stu-id="f2624-112">You can also set this value by using the **Print** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="f2624-113">Para obtener una referencia a la celda Print por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="f2624-113">To get a reference to the Print cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2624-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f2624-114">Cell name:</span></span>  <br/> |<span data-ttu-id="f2624-115">Layers.Print[ *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f2624-115">Layers.Print[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f2624-116">Para obtener una referencia desde un programa a la celda Print por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f2624-116">To get a reference to the Print cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2624-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f2624-117">Section index:</span></span>  <br/> |<span data-ttu-id="f2624-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="f2624-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="f2624-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f2624-119">Row index:</span></span>  <br/> |<span data-ttu-id="f2624-120">**visRowLayer**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f2624-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="f2624-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f2624-121">Cell index:</span></span>  <br/> |<span data-ttu-id="f2624-122">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="f2624-122">**visDocPreviewScope**</span></span> <br/> |
   

