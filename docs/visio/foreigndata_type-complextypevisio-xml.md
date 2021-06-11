---
title: ForeignData_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 39396ef0db5b78d6f32d8828103eecd105f8b91d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539866"
---
# <a name="foreigndata_type-complextype-visio-xml"></a><span data-ttu-id="48560-102">ForeignData_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="48560-102">ForeignData_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="48560-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="48560-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48560-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="48560-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="48560-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="48560-105">**Schema file**</span></span> <br/> |<span data-ttu-id="48560-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="48560-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="48560-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="48560-107">**Extension base**</span></span> <br/> |<span data-ttu-id="48560-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="48560-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="48560-109">Definición</span><span class="sxs-lookup"><span data-stu-id="48560-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="48560-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="48560-110">Elements and attributes</span></span>

<span data-ttu-id="48560-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="48560-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="48560-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="48560-112">Child elements</span></span>

|<span data-ttu-id="48560-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="48560-113">**Element**</span></span>|<span data-ttu-id="48560-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="48560-114">**Type**</span></span>|<span data-ttu-id="48560-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="48560-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="48560-116">Rel</span><span class="sxs-lookup"><span data-stu-id="48560-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="48560-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="48560-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="48560-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="48560-118">Attributes</span></span>

|<span data-ttu-id="48560-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="48560-119">**Attribute**</span></span>|<span data-ttu-id="48560-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="48560-120">**Type**</span></span>|<span data-ttu-id="48560-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="48560-121">**Required**</span></span>|<span data-ttu-id="48560-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="48560-122">**Description**</span></span>|<span data-ttu-id="48560-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="48560-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="48560-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="48560-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="48560-125">xsd:double</span><span class="sxs-lookup"><span data-stu-id="48560-125">xsd:double</span></span>  <br/> |<span data-ttu-id="48560-126">opcional</span><span class="sxs-lookup"><span data-stu-id="48560-126">optional</span></span>  <br/> ||<span data-ttu-id="48560-127">Valores del tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="48560-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="48560-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="48560-128">CompressionType</span></span>  <br/> |<span data-ttu-id="48560-129">xsd:token</span><span class="sxs-lookup"><span data-stu-id="48560-129">xsd:token</span></span>  <br/> |<span data-ttu-id="48560-130">opcional</span><span class="sxs-lookup"><span data-stu-id="48560-130">optional</span></span>  <br/> ||<span data-ttu-id="48560-131">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="48560-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="48560-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="48560-132">ExtentX</span></span>  <br/> |<span data-ttu-id="48560-133">xsd:double</span><span class="sxs-lookup"><span data-stu-id="48560-133">xsd:double</span></span>  <br/> |<span data-ttu-id="48560-134">opcional</span><span class="sxs-lookup"><span data-stu-id="48560-134">optional</span></span>  <br/> ||<span data-ttu-id="48560-135">Valores del tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="48560-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="48560-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="48560-136">ExtentY</span></span>  <br/> |<span data-ttu-id="48560-137">xsd:double</span><span class="sxs-lookup"><span data-stu-id="48560-137">xsd:double</span></span>  <br/> |<span data-ttu-id="48560-138">opcional</span><span class="sxs-lookup"><span data-stu-id="48560-138">optional</span></span>  <br/> ||<span data-ttu-id="48560-139">Valores del tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="48560-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="48560-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="48560-140">ForeignType</span></span>  <br/> |<span data-ttu-id="48560-141">xsd:token</span><span class="sxs-lookup"><span data-stu-id="48560-141">xsd:token</span></span>  <br/> |<span data-ttu-id="48560-142">necesario</span><span class="sxs-lookup"><span data-stu-id="48560-142">required</span></span>  <br/> ||<span data-ttu-id="48560-143">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="48560-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="48560-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="48560-144">MappingMode</span></span>  <br/> |<span data-ttu-id="48560-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="48560-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="48560-146">opcional</span><span class="sxs-lookup"><span data-stu-id="48560-146">optional</span></span>  <br/> ||<span data-ttu-id="48560-147">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="48560-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="48560-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="48560-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="48560-149">xsd:double</span><span class="sxs-lookup"><span data-stu-id="48560-149">xsd:double</span></span>  <br/> |<span data-ttu-id="48560-150">opcional</span><span class="sxs-lookup"><span data-stu-id="48560-150">optional</span></span>  <br/> ||<span data-ttu-id="48560-151">Valores del tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="48560-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="48560-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="48560-152">ObjectType</span></span>  <br/> |<span data-ttu-id="48560-153">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="48560-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="48560-154">opcional</span><span class="sxs-lookup"><span data-stu-id="48560-154">optional</span></span>  <br/> ||<span data-ttu-id="48560-155">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="48560-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="48560-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="48560-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="48560-157">xsd:double</span><span class="sxs-lookup"><span data-stu-id="48560-157">xsd:double</span></span>  <br/> |<span data-ttu-id="48560-158">opcional</span><span class="sxs-lookup"><span data-stu-id="48560-158">optional</span></span>  <br/> ||<span data-ttu-id="48560-159">Valores del tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="48560-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="48560-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="48560-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="48560-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="48560-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="48560-162">opcional</span><span class="sxs-lookup"><span data-stu-id="48560-162">optional</span></span>  <br/> ||<span data-ttu-id="48560-163">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="48560-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

