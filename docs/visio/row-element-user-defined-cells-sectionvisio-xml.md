---
title: Elemento Row (sección celdas definidas por el usuario) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9fc27888-2809-aa29-4dbb-7e4f8a0c4758
description: Información especificada por el usuario a la que se puede hacer referencia en otras celdas y herramientas complementarias.
ms.openlocfilehash: 8852c1db31e9a9b8f0860c111da32de6d44dc7f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332490"
---
# <a name="row-element-user-defined-cells-section-visio-xml"></a><span data-ttu-id="58a77-103">Elemento Row (sección celdas definidas por el usuario) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="58a77-103">Row element (User-defined Cells Section) ('Visio XML')</span></span>

<span data-ttu-id="58a77-104">Información especificada por el usuario a la que se puede hacer referencia en otras celdas y herramientas complementarias.</span><span class="sxs-lookup"><span data-stu-id="58a77-104">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58a77-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="58a77-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58a77-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="58a77-106">**Element type**</span></span> <br/> |[<span data-ttu-id="58a77-107">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="58a77-107">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="58a77-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="58a77-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="58a77-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="58a77-109">**Schema file**</span></span> <br/> |<span data-ttu-id="58a77-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="58a77-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="58a77-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="58a77-111">**Document parts**</span></span> <br/> |<span data-ttu-id="58a77-112">Document. XML, Masters. XML, Master #. XML, Pages. XML, página #. XML</span><span class="sxs-lookup"><span data-stu-id="58a77-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="58a77-113">Definición</span><span class="sxs-lookup"><span data-stu-id="58a77-113">Definition</span></span>

```XML
< xs:element name="Row" type="UserRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="58a77-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="58a77-114">Elements and attributes</span></span>

<span data-ttu-id="58a77-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="58a77-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="58a77-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="58a77-116">Parent elements</span></span>

|<span data-ttu-id="58a77-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="58a77-117">**Element**</span></span>|<span data-ttu-id="58a77-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="58a77-118">**Type**</span></span>|<span data-ttu-id="58a77-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="58a77-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="58a77-120">Section</span><span class="sxs-lookup"><span data-stu-id="58a77-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="58a77-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="58a77-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="58a77-122">Información especificada por el usuario a la que se puede hacer referencia en otras celdas y herramientas complementarias.</span><span class="sxs-lookup"><span data-stu-id="58a77-122">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="58a77-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="58a77-123">Child elements</span></span>

|<span data-ttu-id="58a77-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="58a77-124">**Element**</span></span>|<span data-ttu-id="58a77-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="58a77-125">**Type**</span></span>|<span data-ttu-id="58a77-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="58a77-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="58a77-127">Cell</span><span class="sxs-lookup"><span data-stu-id="58a77-127">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="58a77-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="58a77-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="58a77-129">Una propiedad de una información especificada por el usuario a la que se puede hacer referencia por otras celdas y herramientas complementarias.</span><span class="sxs-lookup"><span data-stu-id="58a77-129">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="58a77-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="58a77-130">Attributes</span></span>

|<span data-ttu-id="58a77-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="58a77-131">**Attribute**</span></span>|<span data-ttu-id="58a77-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="58a77-132">**Type**</span></span>|<span data-ttu-id="58a77-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="58a77-133">**Required**</span></span>|<span data-ttu-id="58a77-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="58a77-134">**Description**</span></span>|<span data-ttu-id="58a77-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="58a77-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="58a77-136">Del</span><span class="sxs-lookup"><span data-stu-id="58a77-136">Del</span></span>  <br/> |<span data-ttu-id="58a77-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="58a77-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="58a77-138">opcional</span><span class="sxs-lookup"><span data-stu-id="58a77-138">optional</span></span>  <br/> |<span data-ttu-id="58a77-139">Especifica si se ha eliminado una fila que, de lo contrario, se heredaría de una forma de patrón.</span><span class="sxs-lookup"><span data-stu-id="58a77-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="58a77-140">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="58a77-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="58a77-141">IX</span><span class="sxs-lookup"><span data-stu-id="58a77-141">IX</span></span>  <br/> |<span data-ttu-id="58a77-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="58a77-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="58a77-143">opcional</span><span class="sxs-lookup"><span data-stu-id="58a77-143">optional</span></span>  <br/> |<span data-ttu-id="58a77-144">Especifica el identificador de base uno de la fila.</span><span class="sxs-lookup"><span data-stu-id="58a77-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="58a77-145">Debe ser único y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, paraGraph, Reviewer, Scratch y Tabs.</span><span class="sxs-lookup"><span data-stu-id="58a77-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="58a77-146">Una fila sólo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="58a77-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="58a77-147">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="58a77-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="58a77-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="58a77-148">LocalName</span></span>  <br/> |<span data-ttu-id="58a77-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="58a77-149">xsd:string</span></span>  <br/> |<span data-ttu-id="58a77-150">opcional</span><span class="sxs-lookup"><span data-stu-id="58a77-150">optional</span></span>  <br/> |<span data-ttu-id="58a77-151">Especifica el nombre único dependiente del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="58a77-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="58a77-152">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="58a77-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="58a77-153">N</span><span class="sxs-lookup"><span data-stu-id="58a77-153">N</span></span>  <br/> |<span data-ttu-id="58a77-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="58a77-154">xsd:string</span></span>  <br/> |<span data-ttu-id="58a77-155">opcional</span><span class="sxs-lookup"><span data-stu-id="58a77-155">optional</span></span>  <br/> |<span data-ttu-id="58a77-156">Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, control, Connection, HYPERLINK y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="58a77-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="58a77-157">Una fila sólo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="58a77-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="58a77-158">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="58a77-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="58a77-159">T</span><span class="sxs-lookup"><span data-stu-id="58a77-159">T</span></span>  <br/> |<span data-ttu-id="58a77-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="58a77-160">xsd:string</span></span>  <br/> |<span data-ttu-id="58a77-161">opcional</span><span class="sxs-lookup"><span data-stu-id="58a77-161">optional</span></span>  <br/> |<span data-ttu-id="58a77-162">Especifica el tipo de la ruta geométrica representada por la fila y utilizada en la visualización de geometría.</span><span class="sxs-lookup"><span data-stu-id="58a77-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="58a77-163">El atributo T solo se usa para la sección Geometry.</span><span class="sxs-lookup"><span data-stu-id="58a77-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="58a77-164">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="58a77-164">Values of the xsd:string type.</span></span>  <br/> |
   

