---
title: Elemento Row (sección campo) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7883cb55-a7db-10c0-be20-5d3c561e490f
description: Presenta funciones y fórmulas insertadas en el texto de una forma con el cuadro de diálogo Campo.
ms.openlocfilehash: 578269b9bcb2a85db2145f1bccafd3c3cff91936
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358496"
---
# <a name="row-element-field-section-visio-xml"></a><span data-ttu-id="ad535-103">Elemento Row (sección campo) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="ad535-103">Row element (Field Section) ('Visio XML')</span></span>

<span data-ttu-id="ad535-104">Presenta funciones y fórmulas insertadas en el texto de una forma con el cuadro de diálogo Campo.</span><span class="sxs-lookup"><span data-stu-id="ad535-104">Displays functions and formulas inserted in the shape's text by using the Field dialog box.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad535-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ad535-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad535-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ad535-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ad535-107">FieldRow_Type</span><span class="sxs-lookup"><span data-stu-id="ad535-107">FieldRow_Type</span></span>](fieldrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ad535-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad535-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ad535-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ad535-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ad535-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="ad535-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ad535-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="ad535-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ad535-112">Master #. XML, página #. XML</span><span class="sxs-lookup"><span data-stu-id="ad535-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad535-113">Definición</span><span class="sxs-lookup"><span data-stu-id="ad535-113">Definition</span></span>

```XML
< xs:element name="Row" type="FieldRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ad535-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ad535-114">Elements and attributes</span></span>

<span data-ttu-id="ad535-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="ad535-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ad535-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ad535-116">Parent elements</span></span>

|<span data-ttu-id="ad535-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ad535-117">**Element**</span></span>|<span data-ttu-id="ad535-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ad535-118">**Type**</span></span>|<span data-ttu-id="ad535-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad535-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad535-120">Section</span><span class="sxs-lookup"><span data-stu-id="ad535-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad535-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="ad535-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad535-122">Presenta funciones y fórmulas insertadas en el texto de una forma con el cuadro de diálogo Campo.</span><span class="sxs-lookup"><span data-stu-id="ad535-122">Displays functions and formulas inserted in the shape's text by using the Field dialog box.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ad535-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ad535-123">Child elements</span></span>

|<span data-ttu-id="ad535-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ad535-124">**Element**</span></span>|<span data-ttu-id="ad535-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ad535-125">**Type**</span></span>|<span data-ttu-id="ad535-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad535-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad535-127">Cell</span><span class="sxs-lookup"><span data-stu-id="ad535-127">Cell</span></span>](cell-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ad535-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ad535-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad535-129">Muestra funciones y fórmulas insertadas en el texto de la forma mediante el cuadro de diálogo campo</span><span class="sxs-lookup"><span data-stu-id="ad535-129">Displays functions and formulas inserted in the shape's text by using the Field dialog box</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ad535-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad535-130">Attributes</span></span>

|<span data-ttu-id="ad535-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ad535-131">**Attribute**</span></span>|<span data-ttu-id="ad535-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ad535-132">**Type**</span></span>|<span data-ttu-id="ad535-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="ad535-133">**Required**</span></span>|<span data-ttu-id="ad535-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad535-134">**Description**</span></span>|<span data-ttu-id="ad535-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="ad535-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ad535-136">Del</span><span class="sxs-lookup"><span data-stu-id="ad535-136">Del</span></span>  <br/> |<span data-ttu-id="ad535-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="ad535-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ad535-138">opcional</span><span class="sxs-lookup"><span data-stu-id="ad535-138">optional</span></span>  <br/> |<span data-ttu-id="ad535-139">Especifica si se ha eliminado una fila que, de lo contrario, se heredaría de una forma de patrón.</span><span class="sxs-lookup"><span data-stu-id="ad535-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="ad535-140">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ad535-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ad535-141">IX</span><span class="sxs-lookup"><span data-stu-id="ad535-141">IX</span></span>  <br/> |<span data-ttu-id="ad535-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ad535-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ad535-143">opcional</span><span class="sxs-lookup"><span data-stu-id="ad535-143">optional</span></span>  <br/> |<span data-ttu-id="ad535-144">Especifica el identificador de base uno de la fila.</span><span class="sxs-lookup"><span data-stu-id="ad535-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="ad535-145">Debe ser único y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, paraGraph, Reviewer, Scratch y Tabs.</span><span class="sxs-lookup"><span data-stu-id="ad535-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="ad535-146">Una fila sólo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="ad535-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="ad535-147">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ad535-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ad535-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="ad535-148">LocalName</span></span>  <br/> |<span data-ttu-id="ad535-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ad535-149">xsd:string</span></span>  <br/> |<span data-ttu-id="ad535-150">opcional</span><span class="sxs-lookup"><span data-stu-id="ad535-150">optional</span></span>  <br/> |<span data-ttu-id="ad535-151">Especifica el nombre único dependiente del idioma de la fila.</span><span class="sxs-lookup"><span data-stu-id="ad535-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="ad535-152">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ad535-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ad535-153">N</span><span class="sxs-lookup"><span data-stu-id="ad535-153">N</span></span>  <br/> |<span data-ttu-id="ad535-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ad535-154">xsd:string</span></span>  <br/> |<span data-ttu-id="ad535-155">opcional</span><span class="sxs-lookup"><span data-stu-id="ad535-155">optional</span></span>  <br/> |<span data-ttu-id="ad535-156">Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, control, Connection, HYPERLINK y ActionTag.</span><span class="sxs-lookup"><span data-stu-id="ad535-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="ad535-157">Una fila sólo puede tener uno de los atributos IX o N.</span><span class="sxs-lookup"><span data-stu-id="ad535-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="ad535-158">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ad535-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ad535-159">T</span><span class="sxs-lookup"><span data-stu-id="ad535-159">T</span></span>  <br/> |<span data-ttu-id="ad535-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ad535-160">xsd:string</span></span>  <br/> |<span data-ttu-id="ad535-161">opcional</span><span class="sxs-lookup"><span data-stu-id="ad535-161">optional</span></span>  <br/> |<span data-ttu-id="ad535-162">Especifica el tipo de la ruta geométrica representada por la fila y utilizada en la visualización de geometría.</span><span class="sxs-lookup"><span data-stu-id="ad535-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="ad535-163">El atributo T solo se usa para la sección Geometry.</span><span class="sxs-lookup"><span data-stu-id="ad535-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="ad535-164">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ad535-164">Values of the xsd:string type.</span></span>  <br/> |
   

