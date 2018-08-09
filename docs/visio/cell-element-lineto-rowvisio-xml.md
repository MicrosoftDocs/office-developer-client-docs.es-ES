---
title: Elemento de celda (fila LineTo) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64f2494d-2de7-6bc5-0db4-91b952bdcb5e
description: Contiene x- o coordenadas y del vértice del extremo de un segmento de línea recta.
ms.openlocfilehash: 284b315c156fed8ea3592d2c6825ff6b4bf4c279
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821714"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="1ae4a-103">Elemento de celda (fila LineTo) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="1ae4a-103">Cell element (LineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="1ae4a-104">Contiene x- o coordenadas y del vértice del extremo de un segmento de línea recta.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ae4a-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1ae4a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ae4a-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1ae4a-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1ae4a-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1ae4a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1ae4a-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1ae4a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1ae4a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1ae4a-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1ae4a-112">master # .xml, # .xml de página</span><span class="sxs-lookup"><span data-stu-id="1ae4a-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1ae4a-113">Definición</span><span class="sxs-lookup"><span data-stu-id="1ae4a-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1ae4a-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1ae4a-114">Elements and attributes</span></span>

<span data-ttu-id="1ae4a-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1ae4a-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1ae4a-116">Parent elements</span></span>

|<span data-ttu-id="1ae4a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-117">**Element**</span></span>|<span data-ttu-id="1ae4a-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-118">**Type**</span></span>|<span data-ttu-id="1ae4a-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1ae4a-120">Elemento de fila (geometría)</span><span class="sxs-lookup"><span data-stu-id="1ae4a-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="1ae4a-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="1ae4a-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1ae4a-122">Contiene x- o coordenadas y del vértice del extremo de un segmento de línea recta.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1ae4a-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1ae4a-123">Child elements</span></span>

|<span data-ttu-id="1ae4a-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-124">**Element**</span></span>|<span data-ttu-id="1ae4a-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-125">**Type**</span></span>|<span data-ttu-id="1ae4a-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1ae4a-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="1ae4a-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1ae4a-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="1ae4a-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1ae4a-129">Especifica una referencia a una página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1ae4a-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="1ae4a-130">Attributes</span></span>

|<span data-ttu-id="1ae4a-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-131">**Attribute**</span></span>|<span data-ttu-id="1ae4a-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-132">**Type**</span></span>|<span data-ttu-id="1ae4a-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-133">**Required**</span></span>|<span data-ttu-id="1ae4a-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-134">**Description**</span></span>|<span data-ttu-id="1ae4a-135">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1ae4a-136">E</span><span class="sxs-lookup"><span data-stu-id="1ae4a-136">E</span></span>  <br/> |<span data-ttu-id="1ae4a-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="1ae4a-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1ae4a-138">opcional</span><span class="sxs-lookup"><span data-stu-id="1ae4a-138">optional</span></span>  <br/> |<span data-ttu-id="1ae4a-139">Indica que la fórmula da como resultado un error.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="1ae4a-140">El valor de **E** es el valor actual (una cadena de mensaje de error); el valor del atributo **V** es el último valor válido.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="1ae4a-141">Una cadena de mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="1ae4a-142">F</span><span class="sxs-lookup"><span data-stu-id="1ae4a-142">F</span></span>  <br/> |<span data-ttu-id="1ae4a-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="1ae4a-143">xsd:string</span></span>  <br/> |<span data-ttu-id="1ae4a-144">opcional</span><span class="sxs-lookup"><span data-stu-id="1ae4a-144">optional</span></span>  <br/> | <span data-ttu-id="1ae4a-145">Representa la fórmula del elemento.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-145">Represents the element's formula.</span></span> <span data-ttu-id="1ae4a-146">Este atributo puede contener uno de las siguientes cadenas:</span><span class="sxs-lookup"><span data-stu-id="1ae4a-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="1ae4a-147">'(algunos fórmula)' Si la fórmula existe localmente</span><span class="sxs-lookup"><span data-stu-id="1ae4a-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="1ae4a-148">`No Formula`Si la fórmula se ha eliminado localmente o bloqueada</span><span class="sxs-lookup"><span data-stu-id="1ae4a-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="1ae4a-149">`Inh`Si la fórmula es heredada.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="1ae4a-150">Una fórmula.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="1ae4a-151">N</span><span class="sxs-lookup"><span data-stu-id="1ae4a-151">N</span></span>  <br/> |<span data-ttu-id="1ae4a-152">xsd: String</span><span class="sxs-lookup"><span data-stu-id="1ae4a-152">xsd:string</span></span>  <br/> |<span data-ttu-id="1ae4a-153">necesario</span><span class="sxs-lookup"><span data-stu-id="1ae4a-153">required</span></span>  <br/> |<span data-ttu-id="1ae4a-154">Representa el nombre de la celda ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="1ae4a-155">El nombre de la celda ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="1ae4a-156">Vea la sección comentarios que aparece a continuación.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="1ae4a-157">U</span><span class="sxs-lookup"><span data-stu-id="1ae4a-157">U</span></span>  <br/> |<span data-ttu-id="1ae4a-158">xsd: String</span><span class="sxs-lookup"><span data-stu-id="1ae4a-158">xsd:string</span></span>  <br/> |<span data-ttu-id="1ae4a-159">opcional</span><span class="sxs-lookup"><span data-stu-id="1ae4a-159">optional</span></span>  <br/> |<span data-ttu-id="1ae4a-160">Representa una unidad de medida, el valor predeterminado es DL.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="1ae4a-161">Las unidades de la celda.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="1ae4a-162">V</span><span class="sxs-lookup"><span data-stu-id="1ae4a-162">V</span></span>  <br/> |<span data-ttu-id="1ae4a-163">xsd: String</span><span class="sxs-lookup"><span data-stu-id="1ae4a-163">xsd:string</span></span>  <br/> |<span data-ttu-id="1ae4a-164">opcional</span><span class="sxs-lookup"><span data-stu-id="1ae4a-164">optional</span></span>  <br/> |<span data-ttu-id="1ae4a-165">Representa el valor de la celda.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="1ae4a-166">El valor de la celda ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ae4a-167">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ae4a-167">Remarks</span></span>

<span data-ttu-id="1ae4a-168">El atributo **N** de este elemento de **celda** debe ser uno de un conjunto limitado de valores que corresponden a las celdas de ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="1ae4a-169">Hacer referencia a la tabla siguiente para determinar los valores del atributo **N** permitidas para este elemento de **celda** .</span><span class="sxs-lookup"><span data-stu-id="1ae4a-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="1ae4a-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-170">**Value**</span></span>|<span data-ttu-id="1ae4a-171">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-171">**Description**</span></span>|<span data-ttu-id="1ae4a-172">**Más información**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ae4a-173">X</span><span class="sxs-lookup"><span data-stu-id="1ae4a-173">X</span></span>  <br/> |<span data-ttu-id="1ae4a-174">Coordenada x del vértice del extremo de un segmento de línea recta.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="1ae4a-175">Fila LineTo (Sección de Geometría)</span><span class="sxs-lookup"><span data-stu-id="1ae4a-175">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="1ae4a-176">v</span><span class="sxs-lookup"><span data-stu-id="1ae4a-176">Y</span></span>  <br/> |<span data-ttu-id="1ae4a-177">Coordenada y del vértice del extremo de un segmento de línea recta.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="1ae4a-178">Fila LineTo (Sección de Geometría)</span><span class="sxs-lookup"><span data-stu-id="1ae4a-178">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
   

