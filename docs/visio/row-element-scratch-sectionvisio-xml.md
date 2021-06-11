---
title: Elemento Row (sección Scratch) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bdbaf263-ae57-2807-f100-8d590ab92927
description: Un área de trabajo para escribir y probar fórmulas a las que hacen referencia otras celdas.
ms.openlocfilehash: fb346785b9cb6539d970ae1bd1c44fc706bd657d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541004"
---
# <a name="row-element-scratch-section-visio-xml"></a><span data-ttu-id="9dbfa-103">Elemento Row (sección Scratch) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9dbfa-103">Row element (Scratch Section) (Visio XML)</span></span>

<span data-ttu-id="9dbfa-104">Un área de trabajo para escribir y probar fórmulas a las que hacen referencia otras celdas.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9dbfa-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9dbfa-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9dbfa-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="9dbfa-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9dbfa-107">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="9dbfa-107">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9dbfa-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9dbfa-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9dbfa-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9dbfa-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9dbfa-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9dbfa-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9dbfa-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="9dbfa-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9dbfa-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="9dbfa-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9dbfa-113">Definición</span><span class="sxs-lookup"><span data-stu-id="9dbfa-113">Definition</span></span>

```XML
< xs:element name="Row" type="ScratchRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9dbfa-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="9dbfa-114">Elements and attributes</span></span>

<span data-ttu-id="9dbfa-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9dbfa-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9dbfa-116">Parent elements</span></span>

|<span data-ttu-id="9dbfa-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9dbfa-117">**Element**</span></span>|<span data-ttu-id="9dbfa-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9dbfa-118">**Type**</span></span>|<span data-ttu-id="9dbfa-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9dbfa-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9dbfa-120">Section</span><span class="sxs-lookup"><span data-stu-id="9dbfa-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9dbfa-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="9dbfa-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9dbfa-122">Un área de trabajo para escribir y probar fórmulas a las que hacen referencia otras celdas.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-122">A work area for entering and testing formulas that can be referred to by other cells.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9dbfa-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9dbfa-123">Child elements</span></span>

|<span data-ttu-id="9dbfa-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9dbfa-124">**Element**</span></span>|<span data-ttu-id="9dbfa-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9dbfa-125">**Type**</span></span>|<span data-ttu-id="9dbfa-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9dbfa-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9dbfa-127">Cell</span><span class="sxs-lookup"><span data-stu-id="9dbfa-127">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="9dbfa-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="9dbfa-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9dbfa-129">Especifica una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9dbfa-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="9dbfa-130">Attributes</span></span>

|<span data-ttu-id="9dbfa-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9dbfa-131">**Attribute**</span></span>|<span data-ttu-id="9dbfa-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9dbfa-132">**Type**</span></span>|<span data-ttu-id="9dbfa-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="9dbfa-133">**Required**</span></span>|<span data-ttu-id="9dbfa-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9dbfa-134">**Description**</span></span>|<span data-ttu-id="9dbfa-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="9dbfa-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9dbfa-136">Del</span><span class="sxs-lookup"><span data-stu-id="9dbfa-136">Del</span></span>  <br/> |<span data-ttu-id="9dbfa-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9dbfa-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9dbfa-138">opcional</span><span class="sxs-lookup"><span data-stu-id="9dbfa-138">optional</span></span>  <br/> |<span data-ttu-id="9dbfa-139">Especifica si se ha eliminado una fila que se heredaría de una forma maestra.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="9dbfa-140">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9dbfa-141">IX</span><span class="sxs-lookup"><span data-stu-id="9dbfa-141">IX</span></span>  <br/> |<span data-ttu-id="9dbfa-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9dbfa-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9dbfa-143">opcional</span><span class="sxs-lookup"><span data-stu-id="9dbfa-143">optional</span></span>  <br/> |<span data-ttu-id="9dbfa-144">Especifica el identificador único de la fila.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="9dbfa-145">Debe ser unqiue y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch y Tabs.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="9dbfa-146">Una fila solo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="9dbfa-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9dbfa-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="9dbfa-148">LocalName</span></span>  <br/> |<span data-ttu-id="9dbfa-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9dbfa-149">xsd:string</span></span>  <br/> |<span data-ttu-id="9dbfa-150">opcional</span><span class="sxs-lookup"><span data-stu-id="9dbfa-150">optional</span></span>  <br/> |<span data-ttu-id="9dbfa-151">Especifica el nombre único dependiente del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="9dbfa-152">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9dbfa-153">N</span><span class="sxs-lookup"><span data-stu-id="9dbfa-153">N</span></span>  <br/> |<span data-ttu-id="9dbfa-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9dbfa-154">xsd:string</span></span>  <br/> |<span data-ttu-id="9dbfa-155">opcional</span><span class="sxs-lookup"><span data-stu-id="9dbfa-155">optional</span></span>  <br/> |<span data-ttu-id="9dbfa-156">Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, Control, Connection, Hyperlink y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="9dbfa-157">Una fila solo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="9dbfa-158">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9dbfa-159">T</span><span class="sxs-lookup"><span data-stu-id="9dbfa-159">T</span></span>  <br/> |<span data-ttu-id="9dbfa-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9dbfa-160">xsd:string</span></span>  <br/> |<span data-ttu-id="9dbfa-161">opcional</span><span class="sxs-lookup"><span data-stu-id="9dbfa-161">optional</span></span>  <br/> |<span data-ttu-id="9dbfa-162">Especifica el tipo de la ruta geométrica representada por la fila y usada en la visualización de geometría.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="9dbfa-163">El atributo T solo se usa para la sección Geometría.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="9dbfa-164">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9dbfa-164">Values of the xsd:string type.</span></span>  <br/> |
   

