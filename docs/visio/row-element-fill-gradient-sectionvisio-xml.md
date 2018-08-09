---
title: Elemento de fila (relleno degradado sección) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f216afb5-4393-6e1c-54c2-3c184a26d934
description: Contiene el color, la transparencia y la posición de un punto de degradado para un degradado de relleno.
ms.openlocfilehash: 54c2d9d7833e6434c19dc863ded994f5c3539a1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823050"
---
# <a name="row-element-fill-gradient-section-visio-xml"></a><span data-ttu-id="b3412-103">Elemento de fila (relleno degradado sección) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="b3412-103">Row element (Fill Gradient Section) ('Visio XML')</span></span>

<span data-ttu-id="b3412-104">Contiene el color, la transparencia y la posición de un punto de degradado para un degradado de relleno.</span><span class="sxs-lookup"><span data-stu-id="b3412-104">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b3412-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b3412-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3412-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="b3412-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b3412-107">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="b3412-107">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b3412-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b3412-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b3412-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b3412-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b3412-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b3412-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b3412-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="b3412-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b3412-112">Document.XML, master # .xml, # .xml de página</span><span class="sxs-lookup"><span data-stu-id="b3412-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b3412-113">Definición</span><span class="sxs-lookup"><span data-stu-id="b3412-113">Definition</span></span>

```XML
< xs:element name="Row" type="FillGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b3412-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b3412-114">Elements and attributes</span></span>

<span data-ttu-id="b3412-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="b3412-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b3412-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b3412-116">Parent elements</span></span>

|<span data-ttu-id="b3412-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="b3412-117">**Element**</span></span>|<span data-ttu-id="b3412-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b3412-118">**Type**</span></span>|<span data-ttu-id="b3412-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b3412-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b3412-120">Section</span><span class="sxs-lookup"><span data-stu-id="b3412-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b3412-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="b3412-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b3412-122">Contiene el color, la transparencia y la posición de un punto de degradado para un degradado de relleno.</span><span class="sxs-lookup"><span data-stu-id="b3412-122">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b3412-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b3412-123">Child elements</span></span>

|<span data-ttu-id="b3412-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="b3412-124">**Element**</span></span>|<span data-ttu-id="b3412-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b3412-125">**Type**</span></span>|<span data-ttu-id="b3412-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b3412-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b3412-127">Cell</span><span class="sxs-lookup"><span data-stu-id="b3412-127">Cell</span></span>](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="b3412-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="b3412-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b3412-129">Especifica una propiedad única.</span><span class="sxs-lookup"><span data-stu-id="b3412-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b3412-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="b3412-130">Attributes</span></span>

|<span data-ttu-id="b3412-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b3412-131">**Attribute**</span></span>|<span data-ttu-id="b3412-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b3412-132">**Type**</span></span>|<span data-ttu-id="b3412-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="b3412-133">**Required**</span></span>|<span data-ttu-id="b3412-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b3412-134">**Description**</span></span>|<span data-ttu-id="b3412-135">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="b3412-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b3412-136">SUPR</span><span class="sxs-lookup"><span data-stu-id="b3412-136">Del</span></span>  <br/> |<span data-ttu-id="b3412-137">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="b3412-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b3412-138">opcional</span><span class="sxs-lookup"><span data-stu-id="b3412-138">optional</span></span>  <br/> |<span data-ttu-id="b3412-139">Especifica si se ha eliminado una fila que de lo contrario heredan la configuración de una forma de patrón.</span><span class="sxs-lookup"><span data-stu-id="b3412-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="b3412-140">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="b3412-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="b3412-141">IX</span><span class="sxs-lookup"><span data-stu-id="b3412-141">IX</span></span>  <br/> |<span data-ttu-id="b3412-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b3412-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b3412-143">opcional</span><span class="sxs-lookup"><span data-stu-id="b3412-143">optional</span></span>  <br/> |<span data-ttu-id="b3412-144">Especifica el identificador basado en uno de la fila.</span><span class="sxs-lookup"><span data-stu-id="b3412-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="b3412-145">Debe ser único y mayor que otros identificadores en la misma sección. El atributo IX solo se usa para las secciones de carácter, conexión, campo, FillGradient, geometría, capa, LineGradient, párrafo, revisor, cero y las fichas.</span><span class="sxs-lookup"><span data-stu-id="b3412-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="b3412-146">Sólo una fila puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="b3412-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="b3412-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b3412-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b3412-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="b3412-148">LocalName</span></span>  <br/> |<span data-ttu-id="b3412-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b3412-149">xsd:string</span></span>  <br/> |<span data-ttu-id="b3412-150">opcional</span><span class="sxs-lookup"><span data-stu-id="b3412-150">optional</span></span>  <br/> |<span data-ttu-id="b3412-151">Especifica el nombre único de dependen del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="b3412-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="b3412-152">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="b3412-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b3412-153">N</span><span class="sxs-lookup"><span data-stu-id="b3412-153">N</span></span>  <br/> |<span data-ttu-id="b3412-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b3412-154">xsd:string</span></span>  <br/> |<span data-ttu-id="b3412-155">opcional</span><span class="sxs-lookup"><span data-stu-id="b3412-155">optional</span></span>  <br/> |<span data-ttu-id="b3412-156">Especifica el nombre único de independiente del idioma de la fila. El atributo N solo se usa para las secciones de usuario, propiedad, acciones, Control, conexión, hipervínculo y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="b3412-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="b3412-157">Sólo una fila puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="b3412-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="b3412-158">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="b3412-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b3412-159">T</span><span class="sxs-lookup"><span data-stu-id="b3412-159">T</span></span>  <br/> |<span data-ttu-id="b3412-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b3412-160">xsd:string</span></span>  <br/> |<span data-ttu-id="b3412-161">opcional</span><span class="sxs-lookup"><span data-stu-id="b3412-161">optional</span></span>  <br/> |<span data-ttu-id="b3412-162">Especifica el tipo de la ruta de acceso geométrica representada por la fila y utilizado en la visualización de la geometría.</span><span class="sxs-lookup"><span data-stu-id="b3412-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="b3412-163">El atributo T solo se usa para la sección de geometría.</span><span class="sxs-lookup"><span data-stu-id="b3412-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="b3412-164">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="b3412-164">Values of the xsd:string type.</span></span>  <br/> |
   

