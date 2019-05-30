---
title: Elemento cell (fila lineTo) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64f2494d-2de7-6bc5-0db4-91b952bdcb5e
description: Contiene las coordenadas x o y del vértice del extremo de un segmento de línea recta.
ms.openlocfilehash: 4b1628549e659712a1c2e79ae0fbf53d594e18f9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539512"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="c64e4-103">Elemento cell (fila lineTo) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="c64e4-103">Cell element (LineTo Row) (Visio XML)</span></span>

<span data-ttu-id="c64e4-104">Contiene las coordenadas x o y del vértice del extremo de un segmento de línea recta.</span><span class="sxs-lookup"><span data-stu-id="c64e4-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c64e4-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c64e4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c64e4-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="c64e4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c64e4-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c64e4-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c64e4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c64e4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c64e4-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c64e4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c64e4-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="c64e4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c64e4-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="c64e4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c64e4-112">Master #. XML, página #. XML</span><span class="sxs-lookup"><span data-stu-id="c64e4-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c64e4-113">Definición</span><span class="sxs-lookup"><span data-stu-id="c64e4-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c64e4-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c64e4-114">Elements and attributes</span></span>

<span data-ttu-id="c64e4-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="c64e4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c64e4-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c64e4-116">Parent elements</span></span>

|<span data-ttu-id="c64e4-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c64e4-117">**Element**</span></span>|<span data-ttu-id="c64e4-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c64e4-118">**Type**</span></span>|<span data-ttu-id="c64e4-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c64e4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c64e4-120">Elemento Row (geometría)</span><span class="sxs-lookup"><span data-stu-id="c64e4-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="c64e4-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="c64e4-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c64e4-122">Contiene las coordenadas x o y del vértice del extremo de un segmento de línea recta.</span><span class="sxs-lookup"><span data-stu-id="c64e4-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c64e4-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c64e4-123">Child elements</span></span>

|<span data-ttu-id="c64e4-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c64e4-124">**Element**</span></span>|<span data-ttu-id="c64e4-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c64e4-125">**Type**</span></span>|<span data-ttu-id="c64e4-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c64e4-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c64e4-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="c64e4-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c64e4-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="c64e4-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c64e4-129">Especifica una referencia a una página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="c64e4-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c64e4-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="c64e4-130">Attributes</span></span>

