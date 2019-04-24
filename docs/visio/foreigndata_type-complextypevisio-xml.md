---
title: ForeignData_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 6630c8b33dc1c4c7cbb12bb9727d4f0b1e1b19d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346014"
---
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="4fdac-102">ForeignData_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="4fdac-102">ForeignData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4fdac-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="4fdac-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4fdac-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4fdac-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4fdac-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4fdac-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4fdac-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="4fdac-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4fdac-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="4fdac-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4fdac-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4fdac-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4fdac-109">Definición</span><span class="sxs-lookup"><span data-stu-id="4fdac-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4fdac-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="4fdac-110">Elements and attributes</span></span>

<span data-ttu-id="4fdac-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="4fdac-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4fdac-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4fdac-112">Child elements</span></span>

|<span data-ttu-id="4fdac-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4fdac-113">**Element**</span></span>|<span data-ttu-id="4fdac-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4fdac-114">**Type**</span></span>|<span data-ttu-id="4fdac-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4fdac-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4fdac-116">REL</span><span class="sxs-lookup"><span data-stu-id="4fdac-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4fdac-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="4fdac-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4fdac-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="4fdac-118">Attributes</span></span>

|<span data-ttu-id="4fdac-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="4fdac-119">**Attribute**</span></span>|<span data-ttu-id="4fdac-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4fdac-120">**Type**</span></span>|<span data-ttu-id="4fdac-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="4fdac-121">**Required**</span></span>|<span data-ttu-id="4fdac-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4fdac-122">**Description**</span></span>|<span data-ttu-id="4fdac-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="4fdac-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4fdac-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="4fdac-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="4fdac-125">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="4fdac-125">xsd:double</span></span>  <br/> |<span data-ttu-id="4fdac-126">opcional</span><span class="sxs-lookup"><span data-stu-id="4fdac-126">optional</span></span>  <br/> ||<span data-ttu-id="4fdac-127">Valores del tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="4fdac-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="4fdac-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="4fdac-128">CompressionType</span></span>  <br/> |<span data-ttu-id="4fdac-129">xsd: token</span><span class="sxs-lookup"><span data-stu-id="4fdac-129">xsd:token</span></span>  <br/> |<span data-ttu-id="4fdac-130">opcional</span><span class="sxs-lookup"><span data-stu-id="4fdac-130">optional</span></span>  <br/> ||<span data-ttu-id="4fdac-131">Valores del tipo xsd: token.</span><span class="sxs-lookup"><span data-stu-id="4fdac-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="4fdac-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="4fdac-132">ExtentX</span></span>  <br/> |<span data-ttu-id="4fdac-133">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="4fdac-133">xsd:double</span></span>  <br/> |<span data-ttu-id="4fdac-134">opcional</span><span class="sxs-lookup"><span data-stu-id="4fdac-134">optional</span></span>  <br/> ||<span data-ttu-id="4fdac-135">Valores del tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="4fdac-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="4fdac-136">Extensión</span><span class="sxs-lookup"><span data-stu-id="4fdac-136">ExtentY</span></span>  <br/> |<span data-ttu-id="4fdac-137">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="4fdac-137">xsd:double</span></span>  <br/> |<span data-ttu-id="4fdac-138">opcional</span><span class="sxs-lookup"><span data-stu-id="4fdac-138">optional</span></span>  <br/> ||<span data-ttu-id="4fdac-139">Valores del tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="4fdac-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="4fdac-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="4fdac-140">ForeignType</span></span>  <br/> |<span data-ttu-id="4fdac-141">xsd: token</span><span class="sxs-lookup"><span data-stu-id="4fdac-141">xsd:token</span></span>  <br/> |<span data-ttu-id="4fdac-142">necesario</span><span class="sxs-lookup"><span data-stu-id="4fdac-142">required</span></span>  <br/> ||<span data-ttu-id="4fdac-143">Valores del tipo xsd: token.</span><span class="sxs-lookup"><span data-stu-id="4fdac-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="4fdac-144">Absolute</span><span class="sxs-lookup"><span data-stu-id="4fdac-144">MappingMode</span></span>  <br/> |<span data-ttu-id="4fdac-145">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="4fdac-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="4fdac-146">opcional</span><span class="sxs-lookup"><span data-stu-id="4fdac-146">optional</span></span>  <br/> ||<span data-ttu-id="4fdac-147">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="4fdac-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="4fdac-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="4fdac-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="4fdac-149">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="4fdac-149">xsd:double</span></span>  <br/> |<span data-ttu-id="4fdac-150">opcional</span><span class="sxs-lookup"><span data-stu-id="4fdac-150">optional</span></span>  <br/> ||<span data-ttu-id="4fdac-151">Valores del tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="4fdac-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="4fdac-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="4fdac-152">ObjectType</span></span>  <br/> |<span data-ttu-id="4fdac-153">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4fdac-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4fdac-154">opcional</span><span class="sxs-lookup"><span data-stu-id="4fdac-154">optional</span></span>  <br/> ||<span data-ttu-id="4fdac-155">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4fdac-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4fdac-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="4fdac-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="4fdac-157">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="4fdac-157">xsd:double</span></span>  <br/> |<span data-ttu-id="4fdac-158">opcional</span><span class="sxs-lookup"><span data-stu-id="4fdac-158">optional</span></span>  <br/> ||<span data-ttu-id="4fdac-159">Valores del tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="4fdac-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="4fdac-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="4fdac-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="4fdac-161">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="4fdac-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4fdac-162">opcional</span><span class="sxs-lookup"><span data-stu-id="4fdac-162">optional</span></span>  <br/> ||<span data-ttu-id="4fdac-163">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4fdac-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

