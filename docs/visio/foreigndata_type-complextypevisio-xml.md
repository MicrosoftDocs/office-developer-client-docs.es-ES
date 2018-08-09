---
title: ForeignData_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 1d9358de2f88a1b9e035ecf4966544ea935f8b2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822196"
---
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="65635-102">ForeignData_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="65635-102">ForeignData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="65635-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="65635-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65635-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="65635-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="65635-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="65635-105">**Schema file**</span></span> <br/> |<span data-ttu-id="65635-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="65635-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="65635-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="65635-107">**Extension base**</span></span> <br/> |<span data-ttu-id="65635-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="65635-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="65635-109">Definición</span><span class="sxs-lookup"><span data-stu-id="65635-109">Definition</span></span>

```XML
          <xs:complexType name="ForeignData_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ForeignType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="ObjectType"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ShowAsIcon"
  type="xsd:boolean"
    />
    <xs:attribute name="ObjectWidth"
  type="xsd:double"
    />
    <xs:attribute name="ObjectHeight"
  type="xsd:double"
    />
    <xs:attribute name="MappingMode"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ExtentX"
  type="xsd:double"
    />
    <xs:attribute name="ExtentY"
  type="xsd:double"
    />
    <xs:attribute name="CompressionType"
  type="xsd:token"
    />
    <xs:attribute name="CompressionLevel"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="65635-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="65635-110">Elements and attributes</span></span>

<span data-ttu-id="65635-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="65635-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="65635-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="65635-112">Child elements</span></span>

|<span data-ttu-id="65635-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="65635-113">**Element**</span></span>|<span data-ttu-id="65635-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="65635-114">**Type**</span></span>|<span data-ttu-id="65635-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65635-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="65635-116">Rel</span><span class="sxs-lookup"><span data-stu-id="65635-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65635-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="65635-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="65635-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="65635-118">Attributes</span></span>

|<span data-ttu-id="65635-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="65635-119">**Attribute**</span></span>|<span data-ttu-id="65635-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="65635-120">**Type**</span></span>|<span data-ttu-id="65635-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="65635-121">**Required**</span></span>|<span data-ttu-id="65635-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65635-122">**Description**</span></span>|<span data-ttu-id="65635-123">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="65635-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="65635-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="65635-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="65635-125">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="65635-125">xsd:double</span></span>  <br/> |<span data-ttu-id="65635-126">opcional</span><span class="sxs-lookup"><span data-stu-id="65635-126">optional</span></span>  <br/> ||<span data-ttu-id="65635-127">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="65635-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="65635-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="65635-128">CompressionType</span></span>  <br/> |<span data-ttu-id="65635-129">xsd:token</span><span class="sxs-lookup"><span data-stu-id="65635-129">xsd:token</span></span>  <br/> |<span data-ttu-id="65635-130">opcional</span><span class="sxs-lookup"><span data-stu-id="65635-130">optional</span></span>  <br/> ||<span data-ttu-id="65635-131">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="65635-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="65635-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="65635-132">ExtentX</span></span>  <br/> |<span data-ttu-id="65635-133">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="65635-133">xsd:double</span></span>  <br/> |<span data-ttu-id="65635-134">opcional</span><span class="sxs-lookup"><span data-stu-id="65635-134">optional</span></span>  <br/> ||<span data-ttu-id="65635-135">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="65635-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="65635-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="65635-136">ExtentY</span></span>  <br/> |<span data-ttu-id="65635-137">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="65635-137">xsd:double</span></span>  <br/> |<span data-ttu-id="65635-138">opcional</span><span class="sxs-lookup"><span data-stu-id="65635-138">optional</span></span>  <br/> ||<span data-ttu-id="65635-139">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="65635-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="65635-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="65635-140">ForeignType</span></span>  <br/> |<span data-ttu-id="65635-141">xsd:token</span><span class="sxs-lookup"><span data-stu-id="65635-141">xsd:token</span></span>  <br/> |<span data-ttu-id="65635-142">necesario</span><span class="sxs-lookup"><span data-stu-id="65635-142">required</span></span>  <br/> ||<span data-ttu-id="65635-143">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="65635-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="65635-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="65635-144">MappingMode</span></span>  <br/> |<span data-ttu-id="65635-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="65635-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="65635-146">opcional</span><span class="sxs-lookup"><span data-stu-id="65635-146">optional</span></span>  <br/> ||<span data-ttu-id="65635-147">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="65635-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="65635-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="65635-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="65635-149">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="65635-149">xsd:double</span></span>  <br/> |<span data-ttu-id="65635-150">opcional</span><span class="sxs-lookup"><span data-stu-id="65635-150">optional</span></span>  <br/> ||<span data-ttu-id="65635-151">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="65635-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="65635-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="65635-152">ObjectType</span></span>  <br/> |<span data-ttu-id="65635-153">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="65635-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="65635-154">opcional</span><span class="sxs-lookup"><span data-stu-id="65635-154">optional</span></span>  <br/> ||<span data-ttu-id="65635-155">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="65635-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="65635-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="65635-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="65635-157">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="65635-157">xsd:double</span></span>  <br/> |<span data-ttu-id="65635-158">opcional</span><span class="sxs-lookup"><span data-stu-id="65635-158">optional</span></span>  <br/> ||<span data-ttu-id="65635-159">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="65635-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="65635-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="65635-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="65635-161">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="65635-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="65635-162">opcional</span><span class="sxs-lookup"><span data-stu-id="65635-162">optional</span></span>  <br/> ||<span data-ttu-id="65635-163">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="65635-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

