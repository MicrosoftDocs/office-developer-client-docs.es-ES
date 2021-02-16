---
title: Elemento Row (Sección de degradado de línea) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d823766-5cb0-925c-f622-18025f44426c
description: Contiene el color, la transparencia y la posición de un delimitador de degradado para un degradado de línea.
ms.openlocfilehash: bfaf3ab8cc16e11051310d7e838b9dddbf7e108d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540829"
---
# <a name="row-element-line-gradient-section-visio-xml"></a><span data-ttu-id="395d3-103">Elemento Row (Sección de degradado de línea) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="395d3-103">Row element (Line Gradient Section) (Visio XML)</span></span>

<span data-ttu-id="395d3-104">Contiene el color, la transparencia y la posición de un delimitador de degradado para un degradado de línea.</span><span class="sxs-lookup"><span data-stu-id="395d3-104">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="395d3-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="395d3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="395d3-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="395d3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="395d3-107">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="395d3-107">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="395d3-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="395d3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="395d3-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="395d3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="395d3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="395d3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="395d3-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="395d3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="395d3-112">document.xml, master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="395d3-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="395d3-113">Definición</span><span class="sxs-lookup"><span data-stu-id="395d3-113">Definition</span></span>

```XML
< xs:element name="Row" type="LineGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="395d3-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="395d3-114">Elements and attributes</span></span>

<span data-ttu-id="395d3-115">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="395d3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="395d3-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="395d3-116">Parent elements</span></span>

|<span data-ttu-id="395d3-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="395d3-117">**Element**</span></span>|<span data-ttu-id="395d3-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="395d3-118">**Type**</span></span>|<span data-ttu-id="395d3-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="395d3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="395d3-120">Section</span><span class="sxs-lookup"><span data-stu-id="395d3-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="395d3-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="395d3-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="395d3-122">Contiene el color, la transparencia y la posición de un delimitador de degradado para un degradado de línea.</span><span class="sxs-lookup"><span data-stu-id="395d3-122">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="395d3-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="395d3-123">Child elements</span></span>

|<span data-ttu-id="395d3-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="395d3-124">**Element**</span></span>|<span data-ttu-id="395d3-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="395d3-125">**Type**</span></span>|<span data-ttu-id="395d3-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="395d3-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="395d3-127">Cell</span><span class="sxs-lookup"><span data-stu-id="395d3-127">Cell</span></span>](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="395d3-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="395d3-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="395d3-129">Especifica una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="395d3-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="395d3-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="395d3-130">Attributes</span></span>

|<span data-ttu-id="395d3-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="395d3-131">**Attribute**</span></span>|<span data-ttu-id="395d3-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="395d3-132">**Type**</span></span>|<span data-ttu-id="395d3-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="395d3-133">**Required**</span></span>|<span data-ttu-id="395d3-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="395d3-134">**Description**</span></span>|<span data-ttu-id="395d3-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="395d3-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="395d3-136">Supr</span><span class="sxs-lookup"><span data-stu-id="395d3-136">Del</span></span>  <br/> |<span data-ttu-id="395d3-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="395d3-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="395d3-138">opcional</span><span class="sxs-lookup"><span data-stu-id="395d3-138">optional</span></span>  <br/> |<span data-ttu-id="395d3-139">Especifica si se ha eliminado una fila que se heredaría de una forma maestra.</span><span class="sxs-lookup"><span data-stu-id="395d3-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="395d3-140">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="395d3-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="395d3-141">IX</span><span class="sxs-lookup"><span data-stu-id="395d3-141">IX</span></span>  <br/> |<span data-ttu-id="395d3-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="395d3-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="395d3-143">opcional</span><span class="sxs-lookup"><span data-stu-id="395d3-143">optional</span></span>  <br/> |<span data-ttu-id="395d3-144">Especifica el identificador único de la fila.</span><span class="sxs-lookup"><span data-stu-id="395d3-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="395d3-145">Debe ser distinto y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch y Tabs.</span><span class="sxs-lookup"><span data-stu-id="395d3-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="395d3-146">Una fila solo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="395d3-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="395d3-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="395d3-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="395d3-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="395d3-148">LocalName</span></span>  <br/> |<span data-ttu-id="395d3-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="395d3-149">xsd:string</span></span>  <br/> |<span data-ttu-id="395d3-150">opcional</span><span class="sxs-lookup"><span data-stu-id="395d3-150">optional</span></span>  <br/> |<span data-ttu-id="395d3-151">Especifica el nombre único dependiente del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="395d3-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="395d3-152">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="395d3-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="395d3-153">N</span><span class="sxs-lookup"><span data-stu-id="395d3-153">N</span></span>  <br/> |<span data-ttu-id="395d3-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="395d3-154">xsd:string</span></span>  <br/> |<span data-ttu-id="395d3-155">opcional</span><span class="sxs-lookup"><span data-stu-id="395d3-155">optional</span></span>  <br/> |<span data-ttu-id="395d3-156">Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, Control, Connection, Hyperlink y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="395d3-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="395d3-157">Una fila solo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="395d3-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="395d3-158">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="395d3-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="395d3-159">T</span><span class="sxs-lookup"><span data-stu-id="395d3-159">T</span></span>  <br/> |<span data-ttu-id="395d3-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="395d3-160">xsd:string</span></span>  <br/> |<span data-ttu-id="395d3-161">opcional</span><span class="sxs-lookup"><span data-stu-id="395d3-161">optional</span></span>  <br/> |<span data-ttu-id="395d3-162">Especifica el tipo de la ruta geométrica representada por la fila y usada en la visualización de geometría.</span><span class="sxs-lookup"><span data-stu-id="395d3-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="395d3-163">El atributo T solo se usa para la sección Geometría.</span><span class="sxs-lookup"><span data-stu-id="395d3-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="395d3-164">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="395d3-164">Values of the xsd:string type.</span></span>  <br/> |
   

