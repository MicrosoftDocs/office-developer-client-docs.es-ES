---
title: DataColumn_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 9d334190b686f3b2c5e25a31336c668c957e820f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821910"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="6d3bd-102">DataColumn_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="6d3bd-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6d3bd-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="6d3bd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d3bd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6d3bd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6d3bd-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6d3bd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6d3bd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6d3bd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6d3bd-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="6d3bd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6d3bd-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="6d3bd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6d3bd-109">Definición</span><span class="sxs-lookup"><span data-stu-id="6d3bd-109">Definition</span></span>

```XML
      <xs:complexType name="DataColumn_Type">
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Label"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="OrigLabel"
  type="xsd:string"
    />
    <xs:attribute name="LangID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Calendar"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="DataType"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="UnitType"
  type="xsd:string"
    />
    <xs:attribute name="Currency"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Degree"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayOrder"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Mapped"
  type="xsd:boolean"
    />
    <xs:attribute name="Hyperlink"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6d3bd-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="6d3bd-110">Elements and attributes</span></span>

<span data-ttu-id="6d3bd-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="6d3bd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6d3bd-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6d3bd-112">Child elements</span></span>

<span data-ttu-id="6d3bd-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6d3bd-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d3bd-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="6d3bd-114">Attributes</span></span>

|<span data-ttu-id="6d3bd-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="6d3bd-115">**Attribute**</span></span>|<span data-ttu-id="6d3bd-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6d3bd-116">**Type**</span></span>|<span data-ttu-id="6d3bd-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="6d3bd-117">**Required**</span></span>|<span data-ttu-id="6d3bd-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6d3bd-118">**Description**</span></span>|<span data-ttu-id="6d3bd-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="6d3bd-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6d3bd-120">Calendario</span><span class="sxs-lookup"><span data-stu-id="6d3bd-120">Calendar</span></span>  <br/> |<span data-ttu-id="6d3bd-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6d3bd-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6d3bd-122">opcional</span><span class="sxs-lookup"><span data-stu-id="6d3bd-122">optional</span></span>  <br/> ||<span data-ttu-id="6d3bd-123">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="6d3bd-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6d3bd-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="6d3bd-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="6d3bd-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="6d3bd-125">xsd:string</span></span>  <br/> |<span data-ttu-id="6d3bd-126">necesario</span><span class="sxs-lookup"><span data-stu-id="6d3bd-126">required</span></span>  <br/> ||<span data-ttu-id="6d3bd-127">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="6d3bd-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6d3bd-128">Moneda</span><span class="sxs-lookup"><span data-stu-id="6d3bd-128">Currency</span></span>  <br/> |<span data-ttu-id="6d3bd-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6d3bd-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6d3bd-130">opcional</span><span class="sxs-lookup"><span data-stu-id="6d3bd-130">optional</span></span>  <br/> ||<span data-ttu-id="6d3bd-131">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="6d3bd-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6d3bd-132">DataType</span><span class="sxs-lookup"><span data-stu-id="6d3bd-132">DataType</span></span>  <br/> |<span data-ttu-id="6d3bd-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6d3bd-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6d3bd-134">opcional</span><span class="sxs-lookup"><span data-stu-id="6d3bd-134">optional</span></span>  <br/> ||<span data-ttu-id="6d3bd-135">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="6d3bd-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6d3bd-136">Degree</span><span class="sxs-lookup"><span data-stu-id="6d3bd-136">Degree</span></span>  <br/> |<span data-ttu-id="6d3bd-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6d3bd-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6d3bd-138">opcional</span><span class="sxs-lookup"><span data-stu-id="6d3bd-138">optional</span></span>  <br/> ||<span data-ttu-id="6d3bd-139">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6d3bd-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6d3bd-140">OrdenVisualización</span><span class="sxs-lookup"><span data-stu-id="6d3bd-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="6d3bd-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6d3bd-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6d3bd-142">opcional</span><span class="sxs-lookup"><span data-stu-id="6d3bd-142">optional</span></span>  <br/> ||<span data-ttu-id="6d3bd-143">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6d3bd-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6d3bd-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="6d3bd-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="6d3bd-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6d3bd-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6d3bd-146">opcional</span><span class="sxs-lookup"><span data-stu-id="6d3bd-146">optional</span></span>  <br/> ||<span data-ttu-id="6d3bd-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6d3bd-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6d3bd-148">Hipervínculo</span><span class="sxs-lookup"><span data-stu-id="6d3bd-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="6d3bd-149">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="6d3bd-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6d3bd-150">opcional</span><span class="sxs-lookup"><span data-stu-id="6d3bd-150">optional</span></span>  <br/> ||<span data-ttu-id="6d3bd-151">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="6d3bd-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6d3bd-152">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="6d3bd-152">Label</span></span>  <br/> |<span data-ttu-id="6d3bd-153">xsd: String</span><span class="sxs-lookup"><span data-stu-id="6d3bd-153">xsd:string</span></span>  <br/> |<span data-ttu-id="6d3bd-154">necesario</span><span class="sxs-lookup"><span data-stu-id="6d3bd-154">required</span></span>  <br/> ||<span data-ttu-id="6d3bd-155">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="6d3bd-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6d3bd-156">LangID</span><span class="sxs-lookup"><span data-stu-id="6d3bd-156">LangID</span></span>  <br/> |<span data-ttu-id="6d3bd-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6d3bd-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6d3bd-158">opcional</span><span class="sxs-lookup"><span data-stu-id="6d3bd-158">optional</span></span>  <br/> ||<span data-ttu-id="6d3bd-159">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6d3bd-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6d3bd-160">Asignadas</span><span class="sxs-lookup"><span data-stu-id="6d3bd-160">Mapped</span></span>  <br/> |<span data-ttu-id="6d3bd-161">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="6d3bd-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6d3bd-162">opcional</span><span class="sxs-lookup"><span data-stu-id="6d3bd-162">optional</span></span>  <br/> ||<span data-ttu-id="6d3bd-163">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="6d3bd-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6d3bd-164">Nombre</span><span class="sxs-lookup"><span data-stu-id="6d3bd-164">Name</span></span>  <br/> |<span data-ttu-id="6d3bd-165">xsd: String</span><span class="sxs-lookup"><span data-stu-id="6d3bd-165">xsd:string</span></span>  <br/> |<span data-ttu-id="6d3bd-166">necesario</span><span class="sxs-lookup"><span data-stu-id="6d3bd-166">required</span></span>  <br/> ||<span data-ttu-id="6d3bd-167">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="6d3bd-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6d3bd-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="6d3bd-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="6d3bd-169">xsd: String</span><span class="sxs-lookup"><span data-stu-id="6d3bd-169">xsd:string</span></span>  <br/> |<span data-ttu-id="6d3bd-170">opcional</span><span class="sxs-lookup"><span data-stu-id="6d3bd-170">optional</span></span>  <br/> ||<span data-ttu-id="6d3bd-171">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="6d3bd-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6d3bd-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="6d3bd-172">UnitType</span></span>  <br/> |<span data-ttu-id="6d3bd-173">xsd: String</span><span class="sxs-lookup"><span data-stu-id="6d3bd-173">xsd:string</span></span>  <br/> |<span data-ttu-id="6d3bd-174">opcional</span><span class="sxs-lookup"><span data-stu-id="6d3bd-174">optional</span></span>  <br/> ||<span data-ttu-id="6d3bd-175">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="6d3bd-175">Values of the xsd:string type.</span></span>  <br/> |
   

