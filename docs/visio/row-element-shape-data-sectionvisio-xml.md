---
title: Elemento Row (sección de datos de formas) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eb74ae8-ff42-6e34-30e2-2080bf8b5754
description: Especifica una entrada de datos de formas para asociar datos con una forma.
ms.openlocfilehash: 19dc4fe4759e7546f56160e41100d73721f9f6e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823048"
---
# <a name="row-element-shape-data-section-visio-xml"></a><span data-ttu-id="980dc-103">Elemento Row (sección de datos de formas) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="980dc-103">Row element (Shape Data Section) ('Visio XML')</span></span>

<span data-ttu-id="980dc-104">Especifica una entrada de datos de formas para asociar datos con una forma.</span><span class="sxs-lookup"><span data-stu-id="980dc-104">Specifies one shape data entry for associating data with a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="980dc-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="980dc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="980dc-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="980dc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="980dc-107">Forma Data_Type</span><span class="sxs-lookup"><span data-stu-id="980dc-107">Shape Data_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="980dc-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="980dc-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="980dc-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="980dc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="980dc-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="980dc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="980dc-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="980dc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="980dc-112">master # .xml, # .xml de página</span><span class="sxs-lookup"><span data-stu-id="980dc-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="980dc-113">Definición</span><span class="sxs-lookup"><span data-stu-id="980dc-113">Definition</span></span>

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="980dc-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="980dc-114">Elements and attributes</span></span>

<span data-ttu-id="980dc-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="980dc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="980dc-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="980dc-116">Parent elements</span></span>

|<span data-ttu-id="980dc-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="980dc-117">**Element**</span></span>|<span data-ttu-id="980dc-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="980dc-118">**Type**</span></span>|<span data-ttu-id="980dc-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="980dc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="980dc-120">Section</span><span class="sxs-lookup"><span data-stu-id="980dc-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="980dc-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="980dc-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="980dc-122">Especifica una entrada de datos de formas para asociar datos con una forma.</span><span class="sxs-lookup"><span data-stu-id="980dc-122">Specifies one shape data entry for associating data with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="980dc-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="980dc-123">Child elements</span></span>

|<span data-ttu-id="980dc-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="980dc-124">**Element**</span></span>|<span data-ttu-id="980dc-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="980dc-125">**Type**</span></span>|<span data-ttu-id="980dc-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="980dc-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="980dc-127">Cell</span><span class="sxs-lookup"><span data-stu-id="980dc-127">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="980dc-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="980dc-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="980dc-129">Especifica una propiedad de los datos de formas.</span><span class="sxs-lookup"><span data-stu-id="980dc-129">Specifies one property of the shape data.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="980dc-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="980dc-130">Attributes</span></span>

|<span data-ttu-id="980dc-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="980dc-131">**Attribute**</span></span>|<span data-ttu-id="980dc-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="980dc-132">**Type**</span></span>|<span data-ttu-id="980dc-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="980dc-133">**Required**</span></span>|<span data-ttu-id="980dc-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="980dc-134">**Description**</span></span>|<span data-ttu-id="980dc-135">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="980dc-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="980dc-136">SUPR</span><span class="sxs-lookup"><span data-stu-id="980dc-136">Del</span></span>  <br/> |<span data-ttu-id="980dc-137">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="980dc-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="980dc-138">opcional</span><span class="sxs-lookup"><span data-stu-id="980dc-138">optional</span></span>  <br/> |<span data-ttu-id="980dc-139">Especifica si se ha eliminado una fila que de lo contrario heredan la configuración de una forma de patrón.</span><span class="sxs-lookup"><span data-stu-id="980dc-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="980dc-140">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="980dc-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="980dc-141">IX</span><span class="sxs-lookup"><span data-stu-id="980dc-141">IX</span></span>  <br/> |<span data-ttu-id="980dc-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="980dc-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="980dc-143">opcional</span><span class="sxs-lookup"><span data-stu-id="980dc-143">optional</span></span>  <br/> |<span data-ttu-id="980dc-144">Especifica el identificador basado en uno de la fila.</span><span class="sxs-lookup"><span data-stu-id="980dc-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="980dc-145">Debe ser único y mayor que otros identificadores en la misma sección. El atributo IX solo se usa para las secciones de carácter, conexión, campo, FillGradient, geometría, capa, LineGradient, párrafo, revisor, cero y las fichas.</span><span class="sxs-lookup"><span data-stu-id="980dc-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="980dc-146">Sólo una fila puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="980dc-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="980dc-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="980dc-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="980dc-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="980dc-148">LocalName</span></span>  <br/> |<span data-ttu-id="980dc-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="980dc-149">xsd:string</span></span>  <br/> |<span data-ttu-id="980dc-150">opcional</span><span class="sxs-lookup"><span data-stu-id="980dc-150">optional</span></span>  <br/> |<span data-ttu-id="980dc-151">Especifica el nombre único de dependen del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="980dc-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="980dc-152">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="980dc-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="980dc-153">N</span><span class="sxs-lookup"><span data-stu-id="980dc-153">N</span></span>  <br/> |<span data-ttu-id="980dc-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="980dc-154">xsd:string</span></span>  <br/> |<span data-ttu-id="980dc-155">opcional</span><span class="sxs-lookup"><span data-stu-id="980dc-155">optional</span></span>  <br/> |<span data-ttu-id="980dc-156">Especifica el nombre único de independiente del idioma de la fila. El atributo N solo se usa para las secciones de usuario, propiedad, acciones, Control, conexión, hipervínculo y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="980dc-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="980dc-157">Sólo una fila puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="980dc-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="980dc-158">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="980dc-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="980dc-159">T</span><span class="sxs-lookup"><span data-stu-id="980dc-159">T</span></span>  <br/> |<span data-ttu-id="980dc-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="980dc-160">xsd:string</span></span>  <br/> |<span data-ttu-id="980dc-161">opcional</span><span class="sxs-lookup"><span data-stu-id="980dc-161">optional</span></span>  <br/> |<span data-ttu-id="980dc-162">Especifica el tipo de la ruta de acceso geométrica representada por la fila y utilizado en la visualización de la geometría.</span><span class="sxs-lookup"><span data-stu-id="980dc-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="980dc-163">El atributo T solo se usa para la sección de geometría.</span><span class="sxs-lookup"><span data-stu-id="980dc-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="980dc-164">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="980dc-164">Values of the xsd:string type.</span></span>  <br/> |
   

