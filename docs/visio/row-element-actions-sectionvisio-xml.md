---
title: Elemento Row (sección Actions) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5141589b-10f3-f908-56d2-206244f449fb
description: Contiene filas que describen los elementos de menú en un menú contextual o de etiqueta de acción para una forma o página.
ms.openlocfilehash: dfe23aa7d635fc09d625c414e5548a0166384fbb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540416"
---
# <a name="row-element-actions-section-visio-xml"></a><span data-ttu-id="b5283-103">Elemento Row (sección Actions) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b5283-103">Row element (Actions Section) (Visio XML)</span></span>

<span data-ttu-id="b5283-104">Contiene filas que describen los elementos de menú en un menú contextual o de etiqueta de acción para una forma o página.</span><span class="sxs-lookup"><span data-stu-id="b5283-104">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5283-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b5283-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5283-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="b5283-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b5283-107">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="b5283-107">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b5283-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b5283-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b5283-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b5283-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b5283-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b5283-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b5283-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="b5283-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b5283-112">masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="b5283-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b5283-113">Definición</span><span class="sxs-lookup"><span data-stu-id="b5283-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b5283-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b5283-114">Elements and attributes</span></span>

<span data-ttu-id="b5283-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="b5283-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b5283-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b5283-116">Parent elements</span></span>

|<span data-ttu-id="b5283-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b5283-117">**Element**</span></span>|<span data-ttu-id="b5283-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b5283-118">**Type**</span></span>|<span data-ttu-id="b5283-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5283-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b5283-120">Section</span><span class="sxs-lookup"><span data-stu-id="b5283-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b5283-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="b5283-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b5283-122">Contiene filas que describen los elementos de menú en un menú contextual o de etiqueta de acción para una forma o página.</span><span class="sxs-lookup"><span data-stu-id="b5283-122">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b5283-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b5283-123">Child elements</span></span>

|<span data-ttu-id="b5283-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b5283-124">**Element**</span></span>|<span data-ttu-id="b5283-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b5283-125">**Type**</span></span>|<span data-ttu-id="b5283-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5283-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b5283-127">Cell</span><span class="sxs-lookup"><span data-stu-id="b5283-127">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="b5283-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="b5283-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b5283-129">Especifica una propiedad de una acción asociada a un comando personalizado en un menú de etiquetas de acción o acceso directo.</span><span class="sxs-lookup"><span data-stu-id="b5283-129">Specifies one property of an action associated with a custom command on a shortcut or action tag menu.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b5283-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="b5283-130">Attributes</span></span>

|<span data-ttu-id="b5283-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b5283-131">**Attribute**</span></span>|<span data-ttu-id="b5283-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b5283-132">**Type**</span></span>|<span data-ttu-id="b5283-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="b5283-133">**Required**</span></span>|<span data-ttu-id="b5283-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5283-134">**Description**</span></span>|<span data-ttu-id="b5283-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="b5283-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b5283-136">Del</span><span class="sxs-lookup"><span data-stu-id="b5283-136">Del</span></span>  <br/> |<span data-ttu-id="b5283-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="b5283-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b5283-138">opcional</span><span class="sxs-lookup"><span data-stu-id="b5283-138">optional</span></span>  <br/> |<span data-ttu-id="b5283-139">Especifica si se ha eliminado una fila que se heredaría de una forma maestra.</span><span class="sxs-lookup"><span data-stu-id="b5283-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="b5283-140">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="b5283-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="b5283-141">IX</span><span class="sxs-lookup"><span data-stu-id="b5283-141">IX</span></span>  <br/> |<span data-ttu-id="b5283-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b5283-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b5283-143">opcional</span><span class="sxs-lookup"><span data-stu-id="b5283-143">optional</span></span>  <br/> |<span data-ttu-id="b5283-144">Especifica el identificador único de la fila.</span><span class="sxs-lookup"><span data-stu-id="b5283-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="b5283-145">Debe ser unqiue y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch y Tabs.</span><span class="sxs-lookup"><span data-stu-id="b5283-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="b5283-146">Una fila solo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="b5283-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="b5283-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b5283-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b5283-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="b5283-148">LocalName</span></span>  <br/> |<span data-ttu-id="b5283-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b5283-149">xsd:string</span></span>  <br/> |<span data-ttu-id="b5283-150">opcional</span><span class="sxs-lookup"><span data-stu-id="b5283-150">optional</span></span>  <br/> |<span data-ttu-id="b5283-151">Especifica el nombre único dependiente del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="b5283-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="b5283-152">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b5283-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b5283-153">N</span><span class="sxs-lookup"><span data-stu-id="b5283-153">N</span></span>  <br/> |<span data-ttu-id="b5283-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b5283-154">xsd:string</span></span>  <br/> |<span data-ttu-id="b5283-155">opcional</span><span class="sxs-lookup"><span data-stu-id="b5283-155">optional</span></span>  <br/> |<span data-ttu-id="b5283-156">Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, Control, Connection, Hyperlink y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="b5283-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="b5283-157">Una fila solo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="b5283-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="b5283-158">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b5283-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b5283-159">T</span><span class="sxs-lookup"><span data-stu-id="b5283-159">T</span></span>  <br/> |<span data-ttu-id="b5283-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b5283-160">xsd:string</span></span>  <br/> |<span data-ttu-id="b5283-161">opcional</span><span class="sxs-lookup"><span data-stu-id="b5283-161">optional</span></span>  <br/> |<span data-ttu-id="b5283-162">Especifica el tipo de la ruta geométrica representada por la fila y usada en la visualización de geometría.</span><span class="sxs-lookup"><span data-stu-id="b5283-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="b5283-163">El atributo T solo se usa para la sección Geometría.</span><span class="sxs-lookup"><span data-stu-id="b5283-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="b5283-164">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b5283-164">Values of the xsd:string type.</span></span>  <br/> |
   

