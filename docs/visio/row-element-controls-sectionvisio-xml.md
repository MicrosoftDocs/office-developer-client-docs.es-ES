---
title: Elemento Row (sección de controles) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: Contiene las celdas de un controlador definido para una forma.
ms.openlocfilehash: cf8015b82f759ba2c166ff5179b2c4324c168e44
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823025"
---
# <a name="row-element-controls-section-visio-xml"></a><span data-ttu-id="491b0-103">Elemento Row (sección de controles) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="491b0-103">Row element (Controls Section) ('Visio XML')</span></span>

<span data-ttu-id="491b0-104">Contiene las celdas de un controlador definido para una forma.</span><span class="sxs-lookup"><span data-stu-id="491b0-104">Contains the cells for a particular control handle defined for a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="491b0-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="491b0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="491b0-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="491b0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="491b0-107">ControlRow_Type</span><span class="sxs-lookup"><span data-stu-id="491b0-107">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="491b0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="491b0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="491b0-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="491b0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="491b0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="491b0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="491b0-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="491b0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="491b0-112">master # .xml, # .xml de página</span><span class="sxs-lookup"><span data-stu-id="491b0-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="491b0-113">Definición</span><span class="sxs-lookup"><span data-stu-id="491b0-113">Definition</span></span>

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="491b0-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="491b0-114">Elements and attributes</span></span>

<span data-ttu-id="491b0-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="491b0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="491b0-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="491b0-116">Parent elements</span></span>

|<span data-ttu-id="491b0-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="491b0-117">**Element**</span></span>|<span data-ttu-id="491b0-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="491b0-118">**Type**</span></span>|<span data-ttu-id="491b0-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="491b0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="491b0-120">Sección</span><span class="sxs-lookup"><span data-stu-id="491b0-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="491b0-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="491b0-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="491b0-122">Contiene las celdas de un controlador definido para una forma.</span><span class="sxs-lookup"><span data-stu-id="491b0-122">Contains the cells for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="491b0-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="491b0-123">Child elements</span></span>

|<span data-ttu-id="491b0-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="491b0-124">**Element**</span></span>|<span data-ttu-id="491b0-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="491b0-125">**Type**</span></span>|<span data-ttu-id="491b0-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="491b0-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="491b0-127">Cell</span><span class="sxs-lookup"><span data-stu-id="491b0-127">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="491b0-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="491b0-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="491b0-129">Contiene una propiedad para un controlador definido para una forma.</span><span class="sxs-lookup"><span data-stu-id="491b0-129">Contains a property for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="491b0-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="491b0-130">Attributes</span></span>

|<span data-ttu-id="491b0-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="491b0-131">**Attribute**</span></span>|<span data-ttu-id="491b0-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="491b0-132">**Type**</span></span>|<span data-ttu-id="491b0-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="491b0-133">**Required**</span></span>|<span data-ttu-id="491b0-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="491b0-134">**Description**</span></span>|<span data-ttu-id="491b0-135">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="491b0-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="491b0-136">SUPR</span><span class="sxs-lookup"><span data-stu-id="491b0-136">Del</span></span>  <br/> |<span data-ttu-id="491b0-137">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="491b0-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="491b0-138">opcional</span><span class="sxs-lookup"><span data-stu-id="491b0-138">optional</span></span>  <br/> |<span data-ttu-id="491b0-139">Especifica si se ha eliminado una fila que de lo contrario heredan la configuración de una forma de patrón.</span><span class="sxs-lookup"><span data-stu-id="491b0-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="491b0-140">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="491b0-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="491b0-141">IX</span><span class="sxs-lookup"><span data-stu-id="491b0-141">IX</span></span>  <br/> |<span data-ttu-id="491b0-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="491b0-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="491b0-143">opcional</span><span class="sxs-lookup"><span data-stu-id="491b0-143">optional</span></span>  <br/> |<span data-ttu-id="491b0-144">Especifica el identificador basado en uno de la fila.</span><span class="sxs-lookup"><span data-stu-id="491b0-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="491b0-145">Debe ser único y mayor que otros identificadores en la misma sección. El atributo IX solo se usa para las secciones de carácter, conexión, campo, FillGradient, geometría, capa, LineGradient, párrafo, revisor, cero y las fichas.</span><span class="sxs-lookup"><span data-stu-id="491b0-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="491b0-146">Sólo una fila puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="491b0-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="491b0-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="491b0-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="491b0-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="491b0-148">LocalName</span></span>  <br/> |<span data-ttu-id="491b0-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="491b0-149">xsd:string</span></span>  <br/> |<span data-ttu-id="491b0-150">opcional</span><span class="sxs-lookup"><span data-stu-id="491b0-150">optional</span></span>  <br/> |<span data-ttu-id="491b0-151">Especifica el nombre único de dependen del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="491b0-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="491b0-152">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="491b0-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="491b0-153">N</span><span class="sxs-lookup"><span data-stu-id="491b0-153">N</span></span>  <br/> |<span data-ttu-id="491b0-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="491b0-154">xsd:string</span></span>  <br/> |<span data-ttu-id="491b0-155">opcional</span><span class="sxs-lookup"><span data-stu-id="491b0-155">optional</span></span>  <br/> |<span data-ttu-id="491b0-156">Especifica el nombre único de independiente del idioma de la fila. El atributo N solo se usa para las secciones de usuario, propiedad, acciones, Control, conexión, hipervínculo y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="491b0-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="491b0-157">Sólo una fila puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="491b0-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="491b0-158">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="491b0-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="491b0-159">T</span><span class="sxs-lookup"><span data-stu-id="491b0-159">T</span></span>  <br/> |<span data-ttu-id="491b0-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="491b0-160">xsd:string</span></span>  <br/> |<span data-ttu-id="491b0-161">opcional</span><span class="sxs-lookup"><span data-stu-id="491b0-161">optional</span></span>  <br/> |<span data-ttu-id="491b0-162">Especifica el tipo de la ruta de acceso geométrica representada por la fila y utilizado en la visualización de la geometría.</span><span class="sxs-lookup"><span data-stu-id="491b0-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="491b0-163">El atributo T solo se usa para la sección de geometría.</span><span class="sxs-lookup"><span data-stu-id="491b0-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="491b0-164">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="491b0-164">Values of the xsd:string type.</span></span>  <br/> |
   

