---
title: ShapeSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: 0094bc9643cc1331e0b47bd11a59769a553e17f7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542061"
---
# <a name="shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="e90ec-102">ShapeSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e90ec-102">ShapeSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="e90ec-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="e90ec-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e90ec-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e90ec-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e90ec-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e90ec-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e90ec-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e90ec-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e90ec-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="e90ec-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e90ec-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="e90ec-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e90ec-109">Definición</span><span class="sxs-lookup"><span data-stu-id="e90ec-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e90ec-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e90ec-110">Elements and attributes</span></span>

<span data-ttu-id="e90ec-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="e90ec-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e90ec-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e90ec-112">Child elements</span></span>

|<span data-ttu-id="e90ec-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e90ec-113">**Element**</span></span>|<span data-ttu-id="e90ec-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e90ec-114">**Type**</span></span>|<span data-ttu-id="e90ec-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e90ec-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e90ec-116">Data1</span><span class="sxs-lookup"><span data-stu-id="e90ec-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e90ec-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="e90ec-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e90ec-118">Data2</span><span class="sxs-lookup"><span data-stu-id="e90ec-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e90ec-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="e90ec-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e90ec-120">Data3</span><span class="sxs-lookup"><span data-stu-id="e90ec-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e90ec-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="e90ec-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e90ec-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="e90ec-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e90ec-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="e90ec-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e90ec-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="e90ec-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e90ec-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="e90ec-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e90ec-126">Text</span><span class="sxs-lookup"><span data-stu-id="e90ec-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e90ec-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="e90ec-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e90ec-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="e90ec-128">Attributes</span></span>

|<span data-ttu-id="e90ec-129">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="e90ec-129">**Attribute**</span></span>|<span data-ttu-id="e90ec-130">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e90ec-130">**Type**</span></span>|<span data-ttu-id="e90ec-131">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="e90ec-131">**Required**</span></span>|<span data-ttu-id="e90ec-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e90ec-132">**Description**</span></span>|<span data-ttu-id="e90ec-133">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="e90ec-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e90ec-134">Supr</span><span class="sxs-lookup"><span data-stu-id="e90ec-134">Del</span></span>  <br/> |<span data-ttu-id="e90ec-135">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="e90ec-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e90ec-136">opcional</span><span class="sxs-lookup"><span data-stu-id="e90ec-136">optional</span></span>  <br/> ||<span data-ttu-id="e90ec-137">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="e90ec-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e90ec-138">ID</span><span class="sxs-lookup"><span data-stu-id="e90ec-138">ID</span></span>  <br/> |<span data-ttu-id="e90ec-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e90ec-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e90ec-140">necesario</span><span class="sxs-lookup"><span data-stu-id="e90ec-140">required</span></span>  <br/> ||<span data-ttu-id="e90ec-141">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e90ec-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e90ec-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="e90ec-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="e90ec-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="e90ec-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e90ec-144">opcional</span><span class="sxs-lookup"><span data-stu-id="e90ec-144">optional</span></span>  <br/> ||<span data-ttu-id="e90ec-145">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="e90ec-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e90ec-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="e90ec-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="e90ec-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="e90ec-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e90ec-148">opcional</span><span class="sxs-lookup"><span data-stu-id="e90ec-148">optional</span></span>  <br/> ||<span data-ttu-id="e90ec-149">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="e90ec-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e90ec-150">Master</span><span class="sxs-lookup"><span data-stu-id="e90ec-150">Master</span></span>  <br/> |<span data-ttu-id="e90ec-151">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e90ec-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e90ec-152">opcional</span><span class="sxs-lookup"><span data-stu-id="e90ec-152">optional</span></span>  <br/> ||<span data-ttu-id="e90ec-153">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e90ec-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e90ec-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="e90ec-154">MasterShape</span></span>  <br/> |<span data-ttu-id="e90ec-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e90ec-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e90ec-156">opcional</span><span class="sxs-lookup"><span data-stu-id="e90ec-156">optional</span></span>  <br/> ||<span data-ttu-id="e90ec-157">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e90ec-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e90ec-158">Nombre</span><span class="sxs-lookup"><span data-stu-id="e90ec-158">Name</span></span>  <br/> |<span data-ttu-id="e90ec-159">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e90ec-159">xsd:string</span></span>  <br/> |<span data-ttu-id="e90ec-160">opcional</span><span class="sxs-lookup"><span data-stu-id="e90ec-160">optional</span></span>  <br/> ||<span data-ttu-id="e90ec-161">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e90ec-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e90ec-162">NameU</span><span class="sxs-lookup"><span data-stu-id="e90ec-162">NameU</span></span>  <br/> |<span data-ttu-id="e90ec-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e90ec-163">xsd:string</span></span>  <br/> |<span data-ttu-id="e90ec-164">opcional</span><span class="sxs-lookup"><span data-stu-id="e90ec-164">optional</span></span>  <br/> ||<span data-ttu-id="e90ec-165">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e90ec-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e90ec-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="e90ec-166">OriginalID</span></span>  <br/> |<span data-ttu-id="e90ec-167">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e90ec-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e90ec-168">opcional</span><span class="sxs-lookup"><span data-stu-id="e90ec-168">optional</span></span>  <br/> ||<span data-ttu-id="e90ec-169">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e90ec-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e90ec-170">Tipo</span><span class="sxs-lookup"><span data-stu-id="e90ec-170">Type</span></span>  <br/> |<span data-ttu-id="e90ec-171">xsd:token</span><span class="sxs-lookup"><span data-stu-id="e90ec-171">xsd:token</span></span>  <br/> |<span data-ttu-id="e90ec-172">opcional</span><span class="sxs-lookup"><span data-stu-id="e90ec-172">optional</span></span>  <br/> ||<span data-ttu-id="e90ec-173">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="e90ec-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="e90ec-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="e90ec-174">UniqueID</span></span>  <br/> |<span data-ttu-id="e90ec-175">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e90ec-175">xsd:string</span></span>  <br/> |<span data-ttu-id="e90ec-176">opcional</span><span class="sxs-lookup"><span data-stu-id="e90ec-176">optional</span></span>  <br/> ||<span data-ttu-id="e90ec-177">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e90ec-177">Values of the xsd:string type.</span></span>  <br/> |
   

