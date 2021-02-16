---
title: Elemento Row (Sección de degradado de relleno) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f216afb5-4393-6e1c-54c2-3c184a26d934
description: Contiene el color, la transparencia y la posición de un delimitador de degradado para un degradado de relleno.
ms.openlocfilehash: d9f3661d91b43bca7ff809c4e41a0c1257660e66
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538623"
---
# <a name="row-element-fill-gradient-section-visio-xml"></a><span data-ttu-id="fc354-103">Elemento Row (Sección de degradado de relleno) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="fc354-103">Row element (Fill Gradient Section) (Visio XML)</span></span>

<span data-ttu-id="fc354-104">Contiene el color, la transparencia y la posición de un delimitador de degradado para un degradado de relleno.</span><span class="sxs-lookup"><span data-stu-id="fc354-104">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fc354-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fc354-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc354-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="fc354-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fc354-107">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="fc354-107">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fc354-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fc354-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fc354-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fc354-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fc354-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="fc354-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fc354-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="fc354-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fc354-112">document.xml, master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="fc354-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fc354-113">Definición</span><span class="sxs-lookup"><span data-stu-id="fc354-113">Definition</span></span>

```XML
< xs:element name="Row" type="FillGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fc354-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="fc354-114">Elements and attributes</span></span>

<span data-ttu-id="fc354-115">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="fc354-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fc354-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fc354-116">Parent elements</span></span>

|<span data-ttu-id="fc354-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fc354-117">**Element**</span></span>|<span data-ttu-id="fc354-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fc354-118">**Type**</span></span>|<span data-ttu-id="fc354-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fc354-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fc354-120">Section</span><span class="sxs-lookup"><span data-stu-id="fc354-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fc354-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="fc354-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fc354-122">Contiene el color, la transparencia y la posición de un delimitador de degradado para un degradado de relleno.</span><span class="sxs-lookup"><span data-stu-id="fc354-122">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fc354-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fc354-123">Child elements</span></span>

|<span data-ttu-id="fc354-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fc354-124">**Element**</span></span>|<span data-ttu-id="fc354-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fc354-125">**Type**</span></span>|<span data-ttu-id="fc354-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fc354-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fc354-127">Cell</span><span class="sxs-lookup"><span data-stu-id="fc354-127">Cell</span></span>](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="fc354-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="fc354-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fc354-129">Especifica una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="fc354-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fc354-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="fc354-130">Attributes</span></span>

|<span data-ttu-id="fc354-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="fc354-131">**Attribute**</span></span>|<span data-ttu-id="fc354-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fc354-132">**Type**</span></span>|<span data-ttu-id="fc354-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="fc354-133">**Required**</span></span>|<span data-ttu-id="fc354-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fc354-134">**Description**</span></span>|<span data-ttu-id="fc354-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="fc354-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fc354-136">Supr</span><span class="sxs-lookup"><span data-stu-id="fc354-136">Del</span></span>  <br/> |<span data-ttu-id="fc354-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="fc354-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fc354-138">opcional</span><span class="sxs-lookup"><span data-stu-id="fc354-138">optional</span></span>  <br/> |<span data-ttu-id="fc354-139">Especifica si se ha eliminado una fila que se heredaría de una forma maestra.</span><span class="sxs-lookup"><span data-stu-id="fc354-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="fc354-140">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="fc354-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="fc354-141">IX</span><span class="sxs-lookup"><span data-stu-id="fc354-141">IX</span></span>  <br/> |<span data-ttu-id="fc354-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fc354-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fc354-143">opcional</span><span class="sxs-lookup"><span data-stu-id="fc354-143">optional</span></span>  <br/> |<span data-ttu-id="fc354-144">Especifica el identificador único de la fila.</span><span class="sxs-lookup"><span data-stu-id="fc354-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="fc354-145">Debe ser distinto y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch y Tabs.</span><span class="sxs-lookup"><span data-stu-id="fc354-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="fc354-146">Una fila solo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="fc354-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="fc354-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fc354-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fc354-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="fc354-148">LocalName</span></span>  <br/> |<span data-ttu-id="fc354-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fc354-149">xsd:string</span></span>  <br/> |<span data-ttu-id="fc354-150">opcional</span><span class="sxs-lookup"><span data-stu-id="fc354-150">optional</span></span>  <br/> |<span data-ttu-id="fc354-151">Especifica el nombre único dependiente del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="fc354-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="fc354-152">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fc354-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fc354-153">N</span><span class="sxs-lookup"><span data-stu-id="fc354-153">N</span></span>  <br/> |<span data-ttu-id="fc354-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fc354-154">xsd:string</span></span>  <br/> |<span data-ttu-id="fc354-155">opcional</span><span class="sxs-lookup"><span data-stu-id="fc354-155">optional</span></span>  <br/> |<span data-ttu-id="fc354-156">Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, Control, Connection, Hyperlink y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="fc354-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="fc354-157">Una fila solo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="fc354-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="fc354-158">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fc354-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fc354-159">T</span><span class="sxs-lookup"><span data-stu-id="fc354-159">T</span></span>  <br/> |<span data-ttu-id="fc354-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fc354-160">xsd:string</span></span>  <br/> |<span data-ttu-id="fc354-161">opcional</span><span class="sxs-lookup"><span data-stu-id="fc354-161">optional</span></span>  <br/> |<span data-ttu-id="fc354-162">Especifica el tipo de la ruta geométrica representada por la fila y usada en la visualización de geometría.</span><span class="sxs-lookup"><span data-stu-id="fc354-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="fc354-163">El atributo T solo se usa para la sección Geometría.</span><span class="sxs-lookup"><span data-stu-id="fc354-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="fc354-164">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fc354-164">Values of the xsd:string type.</span></span>  <br/> |
   

