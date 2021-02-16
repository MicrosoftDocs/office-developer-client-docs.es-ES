---
title: Elemento Cell (fila ArcTo) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 69f1a0cc-90fe-4b49-653c-bba4a1a2b1b2
description: Contiene la coordenada x, la coordenada y o la proa de un arco circular.
ms.openlocfilehash: 6d744366cda7db0f3950ed0962c7ba5bd01b8e36
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538826"
---
# <a name="cell-element-arcto-row-visio-xml"></a><span data-ttu-id="a0683-103">Elemento Cell (fila ArcTo) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="a0683-103">Cell element (ArcTo Row) (Visio XML)</span></span>

<span data-ttu-id="a0683-104">Contiene la coordenada x, la coordenada y o la proa de un arco circular.</span><span class="sxs-lookup"><span data-stu-id="a0683-104">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a0683-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a0683-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a0683-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="a0683-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a0683-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a0683-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a0683-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a0683-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a0683-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a0683-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a0683-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a0683-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a0683-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="a0683-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a0683-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="a0683-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a0683-113">Definición</span><span class="sxs-lookup"><span data-stu-id="a0683-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a0683-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a0683-114">Elements and attributes</span></span>

<span data-ttu-id="a0683-115">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="a0683-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a0683-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a0683-116">Parent elements</span></span>

|<span data-ttu-id="a0683-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a0683-117">**Element**</span></span>|<span data-ttu-id="a0683-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a0683-118">**Type**</span></span>|<span data-ttu-id="a0683-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a0683-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a0683-120">Elemento Row (Geometría)</span><span class="sxs-lookup"><span data-stu-id="a0683-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="a0683-121">ArcTo_Type</span><span class="sxs-lookup"><span data-stu-id="a0683-121">ArcTo_Type</span></span>](arcto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a0683-122">Contiene las coordenadas x e y, y la curvatura de un arco circular.</span><span class="sxs-lookup"><span data-stu-id="a0683-122">Contains the x- and y-coordinates and bow of a circular arc.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a0683-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a0683-123">Child elements</span></span>

|<span data-ttu-id="a0683-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a0683-124">**Element**</span></span>|<span data-ttu-id="a0683-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a0683-125">**Type**</span></span>|<span data-ttu-id="a0683-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a0683-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a0683-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="a0683-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a0683-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="a0683-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a0683-129">Contiene la coordenada x, la coordenada y o la proa de un arco circular.</span><span class="sxs-lookup"><span data-stu-id="a0683-129">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a0683-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="a0683-130">Attributes</span></span>

