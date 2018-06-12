---
title: Master_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: b4dde4d00552525a5ec17116f96151f39c6d0957
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822574"
---
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="d7094-102">Master_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="d7094-102">Master_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d7094-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="d7094-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7094-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d7094-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d7094-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d7094-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d7094-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d7094-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d7094-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="d7094-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d7094-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d7094-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d7094-109">Definición</span><span class="sxs-lookup"><span data-stu-id="d7094-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d7094-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="d7094-110">Elements and attributes</span></span>

<span data-ttu-id="d7094-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="d7094-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d7094-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d7094-112">Child elements</span></span>

|<span data-ttu-id="d7094-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d7094-113">**Element**</span></span>|<span data-ttu-id="d7094-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d7094-114">**Type**</span></span>|<span data-ttu-id="d7094-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d7094-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d7094-116">Icon</span><span class="sxs-lookup"><span data-stu-id="d7094-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d7094-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="d7094-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d7094-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="d7094-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d7094-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="d7094-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d7094-120">Rel</span><span class="sxs-lookup"><span data-stu-id="d7094-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d7094-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="d7094-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d7094-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="d7094-122">Attributes</span></span>

|<span data-ttu-id="d7094-123">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="d7094-123">**Attribute**</span></span>|<span data-ttu-id="d7094-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d7094-124">**Type**</span></span>|<span data-ttu-id="d7094-125">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="d7094-125">**Required**</span></span>|<span data-ttu-id="d7094-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d7094-126">**Description**</span></span>|<span data-ttu-id="d7094-127">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="d7094-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d7094-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="d7094-128">AlignName</span></span>  <br/> |<span data-ttu-id="d7094-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d7094-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d7094-130">opcional</span><span class="sxs-lookup"><span data-stu-id="d7094-130">optional</span></span>  <br/> ||<span data-ttu-id="d7094-131">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d7094-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d7094-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="d7094-132">BaseID</span></span>  <br/> |<span data-ttu-id="d7094-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="d7094-133">xsd:string</span></span>  <br/> |<span data-ttu-id="d7094-134">opcional</span><span class="sxs-lookup"><span data-stu-id="d7094-134">optional</span></span>  <br/> ||<span data-ttu-id="d7094-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="d7094-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d7094-136">Oculta.</span><span class="sxs-lookup"><span data-stu-id="d7094-136">Hidden</span></span>  <br/> |<span data-ttu-id="d7094-137">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="d7094-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d7094-138">opcional</span><span class="sxs-lookup"><span data-stu-id="d7094-138">optional</span></span>  <br/> ||<span data-ttu-id="d7094-139">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="d7094-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d7094-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="d7094-140">IconSize</span></span>  <br/> |<span data-ttu-id="d7094-141">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d7094-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d7094-142">opcional</span><span class="sxs-lookup"><span data-stu-id="d7094-142">optional</span></span>  <br/> ||<span data-ttu-id="d7094-143">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d7094-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d7094-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="d7094-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="d7094-145">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="d7094-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d7094-146">opcional</span><span class="sxs-lookup"><span data-stu-id="d7094-146">optional</span></span>  <br/> ||<span data-ttu-id="d7094-147">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="d7094-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d7094-148">id.</span><span class="sxs-lookup"><span data-stu-id="d7094-148">ID</span></span>  <br/> |<span data-ttu-id="d7094-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d7094-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d7094-150">necesario</span><span class="sxs-lookup"><span data-stu-id="d7094-150">required</span></span>  <br/> ||<span data-ttu-id="d7094-151">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d7094-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d7094-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="d7094-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="d7094-153">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="d7094-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d7094-154">opcional</span><span class="sxs-lookup"><span data-stu-id="d7094-154">optional</span></span>  <br/> ||<span data-ttu-id="d7094-155">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="d7094-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d7094-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="d7094-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="d7094-157">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="d7094-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d7094-158">opcional</span><span class="sxs-lookup"><span data-stu-id="d7094-158">optional</span></span>  <br/> ||<span data-ttu-id="d7094-159">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="d7094-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d7094-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="d7094-160">MasterType</span></span>  <br/> |<span data-ttu-id="d7094-161">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d7094-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d7094-162">opcional</span><span class="sxs-lookup"><span data-stu-id="d7094-162">optional</span></span>  <br/> ||<span data-ttu-id="d7094-163">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d7094-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d7094-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="d7094-164">MatchByName</span></span>  <br/> |<span data-ttu-id="d7094-165">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="d7094-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d7094-166">opcional</span><span class="sxs-lookup"><span data-stu-id="d7094-166">optional</span></span>  <br/> ||<span data-ttu-id="d7094-167">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="d7094-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d7094-168">Nombre</span><span class="sxs-lookup"><span data-stu-id="d7094-168">Name</span></span>  <br/> |<span data-ttu-id="d7094-169">xsd: String</span><span class="sxs-lookup"><span data-stu-id="d7094-169">xsd:string</span></span>  <br/> |<span data-ttu-id="d7094-170">opcional</span><span class="sxs-lookup"><span data-stu-id="d7094-170">optional</span></span>  <br/> ||<span data-ttu-id="d7094-171">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="d7094-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d7094-172">NameU</span><span class="sxs-lookup"><span data-stu-id="d7094-172">NameU</span></span>  <br/> |<span data-ttu-id="d7094-173">xsd: String</span><span class="sxs-lookup"><span data-stu-id="d7094-173">xsd:string</span></span>  <br/> |<span data-ttu-id="d7094-174">opcional</span><span class="sxs-lookup"><span data-stu-id="d7094-174">optional</span></span>  <br/> ||<span data-ttu-id="d7094-175">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="d7094-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d7094-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="d7094-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="d7094-177">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d7094-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d7094-178">opcional</span><span class="sxs-lookup"><span data-stu-id="d7094-178">optional</span></span>  <br/> ||<span data-ttu-id="d7094-179">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d7094-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d7094-180">Prompt</span><span class="sxs-lookup"><span data-stu-id="d7094-180">Prompt</span></span>  <br/> |<span data-ttu-id="d7094-181">xsd: String</span><span class="sxs-lookup"><span data-stu-id="d7094-181">xsd:string</span></span>  <br/> |<span data-ttu-id="d7094-182">opcional</span><span class="sxs-lookup"><span data-stu-id="d7094-182">optional</span></span>  <br/> ||<span data-ttu-id="d7094-183">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="d7094-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d7094-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="d7094-184">UniqueID</span></span>  <br/> |<span data-ttu-id="d7094-185">xsd: String</span><span class="sxs-lookup"><span data-stu-id="d7094-185">xsd:string</span></span>  <br/> |<span data-ttu-id="d7094-186">opcional</span><span class="sxs-lookup"><span data-stu-id="d7094-186">optional</span></span>  <br/> ||<span data-ttu-id="d7094-187">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="d7094-187">Values of the xsd:string type.</span></span>  <br/> |
   

