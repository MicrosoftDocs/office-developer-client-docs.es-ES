---
title: Elemento Row (sección degradado de línea) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d823766-5cb0-925c-f622-18025f44426c
description: Contiene el color, la transparencia y la posición de un punto de degradado de un degradado de línea.
ms.openlocfilehash: 105d93344343f223a6b5d909f1174f7df56ffb4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358432"
---
# <a name="row-element-line-gradient-section-visio-xml"></a><span data-ttu-id="c1992-103">Elemento Row (sección degradado de línea) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="c1992-103">Row element (Line Gradient Section) ('Visio XML')</span></span>

<span data-ttu-id="c1992-104">Contiene el color, la transparencia y la posición de un punto de degradado de un degradado de línea.</span><span class="sxs-lookup"><span data-stu-id="c1992-104">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1992-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c1992-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1992-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="c1992-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c1992-107">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="c1992-107">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c1992-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c1992-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c1992-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c1992-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c1992-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="c1992-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c1992-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="c1992-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c1992-112">Document. XML, Master #. XML, página #. XML</span><span class="sxs-lookup"><span data-stu-id="c1992-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c1992-113">Definición</span><span class="sxs-lookup"><span data-stu-id="c1992-113">Definition</span></span>

```XML
< xs:element name="Row" type="LineGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c1992-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c1992-114">Elements and attributes</span></span>

<span data-ttu-id="c1992-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="c1992-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c1992-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c1992-116">Parent elements</span></span>

|<span data-ttu-id="c1992-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c1992-117">**Element**</span></span>|<span data-ttu-id="c1992-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c1992-118">**Type**</span></span>|<span data-ttu-id="c1992-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1992-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c1992-120">Section</span><span class="sxs-lookup"><span data-stu-id="c1992-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c1992-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="c1992-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1992-122">Contiene el color, la transparencia y la posición de un punto de degradado de un degradado de línea.</span><span class="sxs-lookup"><span data-stu-id="c1992-122">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c1992-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c1992-123">Child elements</span></span>

|<span data-ttu-id="c1992-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c1992-124">**Element**</span></span>|<span data-ttu-id="c1992-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c1992-125">**Type**</span></span>|<span data-ttu-id="c1992-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1992-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c1992-127">Cell</span><span class="sxs-lookup"><span data-stu-id="c1992-127">Cell</span></span>](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="c1992-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c1992-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1992-129">Especifica una propiedad única.</span><span class="sxs-lookup"><span data-stu-id="c1992-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c1992-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="c1992-130">Attributes</span></span>

|<span data-ttu-id="c1992-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c1992-131">**Attribute**</span></span>|<span data-ttu-id="c1992-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c1992-132">**Type**</span></span>|<span data-ttu-id="c1992-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="c1992-133">**Required**</span></span>|<span data-ttu-id="c1992-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1992-134">**Description**</span></span>|<span data-ttu-id="c1992-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="c1992-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c1992-136">Del</span><span class="sxs-lookup"><span data-stu-id="c1992-136">Del</span></span>  <br/> |<span data-ttu-id="c1992-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="c1992-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c1992-138">opcional</span><span class="sxs-lookup"><span data-stu-id="c1992-138">optional</span></span>  <br/> |<span data-ttu-id="c1992-139">Especifica si se ha eliminado una fila que, de lo contrario, se heredaría de una forma de patrón.</span><span class="sxs-lookup"><span data-stu-id="c1992-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="c1992-140">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="c1992-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c1992-141">IX</span><span class="sxs-lookup"><span data-stu-id="c1992-141">IX</span></span>  <br/> |<span data-ttu-id="c1992-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c1992-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c1992-143">opcional</span><span class="sxs-lookup"><span data-stu-id="c1992-143">optional</span></span>  <br/> |<span data-ttu-id="c1992-144">Especifica el identificador de base uno de la fila.</span><span class="sxs-lookup"><span data-stu-id="c1992-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="c1992-145">Debe ser único y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, paraGraph, Reviewer, Scratch y Tabs.</span><span class="sxs-lookup"><span data-stu-id="c1992-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="c1992-146">Una fila sólo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="c1992-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="c1992-147">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c1992-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c1992-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="c1992-148">LocalName</span></span>  <br/> |<span data-ttu-id="c1992-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c1992-149">xsd:string</span></span>  <br/> |<span data-ttu-id="c1992-150">opcional</span><span class="sxs-lookup"><span data-stu-id="c1992-150">optional</span></span>  <br/> |<span data-ttu-id="c1992-151">Especifica el nombre único dependiente del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="c1992-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="c1992-152">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c1992-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c1992-153">N</span><span class="sxs-lookup"><span data-stu-id="c1992-153">N</span></span>  <br/> |<span data-ttu-id="c1992-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c1992-154">xsd:string</span></span>  <br/> |<span data-ttu-id="c1992-155">opcional</span><span class="sxs-lookup"><span data-stu-id="c1992-155">optional</span></span>  <br/> |<span data-ttu-id="c1992-156">Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, control, Connection, HYPERLINK y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="c1992-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="c1992-157">Una fila sólo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="c1992-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="c1992-158">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c1992-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c1992-159">T</span><span class="sxs-lookup"><span data-stu-id="c1992-159">T</span></span>  <br/> |<span data-ttu-id="c1992-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c1992-160">xsd:string</span></span>  <br/> |<span data-ttu-id="c1992-161">opcional</span><span class="sxs-lookup"><span data-stu-id="c1992-161">optional</span></span>  <br/> |<span data-ttu-id="c1992-162">Especifica el tipo de la ruta geométrica representada por la fila y utilizada en la visualización de geometría.</span><span class="sxs-lookup"><span data-stu-id="c1992-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="c1992-163">El atributo T solo se usa para la sección Geometry.</span><span class="sxs-lookup"><span data-stu-id="c1992-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="c1992-164">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c1992-164">Values of the xsd:string type.</span></span>  <br/> |
   

