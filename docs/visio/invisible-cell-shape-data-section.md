---
title: Celda Invisible (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
localization_priority: Normal
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: Especifica si el elemento de datos de formas es visible en la ventana Datos de formas.
ms.openlocfilehash: 2cd3fcad5db7b1752c55055354f1ec842bff4899
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822346"
---
# <a name="invisible-cell-shape-data-section"></a><span data-ttu-id="56a64-103">Celda Invisible (sección Datos de forma)</span><span class="sxs-lookup"><span data-stu-id="56a64-103">Invisible Cell (Shape Data Section)</span></span>

<span data-ttu-id="56a64-104">Especifica si el elemento de datos de formas es visible en la ventana **Datos de formas**.</span><span class="sxs-lookup"><span data-stu-id="56a64-104">Specifies whether the shape data item is visible in the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="56a64-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="56a64-105">**Value**</span></span>|<span data-ttu-id="56a64-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="56a64-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="56a64-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="56a64-107">TRUE</span></span>  <br/> | <span data-ttu-id="56a64-108">El elemento de datos de formas no está visible.</span><span class="sxs-lookup"><span data-stu-id="56a64-108">Shape data item is not visible.</span></span>  <br/> |
| <span data-ttu-id="56a64-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="56a64-109">FALSE</span></span>  <br/> | <span data-ttu-id="56a64-110">El elemento de datos de formas está visible.</span><span class="sxs-lookup"><span data-stu-id="56a64-110">Shape data item is visible.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56a64-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56a64-111">Remarks</span></span>

<span data-ttu-id="56a64-112">El valor de esta celda corresponde a la casilla **Oculto** del cuadro de diálogo **Definir datos de formas** (haga clic con el botón secundario en la forma, seleccione **Datos** y, a continuación, haga clic en **Definir datos de formas**.</span><span class="sxs-lookup"><span data-stu-id="56a64-112">The value in this cell corresponds to the **Hidden** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="56a64-113">Para obtener una referencia a la celda Invisible por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="56a64-113">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56a64-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="56a64-114">Cell name:</span></span>  <br/> | <span data-ttu-id="56a64-115">De propiedades.  *nombre* . Where invisible de propiedades.  *nombre* es el nombre de fila</span><span class="sxs-lookup"><span data-stu-id="56a64-115">Prop.  *name*  .Invisible where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="56a64-116">Para obtener una referencia desde un programa a la celda Invisible por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="56a64-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56a64-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="56a64-117">Section index:</span></span>  <br/> |<span data-ttu-id="56a64-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="56a64-118">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="56a64-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="56a64-119">Row index:</span></span>  <br/> |<span data-ttu-id="56a64-120">**visRowProp** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="56a64-120">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="56a64-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="56a64-121">Cell index:</span></span>  <br/> |<span data-ttu-id="56a64-122">**visCustPropsInvis**</span><span class="sxs-lookup"><span data-stu-id="56a64-122">**visCustPropsInvis**</span></span> <br/> |
   

