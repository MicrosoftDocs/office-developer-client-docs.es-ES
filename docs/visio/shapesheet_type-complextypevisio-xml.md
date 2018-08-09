---
title: ShapeSheet_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: 45282acfc8a399a5c634c1860aba1f926e0b7a94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823179"
---
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="0e2be-102">ShapeSheet_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="0e2be-102">ShapeSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0e2be-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="0e2be-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e2be-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0e2be-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0e2be-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0e2be-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0e2be-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0e2be-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0e2be-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="0e2be-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0e2be-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="0e2be-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0e2be-109">Definición</span><span class="sxs-lookup"><span data-stu-id="0e2be-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0e2be-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0e2be-110">Elements and attributes</span></span>

<span data-ttu-id="0e2be-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="0e2be-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0e2be-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0e2be-112">Child elements</span></span>

|<span data-ttu-id="0e2be-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0e2be-113">**Element**</span></span>|<span data-ttu-id="0e2be-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0e2be-114">**Type**</span></span>|<span data-ttu-id="0e2be-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e2be-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0e2be-116">Data1</span><span class="sxs-lookup"><span data-stu-id="0e2be-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0e2be-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="0e2be-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0e2be-118">Data2</span><span class="sxs-lookup"><span data-stu-id="0e2be-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0e2be-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="0e2be-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0e2be-120">Data3</span><span class="sxs-lookup"><span data-stu-id="0e2be-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0e2be-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="0e2be-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0e2be-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="0e2be-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0e2be-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="0e2be-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0e2be-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="0e2be-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0e2be-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="0e2be-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0e2be-126">Text</span><span class="sxs-lookup"><span data-stu-id="0e2be-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0e2be-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="0e2be-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0e2be-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="0e2be-128">Attributes</span></span>

|<span data-ttu-id="0e2be-129">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0e2be-129">**Attribute**</span></span>|<span data-ttu-id="0e2be-130">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0e2be-130">**Type**</span></span>|<span data-ttu-id="0e2be-131">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="0e2be-131">**Required**</span></span>|<span data-ttu-id="0e2be-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e2be-132">**Description**</span></span>|<span data-ttu-id="0e2be-133">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="0e2be-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0e2be-134">SUPR</span><span class="sxs-lookup"><span data-stu-id="0e2be-134">Del</span></span>  <br/> |<span data-ttu-id="0e2be-135">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="0e2be-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0e2be-136">opcional</span><span class="sxs-lookup"><span data-stu-id="0e2be-136">optional</span></span>  <br/> ||<span data-ttu-id="0e2be-137">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="0e2be-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0e2be-138">ID</span><span class="sxs-lookup"><span data-stu-id="0e2be-138">ID</span></span>  <br/> |<span data-ttu-id="0e2be-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0e2be-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0e2be-140">necesario</span><span class="sxs-lookup"><span data-stu-id="0e2be-140">required</span></span>  <br/> ||<span data-ttu-id="0e2be-141">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0e2be-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0e2be-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="0e2be-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="0e2be-143">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="0e2be-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0e2be-144">opcional</span><span class="sxs-lookup"><span data-stu-id="0e2be-144">optional</span></span>  <br/> ||<span data-ttu-id="0e2be-145">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="0e2be-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0e2be-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="0e2be-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="0e2be-147">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="0e2be-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0e2be-148">opcional</span><span class="sxs-lookup"><span data-stu-id="0e2be-148">optional</span></span>  <br/> ||<span data-ttu-id="0e2be-149">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="0e2be-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0e2be-150">Master</span><span class="sxs-lookup"><span data-stu-id="0e2be-150">Master</span></span>  <br/> |<span data-ttu-id="0e2be-151">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0e2be-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0e2be-152">opcional</span><span class="sxs-lookup"><span data-stu-id="0e2be-152">optional</span></span>  <br/> ||<span data-ttu-id="0e2be-153">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0e2be-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0e2be-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="0e2be-154">MasterShape</span></span>  <br/> |<span data-ttu-id="0e2be-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0e2be-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0e2be-156">opcional</span><span class="sxs-lookup"><span data-stu-id="0e2be-156">optional</span></span>  <br/> ||<span data-ttu-id="0e2be-157">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0e2be-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0e2be-158">Nombre</span><span class="sxs-lookup"><span data-stu-id="0e2be-158">Name</span></span>  <br/> |<span data-ttu-id="0e2be-159">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0e2be-159">xsd:string</span></span>  <br/> |<span data-ttu-id="0e2be-160">opcional</span><span class="sxs-lookup"><span data-stu-id="0e2be-160">optional</span></span>  <br/> ||<span data-ttu-id="0e2be-161">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0e2be-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0e2be-162">NameU</span><span class="sxs-lookup"><span data-stu-id="0e2be-162">NameU</span></span>  <br/> |<span data-ttu-id="0e2be-163">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0e2be-163">xsd:string</span></span>  <br/> |<span data-ttu-id="0e2be-164">opcional</span><span class="sxs-lookup"><span data-stu-id="0e2be-164">optional</span></span>  <br/> ||<span data-ttu-id="0e2be-165">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0e2be-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0e2be-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="0e2be-166">OriginalID</span></span>  <br/> |<span data-ttu-id="0e2be-167">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0e2be-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0e2be-168">opcional</span><span class="sxs-lookup"><span data-stu-id="0e2be-168">optional</span></span>  <br/> ||<span data-ttu-id="0e2be-169">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0e2be-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0e2be-170">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e2be-170">Type</span></span>  <br/> |<span data-ttu-id="0e2be-171">xsd:token</span><span class="sxs-lookup"><span data-stu-id="0e2be-171">xsd:token</span></span>  <br/> |<span data-ttu-id="0e2be-172">opcional</span><span class="sxs-lookup"><span data-stu-id="0e2be-172">optional</span></span>  <br/> ||<span data-ttu-id="0e2be-173">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="0e2be-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="0e2be-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="0e2be-174">UniqueID</span></span>  <br/> |<span data-ttu-id="0e2be-175">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0e2be-175">xsd:string</span></span>  <br/> |<span data-ttu-id="0e2be-176">opcional</span><span class="sxs-lookup"><span data-stu-id="0e2be-176">optional</span></span>  <br/> ||<span data-ttu-id="0e2be-177">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0e2be-177">Values of the xsd:string type.</span></span>  <br/> |
   

