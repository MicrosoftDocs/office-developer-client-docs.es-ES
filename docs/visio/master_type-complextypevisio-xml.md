---
title: ComplexType Master_Type (XML de Visio)
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
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="92372-102">ComplexType Master_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="92372-102">Master_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="92372-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="92372-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92372-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="92372-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="92372-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="92372-105">**Schema file**</span></span> <br/> |<span data-ttu-id="92372-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="92372-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="92372-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="92372-107">**Extension base**</span></span> <br/> |<span data-ttu-id="92372-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="92372-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="92372-109">Definición</span><span class="sxs-lookup"><span data-stu-id="92372-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="92372-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="92372-110">Elements and attributes</span></span>

<span data-ttu-id="92372-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="92372-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="92372-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92372-112">Child elements</span></span>

|<span data-ttu-id="92372-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="92372-113">**Element**</span></span>|<span data-ttu-id="92372-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="92372-114">**Type**</span></span>|<span data-ttu-id="92372-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="92372-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="92372-116">Icon</span><span class="sxs-lookup"><span data-stu-id="92372-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="92372-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="92372-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="92372-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="92372-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="92372-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="92372-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="92372-120">REL</span><span class="sxs-lookup"><span data-stu-id="92372-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="92372-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="92372-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="92372-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="92372-122">Attributes</span></span>

|<span data-ttu-id="92372-123">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="92372-123">**Attribute**</span></span>|<span data-ttu-id="92372-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="92372-124">**Type**</span></span>|<span data-ttu-id="92372-125">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="92372-125">**Required**</span></span>|<span data-ttu-id="92372-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="92372-126">**Description**</span></span>|<span data-ttu-id="92372-127">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="92372-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="92372-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="92372-128">AlignName</span></span>  <br/> |<span data-ttu-id="92372-129">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="92372-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="92372-130">opcional</span><span class="sxs-lookup"><span data-stu-id="92372-130">optional</span></span>  <br/> ||<span data-ttu-id="92372-131">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="92372-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="92372-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="92372-132">BaseID</span></span>  <br/> |<span data-ttu-id="92372-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="92372-133">xsd:string</span></span>  <br/> |<span data-ttu-id="92372-134">opcional</span><span class="sxs-lookup"><span data-stu-id="92372-134">optional</span></span>  <br/> ||<span data-ttu-id="92372-135">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="92372-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="92372-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="92372-136">Hidden</span></span>  <br/> |<span data-ttu-id="92372-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="92372-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="92372-138">opcional</span><span class="sxs-lookup"><span data-stu-id="92372-138">optional</span></span>  <br/> ||<span data-ttu-id="92372-139">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="92372-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="92372-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="92372-140">IconSize</span></span>  <br/> |<span data-ttu-id="92372-141">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="92372-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="92372-142">opcional</span><span class="sxs-lookup"><span data-stu-id="92372-142">optional</span></span>  <br/> ||<span data-ttu-id="92372-143">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="92372-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="92372-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="92372-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="92372-145">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="92372-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="92372-146">opcional</span><span class="sxs-lookup"><span data-stu-id="92372-146">optional</span></span>  <br/> ||<span data-ttu-id="92372-147">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="92372-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="92372-148">ID</span><span class="sxs-lookup"><span data-stu-id="92372-148">ID</span></span>  <br/> |<span data-ttu-id="92372-149">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="92372-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="92372-150">necesario</span><span class="sxs-lookup"><span data-stu-id="92372-150">required</span></span>  <br/> ||<span data-ttu-id="92372-151">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="92372-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="92372-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="92372-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="92372-153">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="92372-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="92372-154">opcional</span><span class="sxs-lookup"><span data-stu-id="92372-154">optional</span></span>  <br/> ||<span data-ttu-id="92372-155">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="92372-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="92372-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="92372-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="92372-157">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="92372-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="92372-158">opcional</span><span class="sxs-lookup"><span data-stu-id="92372-158">optional</span></span>  <br/> ||<span data-ttu-id="92372-159">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="92372-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="92372-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="92372-160">MasterType</span></span>  <br/> |<span data-ttu-id="92372-161">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="92372-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="92372-162">opcional</span><span class="sxs-lookup"><span data-stu-id="92372-162">optional</span></span>  <br/> ||<span data-ttu-id="92372-163">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="92372-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="92372-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="92372-164">MatchByName</span></span>  <br/> |<span data-ttu-id="92372-165">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="92372-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="92372-166">opcional</span><span class="sxs-lookup"><span data-stu-id="92372-166">optional</span></span>  <br/> ||<span data-ttu-id="92372-167">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="92372-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="92372-168">Nombre</span><span class="sxs-lookup"><span data-stu-id="92372-168">Name</span></span>  <br/> |<span data-ttu-id="92372-169">xsd: String</span><span class="sxs-lookup"><span data-stu-id="92372-169">xsd:string</span></span>  <br/> |<span data-ttu-id="92372-170">opcional</span><span class="sxs-lookup"><span data-stu-id="92372-170">optional</span></span>  <br/> ||<span data-ttu-id="92372-171">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="92372-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="92372-172">NameU</span><span class="sxs-lookup"><span data-stu-id="92372-172">NameU</span></span>  <br/> |<span data-ttu-id="92372-173">xsd: String</span><span class="sxs-lookup"><span data-stu-id="92372-173">xsd:string</span></span>  <br/> |<span data-ttu-id="92372-174">opcional</span><span class="sxs-lookup"><span data-stu-id="92372-174">optional</span></span>  <br/> ||<span data-ttu-id="92372-175">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="92372-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="92372-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="92372-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="92372-177">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="92372-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="92372-178">opcional</span><span class="sxs-lookup"><span data-stu-id="92372-178">optional</span></span>  <br/> ||<span data-ttu-id="92372-179">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="92372-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="92372-180">Prompt</span><span class="sxs-lookup"><span data-stu-id="92372-180">Prompt</span></span>  <br/> |<span data-ttu-id="92372-181">xsd: String</span><span class="sxs-lookup"><span data-stu-id="92372-181">xsd:string</span></span>  <br/> |<span data-ttu-id="92372-182">opcional</span><span class="sxs-lookup"><span data-stu-id="92372-182">optional</span></span>  <br/> ||<span data-ttu-id="92372-183">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="92372-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="92372-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="92372-184">UniqueID</span></span>  <br/> |<span data-ttu-id="92372-185">xsd: String</span><span class="sxs-lookup"><span data-stu-id="92372-185">xsd:string</span></span>  <br/> |<span data-ttu-id="92372-186">opcional</span><span class="sxs-lookup"><span data-stu-id="92372-186">optional</span></span>  <br/> ||<span data-ttu-id="92372-187">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="92372-187">Values of the xsd:string type.</span></span>  <br/> |
   

