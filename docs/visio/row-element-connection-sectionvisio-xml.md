---
title: Elemento Row (sección conexión) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f44fc18-4757-7aba-8778-a474ab93a78d
description: Contiene las coordenadas x o y, la dirección horizontal y vertical y el tipo de un único punto de conexión de una forma.
ms.openlocfilehash: 9f8f5f0735f7eeff2f1b2ec4562b79e6550d1716
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358581"
---
# <a name="row-element-connection-section-visio-xml"></a><span data-ttu-id="e931f-103">Elemento Row (sección conexión) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="e931f-103">Row element (Connection Section) ('Visio XML')</span></span>

<span data-ttu-id="e931f-104">Contiene las coordenadas x o y, la dirección horizontal y vertical y el tipo de un único punto de conexión de una forma.</span><span class="sxs-lookup"><span data-stu-id="e931f-104">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e931f-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e931f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e931f-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="e931f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e931f-107">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="e931f-107">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e931f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e931f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e931f-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e931f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e931f-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="e931f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e931f-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="e931f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e931f-112">Master #. XML, página #. XML</span><span class="sxs-lookup"><span data-stu-id="e931f-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e931f-113">Definición</span><span class="sxs-lookup"><span data-stu-id="e931f-113">Definition</span></span>

```XML
< xs:element name="Row" type="ConnectionRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e931f-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e931f-114">Elements and attributes</span></span>

<span data-ttu-id="e931f-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="e931f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e931f-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e931f-116">Parent elements</span></span>

|<span data-ttu-id="e931f-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e931f-117">**Element**</span></span>|<span data-ttu-id="e931f-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e931f-118">**Type**</span></span>|<span data-ttu-id="e931f-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e931f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e931f-120">Section</span><span class="sxs-lookup"><span data-stu-id="e931f-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e931f-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="e931f-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e931f-122">Contiene las coordenadas x o y, la dirección horizontal y vertical y el tipo de un único punto de conexión de una forma.</span><span class="sxs-lookup"><span data-stu-id="e931f-122">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e931f-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e931f-123">Child elements</span></span>

|<span data-ttu-id="e931f-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e931f-124">**Element**</span></span>|<span data-ttu-id="e931f-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e931f-125">**Type**</span></span>|<span data-ttu-id="e931f-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e931f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e931f-127">Cell</span><span class="sxs-lookup"><span data-stu-id="e931f-127">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="e931f-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e931f-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e931f-129">Especifica una propiedad única.</span><span class="sxs-lookup"><span data-stu-id="e931f-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e931f-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="e931f-130">Attributes</span></span>

|<span data-ttu-id="e931f-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="e931f-131">**Attribute**</span></span>|<span data-ttu-id="e931f-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e931f-132">**Type**</span></span>|<span data-ttu-id="e931f-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="e931f-133">**Required**</span></span>|<span data-ttu-id="e931f-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e931f-134">**Description**</span></span>|<span data-ttu-id="e931f-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="e931f-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e931f-136">Del</span><span class="sxs-lookup"><span data-stu-id="e931f-136">Del</span></span>  <br/> |<span data-ttu-id="e931f-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="e931f-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e931f-138">opcional</span><span class="sxs-lookup"><span data-stu-id="e931f-138">optional</span></span>  <br/> |<span data-ttu-id="e931f-139">Especifica si se ha eliminado una fila que, de lo contrario, se heredaría de una forma de patrón.</span><span class="sxs-lookup"><span data-stu-id="e931f-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="e931f-140">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="e931f-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e931f-141">IX</span><span class="sxs-lookup"><span data-stu-id="e931f-141">IX</span></span>  <br/> |<span data-ttu-id="e931f-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e931f-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e931f-143">opcional</span><span class="sxs-lookup"><span data-stu-id="e931f-143">optional</span></span>  <br/> |<span data-ttu-id="e931f-144">Especifica el identificador de base uno de la fila.</span><span class="sxs-lookup"><span data-stu-id="e931f-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="e931f-145">Debe ser único y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, paraGraph, Reviewer, Scratch y Tabs.</span><span class="sxs-lookup"><span data-stu-id="e931f-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="e931f-146">Una fila sólo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="e931f-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="e931f-147">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e931f-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e931f-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="e931f-148">LocalName</span></span>  <br/> |<span data-ttu-id="e931f-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e931f-149">xsd:string</span></span>  <br/> |<span data-ttu-id="e931f-150">opcional</span><span class="sxs-lookup"><span data-stu-id="e931f-150">optional</span></span>  <br/> |<span data-ttu-id="e931f-151">Especifica el nombre único dependiente del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="e931f-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="e931f-152">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e931f-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e931f-153">N</span><span class="sxs-lookup"><span data-stu-id="e931f-153">N</span></span>  <br/> |<span data-ttu-id="e931f-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e931f-154">xsd:string</span></span>  <br/> |<span data-ttu-id="e931f-155">opcional</span><span class="sxs-lookup"><span data-stu-id="e931f-155">optional</span></span>  <br/> |<span data-ttu-id="e931f-156">Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, control, Connection, HYPERLINK y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="e931f-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="e931f-157">Una fila sólo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="e931f-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="e931f-158">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e931f-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e931f-159">T</span><span class="sxs-lookup"><span data-stu-id="e931f-159">T</span></span>  <br/> |<span data-ttu-id="e931f-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e931f-160">xsd:string</span></span>  <br/> |<span data-ttu-id="e931f-161">opcional</span><span class="sxs-lookup"><span data-stu-id="e931f-161">optional</span></span>  <br/> |<span data-ttu-id="e931f-162">Especifica el tipo de la ruta geométrica representada por la fila y utilizada en la visualización de geometría.</span><span class="sxs-lookup"><span data-stu-id="e931f-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="e931f-163">El atributo T solo se usa para la sección Geometry.</span><span class="sxs-lookup"><span data-stu-id="e931f-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="e931f-164">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e931f-164">Values of the xsd:string type.</span></span>  <br/> |
   