|<span data-ttu-id="c64e4-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c64e4-131">**Attribute**</span></span>|<span data-ttu-id="c64e4-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c64e4-132">**Type**</span></span>|<span data-ttu-id="c64e4-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="c64e4-133">**Required**</span></span>|<span data-ttu-id="c64e4-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c64e4-134">**Description**</span></span>|<span data-ttu-id="c64e4-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="c64e4-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c64e4-136">E</span><span class="sxs-lookup"><span data-stu-id="c64e4-136">E</span></span>  <br/> |<span data-ttu-id="c64e4-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c64e4-137">xsd:string</span></span>  <br/> |<span data-ttu-id="c64e4-138">opcional</span><span class="sxs-lookup"><span data-stu-id="c64e4-138">optional</span></span>  <br/> |<span data-ttu-id="c64e4-139">Indica que la fórmula da como resultado un error.</span><span class="sxs-lookup"><span data-stu-id="c64e4-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="c64e4-140">El valor de **E** es el valor actual (una cadena de mensaje de error); el valor del atributo **V** es el último valor válido.</span><span class="sxs-lookup"><span data-stu-id="c64e4-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="c64e4-141">Una cadena de mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="c64e4-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="c64e4-142">F</span><span class="sxs-lookup"><span data-stu-id="c64e4-142">F</span></span>  <br/> |<span data-ttu-id="c64e4-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c64e4-143">xsd:string</span></span>  <br/> |<span data-ttu-id="c64e4-144">opcional</span><span class="sxs-lookup"><span data-stu-id="c64e4-144">optional</span></span>  <br/> | <span data-ttu-id="c64e4-145">Representa la fórmula del elemento.</span><span class="sxs-lookup"><span data-stu-id="c64e4-145">Represents the element's formula.</span></span> <span data-ttu-id="c64e4-146">Este atributo puede contener una de las siguientes cadenas:</span><span class="sxs-lookup"><span data-stu-id="c64e4-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="c64e4-147">' (alguna fórmula) ' si la fórmula existe localmente</span><span class="sxs-lookup"><span data-stu-id="c64e4-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="c64e4-148">`No Formula`Si la fórmula se ha eliminado o bloqueado localmente</span><span class="sxs-lookup"><span data-stu-id="c64e4-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="c64e4-149">`Inh`Si la fórmula es heredada.</span><span class="sxs-lookup"><span data-stu-id="c64e4-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="c64e4-150">Una fórmula.</span><span class="sxs-lookup"><span data-stu-id="c64e4-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="c64e4-151">N</span><span class="sxs-lookup"><span data-stu-id="c64e4-151">N</span></span>  <br/> |<span data-ttu-id="c64e4-152">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c64e4-152">xsd:string</span></span>  <br/> |<span data-ttu-id="c64e4-153">necesario</span><span class="sxs-lookup"><span data-stu-id="c64e4-153">required</span></span>  <br/> |<span data-ttu-id="c64e4-154">Representa el nombre de la celda ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c64e4-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="c64e4-155">Nombre de la celda ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c64e4-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="c64e4-156">Vea la sección Comentarios a continuación.</span><span class="sxs-lookup"><span data-stu-id="c64e4-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="c64e4-157">U</span><span class="sxs-lookup"><span data-stu-id="c64e4-157">U</span></span>  <br/> |<span data-ttu-id="c64e4-158">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c64e4-158">xsd:string</span></span>  <br/> |<span data-ttu-id="c64e4-159">opcional</span><span class="sxs-lookup"><span data-stu-id="c64e4-159">optional</span></span>  <br/> |<span data-ttu-id="c64e4-160">Representa una unidad de medida el valor predeterminado es DL.</span><span class="sxs-lookup"><span data-stu-id="c64e4-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="c64e4-161">Unidades de la celda.</span><span class="sxs-lookup"><span data-stu-id="c64e4-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="c64e4-162">V</span><span class="sxs-lookup"><span data-stu-id="c64e4-162">V</span></span>  <br/> |<span data-ttu-id="c64e4-163">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c64e4-163">xsd:string</span></span>  <br/> |<span data-ttu-id="c64e4-164">opcional</span><span class="sxs-lookup"><span data-stu-id="c64e4-164">optional</span></span>  <br/> |<span data-ttu-id="c64e4-165">Representa el valor de la celda.</span><span class="sxs-lookup"><span data-stu-id="c64e4-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="c64e4-166">El valor de la celda ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c64e4-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c64e4-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c64e4-167">Remarks</span></span>

<span data-ttu-id="c64e4-168">El atributo **N** de este elemento de **celda** debe ser uno de un conjunto de valores limitado que corresponda a las celdas de ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c64e4-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="c64e4-169">Consulte la tabla siguiente para determinar los valores del atributo **N** que se permiten para este elemento de **celda** .</span><span class="sxs-lookup"><span data-stu-id="c64e4-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="c64e4-170">**Value**</span><span class="sxs-lookup"><span data-stu-id="c64e4-170">**Value**</span></span>|<span data-ttu-id="c64e4-171">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c64e4-171">**Description**</span></span>|<span data-ttu-id="c64e4-172">**Más información**</span><span class="sxs-lookup"><span data-stu-id="c64e4-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c64e4-173">X</span><span class="sxs-lookup"><span data-stu-id="c64e4-173">X</span></span>  <br/> |<span data-ttu-id="c64e4-174">Coordenada x del vértice del extremo de un segmento de línea recta.</span><span class="sxs-lookup"><span data-stu-id="c64e4-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="c64e4-175">Fila LineTo (Sección de Geometría)</span><span class="sxs-lookup"><span data-stu-id="c64e4-175">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="c64e4-176">v</span><span class="sxs-lookup"><span data-stu-id="c64e4-176">Y</span></span>  <br/> |<span data-ttu-id="c64e4-177">Coordenada y del vértice del extremo de un segmento de línea recta.</span><span class="sxs-lookup"><span data-stu-id="c64e4-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="c64e4-178">Fila LineTo (Sección de Geometría)</span><span class="sxs-lookup"><span data-stu-id="c64e4-178">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
   

