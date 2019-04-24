---
title: ShapeSheet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: c48af0def561e01fe5a92a57b7416faab40f1200
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349136"
---
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="c08cb-102">ShapeSheet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="c08cb-102">ShapeSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c08cb-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="c08cb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c08cb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c08cb-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c08cb-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c08cb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c08cb-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="c08cb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c08cb-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="c08cb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c08cb-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="c08cb-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c08cb-109">Definición</span><span class="sxs-lookup"><span data-stu-id="c08cb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c08cb-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c08cb-110">Elements and attributes</span></span>

<span data-ttu-id="c08cb-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="c08cb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c08cb-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c08cb-112">Child elements</span></span>

|<span data-ttu-id="c08cb-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c08cb-113">**Element**</span></span>|<span data-ttu-id="c08cb-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c08cb-114">**Type**</span></span>|<span data-ttu-id="c08cb-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c08cb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c08cb-116">Data1</span><span class="sxs-lookup"><span data-stu-id="c08cb-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c08cb-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="c08cb-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c08cb-118">Data2</span><span class="sxs-lookup"><span data-stu-id="c08cb-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c08cb-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="c08cb-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c08cb-120">Data3</span><span class="sxs-lookup"><span data-stu-id="c08cb-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c08cb-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="c08cb-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c08cb-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="c08cb-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c08cb-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="c08cb-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c08cb-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="c08cb-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c08cb-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="c08cb-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c08cb-126">Text</span><span class="sxs-lookup"><span data-stu-id="c08cb-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c08cb-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="c08cb-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c08cb-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="c08cb-128">Attributes</span></span>

|<span data-ttu-id="c08cb-129">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c08cb-129">**Attribute**</span></span>|<span data-ttu-id="c08cb-130">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c08cb-130">**Type**</span></span>|<span data-ttu-id="c08cb-131">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="c08cb-131">**Required**</span></span>|<span data-ttu-id="c08cb-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c08cb-132">**Description**</span></span>|<span data-ttu-id="c08cb-133">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="c08cb-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c08cb-134">Del</span><span class="sxs-lookup"><span data-stu-id="c08cb-134">Del</span></span>  <br/> |<span data-ttu-id="c08cb-135">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="c08cb-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c08cb-136">opcional</span><span class="sxs-lookup"><span data-stu-id="c08cb-136">optional</span></span>  <br/> ||<span data-ttu-id="c08cb-137">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="c08cb-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c08cb-138">ID</span><span class="sxs-lookup"><span data-stu-id="c08cb-138">ID</span></span>  <br/> |<span data-ttu-id="c08cb-139">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c08cb-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c08cb-140">necesario</span><span class="sxs-lookup"><span data-stu-id="c08cb-140">required</span></span>  <br/> ||<span data-ttu-id="c08cb-141">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c08cb-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c08cb-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="c08cb-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="c08cb-143">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="c08cb-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c08cb-144">opcional</span><span class="sxs-lookup"><span data-stu-id="c08cb-144">optional</span></span>  <br/> ||<span data-ttu-id="c08cb-145">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="c08cb-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c08cb-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="c08cb-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="c08cb-147">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="c08cb-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c08cb-148">opcional</span><span class="sxs-lookup"><span data-stu-id="c08cb-148">optional</span></span>  <br/> ||<span data-ttu-id="c08cb-149">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="c08cb-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c08cb-150">Master</span><span class="sxs-lookup"><span data-stu-id="c08cb-150">Master</span></span>  <br/> |<span data-ttu-id="c08cb-151">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c08cb-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c08cb-152">opcional</span><span class="sxs-lookup"><span data-stu-id="c08cb-152">optional</span></span>  <br/> ||<span data-ttu-id="c08cb-153">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c08cb-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c08cb-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="c08cb-154">MasterShape</span></span>  <br/> |<span data-ttu-id="c08cb-155">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c08cb-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c08cb-156">opcional</span><span class="sxs-lookup"><span data-stu-id="c08cb-156">optional</span></span>  <br/> ||<span data-ttu-id="c08cb-157">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c08cb-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c08cb-158">Nombre</span><span class="sxs-lookup"><span data-stu-id="c08cb-158">Name</span></span>  <br/> |<span data-ttu-id="c08cb-159">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c08cb-159">xsd:string</span></span>  <br/> |<span data-ttu-id="c08cb-160">opcional</span><span class="sxs-lookup"><span data-stu-id="c08cb-160">optional</span></span>  <br/> ||<span data-ttu-id="c08cb-161">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c08cb-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c08cb-162">NameU</span><span class="sxs-lookup"><span data-stu-id="c08cb-162">NameU</span></span>  <br/> |<span data-ttu-id="c08cb-163">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c08cb-163">xsd:string</span></span>  <br/> |<span data-ttu-id="c08cb-164">opcional</span><span class="sxs-lookup"><span data-stu-id="c08cb-164">optional</span></span>  <br/> ||<span data-ttu-id="c08cb-165">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c08cb-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c08cb-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="c08cb-166">OriginalID</span></span>  <br/> |<span data-ttu-id="c08cb-167">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c08cb-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c08cb-168">opcional</span><span class="sxs-lookup"><span data-stu-id="c08cb-168">optional</span></span>  <br/> ||<span data-ttu-id="c08cb-169">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c08cb-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c08cb-170">Tipo</span><span class="sxs-lookup"><span data-stu-id="c08cb-170">Type</span></span>  <br/> |<span data-ttu-id="c08cb-171">xsd: token</span><span class="sxs-lookup"><span data-stu-id="c08cb-171">xsd:token</span></span>  <br/> |<span data-ttu-id="c08cb-172">opcional</span><span class="sxs-lookup"><span data-stu-id="c08cb-172">optional</span></span>  <br/> ||<span data-ttu-id="c08cb-173">Valores del tipo xsd: token.</span><span class="sxs-lookup"><span data-stu-id="c08cb-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="c08cb-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="c08cb-174">UniqueID</span></span>  <br/> |<span data-ttu-id="c08cb-175">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c08cb-175">xsd:string</span></span>  <br/> |<span data-ttu-id="c08cb-176">opcional</span><span class="sxs-lookup"><span data-stu-id="c08cb-176">optional</span></span>  <br/> ||<span data-ttu-id="c08cb-177">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c08cb-177">Values of the xsd:string type.</span></span>  <br/> |
   

