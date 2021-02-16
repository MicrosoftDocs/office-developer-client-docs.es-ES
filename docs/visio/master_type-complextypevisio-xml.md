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
# <a name="master_type-complextype-visio-xml"></a><span data-ttu-id="957c7-102">Master_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="957c7-102">Master_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="957c7-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="957c7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="957c7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="957c7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="957c7-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="957c7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="957c7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="957c7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="957c7-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="957c7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="957c7-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="957c7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="957c7-109">Definición</span><span class="sxs-lookup"><span data-stu-id="957c7-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="957c7-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="957c7-110">Elements and attributes</span></span>

<span data-ttu-id="957c7-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="957c7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="957c7-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="957c7-112">Child elements</span></span>

|<span data-ttu-id="957c7-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="957c7-113">**Element**</span></span>|<span data-ttu-id="957c7-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="957c7-114">**Type**</span></span>|<span data-ttu-id="957c7-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="957c7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="957c7-116">Icon</span><span class="sxs-lookup"><span data-stu-id="957c7-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="957c7-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="957c7-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="957c7-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="957c7-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="957c7-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="957c7-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="957c7-120">Rel</span><span class="sxs-lookup"><span data-stu-id="957c7-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="957c7-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="957c7-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="957c7-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="957c7-122">Attributes</span></span>

|<span data-ttu-id="957c7-123">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="957c7-123">**Attribute**</span></span>|<span data-ttu-id="957c7-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="957c7-124">**Type**</span></span>|<span data-ttu-id="957c7-125">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="957c7-125">**Required**</span></span>|<span data-ttu-id="957c7-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="957c7-126">**Description**</span></span>|<span data-ttu-id="957c7-127">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="957c7-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="957c7-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="957c7-128">AlignName</span></span>  <br/> |<span data-ttu-id="957c7-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="957c7-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="957c7-130">opcional</span><span class="sxs-lookup"><span data-stu-id="957c7-130">optional</span></span>  <br/> ||<span data-ttu-id="957c7-131">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="957c7-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="957c7-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="957c7-132">BaseID</span></span>  <br/> |<span data-ttu-id="957c7-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="957c7-133">xsd:string</span></span>  <br/> |<span data-ttu-id="957c7-134">opcional</span><span class="sxs-lookup"><span data-stu-id="957c7-134">optional</span></span>  <br/> ||<span data-ttu-id="957c7-135">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="957c7-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="957c7-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="957c7-136">Hidden</span></span>  <br/> |<span data-ttu-id="957c7-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="957c7-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="957c7-138">opcional</span><span class="sxs-lookup"><span data-stu-id="957c7-138">optional</span></span>  <br/> ||<span data-ttu-id="957c7-139">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="957c7-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="957c7-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="957c7-140">IconSize</span></span>  <br/> |<span data-ttu-id="957c7-141">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="957c7-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="957c7-142">opcional</span><span class="sxs-lookup"><span data-stu-id="957c7-142">optional</span></span>  <br/> ||<span data-ttu-id="957c7-143">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="957c7-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="957c7-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="957c7-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="957c7-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="957c7-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="957c7-146">opcional</span><span class="sxs-lookup"><span data-stu-id="957c7-146">optional</span></span>  <br/> ||<span data-ttu-id="957c7-147">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="957c7-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="957c7-148">ID</span><span class="sxs-lookup"><span data-stu-id="957c7-148">ID</span></span>  <br/> |<span data-ttu-id="957c7-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="957c7-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="957c7-150">necesario</span><span class="sxs-lookup"><span data-stu-id="957c7-150">required</span></span>  <br/> ||<span data-ttu-id="957c7-151">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="957c7-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="957c7-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="957c7-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="957c7-153">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="957c7-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="957c7-154">opcional</span><span class="sxs-lookup"><span data-stu-id="957c7-154">optional</span></span>  <br/> ||<span data-ttu-id="957c7-155">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="957c7-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="957c7-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="957c7-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="957c7-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="957c7-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="957c7-158">opcional</span><span class="sxs-lookup"><span data-stu-id="957c7-158">optional</span></span>  <br/> ||<span data-ttu-id="957c7-159">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="957c7-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="957c7-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="957c7-160">MasterType</span></span>  <br/> |<span data-ttu-id="957c7-161">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="957c7-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="957c7-162">opcional</span><span class="sxs-lookup"><span data-stu-id="957c7-162">optional</span></span>  <br/> ||<span data-ttu-id="957c7-163">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="957c7-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="957c7-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="957c7-164">MatchByName</span></span>  <br/> |<span data-ttu-id="957c7-165">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="957c7-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="957c7-166">opcional</span><span class="sxs-lookup"><span data-stu-id="957c7-166">optional</span></span>  <br/> ||<span data-ttu-id="957c7-167">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="957c7-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="957c7-168">Nombre</span><span class="sxs-lookup"><span data-stu-id="957c7-168">Name</span></span>  <br/> |<span data-ttu-id="957c7-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="957c7-169">xsd:string</span></span>  <br/> |<span data-ttu-id="957c7-170">opcional</span><span class="sxs-lookup"><span data-stu-id="957c7-170">optional</span></span>  <br/> ||<span data-ttu-id="957c7-171">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="957c7-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="957c7-172">NameU</span><span class="sxs-lookup"><span data-stu-id="957c7-172">NameU</span></span>  <br/> |<span data-ttu-id="957c7-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="957c7-173">xsd:string</span></span>  <br/> |<span data-ttu-id="957c7-174">opcional</span><span class="sxs-lookup"><span data-stu-id="957c7-174">optional</span></span>  <br/> ||<span data-ttu-id="957c7-175">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="957c7-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="957c7-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="957c7-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="957c7-177">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="957c7-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="957c7-178">opcional</span><span class="sxs-lookup"><span data-stu-id="957c7-178">optional</span></span>  <br/> ||<span data-ttu-id="957c7-179">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="957c7-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="957c7-180">Prompt</span><span class="sxs-lookup"><span data-stu-id="957c7-180">Prompt</span></span>  <br/> |<span data-ttu-id="957c7-181">xsd:string</span><span class="sxs-lookup"><span data-stu-id="957c7-181">xsd:string</span></span>  <br/> |<span data-ttu-id="957c7-182">opcional</span><span class="sxs-lookup"><span data-stu-id="957c7-182">optional</span></span>  <br/> ||<span data-ttu-id="957c7-183">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="957c7-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="957c7-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="957c7-184">UniqueID</span></span>  <br/> |<span data-ttu-id="957c7-185">xsd:string</span><span class="sxs-lookup"><span data-stu-id="957c7-185">xsd:string</span></span>  <br/> |<span data-ttu-id="957c7-186">opcional</span><span class="sxs-lookup"><span data-stu-id="957c7-186">optional</span></span>  <br/> ||<span data-ttu-id="957c7-187">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="957c7-187">Values of the xsd:string type.</span></span>  <br/> |
   

