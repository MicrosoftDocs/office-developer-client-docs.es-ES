---
title: Elemento Row (sección campo) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7883cb55-a7db-10c0-be20-5d3c561e490f
description: Presenta funciones y fórmulas insertadas en el texto de una forma con el cuadro de diálogo Campo.
ms.openlocfilehash: c05f704610d7061b9e2c8b742adc39f2b72ba4ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541760"
---
# <a name="row-element-field-section-visio-xml"></a><span data-ttu-id="61037-103">Elemento Row (sección campo) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="61037-103">Row element (Field Section) (Visio XML)</span></span>

<span data-ttu-id="61037-104">Presenta funciones y fórmulas insertadas en el texto de una forma con el cuadro de diálogo Campo.</span><span class="sxs-lookup"><span data-stu-id="61037-104">Displays functions and formulas inserted in the shape's text by using the Field dialog box.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61037-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="61037-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61037-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="61037-106">**Element type**</span></span> <br/> |[<span data-ttu-id="61037-107">FieldRow_Type</span><span class="sxs-lookup"><span data-stu-id="61037-107">FieldRow_Type</span></span>](fieldrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="61037-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="61037-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="61037-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="61037-109">**Schema file**</span></span> <br/> |<span data-ttu-id="61037-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="61037-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="61037-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="61037-111">**Document parts**</span></span> <br/> |<span data-ttu-id="61037-112">Master #. XML, página #. XML</span><span class="sxs-lookup"><span data-stu-id="61037-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="61037-113">Definición</span><span class="sxs-lookup"><span data-stu-id="61037-113">Definition</span></span>

```XML
< xs:element name="Row" type="FieldRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="61037-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="61037-114">Elements and attributes</span></span>

<span data-ttu-id="61037-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="61037-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="61037-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="61037-116">Parent elements</span></span>

|<span data-ttu-id="61037-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="61037-117">**Element**</span></span>|<span data-ttu-id="61037-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="61037-118">**Type**</span></span>|<span data-ttu-id="61037-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="61037-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="61037-120">Section</span><span class="sxs-lookup"><span data-stu-id="61037-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61037-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="61037-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="61037-122">Presenta funciones y fórmulas insertadas en el texto de una forma con el cuadro de diálogo Campo.</span><span class="sxs-lookup"><span data-stu-id="61037-122">Displays functions and formulas inserted in the shape's text by using the Field dialog box.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="61037-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="61037-123">Child elements</span></span>

|<span data-ttu-id="61037-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="61037-124">**Element**</span></span>|<span data-ttu-id="61037-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="61037-125">**Type**</span></span>|<span data-ttu-id="61037-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="61037-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="61037-127">Cell</span><span class="sxs-lookup"><span data-stu-id="61037-127">Cell</span></span>](cell-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="61037-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="61037-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="61037-129">Muestra funciones y fórmulas insertadas en el texto de la forma mediante el cuadro de diálogo campo</span><span class="sxs-lookup"><span data-stu-id="61037-129">Displays functions and formulas inserted in the shape's text by using the Field dialog box</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="61037-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="61037-130">Attributes</span></span>

|<span data-ttu-id="61037-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="61037-131">**Attribute**</span></span>|<span data-ttu-id="61037-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="61037-132">**Type**</span></span>|<span data-ttu-id="61037-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="61037-133">**Required**</span></span>|<span data-ttu-id="61037-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="61037-134">**Description**</span></span>|<span data-ttu-id="61037-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="61037-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="61037-136">Del</span><span class="sxs-lookup"><span data-stu-id="61037-136">Del</span></span>  <br/> |<span data-ttu-id="61037-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="61037-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="61037-138">opcional</span><span class="sxs-lookup"><span data-stu-id="61037-138">optional</span></span>  <br/> |<span data-ttu-id="61037-139">Especifica si se ha eliminado una fila que, de lo contrario, se heredaría de una forma de patrón.</span><span class="sxs-lookup"><span data-stu-id="61037-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="61037-140">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="61037-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="61037-141">IX</span><span class="sxs-lookup"><span data-stu-id="61037-141">IX</span></span>  <br/> |<span data-ttu-id="61037-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61037-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61037-143">opcional</span><span class="sxs-lookup"><span data-stu-id="61037-143">optional</span></span>  <br/> |<span data-ttu-id="61037-144">Especifica el identificador de base uno de la fila.</span><span class="sxs-lookup"><span data-stu-id="61037-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="61037-145">Debe ser único y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch y Tabs.</span><span class="sxs-lookup"><span data-stu-id="61037-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="61037-146">Una fila sólo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="61037-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="61037-147">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="61037-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61037-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="61037-148">LocalName</span></span>  <br/> |<span data-ttu-id="61037-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="61037-149">xsd:string</span></span>  <br/> |<span data-ttu-id="61037-150">opcional</span><span class="sxs-lookup"><span data-stu-id="61037-150">optional</span></span>  <br/> |<span data-ttu-id="61037-151">Especifica el nombre único dependiente del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="61037-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="61037-152">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="61037-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="61037-153">N</span><span class="sxs-lookup"><span data-stu-id="61037-153">N</span></span>  <br/> |<span data-ttu-id="61037-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="61037-154">xsd:string</span></span>  <br/> |<span data-ttu-id="61037-155">opcional</span><span class="sxs-lookup"><span data-stu-id="61037-155">optional</span></span>  <br/> |<span data-ttu-id="61037-156">Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, control, Connection, HYPERLINK y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="61037-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="61037-157">Una fila sólo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="61037-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="61037-158">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="61037-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="61037-159">T</span><span class="sxs-lookup"><span data-stu-id="61037-159">T</span></span>  <br/> |<span data-ttu-id="61037-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="61037-160">xsd:string</span></span>  <br/> |<span data-ttu-id="61037-161">opcional</span><span class="sxs-lookup"><span data-stu-id="61037-161">optional</span></span>  <br/> |<span data-ttu-id="61037-162">Especifica el tipo de la ruta geométrica representada por la fila y utilizada en la visualización de geometría.</span><span class="sxs-lookup"><span data-stu-id="61037-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="61037-163">El atributo T solo se usa para la sección Geometry.</span><span class="sxs-lookup"><span data-stu-id="61037-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="61037-164">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="61037-164">Values of the xsd:string type.</span></span>  <br/> |
   

