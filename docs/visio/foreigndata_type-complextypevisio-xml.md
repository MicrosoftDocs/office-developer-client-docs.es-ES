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
# <a name="foreigndata_type-complextype-visio-xml"></a><span data-ttu-id="d5afe-102">ForeignData_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d5afe-102">ForeignData_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d5afe-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="d5afe-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5afe-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d5afe-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d5afe-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d5afe-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d5afe-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d5afe-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d5afe-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="d5afe-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d5afe-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d5afe-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d5afe-109">Definición</span><span class="sxs-lookup"><span data-stu-id="d5afe-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d5afe-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="d5afe-110">Elements and attributes</span></span>

<span data-ttu-id="d5afe-111">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="d5afe-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d5afe-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d5afe-112">Child elements</span></span>

|<span data-ttu-id="d5afe-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d5afe-113">**Element**</span></span>|<span data-ttu-id="d5afe-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d5afe-114">**Type**</span></span>|<span data-ttu-id="d5afe-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d5afe-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d5afe-116">Rel</span><span class="sxs-lookup"><span data-stu-id="d5afe-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5afe-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="d5afe-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d5afe-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="d5afe-118">Attributes</span></span>

|<span data-ttu-id="d5afe-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="d5afe-119">**Attribute**</span></span>|<span data-ttu-id="d5afe-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d5afe-120">**Type**</span></span>|<span data-ttu-id="d5afe-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="d5afe-121">**Required**</span></span>|<span data-ttu-id="d5afe-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d5afe-122">**Description**</span></span>|<span data-ttu-id="d5afe-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="d5afe-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d5afe-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="d5afe-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="d5afe-125">xsd:double</span><span class="sxs-lookup"><span data-stu-id="d5afe-125">xsd:double</span></span>  <br/> |<span data-ttu-id="d5afe-126">opcional</span><span class="sxs-lookup"><span data-stu-id="d5afe-126">optional</span></span>  <br/> ||<span data-ttu-id="d5afe-127">Valores del tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="d5afe-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="d5afe-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="d5afe-128">CompressionType</span></span>  <br/> |<span data-ttu-id="d5afe-129">xsd:token</span><span class="sxs-lookup"><span data-stu-id="d5afe-129">xsd:token</span></span>  <br/> |<span data-ttu-id="d5afe-130">opcional</span><span class="sxs-lookup"><span data-stu-id="d5afe-130">optional</span></span>  <br/> ||<span data-ttu-id="d5afe-131">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="d5afe-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="d5afe-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="d5afe-132">ExtentX</span></span>  <br/> |<span data-ttu-id="d5afe-133">xsd:double</span><span class="sxs-lookup"><span data-stu-id="d5afe-133">xsd:double</span></span>  <br/> |<span data-ttu-id="d5afe-134">opcional</span><span class="sxs-lookup"><span data-stu-id="d5afe-134">optional</span></span>  <br/> ||<span data-ttu-id="d5afe-135">Valores del tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="d5afe-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="d5afe-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="d5afe-136">ExtentY</span></span>  <br/> |<span data-ttu-id="d5afe-137">xsd:double</span><span class="sxs-lookup"><span data-stu-id="d5afe-137">xsd:double</span></span>  <br/> |<span data-ttu-id="d5afe-138">opcional</span><span class="sxs-lookup"><span data-stu-id="d5afe-138">optional</span></span>  <br/> ||<span data-ttu-id="d5afe-139">Valores del tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="d5afe-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="d5afe-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="d5afe-140">ForeignType</span></span>  <br/> |<span data-ttu-id="d5afe-141">xsd:token</span><span class="sxs-lookup"><span data-stu-id="d5afe-141">xsd:token</span></span>  <br/> |<span data-ttu-id="d5afe-142">necesario</span><span class="sxs-lookup"><span data-stu-id="d5afe-142">required</span></span>  <br/> ||<span data-ttu-id="d5afe-143">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="d5afe-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="d5afe-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="d5afe-144">MappingMode</span></span>  <br/> |<span data-ttu-id="d5afe-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d5afe-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d5afe-146">opcional</span><span class="sxs-lookup"><span data-stu-id="d5afe-146">optional</span></span>  <br/> ||<span data-ttu-id="d5afe-147">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d5afe-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d5afe-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="d5afe-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="d5afe-149">xsd:double</span><span class="sxs-lookup"><span data-stu-id="d5afe-149">xsd:double</span></span>  <br/> |<span data-ttu-id="d5afe-150">opcional</span><span class="sxs-lookup"><span data-stu-id="d5afe-150">optional</span></span>  <br/> ||<span data-ttu-id="d5afe-151">Valores del tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="d5afe-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="d5afe-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="d5afe-152">ObjectType</span></span>  <br/> |<span data-ttu-id="d5afe-153">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d5afe-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5afe-154">opcional</span><span class="sxs-lookup"><span data-stu-id="d5afe-154">optional</span></span>  <br/> ||<span data-ttu-id="d5afe-155">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d5afe-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d5afe-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="d5afe-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="d5afe-157">xsd:double</span><span class="sxs-lookup"><span data-stu-id="d5afe-157">xsd:double</span></span>  <br/> |<span data-ttu-id="d5afe-158">opcional</span><span class="sxs-lookup"><span data-stu-id="d5afe-158">optional</span></span>  <br/> ||<span data-ttu-id="d5afe-159">Valores del tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="d5afe-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="d5afe-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="d5afe-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="d5afe-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="d5afe-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d5afe-162">opcional</span><span class="sxs-lookup"><span data-stu-id="d5afe-162">optional</span></span>  <br/> ||<span data-ttu-id="d5afe-163">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="d5afe-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

