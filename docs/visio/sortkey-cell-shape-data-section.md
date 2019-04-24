---
title: Celda SortKey (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251345
localization_priority: Normal
ms.assetid: 67fa5389-f0b9-a9db-8d19-9b16e256dfa3
description: Da como resultado una cadena que influye en el orden en el que se presentan los elementos en la ventana Datos de formas.
ms.openlocfilehash: d166ea18a36f6a4101b8933fce804be2243954bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335185"
---
# <a name="sortkey-cell-shape-data-section"></a><span data-ttu-id="ab4d1-103">Celda SortKey (Sección de datos de formas)</span><span class="sxs-lookup"><span data-stu-id="ab4d1-103">SortKey Cell (Shape Data Section)</span></span>

<span data-ttu-id="ab4d1-104">Da como resultado una cadena que influye en el orden en el que se presentan los elementos en la ventana **Datos de formas**.</span><span class="sxs-lookup"><span data-stu-id="ab4d1-104">Evaluates to a string that influences the order in which items in the **Shape Data** window are listed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ab4d1-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ab4d1-105">Remarks</span></span>

<span data-ttu-id="ab4d1-106">El cálculo que se utiliza para comparar los valores de SortKey depende de la configuración regional y no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ab4d1-106">The calculation used to compare SortKey values is locale-specific and case insensitive.</span></span> <span data-ttu-id="ab4d1-107">Si los valores de SortKey son iguales, los datos de formas aparecen según el orden de las filas.</span><span class="sxs-lookup"><span data-stu-id="ab4d1-107">If SortKey values are equal, the shape data is listed in row order.</span></span> <span data-ttu-id="ab4d1-108">Los datos de formas que no tienen ningún criterio de ordenación se muestran después de los datos de forma que contienen un criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="ab4d1-108">Shape data that have no sort key are listed after shape data that contain a sort key.</span></span>
  
<span data-ttu-id="ab4d1-109">El siguiente es un ejemplo del uso de claves de orden para mostrar los datos de formas en la ventana **Datos de formas** según el orden: Número de artículo, Cantidad, Precio.</span><span class="sxs-lookup"><span data-stu-id="ab4d1-109">Following is an example of using sort keys to display the shape data in the **Shape Data** window in the order: Item Number, Quantity, Price.</span></span> 
  
 <span data-ttu-id="ab4d1-110">*Row, Label* y *SortKey* hacen referencia a celdas de la fila de datos de formas.</span><span class="sxs-lookup"><span data-stu-id="ab4d1-110">*Row, Label,*  and  *SortKey*  refer to cells in the shape data row.</span></span> <span data-ttu-id="ab4d1-111">En este caso se ha asignado un nombre a las filas de datos de formas.</span><span class="sxs-lookup"><span data-stu-id="ab4d1-111">In this case, the shape data rows have been named.</span></span> 
  
|<span data-ttu-id="ab4d1-112">**Fila**</span><span class="sxs-lookup"><span data-stu-id="ab4d1-112">**Row**</span></span>|<span data-ttu-id="ab4d1-113">**Label**</span><span class="sxs-lookup"><span data-stu-id="ab4d1-113">**Label**</span></span>|<span data-ttu-id="ab4d1-114">**Criterio**</span><span class="sxs-lookup"><span data-stu-id="ab4d1-114">**SortKey**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ab4d1-115">Prop. Item</span><span class="sxs-lookup"><span data-stu-id="ab4d1-115">Prop.Item</span></span>  <br/> | <span data-ttu-id="ab4d1-116">Número de elemento</span><span class="sxs-lookup"><span data-stu-id="ab4d1-116">Item Number</span></span>  <br/> | <span data-ttu-id="ab4d1-117">1</span><span class="sxs-lookup"><span data-stu-id="ab4d1-117">1</span></span>  <br/> |
| <span data-ttu-id="ab4d1-118">Prop. Price</span><span class="sxs-lookup"><span data-stu-id="ab4d1-118">Prop.Price</span></span>  <br/> | <span data-ttu-id="ab4d1-119">Precio</span><span class="sxs-lookup"><span data-stu-id="ab4d1-119">Price</span></span>  <br/> | <span data-ttu-id="ab4d1-120">3</span><span class="sxs-lookup"><span data-stu-id="ab4d1-120">3</span></span>  <br/> |
| <span data-ttu-id="ab4d1-121">Prop. Quan</span><span class="sxs-lookup"><span data-stu-id="ab4d1-121">Prop.Quan</span></span>  <br/> | <span data-ttu-id="ab4d1-122">Cantidad</span><span class="sxs-lookup"><span data-stu-id="ab4d1-122">Quantity</span></span>  <br/> | <span data-ttu-id="ab4d1-123">segundo</span><span class="sxs-lookup"><span data-stu-id="ab4d1-123">2</span></span>  <br/> |
   
<span data-ttu-id="ab4d1-124">Para obtener una referencia a la celda SortKey por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="ab4d1-124">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ab4d1-125">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="ab4d1-125">Cell name:</span></span>  <br/> | <span data-ttu-id="ab4d1-126">Polyprop.  *Nombre* . SortKey donde prop.  *Nombre* es el nombre de la fila de propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="ab4d1-126">Prop.  *Name*  .SortKey where Prop.  *Name*  is the name of the custom property row</span></span>  <br/> |
   
<span data-ttu-id="ab4d1-127">Para obtener una referencia desde un programa a la celda SortKey por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ab4d1-127">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ab4d1-128">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="ab4d1-128">Section index:</span></span>  <br/> |<span data-ttu-id="ab4d1-129">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="ab4d1-129">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="ab4d1-130">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="ab4d1-130">Row index:</span></span>  <br/> |<span data-ttu-id="ab4d1-131">**visRowProp** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ab4d1-131">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ab4d1-132">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="ab4d1-132">Cell index:</span></span>  <br/> |<span data-ttu-id="ab4d1-133">**visCustPropsSortKey**</span><span class="sxs-lookup"><span data-stu-id="ab4d1-133">**visCustPropsSortKey**</span></span> <br/> |
   

