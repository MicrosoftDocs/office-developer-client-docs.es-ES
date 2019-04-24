---
title: Master_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 186099d495849706f68113abb269de4a1f5a2ce7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341807"
---
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="f3b6c-102">Master_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="f3b6c-102">Master_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f3b6c-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="f3b6c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3b6c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f3b6c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f3b6c-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f3b6c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f3b6c-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="f3b6c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f3b6c-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="f3b6c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f3b6c-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f3b6c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f3b6c-109">Definición</span><span class="sxs-lookup"><span data-stu-id="f3b6c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f3b6c-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f3b6c-110">Elements and attributes</span></span>

<span data-ttu-id="f3b6c-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="f3b6c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f3b6c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f3b6c-112">Child elements</span></span>

|<span data-ttu-id="f3b6c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f3b6c-113">**Element**</span></span>|<span data-ttu-id="f3b6c-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f3b6c-114">**Type**</span></span>|<span data-ttu-id="f3b6c-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f3b6c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f3b6c-116">Icon</span><span class="sxs-lookup"><span data-stu-id="f3b6c-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f3b6c-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="f3b6c-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f3b6c-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="f3b6c-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f3b6c-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="f3b6c-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f3b6c-120">REL</span><span class="sxs-lookup"><span data-stu-id="f3b6c-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f3b6c-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="f3b6c-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f3b6c-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="f3b6c-122">Attributes</span></span>

|<span data-ttu-id="f3b6c-123">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f3b6c-123">**Attribute**</span></span>|<span data-ttu-id="f3b6c-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f3b6c-124">**Type**</span></span>|<span data-ttu-id="f3b6c-125">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="f3b6c-125">**Required**</span></span>|<span data-ttu-id="f3b6c-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f3b6c-126">**Description**</span></span>|<span data-ttu-id="f3b6c-127">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="f3b6c-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f3b6c-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="f3b6c-128">AlignName</span></span>  <br/> |<span data-ttu-id="f3b6c-129">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f3b6c-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f3b6c-130">opcional</span><span class="sxs-lookup"><span data-stu-id="f3b6c-130">optional</span></span>  <br/> ||<span data-ttu-id="f3b6c-131">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f3b6c-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f3b6c-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="f3b6c-132">BaseID</span></span>  <br/> |<span data-ttu-id="f3b6c-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f3b6c-133">xsd:string</span></span>  <br/> |<span data-ttu-id="f3b6c-134">opcional</span><span class="sxs-lookup"><span data-stu-id="f3b6c-134">optional</span></span>  <br/> ||<span data-ttu-id="f3b6c-135">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f3b6c-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f3b6c-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="f3b6c-136">Hidden</span></span>  <br/> |<span data-ttu-id="f3b6c-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="f3b6c-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f3b6c-138">opcional</span><span class="sxs-lookup"><span data-stu-id="f3b6c-138">optional</span></span>  <br/> ||<span data-ttu-id="f3b6c-139">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f3b6c-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f3b6c-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="f3b6c-140">IconSize</span></span>  <br/> |<span data-ttu-id="f3b6c-141">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f3b6c-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f3b6c-142">opcional</span><span class="sxs-lookup"><span data-stu-id="f3b6c-142">optional</span></span>  <br/> ||<span data-ttu-id="f3b6c-143">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f3b6c-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f3b6c-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="f3b6c-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="f3b6c-145">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="f3b6c-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f3b6c-146">opcional</span><span class="sxs-lookup"><span data-stu-id="f3b6c-146">optional</span></span>  <br/> ||<span data-ttu-id="f3b6c-147">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f3b6c-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f3b6c-148">ID</span><span class="sxs-lookup"><span data-stu-id="f3b6c-148">ID</span></span>  <br/> |<span data-ttu-id="f3b6c-149">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f3b6c-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f3b6c-150">necesario</span><span class="sxs-lookup"><span data-stu-id="f3b6c-150">required</span></span>  <br/> ||<span data-ttu-id="f3b6c-151">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f3b6c-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f3b6c-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="f3b6c-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="f3b6c-153">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="f3b6c-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f3b6c-154">opcional</span><span class="sxs-lookup"><span data-stu-id="f3b6c-154">optional</span></span>  <br/> ||<span data-ttu-id="f3b6c-155">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f3b6c-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f3b6c-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="f3b6c-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="f3b6c-157">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="f3b6c-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f3b6c-158">opcional</span><span class="sxs-lookup"><span data-stu-id="f3b6c-158">optional</span></span>  <br/> ||<span data-ttu-id="f3b6c-159">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f3b6c-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f3b6c-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="f3b6c-160">MasterType</span></span>  <br/> |<span data-ttu-id="f3b6c-161">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f3b6c-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f3b6c-162">opcional</span><span class="sxs-lookup"><span data-stu-id="f3b6c-162">optional</span></span>  <br/> ||<span data-ttu-id="f3b6c-163">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f3b6c-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f3b6c-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="f3b6c-164">MatchByName</span></span>  <br/> |<span data-ttu-id="f3b6c-165">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="f3b6c-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f3b6c-166">opcional</span><span class="sxs-lookup"><span data-stu-id="f3b6c-166">optional</span></span>  <br/> ||<span data-ttu-id="f3b6c-167">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f3b6c-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f3b6c-168">Nombre</span><span class="sxs-lookup"><span data-stu-id="f3b6c-168">Name</span></span>  <br/> |<span data-ttu-id="f3b6c-169">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f3b6c-169">xsd:string</span></span>  <br/> |<span data-ttu-id="f3b6c-170">opcional</span><span class="sxs-lookup"><span data-stu-id="f3b6c-170">optional</span></span>  <br/> ||<span data-ttu-id="f3b6c-171">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f3b6c-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f3b6c-172">NameU</span><span class="sxs-lookup"><span data-stu-id="f3b6c-172">NameU</span></span>  <br/> |<span data-ttu-id="f3b6c-173">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f3b6c-173">xsd:string</span></span>  <br/> |<span data-ttu-id="f3b6c-174">opcional</span><span class="sxs-lookup"><span data-stu-id="f3b6c-174">optional</span></span>  <br/> ||<span data-ttu-id="f3b6c-175">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f3b6c-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f3b6c-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="f3b6c-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="f3b6c-177">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f3b6c-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f3b6c-178">opcional</span><span class="sxs-lookup"><span data-stu-id="f3b6c-178">optional</span></span>  <br/> ||<span data-ttu-id="f3b6c-179">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f3b6c-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f3b6c-180">Prompt</span><span class="sxs-lookup"><span data-stu-id="f3b6c-180">Prompt</span></span>  <br/> |<span data-ttu-id="f3b6c-181">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f3b6c-181">xsd:string</span></span>  <br/> |<span data-ttu-id="f3b6c-182">opcional</span><span class="sxs-lookup"><span data-stu-id="f3b6c-182">optional</span></span>  <br/> ||<span data-ttu-id="f3b6c-183">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f3b6c-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f3b6c-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="f3b6c-184">UniqueID</span></span>  <br/> |<span data-ttu-id="f3b6c-185">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f3b6c-185">xsd:string</span></span>  <br/> |<span data-ttu-id="f3b6c-186">opcional</span><span class="sxs-lookup"><span data-stu-id="f3b6c-186">optional</span></span>  <br/> ||<span data-ttu-id="f3b6c-187">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f3b6c-187">Values of the xsd:string type.</span></span>  <br/> |
   

