---
title: Celda Type (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1055
localization_priority: Normal
ms.assetid: 1e24a906-83ce-32d2-5d7b-ba6dd6eea2d3
description: Especifica un tipo de datos para el valor de los datos de formas.
ms.openlocfilehash: c2d38b521a8597a4582a4145ad808b0c0e26ff0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406251"
---
# <a name="type-cell-shape-data-section"></a><span data-ttu-id="ca3af-103">Celda Type (Sección de datos de formas)</span><span class="sxs-lookup"><span data-stu-id="ca3af-103">Type Cell (Shape Data Section)</span></span>

<span data-ttu-id="ca3af-104">Especifica un tipo de datos para el valor de los datos de formas.</span><span class="sxs-lookup"><span data-stu-id="ca3af-104">Specifies a data type for the shape data value.</span></span>
  
|<span data-ttu-id="ca3af-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ca3af-105">**Value**</span></span>|<span data-ttu-id="ca3af-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ca3af-106">**Description**</span></span>|<span data-ttu-id="ca3af-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="ca3af-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ca3af-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="ca3af-108">0</span></span>  <br/> |<span data-ttu-id="ca3af-p101">Cadena. Éste es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ca3af-p101">String. This is the default.</span></span>  <br/> |<span data-ttu-id="ca3af-111">**visPropTypeString**</span><span class="sxs-lookup"><span data-stu-id="ca3af-111">**visPropTypeString**</span></span> <br/> |
|<span data-ttu-id="ca3af-112">1</span><span class="sxs-lookup"><span data-stu-id="ca3af-112">1</span></span>  <br/> |<span data-ttu-id="ca3af-p102">Lista fija. Muestra los elementos de la lista en un cuadro combinado desplegable en el cuadro de diálogo **Definir datos de formas**. Especifique los elementos de la lista en la celda Format. Los usuarios solo pueden seleccionar un elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="ca3af-p102">Fixed list. Displays the list items in a drop-down combo box in the **Define Shape Data** dialog box. Specify the list items in the Format cell. Users can select only one item from the list.  </span></span><br/> |<span data-ttu-id="ca3af-117">**visPropTypeListFix**</span><span class="sxs-lookup"><span data-stu-id="ca3af-117">**visPropTypeListFix**</span></span> <br/> |
|<span data-ttu-id="ca3af-118">segundo</span><span class="sxs-lookup"><span data-stu-id="ca3af-118">2</span></span>  <br/> |<span data-ttu-id="ca3af-p103">Número. Incluye los valores de fecha, hora, duración y moneda, así como escalares, dimensiones y ángulos. Especifique una imagen de formato en la celda Format.</span><span class="sxs-lookup"><span data-stu-id="ca3af-p103">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="ca3af-122">**visPropTypeNumber**</span><span class="sxs-lookup"><span data-stu-id="ca3af-122">**visPropTypeNumber**</span></span> <br/> |
|<span data-ttu-id="ca3af-123">3</span><span class="sxs-lookup"><span data-stu-id="ca3af-123">3</span></span>  <br/> |<span data-ttu-id="ca3af-p104">Booleano. Muestra FALSE (falso) y TRUE (verdadero) como elementos que los usuarios pueden seleccionar en un cuadro de lista desplegable en el cuadro de diálogo **Definir datos de formas**.</span><span class="sxs-lookup"><span data-stu-id="ca3af-p104">Boolean. Displays FALSE and TRUE as items users can select from a drop-down list box in the **Define Shape Data** dialog box.  </span></span><br/> |<span data-ttu-id="ca3af-126">**visPropTypeBool**</span><span class="sxs-lookup"><span data-stu-id="ca3af-126">**visPropTypeBool**</span></span> <br/> |
|<span data-ttu-id="ca3af-127">4 </span><span class="sxs-lookup"><span data-stu-id="ca3af-127">4</span></span>  <br/> |<span data-ttu-id="ca3af-p105">Lista variable. Muestra los elementos de la lista en un cuadro combinado desplegable en el cuadro de diálogo **Definir datos de formas**. Especifique los elementos de la lista en la celda Format. Los usuarios pueden seleccionar un elemento de la lista o especificar uno nuevo que se agrega a la lista actual en la celda Format.</span><span class="sxs-lookup"><span data-stu-id="ca3af-p105">Variable list. Displays the list items in a drop-down combo box in the **Define Shape Data** dialog box. Specify the list items in the Format cell. Users can select a list item or enter a new item that is added to the current list in the Format cell.  </span></span><br/> |<span data-ttu-id="ca3af-132">**visPropTypeListVar**</span><span class="sxs-lookup"><span data-stu-id="ca3af-132">**visPropTypeListVar**</span></span> <br/> |
|<span data-ttu-id="ca3af-133">5 </span><span class="sxs-lookup"><span data-stu-id="ca3af-133">5</span></span>  <br/> |<span data-ttu-id="ca3af-p106">Valor de fecha u hora. Muestra días, meses y años; o segundos, minutos y horas; o un valor combinado de fecha y hora. Especifique una imagen de formato en la celda Format.</span><span class="sxs-lookup"><span data-stu-id="ca3af-p106">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="ca3af-137">**visPropTypeDate**</span><span class="sxs-lookup"><span data-stu-id="ca3af-137">**visPropTypeDate**</span></span> <br/> |
|<span data-ttu-id="ca3af-138">6 </span><span class="sxs-lookup"><span data-stu-id="ca3af-138">6</span></span>  <br/> |<span data-ttu-id="ca3af-p107">Valor de duración. Muestra el tiempo transcurrido. Especifique una imagen de formato en la celda Format.</span><span class="sxs-lookup"><span data-stu-id="ca3af-p107">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="ca3af-142">**visPropTypeDuration**</span><span class="sxs-lookup"><span data-stu-id="ca3af-142">**visPropTypeDuration**</span></span> <br/> |
|<span data-ttu-id="ca3af-143">7 </span><span class="sxs-lookup"><span data-stu-id="ca3af-143">7</span></span>  <br/> |<span data-ttu-id="ca3af-p108">Valor de moneda. Utiliza la configuración regional actual del sistema. Especifique una imagen de formato en la celda Format.</span><span class="sxs-lookup"><span data-stu-id="ca3af-p108">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="ca3af-147">**visPropTypeCurrency**</span><span class="sxs-lookup"><span data-stu-id="ca3af-147">**visPropTypeCurrency**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca3af-148">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ca3af-148">Remarks</span></span>

<span data-ttu-id="ca3af-149">Para obtener una referencia a la celda Type por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="ca3af-149">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca3af-150">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="ca3af-150">Cell name:</span></span>  <br/> |<span data-ttu-id="ca3af-151">Polyprop. *Nombre* . Tipo donde prop.  *Name* es el nombre de la fila</span><span class="sxs-lookup"><span data-stu-id="ca3af-151">Prop. *Name*  .Type where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="ca3af-152">Para obtener una referencia desde un programa a la celda Type por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ca3af-152">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca3af-153">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="ca3af-153">Section index:</span></span>  <br/> |<span data-ttu-id="ca3af-154">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="ca3af-154">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="ca3af-155">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="ca3af-155">Row index:</span></span>  <br/> |<span data-ttu-id="ca3af-156">**visRowProp** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ca3af-156">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="ca3af-157">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="ca3af-157">Cell index:</span></span>  <br/> |<span data-ttu-id="ca3af-158">**visCustPropsType**</span><span class="sxs-lookup"><span data-stu-id="ca3af-158">**visCustPropsType**</span></span> <br/> |
   

