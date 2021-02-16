---
title: Elemento Row (Sección de celdas definidas por el usuario) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9fc27888-2809-aa29-4dbb-7e4f8a0c4758
description: Información especificada por el usuario a la que pueden hacer referencia otras celdas y herramientas de complementos.
ms.openlocfilehash: 1573fd6ab27cc1dbec9559552ec33d9a4ad19fd2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538175"
---
# <a name="row-element-user-defined-cells-section-visio-xml"></a><span data-ttu-id="c6e04-103">Elemento Row (Sección de celdas definidas por el usuario) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="c6e04-103">Row element (User-defined Cells Section) (Visio XML)</span></span>

<span data-ttu-id="c6e04-104">Información especificada por el usuario a la que pueden hacer referencia otras celdas y herramientas de complementos.</span><span class="sxs-lookup"><span data-stu-id="c6e04-104">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c6e04-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c6e04-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6e04-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="c6e04-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c6e04-107">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="c6e04-107">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c6e04-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c6e04-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c6e04-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c6e04-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c6e04-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c6e04-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c6e04-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="c6e04-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c6e04-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="c6e04-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c6e04-113">Definición</span><span class="sxs-lookup"><span data-stu-id="c6e04-113">Definition</span></span>

```XML
< xs:element name="Row" type="UserRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c6e04-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c6e04-114">Elements and attributes</span></span>

<span data-ttu-id="c6e04-115">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="c6e04-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c6e04-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c6e04-116">Parent elements</span></span>

|<span data-ttu-id="c6e04-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c6e04-117">**Element**</span></span>|<span data-ttu-id="c6e04-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c6e04-118">**Type**</span></span>|<span data-ttu-id="c6e04-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c6e04-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c6e04-120">Section</span><span class="sxs-lookup"><span data-stu-id="c6e04-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c6e04-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="c6e04-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c6e04-122">Información especificada por el usuario a la que pueden hacer referencia otras celdas y herramientas de complementos.</span><span class="sxs-lookup"><span data-stu-id="c6e04-122">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c6e04-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c6e04-123">Child elements</span></span>

|<span data-ttu-id="c6e04-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c6e04-124">**Element**</span></span>|<span data-ttu-id="c6e04-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c6e04-125">**Type**</span></span>|<span data-ttu-id="c6e04-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c6e04-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c6e04-127">Cell</span><span class="sxs-lookup"><span data-stu-id="c6e04-127">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="c6e04-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c6e04-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c6e04-129">Una propiedad de una información especificada por el usuario a la que pueden hacer referencia otras celdas y herramientas de complementos.</span><span class="sxs-lookup"><span data-stu-id="c6e04-129">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c6e04-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="c6e04-130">Attributes</span></span>

|<span data-ttu-id="c6e04-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c6e04-131">**Attribute**</span></span>|<span data-ttu-id="c6e04-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c6e04-132">**Type**</span></span>|<span data-ttu-id="c6e04-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="c6e04-133">**Required**</span></span>|<span data-ttu-id="c6e04-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c6e04-134">**Description**</span></span>|<span data-ttu-id="c6e04-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="c6e04-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c6e04-136">Supr</span><span class="sxs-lookup"><span data-stu-id="c6e04-136">Del</span></span>  <br/> |<span data-ttu-id="c6e04-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c6e04-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c6e04-138">opcional</span><span class="sxs-lookup"><span data-stu-id="c6e04-138">optional</span></span>  <br/> |<span data-ttu-id="c6e04-139">Especifica si se ha eliminado una fila que se heredaría de una forma maestra.</span><span class="sxs-lookup"><span data-stu-id="c6e04-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="c6e04-140">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c6e04-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c6e04-141">IX</span><span class="sxs-lookup"><span data-stu-id="c6e04-141">IX</span></span>  <br/> |<span data-ttu-id="c6e04-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c6e04-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c6e04-143">opcional</span><span class="sxs-lookup"><span data-stu-id="c6e04-143">optional</span></span>  <br/> |<span data-ttu-id="c6e04-144">Especifica el identificador basado en uno de la fila.</span><span class="sxs-lookup"><span data-stu-id="c6e04-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="c6e04-145">Debe ser distinto y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch y Tabs.</span><span class="sxs-lookup"><span data-stu-id="c6e04-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="c6e04-146">Una fila solo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="c6e04-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="c6e04-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c6e04-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c6e04-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="c6e04-148">LocalName</span></span>  <br/> |<span data-ttu-id="c6e04-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c6e04-149">xsd:string</span></span>  <br/> |<span data-ttu-id="c6e04-150">opcional</span><span class="sxs-lookup"><span data-stu-id="c6e04-150">optional</span></span>  <br/> |<span data-ttu-id="c6e04-151">Especifica el nombre único dependiente del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="c6e04-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="c6e04-152">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c6e04-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c6e04-153">N</span><span class="sxs-lookup"><span data-stu-id="c6e04-153">N</span></span>  <br/> |<span data-ttu-id="c6e04-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c6e04-154">xsd:string</span></span>  <br/> |<span data-ttu-id="c6e04-155">opcional</span><span class="sxs-lookup"><span data-stu-id="c6e04-155">optional</span></span>  <br/> |<span data-ttu-id="c6e04-156">Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, Control, Connection, Hyperlink y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="c6e04-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="c6e04-157">Una fila solo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="c6e04-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="c6e04-158">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c6e04-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c6e04-159">T</span><span class="sxs-lookup"><span data-stu-id="c6e04-159">T</span></span>  <br/> |<span data-ttu-id="c6e04-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c6e04-160">xsd:string</span></span>  <br/> |<span data-ttu-id="c6e04-161">opcional</span><span class="sxs-lookup"><span data-stu-id="c6e04-161">optional</span></span>  <br/> |<span data-ttu-id="c6e04-162">Especifica el tipo de la ruta geométrica representada por la fila y usada en la visualización de geometría.</span><span class="sxs-lookup"><span data-stu-id="c6e04-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="c6e04-163">El atributo T solo se usa para la sección Geometría.</span><span class="sxs-lookup"><span data-stu-id="c6e04-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="c6e04-164">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c6e04-164">Values of the xsd:string type.</span></span>  <br/> |
   

