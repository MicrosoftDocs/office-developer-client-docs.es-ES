---
title: Elemento Row (sección etiqueta de acción) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 54c3315f-770f-6995-d0d8-ab66e4fe10d9
description: Define una etiqueta de acción en una forma o página.
ms.openlocfilehash: 44008d43871bfec9b5b943f19ce6ce0a069323d7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540430"
---
# <a name="row-element-action-tag-section-visio-xml"></a><span data-ttu-id="95edb-103">Elemento Row (sección etiqueta de acción) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="95edb-103">Row element (Action Tag Section) (Visio XML)</span></span>

<span data-ttu-id="95edb-104">Define una etiqueta de acción en una forma o página.</span><span class="sxs-lookup"><span data-stu-id="95edb-104">Defines an action tag on a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95edb-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="95edb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95edb-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="95edb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="95edb-107">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="95edb-107">ActionTagRow_Type</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="95edb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="95edb-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="95edb-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="95edb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="95edb-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="95edb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="95edb-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="95edb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="95edb-112">Masters. XML, Master #. XML, Pages. XML, página #. XML</span><span class="sxs-lookup"><span data-stu-id="95edb-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="95edb-113">Definición</span><span class="sxs-lookup"><span data-stu-id="95edb-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionTagRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="95edb-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="95edb-114">Elements and attributes</span></span>

<span data-ttu-id="95edb-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="95edb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="95edb-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="95edb-116">Parent elements</span></span>

|<span data-ttu-id="95edb-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="95edb-117">**Element**</span></span>|<span data-ttu-id="95edb-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="95edb-118">**Type**</span></span>|<span data-ttu-id="95edb-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95edb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95edb-120">Section</span><span class="sxs-lookup"><span data-stu-id="95edb-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="95edb-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="95edb-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="95edb-122">Define una etiqueta de acción en una forma o página.</span><span class="sxs-lookup"><span data-stu-id="95edb-122">Defines an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="95edb-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="95edb-123">Child elements</span></span>

|<span data-ttu-id="95edb-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="95edb-124">**Element**</span></span>|<span data-ttu-id="95edb-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="95edb-125">**Type**</span></span>|<span data-ttu-id="95edb-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95edb-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95edb-127">Cell</span><span class="sxs-lookup"><span data-stu-id="95edb-127">Cell</span></span>](cell-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="95edb-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="95edb-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="95edb-129">Define una propiedad para una etiqueta de acción en una forma o una página.</span><span class="sxs-lookup"><span data-stu-id="95edb-129">Defines one property for an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="95edb-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="95edb-130">Attributes</span></span>

|<span data-ttu-id="95edb-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="95edb-131">**Attribute**</span></span>|<span data-ttu-id="95edb-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="95edb-132">**Type**</span></span>|<span data-ttu-id="95edb-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="95edb-133">**Required**</span></span>|<span data-ttu-id="95edb-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95edb-134">**Description**</span></span>|<span data-ttu-id="95edb-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="95edb-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="95edb-136">Del</span><span class="sxs-lookup"><span data-stu-id="95edb-136">Del</span></span>  <br/> |<span data-ttu-id="95edb-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="95edb-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="95edb-138">opcional</span><span class="sxs-lookup"><span data-stu-id="95edb-138">optional</span></span>  <br/> |<span data-ttu-id="95edb-139">Especifica si se ha eliminado una fila que, de lo contrario, se heredaría de una forma de patrón.</span><span class="sxs-lookup"><span data-stu-id="95edb-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="95edb-140">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="95edb-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="95edb-141">IX</span><span class="sxs-lookup"><span data-stu-id="95edb-141">IX</span></span>  <br/> |<span data-ttu-id="95edb-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="95edb-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="95edb-143">opcional</span><span class="sxs-lookup"><span data-stu-id="95edb-143">optional</span></span>  <br/> |<span data-ttu-id="95edb-144">Especifica el identificador de base uno de la fila.</span><span class="sxs-lookup"><span data-stu-id="95edb-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="95edb-145">Debe ser único y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch y Tabs.</span><span class="sxs-lookup"><span data-stu-id="95edb-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="95edb-146">Una fila sólo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="95edb-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="95edb-147">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="95edb-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="95edb-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="95edb-148">LocalName</span></span>  <br/> |<span data-ttu-id="95edb-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="95edb-149">xsd:string</span></span>  <br/> |<span data-ttu-id="95edb-150">opcional</span><span class="sxs-lookup"><span data-stu-id="95edb-150">optional</span></span>  <br/> |<span data-ttu-id="95edb-151">Especifica el nombre único dependiente del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="95edb-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="95edb-152">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="95edb-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="95edb-153">N</span><span class="sxs-lookup"><span data-stu-id="95edb-153">N</span></span>  <br/> |<span data-ttu-id="95edb-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="95edb-154">xsd:string</span></span>  <br/> |<span data-ttu-id="95edb-155">opcional</span><span class="sxs-lookup"><span data-stu-id="95edb-155">optional</span></span>  <br/> |<span data-ttu-id="95edb-156">Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, control, Connection, HYPERLINK y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="95edb-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="95edb-157">Una fila sólo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="95edb-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="95edb-158">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="95edb-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="95edb-159">T</span><span class="sxs-lookup"><span data-stu-id="95edb-159">T</span></span>  <br/> |<span data-ttu-id="95edb-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="95edb-160">xsd:string</span></span>  <br/> |<span data-ttu-id="95edb-161">opcional</span><span class="sxs-lookup"><span data-stu-id="95edb-161">optional</span></span>  <br/> |<span data-ttu-id="95edb-162">Especifica el tipo de la ruta geométrica representada por la fila y utilizada en la visualización de geometría.</span><span class="sxs-lookup"><span data-stu-id="95edb-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="95edb-163">El atributo T solo se usa para la sección Geometry.</span><span class="sxs-lookup"><span data-stu-id="95edb-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="95edb-164">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="95edb-164">Values of the xsd:string type.</span></span>  <br/> |
   

