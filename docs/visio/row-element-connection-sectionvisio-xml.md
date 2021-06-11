---
title: Elemento Row (sección Connection) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f44fc18-4757-7aba-8778-a474ab93a78d
description: Contiene las coordenadas x o Y, la dirección horizontal y vertical y el tipo de un único punto de conexión en una forma.
ms.openlocfilehash: eb32030e89d3ac77adfdc64e2d20a5fb954dbb53
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541767"
---
# <a name="row-element-connection-section-visio-xml"></a><span data-ttu-id="1cf97-103">Elemento Row (sección Connection) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1cf97-103">Row element (Connection Section) (Visio XML)</span></span>

<span data-ttu-id="1cf97-104">Contiene las coordenadas x o Y, la dirección horizontal y vertical y el tipo de un único punto de conexión en una forma.</span><span class="sxs-lookup"><span data-stu-id="1cf97-104">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1cf97-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1cf97-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1cf97-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="1cf97-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1cf97-107">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="1cf97-107">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1cf97-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1cf97-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1cf97-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1cf97-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1cf97-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1cf97-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1cf97-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="1cf97-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1cf97-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="1cf97-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1cf97-113">Definición</span><span class="sxs-lookup"><span data-stu-id="1cf97-113">Definition</span></span>

```XML
< xs:element name="Row" type="ConnectionRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1cf97-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1cf97-114">Elements and attributes</span></span>

<span data-ttu-id="1cf97-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="1cf97-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1cf97-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1cf97-116">Parent elements</span></span>

|<span data-ttu-id="1cf97-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1cf97-117">**Element**</span></span>|<span data-ttu-id="1cf97-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1cf97-118">**Type**</span></span>|<span data-ttu-id="1cf97-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1cf97-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1cf97-120">Section</span><span class="sxs-lookup"><span data-stu-id="1cf97-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1cf97-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="1cf97-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1cf97-122">Contiene las coordenadas x o Y, la dirección horizontal y vertical y el tipo de un único punto de conexión en una forma.</span><span class="sxs-lookup"><span data-stu-id="1cf97-122">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1cf97-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1cf97-123">Child elements</span></span>

|<span data-ttu-id="1cf97-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1cf97-124">**Element**</span></span>|<span data-ttu-id="1cf97-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1cf97-125">**Type**</span></span>|<span data-ttu-id="1cf97-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1cf97-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1cf97-127">Cell</span><span class="sxs-lookup"><span data-stu-id="1cf97-127">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="1cf97-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1cf97-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1cf97-129">Especifica una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="1cf97-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1cf97-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="1cf97-130">Attributes</span></span>

|<span data-ttu-id="1cf97-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1cf97-131">**Attribute**</span></span>|<span data-ttu-id="1cf97-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1cf97-132">**Type**</span></span>|<span data-ttu-id="1cf97-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="1cf97-133">**Required**</span></span>|<span data-ttu-id="1cf97-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1cf97-134">**Description**</span></span>|<span data-ttu-id="1cf97-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="1cf97-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1cf97-136">Del</span><span class="sxs-lookup"><span data-stu-id="1cf97-136">Del</span></span>  <br/> |<span data-ttu-id="1cf97-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="1cf97-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1cf97-138">opcional</span><span class="sxs-lookup"><span data-stu-id="1cf97-138">optional</span></span>  <br/> |<span data-ttu-id="1cf97-139">Especifica si se ha eliminado una fila que se heredaría de una forma maestra.</span><span class="sxs-lookup"><span data-stu-id="1cf97-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="1cf97-140">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="1cf97-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1cf97-141">IX</span><span class="sxs-lookup"><span data-stu-id="1cf97-141">IX</span></span>  <br/> |<span data-ttu-id="1cf97-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1cf97-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1cf97-143">opcional</span><span class="sxs-lookup"><span data-stu-id="1cf97-143">optional</span></span>  <br/> |<span data-ttu-id="1cf97-144">Especifica el identificador único de la fila.</span><span class="sxs-lookup"><span data-stu-id="1cf97-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="1cf97-145">Debe ser unqiue y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch y Tabs.</span><span class="sxs-lookup"><span data-stu-id="1cf97-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="1cf97-146">Una fila solo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="1cf97-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="1cf97-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1cf97-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1cf97-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="1cf97-148">LocalName</span></span>  <br/> |<span data-ttu-id="1cf97-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1cf97-149">xsd:string</span></span>  <br/> |<span data-ttu-id="1cf97-150">opcional</span><span class="sxs-lookup"><span data-stu-id="1cf97-150">optional</span></span>  <br/> |<span data-ttu-id="1cf97-151">Especifica el nombre único dependiente del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="1cf97-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="1cf97-152">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1cf97-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1cf97-153">N</span><span class="sxs-lookup"><span data-stu-id="1cf97-153">N</span></span>  <br/> |<span data-ttu-id="1cf97-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1cf97-154">xsd:string</span></span>  <br/> |<span data-ttu-id="1cf97-155">opcional</span><span class="sxs-lookup"><span data-stu-id="1cf97-155">optional</span></span>  <br/> |<span data-ttu-id="1cf97-156">Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, Control, Connection, Hyperlink y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="1cf97-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="1cf97-157">Una fila solo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="1cf97-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="1cf97-158">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1cf97-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1cf97-159">T</span><span class="sxs-lookup"><span data-stu-id="1cf97-159">T</span></span>  <br/> |<span data-ttu-id="1cf97-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1cf97-160">xsd:string</span></span>  <br/> |<span data-ttu-id="1cf97-161">opcional</span><span class="sxs-lookup"><span data-stu-id="1cf97-161">optional</span></span>  <br/> |<span data-ttu-id="1cf97-162">Especifica el tipo de la ruta geométrica representada por la fila y usada en la visualización de geometría.</span><span class="sxs-lookup"><span data-stu-id="1cf97-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="1cf97-163">El atributo T solo se usa para la sección Geometría.</span><span class="sxs-lookup"><span data-stu-id="1cf97-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="1cf97-164">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1cf97-164">Values of the xsd:string type.</span></span>  <br/> |
   

