---
title: DataColumn_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 69f994b9516b04ddca8d26a645161772dc77c470
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388661"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="874cb-102">DataColumn_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="874cb-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="874cb-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="874cb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="874cb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="874cb-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="874cb-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="874cb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="874cb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="874cb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="874cb-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="874cb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="874cb-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="874cb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="874cb-109">Definición</span><span class="sxs-lookup"><span data-stu-id="874cb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="874cb-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="874cb-110">Elements and attributes</span></span>

<span data-ttu-id="874cb-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="874cb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="874cb-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="874cb-112">Child elements</span></span>

<span data-ttu-id="874cb-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="874cb-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="874cb-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="874cb-114">Attributes</span></span>

|<span data-ttu-id="874cb-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="874cb-115">**Attribute**</span></span>|<span data-ttu-id="874cb-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="874cb-116">**Type**</span></span>|<span data-ttu-id="874cb-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="874cb-117">**Required**</span></span>|<span data-ttu-id="874cb-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="874cb-118">**Description**</span></span>|<span data-ttu-id="874cb-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="874cb-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="874cb-120">Calendario</span><span class="sxs-lookup"><span data-stu-id="874cb-120">Calendar</span></span>  <br/> |<span data-ttu-id="874cb-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="874cb-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="874cb-122">opcional</span><span class="sxs-lookup"><span data-stu-id="874cb-122">optional</span></span>  <br/> ||<span data-ttu-id="874cb-123">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="874cb-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="874cb-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="874cb-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="874cb-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="874cb-125">xsd:string</span></span>  <br/> |<span data-ttu-id="874cb-126">necesario</span><span class="sxs-lookup"><span data-stu-id="874cb-126">required</span></span>  <br/> ||<span data-ttu-id="874cb-127">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="874cb-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="874cb-128">Moneda</span><span class="sxs-lookup"><span data-stu-id="874cb-128">Currency</span></span>  <br/> |<span data-ttu-id="874cb-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="874cb-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="874cb-130">opcional</span><span class="sxs-lookup"><span data-stu-id="874cb-130">optional</span></span>  <br/> ||<span data-ttu-id="874cb-131">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="874cb-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="874cb-132">DataType</span><span class="sxs-lookup"><span data-stu-id="874cb-132">DataType</span></span>  <br/> |<span data-ttu-id="874cb-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="874cb-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="874cb-134">opcional</span><span class="sxs-lookup"><span data-stu-id="874cb-134">optional</span></span>  <br/> ||<span data-ttu-id="874cb-135">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="874cb-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="874cb-136">Degree</span><span class="sxs-lookup"><span data-stu-id="874cb-136">Degree</span></span>  <br/> |<span data-ttu-id="874cb-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="874cb-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="874cb-138">opcional</span><span class="sxs-lookup"><span data-stu-id="874cb-138">optional</span></span>  <br/> ||<span data-ttu-id="874cb-139">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="874cb-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="874cb-140">OrdenVisualización</span><span class="sxs-lookup"><span data-stu-id="874cb-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="874cb-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="874cb-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="874cb-142">opcional</span><span class="sxs-lookup"><span data-stu-id="874cb-142">optional</span></span>  <br/> ||<span data-ttu-id="874cb-143">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="874cb-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="874cb-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="874cb-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="874cb-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="874cb-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="874cb-146">opcional</span><span class="sxs-lookup"><span data-stu-id="874cb-146">optional</span></span>  <br/> ||<span data-ttu-id="874cb-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="874cb-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="874cb-148">Hipervínculo</span><span class="sxs-lookup"><span data-stu-id="874cb-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="874cb-149">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="874cb-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="874cb-150">opcional</span><span class="sxs-lookup"><span data-stu-id="874cb-150">optional</span></span>  <br/> ||<span data-ttu-id="874cb-151">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="874cb-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="874cb-152">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="874cb-152">Label</span></span>  <br/> |<span data-ttu-id="874cb-153">xsd: String</span><span class="sxs-lookup"><span data-stu-id="874cb-153">xsd:string</span></span>  <br/> |<span data-ttu-id="874cb-154">necesario</span><span class="sxs-lookup"><span data-stu-id="874cb-154">required</span></span>  <br/> ||<span data-ttu-id="874cb-155">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="874cb-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="874cb-156">LangID</span><span class="sxs-lookup"><span data-stu-id="874cb-156">LangID</span></span>  <br/> |<span data-ttu-id="874cb-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="874cb-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="874cb-158">opcional</span><span class="sxs-lookup"><span data-stu-id="874cb-158">optional</span></span>  <br/> ||<span data-ttu-id="874cb-159">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="874cb-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="874cb-160">Asignadas</span><span class="sxs-lookup"><span data-stu-id="874cb-160">Mapped</span></span>  <br/> |<span data-ttu-id="874cb-161">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="874cb-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="874cb-162">opcional</span><span class="sxs-lookup"><span data-stu-id="874cb-162">optional</span></span>  <br/> ||<span data-ttu-id="874cb-163">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="874cb-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="874cb-164">Nombre</span><span class="sxs-lookup"><span data-stu-id="874cb-164">Name</span></span>  <br/> |<span data-ttu-id="874cb-165">xsd: String</span><span class="sxs-lookup"><span data-stu-id="874cb-165">xsd:string</span></span>  <br/> |<span data-ttu-id="874cb-166">necesario</span><span class="sxs-lookup"><span data-stu-id="874cb-166">required</span></span>  <br/> ||<span data-ttu-id="874cb-167">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="874cb-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="874cb-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="874cb-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="874cb-169">xsd: String</span><span class="sxs-lookup"><span data-stu-id="874cb-169">xsd:string</span></span>  <br/> |<span data-ttu-id="874cb-170">opcional</span><span class="sxs-lookup"><span data-stu-id="874cb-170">optional</span></span>  <br/> ||<span data-ttu-id="874cb-171">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="874cb-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="874cb-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="874cb-172">UnitType</span></span>  <br/> |<span data-ttu-id="874cb-173">xsd: String</span><span class="sxs-lookup"><span data-stu-id="874cb-173">xsd:string</span></span>  <br/> |<span data-ttu-id="874cb-174">opcional</span><span class="sxs-lookup"><span data-stu-id="874cb-174">optional</span></span>  <br/> ||<span data-ttu-id="874cb-175">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="874cb-175">Values of the xsd:string type.</span></span>  <br/> |
   

