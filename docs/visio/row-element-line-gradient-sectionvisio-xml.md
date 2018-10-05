---
title: Elemento de fila (línea degradado sección) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d823766-5cb0-925c-f622-18025f44426c
description: Contiene el color, la transparencia y la posición de un punto de degradado para un degradado de línea.
ms.openlocfilehash: 105d93344343f223a6b5d909f1174f7df56ffb4d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383187"
---
# <a name="row-element-line-gradient-section-visio-xml"></a><span data-ttu-id="0ccc4-103">Elemento de fila (línea degradado sección) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="0ccc4-103">Row element (Line Gradient Section) ('Visio XML')</span></span>

<span data-ttu-id="0ccc4-104">Contiene el color, la transparencia y la posición de un punto de degradado para un degradado de línea.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-104">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ccc4-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0ccc4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ccc4-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="0ccc4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0ccc4-107">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="0ccc4-107">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0ccc4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0ccc4-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0ccc4-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0ccc4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0ccc4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0ccc4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0ccc4-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="0ccc4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0ccc4-112">Document.XML, master # .xml, # .xml de página</span><span class="sxs-lookup"><span data-stu-id="0ccc4-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0ccc4-113">Definición</span><span class="sxs-lookup"><span data-stu-id="0ccc4-113">Definition</span></span>

```XML
< xs:element name="Row" type="LineGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0ccc4-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0ccc4-114">Elements and attributes</span></span>

<span data-ttu-id="0ccc4-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0ccc4-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0ccc4-116">Parent elements</span></span>

|<span data-ttu-id="0ccc4-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="0ccc4-117">**Element**</span></span>|<span data-ttu-id="0ccc4-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0ccc4-118">**Type**</span></span>|<span data-ttu-id="0ccc4-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ccc4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0ccc4-120">Section</span><span class="sxs-lookup"><span data-stu-id="0ccc4-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0ccc4-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="0ccc4-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0ccc4-122">Contiene el color, la transparencia y la posición de un punto de degradado para un degradado de línea.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-122">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0ccc4-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0ccc4-123">Child elements</span></span>

|<span data-ttu-id="0ccc4-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="0ccc4-124">**Element**</span></span>|<span data-ttu-id="0ccc4-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0ccc4-125">**Type**</span></span>|<span data-ttu-id="0ccc4-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ccc4-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0ccc4-127">Cell</span><span class="sxs-lookup"><span data-stu-id="0ccc4-127">Cell</span></span>](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="0ccc4-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="0ccc4-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0ccc4-129">Especifica una propiedad única.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0ccc4-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="0ccc4-130">Attributes</span></span>

|<span data-ttu-id="0ccc4-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0ccc4-131">**Attribute**</span></span>|<span data-ttu-id="0ccc4-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0ccc4-132">**Type**</span></span>|<span data-ttu-id="0ccc4-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="0ccc4-133">**Required**</span></span>|<span data-ttu-id="0ccc4-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ccc4-134">**Description**</span></span>|<span data-ttu-id="0ccc4-135">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="0ccc4-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0ccc4-136">SUPR</span><span class="sxs-lookup"><span data-stu-id="0ccc4-136">Del</span></span>  <br/> |<span data-ttu-id="0ccc4-137">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="0ccc4-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0ccc4-138">opcional</span><span class="sxs-lookup"><span data-stu-id="0ccc4-138">optional</span></span>  <br/> |<span data-ttu-id="0ccc4-139">Especifica si se ha eliminado una fila que de lo contrario heredan la configuración de una forma de patrón.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="0ccc4-140">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0ccc4-141">IX</span><span class="sxs-lookup"><span data-stu-id="0ccc4-141">IX</span></span>  <br/> |<span data-ttu-id="0ccc4-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0ccc4-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0ccc4-143">opcional</span><span class="sxs-lookup"><span data-stu-id="0ccc4-143">optional</span></span>  <br/> |<span data-ttu-id="0ccc4-144">Especifica el identificador basado en uno de la fila.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="0ccc4-145">Debe ser único y mayor que otros identificadores en la misma sección. El atributo IX solo se usa para las secciones de carácter, conexión, campo, FillGradient, geometría, capa, LineGradient, párrafo, revisor, cero y las fichas.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="0ccc4-146">Sólo una fila puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="0ccc4-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0ccc4-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="0ccc4-148">LocalName</span></span>  <br/> |<span data-ttu-id="0ccc4-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0ccc4-149">xsd:string</span></span>  <br/> |<span data-ttu-id="0ccc4-150">opcional</span><span class="sxs-lookup"><span data-stu-id="0ccc4-150">optional</span></span>  <br/> |<span data-ttu-id="0ccc4-151">Especifica el nombre único de dependen del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="0ccc4-152">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0ccc4-153">N</span><span class="sxs-lookup"><span data-stu-id="0ccc4-153">N</span></span>  <br/> |<span data-ttu-id="0ccc4-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0ccc4-154">xsd:string</span></span>  <br/> |<span data-ttu-id="0ccc4-155">opcional</span><span class="sxs-lookup"><span data-stu-id="0ccc4-155">optional</span></span>  <br/> |<span data-ttu-id="0ccc4-156">Especifica el nombre único de independiente del idioma de la fila. El atributo N solo se usa para las secciones de usuario, propiedad, acciones, Control, conexión, hipervínculo y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="0ccc4-157">Sólo una fila puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="0ccc4-158">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0ccc4-159">T</span><span class="sxs-lookup"><span data-stu-id="0ccc4-159">T</span></span>  <br/> |<span data-ttu-id="0ccc4-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0ccc4-160">xsd:string</span></span>  <br/> |<span data-ttu-id="0ccc4-161">opcional</span><span class="sxs-lookup"><span data-stu-id="0ccc4-161">optional</span></span>  <br/> |<span data-ttu-id="0ccc4-162">Especifica el tipo de la ruta de acceso geométrica representada por la fila y utilizado en la visualización de la geometría.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="0ccc4-163">El atributo T solo se usa para la sección de geometría.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="0ccc4-164">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0ccc4-164">Values of the xsd:string type.</span></span>  <br/> |
   

