---
title: Elemento Row (sección acciones) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5141589b-10f3-f908-56d2-206244f449fb
description: Contiene filas que describen los elementos de menú en un menú contextual o de etiqueta de acción para una forma o página.
ms.openlocfilehash: 509fd06a77419bf684b214ff5a5d16f24a1f4a84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2019
ms.locfileid: "32356423"
---
# <a name="row-element-actions-section-visio-xml"></a><span data-ttu-id="c11ed-103">Elemento Row (sección acciones) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="c11ed-103">Row element (Actions Section) ('Visio XML')</span></span>

<span data-ttu-id="c11ed-104">Contiene filas que describen los elementos de menú en un menú contextual o de etiqueta de acción para una forma o página.</span><span class="sxs-lookup"><span data-stu-id="c11ed-104">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c11ed-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c11ed-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c11ed-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="c11ed-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c11ed-107">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="c11ed-107">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c11ed-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c11ed-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c11ed-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c11ed-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c11ed-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="c11ed-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c11ed-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="c11ed-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c11ed-112">Masters. XML, Master #. XML, Pages. XML, página #. XML</span><span class="sxs-lookup"><span data-stu-id="c11ed-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c11ed-113">Definición</span><span class="sxs-lookup"><span data-stu-id="c11ed-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c11ed-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c11ed-114">Elements and attributes</span></span>

<span data-ttu-id="c11ed-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="c11ed-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c11ed-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c11ed-116">Parent elements</span></span>

|<span data-ttu-id="c11ed-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c11ed-117">**Element**</span></span>|<span data-ttu-id="c11ed-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c11ed-118">**Type**</span></span>|<span data-ttu-id="c11ed-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c11ed-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c11ed-120">Section</span><span class="sxs-lookup"><span data-stu-id="c11ed-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c11ed-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="c11ed-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c11ed-122">Contiene filas que describen los elementos de menú en un menú contextual o de etiqueta de acción para una forma o página.</span><span class="sxs-lookup"><span data-stu-id="c11ed-122">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c11ed-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c11ed-123">Child elements</span></span>

|<span data-ttu-id="c11ed-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c11ed-124">**Element**</span></span>|<span data-ttu-id="c11ed-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c11ed-125">**Type**</span></span>|<span data-ttu-id="c11ed-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c11ed-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c11ed-127">Cell</span><span class="sxs-lookup"><span data-stu-id="c11ed-127">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="c11ed-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c11ed-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c11ed-129">Especifica una propiedad de una acción asociada con un comando personalizado en un menú contextual o de etiquetas de acción.</span><span class="sxs-lookup"><span data-stu-id="c11ed-129">Specifies one property of an action associated with a custom command on a shortcut or action tag menu.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c11ed-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="c11ed-130">Attributes</span></span>

|<span data-ttu-id="c11ed-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c11ed-131">**Attribute**</span></span>|<span data-ttu-id="c11ed-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c11ed-132">**Type**</span></span>|<span data-ttu-id="c11ed-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="c11ed-133">**Required**</span></span>|<span data-ttu-id="c11ed-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c11ed-134">**Description**</span></span>|<span data-ttu-id="c11ed-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="c11ed-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c11ed-136">Del</span><span class="sxs-lookup"><span data-stu-id="c11ed-136">Del</span></span>  <br/> |<span data-ttu-id="c11ed-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="c11ed-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c11ed-138">opcional</span><span class="sxs-lookup"><span data-stu-id="c11ed-138">optional</span></span>  <br/> |<span data-ttu-id="c11ed-139">Especifica si se ha eliminado una fila que, de lo contrario, se heredaría de una forma de patrón.</span><span class="sxs-lookup"><span data-stu-id="c11ed-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="c11ed-140">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="c11ed-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c11ed-141">IX</span><span class="sxs-lookup"><span data-stu-id="c11ed-141">IX</span></span>  <br/> |<span data-ttu-id="c11ed-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c11ed-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c11ed-143">opcional</span><span class="sxs-lookup"><span data-stu-id="c11ed-143">optional</span></span>  <br/> |<span data-ttu-id="c11ed-144">Especifica el identificador de base uno de la fila.</span><span class="sxs-lookup"><span data-stu-id="c11ed-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="c11ed-145">Debe ser único y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, paraGraph, Reviewer, Scratch y Tabs.</span><span class="sxs-lookup"><span data-stu-id="c11ed-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="c11ed-146">Una fila sólo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="c11ed-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="c11ed-147">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c11ed-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c11ed-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="c11ed-148">LocalName</span></span>  <br/> |<span data-ttu-id="c11ed-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c11ed-149">xsd:string</span></span>  <br/> |<span data-ttu-id="c11ed-150">opcional</span><span class="sxs-lookup"><span data-stu-id="c11ed-150">optional</span></span>  <br/> |<span data-ttu-id="c11ed-151">Especifica el nombre único dependiente del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="c11ed-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="c11ed-152">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c11ed-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c11ed-153">N</span><span class="sxs-lookup"><span data-stu-id="c11ed-153">N</span></span>  <br/> |<span data-ttu-id="c11ed-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c11ed-154">xsd:string</span></span>  <br/> |<span data-ttu-id="c11ed-155">opcional</span><span class="sxs-lookup"><span data-stu-id="c11ed-155">optional</span></span>  <br/> |<span data-ttu-id="c11ed-156">Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, control, Connection, HYPERLINK y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="c11ed-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="c11ed-157">Una fila sólo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="c11ed-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="c11ed-158">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c11ed-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c11ed-159">T</span><span class="sxs-lookup"><span data-stu-id="c11ed-159">T</span></span>  <br/> |<span data-ttu-id="c11ed-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c11ed-160">xsd:string</span></span>  <br/> |<span data-ttu-id="c11ed-161">opcional</span><span class="sxs-lookup"><span data-stu-id="c11ed-161">optional</span></span>  <br/> |<span data-ttu-id="c11ed-162">Especifica el tipo de la ruta geométrica representada por la fila y utilizada en la visualización de geometría.</span><span class="sxs-lookup"><span data-stu-id="c11ed-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="c11ed-163">El atributo T solo se usa para la sección Geometry.</span><span class="sxs-lookup"><span data-stu-id="c11ed-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="c11ed-164">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c11ed-164">Values of the xsd:string type.</span></span>  <br/> |
   

