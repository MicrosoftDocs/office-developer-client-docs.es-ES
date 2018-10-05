---
title: ShapeSheet_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: c48af0def561e01fe5a92a57b7416faab40f1200
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383635"
---
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="17414-102">ShapeSheet_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="17414-102">ShapeSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="17414-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="17414-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17414-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="17414-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="17414-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="17414-105">**Schema file**</span></span> <br/> |<span data-ttu-id="17414-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="17414-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="17414-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="17414-107">**Extension base**</span></span> <br/> |<span data-ttu-id="17414-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="17414-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="17414-109">Definición</span><span class="sxs-lookup"><span data-stu-id="17414-109">Definition</span></span>

```XML
          <xs:complexType name="ShapeSheet_Type">
          
          <xs:complexContent>
          <xs:extension base="Sheet_Type">
          <xs:sequence>
    <xs:element name="Shapes"  type="Shapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Text"  type="Text_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data1"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data2"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data3"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ForeignData"  type="ForeignData_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="OriginalID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
    <xs:attribute name="MasterShape"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="Master"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Type"
  type="xsd:token"
    />
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="17414-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="17414-110">Elements and attributes</span></span>

<span data-ttu-id="17414-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="17414-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="17414-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="17414-112">Child elements</span></span>

|<span data-ttu-id="17414-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="17414-113">**Element**</span></span>|<span data-ttu-id="17414-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="17414-114">**Type**</span></span>|<span data-ttu-id="17414-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="17414-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="17414-116">Data1</span><span class="sxs-lookup"><span data-stu-id="17414-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="17414-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="17414-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="17414-118">Data2</span><span class="sxs-lookup"><span data-stu-id="17414-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="17414-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="17414-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="17414-120">Data3</span><span class="sxs-lookup"><span data-stu-id="17414-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="17414-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="17414-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="17414-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="17414-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="17414-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="17414-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="17414-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="17414-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="17414-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="17414-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="17414-126">Text</span><span class="sxs-lookup"><span data-stu-id="17414-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="17414-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="17414-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="17414-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="17414-128">Attributes</span></span>

|<span data-ttu-id="17414-129">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="17414-129">**Attribute**</span></span>|<span data-ttu-id="17414-130">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="17414-130">**Type**</span></span>|<span data-ttu-id="17414-131">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="17414-131">**Required**</span></span>|<span data-ttu-id="17414-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="17414-132">**Description**</span></span>|<span data-ttu-id="17414-133">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="17414-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="17414-134">SUPR</span><span class="sxs-lookup"><span data-stu-id="17414-134">Del</span></span>  <br/> |<span data-ttu-id="17414-135">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="17414-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="17414-136">opcional</span><span class="sxs-lookup"><span data-stu-id="17414-136">optional</span></span>  <br/> ||<span data-ttu-id="17414-137">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="17414-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="17414-138">ID</span><span class="sxs-lookup"><span data-stu-id="17414-138">ID</span></span>  <br/> |<span data-ttu-id="17414-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="17414-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="17414-140">necesario</span><span class="sxs-lookup"><span data-stu-id="17414-140">required</span></span>  <br/> ||<span data-ttu-id="17414-141">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="17414-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="17414-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="17414-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="17414-143">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="17414-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="17414-144">opcional</span><span class="sxs-lookup"><span data-stu-id="17414-144">optional</span></span>  <br/> ||<span data-ttu-id="17414-145">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="17414-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="17414-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="17414-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="17414-147">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="17414-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="17414-148">opcional</span><span class="sxs-lookup"><span data-stu-id="17414-148">optional</span></span>  <br/> ||<span data-ttu-id="17414-149">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="17414-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="17414-150">Master</span><span class="sxs-lookup"><span data-stu-id="17414-150">Master</span></span>  <br/> |<span data-ttu-id="17414-151">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="17414-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="17414-152">opcional</span><span class="sxs-lookup"><span data-stu-id="17414-152">optional</span></span>  <br/> ||<span data-ttu-id="17414-153">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="17414-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="17414-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="17414-154">MasterShape</span></span>  <br/> |<span data-ttu-id="17414-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="17414-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="17414-156">opcional</span><span class="sxs-lookup"><span data-stu-id="17414-156">optional</span></span>  <br/> ||<span data-ttu-id="17414-157">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="17414-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="17414-158">Nombre</span><span class="sxs-lookup"><span data-stu-id="17414-158">Name</span></span>  <br/> |<span data-ttu-id="17414-159">xsd: String</span><span class="sxs-lookup"><span data-stu-id="17414-159">xsd:string</span></span>  <br/> |<span data-ttu-id="17414-160">opcional</span><span class="sxs-lookup"><span data-stu-id="17414-160">optional</span></span>  <br/> ||<span data-ttu-id="17414-161">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="17414-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="17414-162">NameU</span><span class="sxs-lookup"><span data-stu-id="17414-162">NameU</span></span>  <br/> |<span data-ttu-id="17414-163">xsd: String</span><span class="sxs-lookup"><span data-stu-id="17414-163">xsd:string</span></span>  <br/> |<span data-ttu-id="17414-164">opcional</span><span class="sxs-lookup"><span data-stu-id="17414-164">optional</span></span>  <br/> ||<span data-ttu-id="17414-165">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="17414-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="17414-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="17414-166">OriginalID</span></span>  <br/> |<span data-ttu-id="17414-167">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="17414-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="17414-168">opcional</span><span class="sxs-lookup"><span data-stu-id="17414-168">optional</span></span>  <br/> ||<span data-ttu-id="17414-169">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="17414-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="17414-170">Tipo</span><span class="sxs-lookup"><span data-stu-id="17414-170">Type</span></span>  <br/> |<span data-ttu-id="17414-171">xsd:token</span><span class="sxs-lookup"><span data-stu-id="17414-171">xsd:token</span></span>  <br/> |<span data-ttu-id="17414-172">opcional</span><span class="sxs-lookup"><span data-stu-id="17414-172">optional</span></span>  <br/> ||<span data-ttu-id="17414-173">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="17414-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="17414-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="17414-174">UniqueID</span></span>  <br/> |<span data-ttu-id="17414-175">xsd: String</span><span class="sxs-lookup"><span data-stu-id="17414-175">xsd:string</span></span>  <br/> |<span data-ttu-id="17414-176">opcional</span><span class="sxs-lookup"><span data-stu-id="17414-176">optional</span></span>  <br/> ||<span data-ttu-id="17414-177">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="17414-177">Values of the xsd:string type.</span></span>  <br/> |
   

