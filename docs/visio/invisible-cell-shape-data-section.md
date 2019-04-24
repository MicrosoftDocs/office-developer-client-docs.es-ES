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
ms.openlocfilehash: 8671fcc249b7ca81c011f697721093e7842c1558
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357270"
---
# <a name="invisible-cell-shape-data-section"></a><span data-ttu-id="6284e-103">Celda Invisible (sección de datos de formas)</span><span class="sxs-lookup"><span data-stu-id="6284e-103">Invisible Cell (Shape Data Section)</span></span>

<span data-ttu-id="6284e-104">Especifica si el elemento de datos de formas es visible en la ventana **Datos de formas**.</span><span class="sxs-lookup"><span data-stu-id="6284e-104">Specifies whether the shape data item is visible in the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="6284e-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="6284e-105">**Value**</span></span>|<span data-ttu-id="6284e-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6284e-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6284e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="6284e-107">TRUE</span></span>  <br/> | <span data-ttu-id="6284e-108">El elemento de datos de formas no está visible.</span><span class="sxs-lookup"><span data-stu-id="6284e-108">Shape data item is not visible.</span></span>  <br/> |
| <span data-ttu-id="6284e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="6284e-109">FALSE</span></span>  <br/> | <span data-ttu-id="6284e-110">El elemento de datos de formas está visible.</span><span class="sxs-lookup"><span data-stu-id="6284e-110">Shape data item is visible.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6284e-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6284e-111">Remarks</span></span>

<span data-ttu-id="6284e-112">El valor de esta celda corresponde a la casilla **Oculto** del cuadro de diálogo **Definir datos de formas** (haga clic con el botón secundario en la forma, seleccione **Datos** y, a continuación, haga clic en **Definir datos de formas**.</span><span class="sxs-lookup"><span data-stu-id="6284e-112">The value in this cell corresponds to the **Hidden** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="6284e-113">Para obtener una referencia a la celda Invisible por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="6284e-113">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6284e-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6284e-114">Cell name:</span></span>  <br/> | <span data-ttu-id="6284e-115">Polyprop.  *nombre* . Invisible donde prop.  *Name* es el nombre de la fila</span><span class="sxs-lookup"><span data-stu-id="6284e-115">Prop.  *name*  .Invisible where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="6284e-116">Para obtener una referencia desde un programa a la celda Invisible por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6284e-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6284e-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6284e-117">Section index:</span></span>  <br/> |<span data-ttu-id="6284e-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="6284e-118">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="6284e-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6284e-119">Row index:</span></span>  <br/> |<span data-ttu-id="6284e-120">**visRowProp** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6284e-120">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6284e-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6284e-121">Cell index:</span></span>  <br/> |<span data-ttu-id="6284e-122">**visCustPropsInvis**</span><span class="sxs-lookup"><span data-stu-id="6284e-122">**visCustPropsInvis**</span></span> <br/> |
   

