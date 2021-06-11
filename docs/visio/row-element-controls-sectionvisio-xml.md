---
title: Elemento Row (sección Controls) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: Contiene las celdas de un controlador de control determinado definido para una forma.
ms.openlocfilehash: 0fb31d8066e0a76bfe00735cb5dcc984d02685f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541746"
---
# <a name="row-element-controls-section-visio-xml"></a><span data-ttu-id="8de3b-103">Elemento Row (sección Controls) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8de3b-103">Row element (Controls Section) (Visio XML)</span></span>

<span data-ttu-id="8de3b-104">Contiene las celdas de un controlador de control determinado definido para una forma.</span><span class="sxs-lookup"><span data-stu-id="8de3b-104">Contains the cells for a particular control handle defined for a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8de3b-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8de3b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8de3b-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="8de3b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8de3b-107">ControlRow_Type</span><span class="sxs-lookup"><span data-stu-id="8de3b-107">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8de3b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8de3b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8de3b-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8de3b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8de3b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8de3b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8de3b-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="8de3b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8de3b-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="8de3b-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8de3b-113">Definición</span><span class="sxs-lookup"><span data-stu-id="8de3b-113">Definition</span></span>

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8de3b-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="8de3b-114">Elements and attributes</span></span>

<span data-ttu-id="8de3b-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="8de3b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8de3b-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8de3b-116">Parent elements</span></span>

|<span data-ttu-id="8de3b-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8de3b-117">**Element**</span></span>|<span data-ttu-id="8de3b-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8de3b-118">**Type**</span></span>|<span data-ttu-id="8de3b-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8de3b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8de3b-120">Section</span><span class="sxs-lookup"><span data-stu-id="8de3b-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8de3b-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="8de3b-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8de3b-122">Contiene las celdas de un controlador de control determinado definido para una forma.</span><span class="sxs-lookup"><span data-stu-id="8de3b-122">Contains the cells for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8de3b-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8de3b-123">Child elements</span></span>

|<span data-ttu-id="8de3b-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8de3b-124">**Element**</span></span>|<span data-ttu-id="8de3b-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8de3b-125">**Type**</span></span>|<span data-ttu-id="8de3b-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8de3b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8de3b-127">Cell</span><span class="sxs-lookup"><span data-stu-id="8de3b-127">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="8de3b-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="8de3b-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8de3b-129">Contiene una propiedad para un controlador de control determinado definido para una forma.</span><span class="sxs-lookup"><span data-stu-id="8de3b-129">Contains a property for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8de3b-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="8de3b-130">Attributes</span></span>

|<span data-ttu-id="8de3b-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="8de3b-131">**Attribute**</span></span>|<span data-ttu-id="8de3b-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8de3b-132">**Type**</span></span>|<span data-ttu-id="8de3b-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="8de3b-133">**Required**</span></span>|<span data-ttu-id="8de3b-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8de3b-134">**Description**</span></span>|<span data-ttu-id="8de3b-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="8de3b-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8de3b-136">Del</span><span class="sxs-lookup"><span data-stu-id="8de3b-136">Del</span></span>  <br/> |<span data-ttu-id="8de3b-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="8de3b-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8de3b-138">opcional</span><span class="sxs-lookup"><span data-stu-id="8de3b-138">optional</span></span>  <br/> |<span data-ttu-id="8de3b-139">Especifica si se ha eliminado una fila que se heredaría de una forma maestra.</span><span class="sxs-lookup"><span data-stu-id="8de3b-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="8de3b-140">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8de3b-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8de3b-141">IX</span><span class="sxs-lookup"><span data-stu-id="8de3b-141">IX</span></span>  <br/> |<span data-ttu-id="8de3b-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8de3b-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8de3b-143">opcional</span><span class="sxs-lookup"><span data-stu-id="8de3b-143">optional</span></span>  <br/> |<span data-ttu-id="8de3b-144">Especifica el identificador único de la fila.</span><span class="sxs-lookup"><span data-stu-id="8de3b-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="8de3b-145">Debe ser unqiue y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch y Tabs.</span><span class="sxs-lookup"><span data-stu-id="8de3b-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="8de3b-146">Una fila solo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="8de3b-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="8de3b-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8de3b-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8de3b-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="8de3b-148">LocalName</span></span>  <br/> |<span data-ttu-id="8de3b-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8de3b-149">xsd:string</span></span>  <br/> |<span data-ttu-id="8de3b-150">opcional</span><span class="sxs-lookup"><span data-stu-id="8de3b-150">optional</span></span>  <br/> |<span data-ttu-id="8de3b-151">Especifica el nombre único dependiente del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="8de3b-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="8de3b-152">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8de3b-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8de3b-153">N</span><span class="sxs-lookup"><span data-stu-id="8de3b-153">N</span></span>  <br/> |<span data-ttu-id="8de3b-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8de3b-154">xsd:string</span></span>  <br/> |<span data-ttu-id="8de3b-155">opcional</span><span class="sxs-lookup"><span data-stu-id="8de3b-155">optional</span></span>  <br/> |<span data-ttu-id="8de3b-156">Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, Control, Connection, Hyperlink y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="8de3b-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="8de3b-157">Una fila solo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="8de3b-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="8de3b-158">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8de3b-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8de3b-159">T</span><span class="sxs-lookup"><span data-stu-id="8de3b-159">T</span></span>  <br/> |<span data-ttu-id="8de3b-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8de3b-160">xsd:string</span></span>  <br/> |<span data-ttu-id="8de3b-161">opcional</span><span class="sxs-lookup"><span data-stu-id="8de3b-161">optional</span></span>  <br/> |<span data-ttu-id="8de3b-162">Especifica el tipo de la ruta geométrica representada por la fila y usada en la visualización de geometría.</span><span class="sxs-lookup"><span data-stu-id="8de3b-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="8de3b-163">El atributo T solo se usa para la sección Geometría.</span><span class="sxs-lookup"><span data-stu-id="8de3b-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="8de3b-164">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8de3b-164">Values of the xsd:string type.</span></span>  <br/> |
   

