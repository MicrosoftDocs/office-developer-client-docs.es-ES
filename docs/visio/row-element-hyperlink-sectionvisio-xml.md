---
title: Elemento Row (sección de hipervínculos) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f87cd7a4-b9de-5fb1-20ec-90759c966bd9
description: Contiene los elementos para crear varios saltos entre una forma o un sitio Web y otra página de dibujo, otro archivo o página de dibujo.
ms.openlocfilehash: ea2428ffbefa9ac2bf592e37d10c0089e72f6ef1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823066"
---
# <a name="row-element-hyperlink-section-visio-xml"></a><span data-ttu-id="bbade-103">Elemento Row (sección de hipervínculos) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="bbade-103">Row element (Hyperlink Section) ('Visio XML')</span></span>

<span data-ttu-id="bbade-104">Contiene los elementos para crear varios saltos entre una forma o un sitio Web y otra página de dibujo, otro archivo o página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="bbade-104">Contains elements for creating multiple jumps between a shape or drawing page and another drawing page, another file, or a Web site.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bbade-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bbade-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bbade-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="bbade-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bbade-107">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="bbade-107">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bbade-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bbade-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bbade-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="bbade-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bbade-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="bbade-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bbade-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="bbade-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bbade-112">master # .xml, # .xml de página</span><span class="sxs-lookup"><span data-stu-id="bbade-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bbade-113">Definición</span><span class="sxs-lookup"><span data-stu-id="bbade-113">Definition</span></span>

```XML
< xs:element name="Row" type="HyperlinkRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bbade-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="bbade-114">Elements and attributes</span></span>

<span data-ttu-id="bbade-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="bbade-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bbade-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bbade-116">Parent elements</span></span>

|<span data-ttu-id="bbade-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="bbade-117">**Element**</span></span>|<span data-ttu-id="bbade-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bbade-118">**Type**</span></span>|<span data-ttu-id="bbade-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bbade-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bbade-120">Section</span><span class="sxs-lookup"><span data-stu-id="bbade-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bbade-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="bbade-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bbade-122">Contiene los elementos para crear varios saltos entre una forma o un sitio Web y otra página de dibujo, otro archivo o página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="bbade-122">Contains elements for creating multiple jumps between a shape or drawing page and another drawing page, another file, or a Web site.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bbade-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bbade-123">Child elements</span></span>

|<span data-ttu-id="bbade-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="bbade-124">**Element**</span></span>|<span data-ttu-id="bbade-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bbade-125">**Type**</span></span>|<span data-ttu-id="bbade-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bbade-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bbade-127">Cell</span><span class="sxs-lookup"><span data-stu-id="bbade-127">Cell</span></span>](cell-element-hyperlink-rowvisio-xml.md) <br/> |[<span data-ttu-id="bbade-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="bbade-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bbade-129">Contiene la información de un único hipervínculo asociado a una forma</span><span class="sxs-lookup"><span data-stu-id="bbade-129">Contains the information for a single hyperlink associated with a shape</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="bbade-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="bbade-130">Attributes</span></span>

|<span data-ttu-id="bbade-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="bbade-131">**Attribute**</span></span>|<span data-ttu-id="bbade-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bbade-132">**Type**</span></span>|<span data-ttu-id="bbade-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="bbade-133">**Required**</span></span>|<span data-ttu-id="bbade-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bbade-134">**Description**</span></span>|<span data-ttu-id="bbade-135">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="bbade-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bbade-136">SUPR</span><span class="sxs-lookup"><span data-stu-id="bbade-136">Del</span></span>  <br/> |<span data-ttu-id="bbade-137">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="bbade-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bbade-138">opcional</span><span class="sxs-lookup"><span data-stu-id="bbade-138">optional</span></span>  <br/> |<span data-ttu-id="bbade-139">Especifica si se ha eliminado una fila que de lo contrario heredan la configuración de una forma de patrón.</span><span class="sxs-lookup"><span data-stu-id="bbade-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="bbade-140">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="bbade-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="bbade-141">IX</span><span class="sxs-lookup"><span data-stu-id="bbade-141">IX</span></span>  <br/> |<span data-ttu-id="bbade-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bbade-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bbade-143">opcional</span><span class="sxs-lookup"><span data-stu-id="bbade-143">optional</span></span>  <br/> |<span data-ttu-id="bbade-144">Especifica el identificador basado en uno de la fila.</span><span class="sxs-lookup"><span data-stu-id="bbade-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="bbade-145">Debe ser único y mayor que otros identificadores en la misma sección. El atributo IX solo se usa para las secciones de carácter, conexión, campo, FillGradient, geometría, capa, LineGradient, párrafo, revisor, cero y las fichas.</span><span class="sxs-lookup"><span data-stu-id="bbade-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="bbade-146">Sólo una fila puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="bbade-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="bbade-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bbade-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bbade-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="bbade-148">LocalName</span></span>  <br/> |<span data-ttu-id="bbade-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="bbade-149">xsd:string</span></span>  <br/> |<span data-ttu-id="bbade-150">opcional</span><span class="sxs-lookup"><span data-stu-id="bbade-150">optional</span></span>  <br/> |<span data-ttu-id="bbade-151">Especifica el nombre único de dependen del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="bbade-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="bbade-152">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="bbade-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bbade-153">N</span><span class="sxs-lookup"><span data-stu-id="bbade-153">N</span></span>  <br/> |<span data-ttu-id="bbade-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="bbade-154">xsd:string</span></span>  <br/> |<span data-ttu-id="bbade-155">opcional</span><span class="sxs-lookup"><span data-stu-id="bbade-155">optional</span></span>  <br/> |<span data-ttu-id="bbade-156">Especifica el nombre único de independiente del idioma de la fila. El atributo N solo se usa para las secciones de usuario, propiedad, acciones, Control, conexión, hipervínculo y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="bbade-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="bbade-157">Sólo una fila puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="bbade-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="bbade-158">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="bbade-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bbade-159">T</span><span class="sxs-lookup"><span data-stu-id="bbade-159">T</span></span>  <br/> |<span data-ttu-id="bbade-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="bbade-160">xsd:string</span></span>  <br/> |<span data-ttu-id="bbade-161">opcional</span><span class="sxs-lookup"><span data-stu-id="bbade-161">optional</span></span>  <br/> |<span data-ttu-id="bbade-162">Especifica el tipo de la ruta de acceso geométrica representada por la fila y utilizado en la visualización de la geometría.</span><span class="sxs-lookup"><span data-stu-id="bbade-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="bbade-163">El atributo T solo se usa para la sección de geometría.</span><span class="sxs-lookup"><span data-stu-id="bbade-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="bbade-164">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="bbade-164">Values of the xsd:string type.</span></span>  <br/> |
   