|<span data-ttu-id="a0683-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a0683-131">**Attribute**</span></span>|<span data-ttu-id="a0683-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a0683-132">**Type**</span></span>|<span data-ttu-id="a0683-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="a0683-133">**Required**</span></span>|<span data-ttu-id="a0683-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a0683-134">**Description**</span></span>|<span data-ttu-id="a0683-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="a0683-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a0683-136">E</span><span class="sxs-lookup"><span data-stu-id="a0683-136">E</span></span>  <br/> |<span data-ttu-id="a0683-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a0683-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a0683-138">opcional</span><span class="sxs-lookup"><span data-stu-id="a0683-138">optional</span></span>  <br/> |<span data-ttu-id="a0683-139">Indica que la fórmula se evalúa como un error.</span><span class="sxs-lookup"><span data-stu-id="a0683-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="a0683-140">El valor de **E** es el valor actual (una cadena de mensaje de error); el valor del atributo **V** es el último valor válido.</span><span class="sxs-lookup"><span data-stu-id="a0683-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="a0683-141">Una cadena de mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="a0683-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="a0683-142">F</span><span class="sxs-lookup"><span data-stu-id="a0683-142">F</span></span>  <br/> |<span data-ttu-id="a0683-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a0683-143">xsd:string</span></span>  <br/> |<span data-ttu-id="a0683-144">opcional</span><span class="sxs-lookup"><span data-stu-id="a0683-144">optional</span></span>  <br/> | <span data-ttu-id="a0683-145">Representa la fórmula del elemento.</span><span class="sxs-lookup"><span data-stu-id="a0683-145">Represents the element's formula.</span></span> <span data-ttu-id="a0683-146">Este atributo puede contener una de las siguientes cadenas:</span><span class="sxs-lookup"><span data-stu-id="a0683-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="a0683-147">'(alguna fórmula)' si la fórmula existe localmente</span><span class="sxs-lookup"><span data-stu-id="a0683-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="a0683-148">`No Formula` si la fórmula se elimina o bloquea localmente</span><span class="sxs-lookup"><span data-stu-id="a0683-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="a0683-149">`Inh` si la fórmula se hereda.</span><span class="sxs-lookup"><span data-stu-id="a0683-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="a0683-150">Una fórmula.</span><span class="sxs-lookup"><span data-stu-id="a0683-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="a0683-151">N</span><span class="sxs-lookup"><span data-stu-id="a0683-151">N</span></span>  <br/> |<span data-ttu-id="a0683-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a0683-152">xsd:string</span></span>  <br/> |<span data-ttu-id="a0683-153">necesario</span><span class="sxs-lookup"><span data-stu-id="a0683-153">required</span></span>  <br/> |<span data-ttu-id="a0683-154">Representa el nombre de la celda ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="a0683-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="a0683-155">Nombre de la celda ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="a0683-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="a0683-156">Vea la sección Comentarios a continuación.</span><span class="sxs-lookup"><span data-stu-id="a0683-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="a0683-157">U</span><span class="sxs-lookup"><span data-stu-id="a0683-157">U</span></span>  <br/> |<span data-ttu-id="a0683-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a0683-158">xsd:string</span></span>  <br/> |<span data-ttu-id="a0683-159">opcional</span><span class="sxs-lookup"><span data-stu-id="a0683-159">optional</span></span>  <br/> |<span data-ttu-id="a0683-160">Representa una unidad de medida El valor predeterminado es DL.</span><span class="sxs-lookup"><span data-stu-id="a0683-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="a0683-161">Las unidades de la celda.</span><span class="sxs-lookup"><span data-stu-id="a0683-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="a0683-162">V</span><span class="sxs-lookup"><span data-stu-id="a0683-162">V</span></span>  <br/> |<span data-ttu-id="a0683-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a0683-163">xsd:string</span></span>  <br/> |<span data-ttu-id="a0683-164">opcional</span><span class="sxs-lookup"><span data-stu-id="a0683-164">optional</span></span>  <br/> |<span data-ttu-id="a0683-165">Representa el valor de la celda.</span><span class="sxs-lookup"><span data-stu-id="a0683-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="a0683-166">Valor de la celda ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="a0683-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0683-167">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a0683-167">Remarks</span></span>

<span data-ttu-id="a0683-168">El **atributo N** de este elemento **Cell** debe ser uno de un conjunto limitado de valores que corresponden a las celdas de ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="a0683-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="a0683-169">Consulte la tabla siguiente para determinar los valores del atributo **N** que se permiten para este **elemento Cell.**</span><span class="sxs-lookup"><span data-stu-id="a0683-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="a0683-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a0683-170">**Value**</span></span>|<span data-ttu-id="a0683-171">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a0683-171">**Description**</span></span>|<span data-ttu-id="a0683-172">**Más información**</span><span class="sxs-lookup"><span data-stu-id="a0683-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a0683-173">A</span><span class="sxs-lookup"><span data-stu-id="a0683-173">A</span></span>  <br/> |<span data-ttu-id="a0683-174">Distancia desde el punto medio del arco hasta el punto medio de su cuerda.</span><span class="sxs-lookup"><span data-stu-id="a0683-174">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |[<span data-ttu-id="a0683-175">Fila ArcTo (Sección de geometría)</span><span class="sxs-lookup"><span data-stu-id="a0683-175">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="a0683-176">X</span><span class="sxs-lookup"><span data-stu-id="a0683-176">X</span></span>  <br/> |<span data-ttu-id="a0683-177">Coordenada x del vértice del extremo de un arco.</span><span class="sxs-lookup"><span data-stu-id="a0683-177">The x-coordinate of the ending vertex of an arc.</span></span>  <br/> |[<span data-ttu-id="a0683-178">Fila ArcTo (Sección de geometría)</span><span class="sxs-lookup"><span data-stu-id="a0683-178">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="a0683-179">v</span><span class="sxs-lookup"><span data-stu-id="a0683-179">Y</span></span>  <br/> |<span data-ttu-id="a0683-180">Coordenada y del vértice del extremo de un arco.</span><span class="sxs-lookup"><span data-stu-id="a0683-180">The y-coordinate of the ending vertex of an arc.</span></span>  <br/> |[<span data-ttu-id="a0683-181">Fila ArcTo (Sección de geometría)</span><span class="sxs-lookup"><span data-stu-id="a0683-181">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
   

