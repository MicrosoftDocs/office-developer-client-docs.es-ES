---
title: ForeignData_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 6630c8b33dc1c4c7cbb12bb9727d4f0b1e1b19d2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384160"
---
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="3fb09-102">ForeignData_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="3fb09-102">ForeignData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3fb09-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="3fb09-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3fb09-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3fb09-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3fb09-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3fb09-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3fb09-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3fb09-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3fb09-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="3fb09-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3fb09-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3fb09-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3fb09-109">Definición</span><span class="sxs-lookup"><span data-stu-id="3fb09-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3fb09-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="3fb09-110">Elements and attributes</span></span>

<span data-ttu-id="3fb09-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="3fb09-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3fb09-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3fb09-112">Child elements</span></span>

|<span data-ttu-id="3fb09-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3fb09-113">**Element**</span></span>|<span data-ttu-id="3fb09-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3fb09-114">**Type**</span></span>|<span data-ttu-id="3fb09-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3fb09-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3fb09-116">Rel</span><span class="sxs-lookup"><span data-stu-id="3fb09-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3fb09-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="3fb09-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3fb09-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="3fb09-118">Attributes</span></span>

|<span data-ttu-id="3fb09-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="3fb09-119">**Attribute**</span></span>|<span data-ttu-id="3fb09-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3fb09-120">**Type**</span></span>|<span data-ttu-id="3fb09-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="3fb09-121">**Required**</span></span>|<span data-ttu-id="3fb09-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3fb09-122">**Description**</span></span>|<span data-ttu-id="3fb09-123">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="3fb09-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3fb09-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="3fb09-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="3fb09-125">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="3fb09-125">xsd:double</span></span>  <br/> |<span data-ttu-id="3fb09-126">opcional</span><span class="sxs-lookup"><span data-stu-id="3fb09-126">optional</span></span>  <br/> ||<span data-ttu-id="3fb09-127">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="3fb09-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="3fb09-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="3fb09-128">CompressionType</span></span>  <br/> |<span data-ttu-id="3fb09-129">xsd:token</span><span class="sxs-lookup"><span data-stu-id="3fb09-129">xsd:token</span></span>  <br/> |<span data-ttu-id="3fb09-130">opcional</span><span class="sxs-lookup"><span data-stu-id="3fb09-130">optional</span></span>  <br/> ||<span data-ttu-id="3fb09-131">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="3fb09-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="3fb09-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="3fb09-132">ExtentX</span></span>  <br/> |<span data-ttu-id="3fb09-133">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="3fb09-133">xsd:double</span></span>  <br/> |<span data-ttu-id="3fb09-134">opcional</span><span class="sxs-lookup"><span data-stu-id="3fb09-134">optional</span></span>  <br/> ||<span data-ttu-id="3fb09-135">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="3fb09-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="3fb09-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="3fb09-136">ExtentY</span></span>  <br/> |<span data-ttu-id="3fb09-137">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="3fb09-137">xsd:double</span></span>  <br/> |<span data-ttu-id="3fb09-138">opcional</span><span class="sxs-lookup"><span data-stu-id="3fb09-138">optional</span></span>  <br/> ||<span data-ttu-id="3fb09-139">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="3fb09-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="3fb09-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="3fb09-140">ForeignType</span></span>  <br/> |<span data-ttu-id="3fb09-141">xsd:token</span><span class="sxs-lookup"><span data-stu-id="3fb09-141">xsd:token</span></span>  <br/> |<span data-ttu-id="3fb09-142">necesario</span><span class="sxs-lookup"><span data-stu-id="3fb09-142">required</span></span>  <br/> ||<span data-ttu-id="3fb09-143">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="3fb09-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="3fb09-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="3fb09-144">MappingMode</span></span>  <br/> |<span data-ttu-id="3fb09-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="3fb09-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="3fb09-146">opcional</span><span class="sxs-lookup"><span data-stu-id="3fb09-146">optional</span></span>  <br/> ||<span data-ttu-id="3fb09-147">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="3fb09-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="3fb09-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="3fb09-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="3fb09-149">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="3fb09-149">xsd:double</span></span>  <br/> |<span data-ttu-id="3fb09-150">opcional</span><span class="sxs-lookup"><span data-stu-id="3fb09-150">optional</span></span>  <br/> ||<span data-ttu-id="3fb09-151">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="3fb09-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="3fb09-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="3fb09-152">ObjectType</span></span>  <br/> |<span data-ttu-id="3fb09-153">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3fb09-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3fb09-154">opcional</span><span class="sxs-lookup"><span data-stu-id="3fb09-154">optional</span></span>  <br/> ||<span data-ttu-id="3fb09-155">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3fb09-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3fb09-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="3fb09-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="3fb09-157">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="3fb09-157">xsd:double</span></span>  <br/> |<span data-ttu-id="3fb09-158">opcional</span><span class="sxs-lookup"><span data-stu-id="3fb09-158">optional</span></span>  <br/> ||<span data-ttu-id="3fb09-159">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="3fb09-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="3fb09-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="3fb09-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="3fb09-161">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="3fb09-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3fb09-162">opcional</span><span class="sxs-lookup"><span data-stu-id="3fb09-162">optional</span></span>  <br/> ||<span data-ttu-id="3fb09-163">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="3fb09-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

