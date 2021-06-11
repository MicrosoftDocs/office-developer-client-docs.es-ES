---
title: Elemento Row (sección Shape Data) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eb74ae8-ff42-6e34-30e2-2080bf8b5754
description: Especifica una entrada de datos de forma para asociar datos a una forma.
ms.openlocfilehash: 4c5644aa2088dcaf3be81ea9aeaa549c911a31f6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538273"
---
# <a name="row-element-shape-data-section-visio-xml"></a><span data-ttu-id="02fcd-103">Elemento Row (sección Shape Data) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="02fcd-103">Row element (Shape Data Section) (Visio XML)</span></span>

<span data-ttu-id="02fcd-104">Especifica una entrada de datos de forma para asociar datos a una forma.</span><span class="sxs-lookup"><span data-stu-id="02fcd-104">Specifies one shape data entry for associating data with a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02fcd-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="02fcd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02fcd-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="02fcd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="02fcd-107">Shape Data_Type</span><span class="sxs-lookup"><span data-stu-id="02fcd-107">Shape Data_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="02fcd-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="02fcd-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="02fcd-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="02fcd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="02fcd-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="02fcd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="02fcd-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="02fcd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="02fcd-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="02fcd-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="02fcd-113">Definición</span><span class="sxs-lookup"><span data-stu-id="02fcd-113">Definition</span></span>

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="02fcd-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="02fcd-114">Elements and attributes</span></span>

<span data-ttu-id="02fcd-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="02fcd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="02fcd-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="02fcd-116">Parent elements</span></span>

|<span data-ttu-id="02fcd-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="02fcd-117">**Element**</span></span>|<span data-ttu-id="02fcd-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="02fcd-118">**Type**</span></span>|<span data-ttu-id="02fcd-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02fcd-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="02fcd-120">Section</span><span class="sxs-lookup"><span data-stu-id="02fcd-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="02fcd-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="02fcd-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="02fcd-122">Especifica una entrada de datos de forma para asociar datos a una forma.</span><span class="sxs-lookup"><span data-stu-id="02fcd-122">Specifies one shape data entry for associating data with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="02fcd-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="02fcd-123">Child elements</span></span>

|<span data-ttu-id="02fcd-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="02fcd-124">**Element**</span></span>|<span data-ttu-id="02fcd-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="02fcd-125">**Type**</span></span>|<span data-ttu-id="02fcd-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02fcd-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="02fcd-127">Cell</span><span class="sxs-lookup"><span data-stu-id="02fcd-127">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="02fcd-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="02fcd-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="02fcd-129">Especifica una propiedad de los datos de forma.</span><span class="sxs-lookup"><span data-stu-id="02fcd-129">Specifies one property of the shape data.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="02fcd-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="02fcd-130">Attributes</span></span>

|<span data-ttu-id="02fcd-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="02fcd-131">**Attribute**</span></span>|<span data-ttu-id="02fcd-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="02fcd-132">**Type**</span></span>|<span data-ttu-id="02fcd-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="02fcd-133">**Required**</span></span>|<span data-ttu-id="02fcd-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02fcd-134">**Description**</span></span>|<span data-ttu-id="02fcd-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="02fcd-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="02fcd-136">Del</span><span class="sxs-lookup"><span data-stu-id="02fcd-136">Del</span></span>  <br/> |<span data-ttu-id="02fcd-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="02fcd-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="02fcd-138">opcional</span><span class="sxs-lookup"><span data-stu-id="02fcd-138">optional</span></span>  <br/> |<span data-ttu-id="02fcd-139">Especifica si se ha eliminado una fila que se heredaría de una forma maestra.</span><span class="sxs-lookup"><span data-stu-id="02fcd-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="02fcd-140">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="02fcd-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="02fcd-141">IX</span><span class="sxs-lookup"><span data-stu-id="02fcd-141">IX</span></span>  <br/> |<span data-ttu-id="02fcd-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="02fcd-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="02fcd-143">opcional</span><span class="sxs-lookup"><span data-stu-id="02fcd-143">optional</span></span>  <br/> |<span data-ttu-id="02fcd-144">Especifica el identificador único de la fila.</span><span class="sxs-lookup"><span data-stu-id="02fcd-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="02fcd-145">Debe ser unqiue y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch y Tabs.</span><span class="sxs-lookup"><span data-stu-id="02fcd-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="02fcd-146">Una fila solo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="02fcd-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="02fcd-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="02fcd-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="02fcd-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="02fcd-148">LocalName</span></span>  <br/> |<span data-ttu-id="02fcd-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="02fcd-149">xsd:string</span></span>  <br/> |<span data-ttu-id="02fcd-150">opcional</span><span class="sxs-lookup"><span data-stu-id="02fcd-150">optional</span></span>  <br/> |<span data-ttu-id="02fcd-151">Especifica el nombre único dependiente del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="02fcd-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="02fcd-152">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="02fcd-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="02fcd-153">N</span><span class="sxs-lookup"><span data-stu-id="02fcd-153">N</span></span>  <br/> |<span data-ttu-id="02fcd-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="02fcd-154">xsd:string</span></span>  <br/> |<span data-ttu-id="02fcd-155">opcional</span><span class="sxs-lookup"><span data-stu-id="02fcd-155">optional</span></span>  <br/> |<span data-ttu-id="02fcd-156">Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, Control, Connection, Hyperlink y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="02fcd-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="02fcd-157">Una fila solo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="02fcd-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="02fcd-158">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="02fcd-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="02fcd-159">T</span><span class="sxs-lookup"><span data-stu-id="02fcd-159">T</span></span>  <br/> |<span data-ttu-id="02fcd-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="02fcd-160">xsd:string</span></span>  <br/> |<span data-ttu-id="02fcd-161">opcional</span><span class="sxs-lookup"><span data-stu-id="02fcd-161">optional</span></span>  <br/> |<span data-ttu-id="02fcd-162">Especifica el tipo de la ruta geométrica representada por la fila y usada en la visualización de geometría.</span><span class="sxs-lookup"><span data-stu-id="02fcd-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="02fcd-163">El atributo T solo se usa para la sección Geometría.</span><span class="sxs-lookup"><span data-stu-id="02fcd-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="02fcd-164">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="02fcd-164">Values of the xsd:string type.</span></span>  <br/> |
   

