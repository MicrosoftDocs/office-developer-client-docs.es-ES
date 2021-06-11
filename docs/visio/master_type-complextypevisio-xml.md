---
title: Master_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 22b619149fc5393f085ca6e245c65ed6058538ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538070"
---
# <a name="master_type-complextype-visio-xml"></a><span data-ttu-id="2b4f4-102">Master_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="2b4f4-102">Master_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="2b4f4-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="2b4f4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b4f4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2b4f4-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2b4f4-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2b4f4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2b4f4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2b4f4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2b4f4-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="2b4f4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2b4f4-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="2b4f4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2b4f4-109">Definición</span><span class="sxs-lookup"><span data-stu-id="2b4f4-109">Definition</span></span>

```XML
          <xs:complexType name="Master_Type">
          
          <xs:all>
    <xs:element name="PageSheet"  type="PageSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Icon"  type="Icon_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="BaseID"
  type="xsd:string"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="MatchByName"
  type="xsd:boolean"
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
    <xs:attribute name="IconSize"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="PatternFlags"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Prompt"
  type="xsd:string"
    />
    <xs:attribute name="Hidden"
  type="xsd:boolean"
    />
    <xs:attribute name="IconUpdate"
  type="xsd:boolean"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2b4f4-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="2b4f4-110">Elements and attributes</span></span>

<span data-ttu-id="2b4f4-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="2b4f4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2b4f4-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2b4f4-112">Child elements</span></span>

|<span data-ttu-id="2b4f4-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2b4f4-113">**Element**</span></span>|<span data-ttu-id="2b4f4-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2b4f4-114">**Type**</span></span>|<span data-ttu-id="2b4f4-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b4f4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2b4f4-116">Icon</span><span class="sxs-lookup"><span data-stu-id="2b4f4-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2b4f4-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="2b4f4-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2b4f4-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="2b4f4-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2b4f4-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="2b4f4-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2b4f4-120">Rel</span><span class="sxs-lookup"><span data-stu-id="2b4f4-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2b4f4-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="2b4f4-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2b4f4-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="2b4f4-122">Attributes</span></span>

|<span data-ttu-id="2b4f4-123">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2b4f4-123">**Attribute**</span></span>|<span data-ttu-id="2b4f4-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2b4f4-124">**Type**</span></span>|<span data-ttu-id="2b4f4-125">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="2b4f4-125">**Required**</span></span>|<span data-ttu-id="2b4f4-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b4f4-126">**Description**</span></span>|<span data-ttu-id="2b4f4-127">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="2b4f4-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2b4f4-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="2b4f4-128">AlignName</span></span>  <br/> |<span data-ttu-id="2b4f4-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="2b4f4-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2b4f4-130">opcional</span><span class="sxs-lookup"><span data-stu-id="2b4f4-130">optional</span></span>  <br/> ||<span data-ttu-id="2b4f4-131">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="2b4f4-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="2b4f4-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="2b4f4-132">BaseID</span></span>  <br/> |<span data-ttu-id="2b4f4-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2b4f4-133">xsd:string</span></span>  <br/> |<span data-ttu-id="2b4f4-134">opcional</span><span class="sxs-lookup"><span data-stu-id="2b4f4-134">optional</span></span>  <br/> ||<span data-ttu-id="2b4f4-135">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2b4f4-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2b4f4-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="2b4f4-136">Hidden</span></span>  <br/> |<span data-ttu-id="2b4f4-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2b4f4-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2b4f4-138">opcional</span><span class="sxs-lookup"><span data-stu-id="2b4f4-138">optional</span></span>  <br/> ||<span data-ttu-id="2b4f4-139">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2b4f4-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2b4f4-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="2b4f4-140">IconSize</span></span>  <br/> |<span data-ttu-id="2b4f4-141">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="2b4f4-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2b4f4-142">opcional</span><span class="sxs-lookup"><span data-stu-id="2b4f4-142">optional</span></span>  <br/> ||<span data-ttu-id="2b4f4-143">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="2b4f4-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="2b4f4-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="2b4f4-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="2b4f4-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2b4f4-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2b4f4-146">opcional</span><span class="sxs-lookup"><span data-stu-id="2b4f4-146">optional</span></span>  <br/> ||<span data-ttu-id="2b4f4-147">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2b4f4-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2b4f4-148">ID</span><span class="sxs-lookup"><span data-stu-id="2b4f4-148">ID</span></span>  <br/> |<span data-ttu-id="2b4f4-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2b4f4-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2b4f4-150">necesario</span><span class="sxs-lookup"><span data-stu-id="2b4f4-150">required</span></span>  <br/> ||<span data-ttu-id="2b4f4-151">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2b4f4-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2b4f4-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="2b4f4-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="2b4f4-153">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2b4f4-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2b4f4-154">opcional</span><span class="sxs-lookup"><span data-stu-id="2b4f4-154">optional</span></span>  <br/> ||<span data-ttu-id="2b4f4-155">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2b4f4-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2b4f4-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="2b4f4-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="2b4f4-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2b4f4-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2b4f4-158">opcional</span><span class="sxs-lookup"><span data-stu-id="2b4f4-158">optional</span></span>  <br/> ||<span data-ttu-id="2b4f4-159">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2b4f4-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2b4f4-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="2b4f4-160">MasterType</span></span>  <br/> |<span data-ttu-id="2b4f4-161">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="2b4f4-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2b4f4-162">opcional</span><span class="sxs-lookup"><span data-stu-id="2b4f4-162">optional</span></span>  <br/> ||<span data-ttu-id="2b4f4-163">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="2b4f4-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="2b4f4-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="2b4f4-164">MatchByName</span></span>  <br/> |<span data-ttu-id="2b4f4-165">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2b4f4-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2b4f4-166">opcional</span><span class="sxs-lookup"><span data-stu-id="2b4f4-166">optional</span></span>  <br/> ||<span data-ttu-id="2b4f4-167">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2b4f4-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2b4f4-168">Nombre</span><span class="sxs-lookup"><span data-stu-id="2b4f4-168">Name</span></span>  <br/> |<span data-ttu-id="2b4f4-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2b4f4-169">xsd:string</span></span>  <br/> |<span data-ttu-id="2b4f4-170">opcional</span><span class="sxs-lookup"><span data-stu-id="2b4f4-170">optional</span></span>  <br/> ||<span data-ttu-id="2b4f4-171">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2b4f4-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2b4f4-172">NameU</span><span class="sxs-lookup"><span data-stu-id="2b4f4-172">NameU</span></span>  <br/> |<span data-ttu-id="2b4f4-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2b4f4-173">xsd:string</span></span>  <br/> |<span data-ttu-id="2b4f4-174">opcional</span><span class="sxs-lookup"><span data-stu-id="2b4f4-174">optional</span></span>  <br/> ||<span data-ttu-id="2b4f4-175">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2b4f4-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2b4f4-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="2b4f4-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="2b4f4-177">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="2b4f4-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2b4f4-178">opcional</span><span class="sxs-lookup"><span data-stu-id="2b4f4-178">optional</span></span>  <br/> ||<span data-ttu-id="2b4f4-179">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="2b4f4-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="2b4f4-180">Prompt</span><span class="sxs-lookup"><span data-stu-id="2b4f4-180">Prompt</span></span>  <br/> |<span data-ttu-id="2b4f4-181">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2b4f4-181">xsd:string</span></span>  <br/> |<span data-ttu-id="2b4f4-182">opcional</span><span class="sxs-lookup"><span data-stu-id="2b4f4-182">optional</span></span>  <br/> ||<span data-ttu-id="2b4f4-183">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2b4f4-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2b4f4-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="2b4f4-184">UniqueID</span></span>  <br/> |<span data-ttu-id="2b4f4-185">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2b4f4-185">xsd:string</span></span>  <br/> |<span data-ttu-id="2b4f4-186">opcional</span><span class="sxs-lookup"><span data-stu-id="2b4f4-186">optional</span></span>  <br/> ||<span data-ttu-id="2b4f4-187">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2b4f4-187">Values of the xsd:string type.</span></span>  <br/> |
   

