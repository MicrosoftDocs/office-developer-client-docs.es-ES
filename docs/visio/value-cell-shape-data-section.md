---
title: Celda Value (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1090
localization_priority: Normal
ms.assetid: fd42a6ce-f621-4e9e-aba3-23a1b87a5651
description: Contiene el valor del elemento de datos de formas tal como se especificó en el cuadro de diálogo Definir datos de formas.
ms.openlocfilehash: 40d9e7fdd92ac8fa800a146ea45bbcd002ace87b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355975"
---
# <a name="value-cell-shape-data-section"></a><span data-ttu-id="1899d-103">Celda Value (Sección de datos de formas)</span><span class="sxs-lookup"><span data-stu-id="1899d-103">Value Cell (Shape Data Section)</span></span>

<span data-ttu-id="1899d-104">Contiene el valor del elemento de datos de formas tal como se especificó en el cuadro de diálogo **Definir datos de formas**.</span><span class="sxs-lookup"><span data-stu-id="1899d-104">Contains the shape data item's value as entered in the **Define Shape Data** dialog box.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1899d-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1899d-105">Remarks</span></span>

<span data-ttu-id="1899d-p101">Los valores especificados en el cuadro de diálogo **Definir datos de formas** reemplazan las fórmulas escritas en esta celda. Esto se cumple aunque se use la función GUARD para proteger la fórmula.</span><span class="sxs-lookup"><span data-stu-id="1899d-p101">Formulas entered in this cell are overridden by values entered in the **Define Shape Data** dialog box. This is true even if you use the GUARD function to protect the formula.</span></span> 
  
<span data-ttu-id="1899d-108">Para obtener una referencia a la celda Value por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="1899d-108">To get a reference to the Value cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1899d-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="1899d-109">Cell name:</span></span>  <br/> | <span data-ttu-id="1899d-110">Polyprop.  *Nombre* . Valor en el que prop.  *Name* es el nombre de la fila</span><span class="sxs-lookup"><span data-stu-id="1899d-110">Prop.  *Name*  .Value where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="1899d-111">Para obtener una referencia desde un programa a la celda Value por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1899d-111">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1899d-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="1899d-112">Section index:</span></span>  <br/> |<span data-ttu-id="1899d-113">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="1899d-113">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="1899d-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="1899d-114">Row index:</span></span>  <br/> |<span data-ttu-id="1899d-115">**visRowProp** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1899d-115">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1899d-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="1899d-116">Cell index:</span></span>  <br/> |<span data-ttu-id="1899d-117">**visCustPropsValue**</span><span class="sxs-lookup"><span data-stu-id="1899d-117">**visCustPropsValue**</span></span> <br/> |
   

