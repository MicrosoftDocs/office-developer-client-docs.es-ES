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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417857"
---
# <a name="sortkey-cell-shape-data-section"></a><span data-ttu-id="10def-103">Celda SortKey (Sección de datos de formas)</span><span class="sxs-lookup"><span data-stu-id="10def-103">SortKey Cell (Shape Data Section)</span></span>

<span data-ttu-id="10def-104">Da como resultado una cadena que influye en el orden en el que se presentan los elementos en la ventana **Datos de formas**.</span><span class="sxs-lookup"><span data-stu-id="10def-104">Evaluates to a string that influences the order in which items in the **Shape Data** window are listed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="10def-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="10def-105">Remarks</span></span>

<span data-ttu-id="10def-106">El cálculo que se utiliza para comparar los valores de SortKey depende de la configuración regional y no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="10def-106">The calculation used to compare SortKey values is locale-specific and case insensitive.</span></span> <span data-ttu-id="10def-107">Si los valores de SortKey son iguales, los datos de formas aparecen según el orden de las filas.</span><span class="sxs-lookup"><span data-stu-id="10def-107">If SortKey values are equal, the shape data is listed in row order.</span></span> <span data-ttu-id="10def-108">Los datos de formas que no tienen clave de ordenación se enumeran después de los datos de formas que contienen una clave de ordenación.</span><span class="sxs-lookup"><span data-stu-id="10def-108">Shape data that have no sort key are listed after shape data that contain a sort key.</span></span>
  
<span data-ttu-id="10def-109">El siguiente es un ejemplo del uso de claves de orden para mostrar los datos de formas en la ventana **Datos de formas** según el orden: Número de artículo, Cantidad, Precio.</span><span class="sxs-lookup"><span data-stu-id="10def-109">Following is an example of using sort keys to display the shape data in the **Shape Data** window in the order: Item Number, Quantity, Price.</span></span> 
  
 <span data-ttu-id="10def-110">*Row, Label y*  *SortKey*  hacen referencia a las celdas de la fila de datos de formas.</span><span class="sxs-lookup"><span data-stu-id="10def-110">*Row, Label,*  and  *SortKey*  refer to cells in the shape data row.</span></span> <span data-ttu-id="10def-111">En este caso se ha asignado un nombre a las filas de datos de formas.</span><span class="sxs-lookup"><span data-stu-id="10def-111">In this case, the shape data rows have been named.</span></span> 
  
|<span data-ttu-id="10def-112">**Fila**</span><span class="sxs-lookup"><span data-stu-id="10def-112">**Row**</span></span>|<span data-ttu-id="10def-113">**Label**</span><span class="sxs-lookup"><span data-stu-id="10def-113">**Label**</span></span>|<span data-ttu-id="10def-114">**SortKey**</span><span class="sxs-lookup"><span data-stu-id="10def-114">**SortKey**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="10def-115">Prop.Item</span><span class="sxs-lookup"><span data-stu-id="10def-115">Prop.Item</span></span>  <br/> | <span data-ttu-id="10def-116">Número de elemento</span><span class="sxs-lookup"><span data-stu-id="10def-116">Item Number</span></span>  <br/> | <span data-ttu-id="10def-117">1 </span><span class="sxs-lookup"><span data-stu-id="10def-117">1</span></span>  <br/> |
| <span data-ttu-id="10def-118">Prop.Price</span><span class="sxs-lookup"><span data-stu-id="10def-118">Prop.Price</span></span>  <br/> | <span data-ttu-id="10def-119">Precio</span><span class="sxs-lookup"><span data-stu-id="10def-119">Price</span></span>  <br/> | <span data-ttu-id="10def-120">3 </span><span class="sxs-lookup"><span data-stu-id="10def-120">3</span></span>  <br/> |
| <span data-ttu-id="10def-121">Prop.Quan</span><span class="sxs-lookup"><span data-stu-id="10def-121">Prop.Quan</span></span>  <br/> | <span data-ttu-id="10def-122">Cantidad</span><span class="sxs-lookup"><span data-stu-id="10def-122">Quantity</span></span>  <br/> | <span data-ttu-id="10def-123">2 </span><span class="sxs-lookup"><span data-stu-id="10def-123">2</span></span>  <br/> |
   
<span data-ttu-id="10def-124">Para obtener una referencia a la celda SortKey por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="10def-124">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="10def-125">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="10def-125">Cell name:</span></span>  <br/> | <span data-ttu-id="10def-126">Prop.  *Nombre*  . SortKey donde Prop.  *El*  nombre es el nombre de la fila de propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="10def-126">Prop.  *Name*  .SortKey where Prop.  *Name*  is the name of the custom property row</span></span>  <br/> |
   
<span data-ttu-id="10def-127">Para obtener una referencia desde un programa a la celda SortKey por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="10def-127">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="10def-128">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="10def-128">Section index:</span></span>  <br/> |<span data-ttu-id="10def-129">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="10def-129">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="10def-130">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="10def-130">Row index:</span></span>  <br/> |<span data-ttu-id="10def-131">**visRowProp**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="10def-131">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="10def-132">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="10def-132">Cell index:</span></span>  <br/> |<span data-ttu-id="10def-133">**visCustPropsSortKey**</span><span class="sxs-lookup"><span data-stu-id="10def-133">**visCustPropsSortKey**</span></span> <br/> |
   

