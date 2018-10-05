---
title: MasterShortcut_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: 23d5de92be151b9ab6819296456746087573e7c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396487"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="bc9e0-102">MasterShortcut_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="bc9e0-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bc9e0-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="bc9e0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bc9e0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bc9e0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bc9e0-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="bc9e0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bc9e0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bc9e0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bc9e0-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="bc9e0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bc9e0-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="bc9e0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bc9e0-109">Definición</span><span class="sxs-lookup"><span data-stu-id="bc9e0-109">Definition</span></span>

```XML
          <xs:complexType name="MasterShortcut_Type">
          
          <xs:all>
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
    <xs:attribute name="ShortcutURL"
  type="xsd:string"
    />
    <xs:attribute name="ShortcutHelp"
  type="xsd:string"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bc9e0-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="bc9e0-110">Elements and attributes</span></span>

<span data-ttu-id="bc9e0-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bc9e0-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bc9e0-112">Child elements</span></span>

|<span data-ttu-id="bc9e0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bc9e0-113">**Element**</span></span>|<span data-ttu-id="bc9e0-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bc9e0-114">**Type**</span></span>|<span data-ttu-id="bc9e0-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bc9e0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bc9e0-116">Icon</span><span class="sxs-lookup"><span data-stu-id="bc9e0-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bc9e0-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="bc9e0-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bc9e0-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="bc9e0-118">Attributes</span></span>

|<span data-ttu-id="bc9e0-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="bc9e0-119">**Attribute**</span></span>|<span data-ttu-id="bc9e0-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bc9e0-120">**Type**</span></span>|<span data-ttu-id="bc9e0-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="bc9e0-121">**Required**</span></span>|<span data-ttu-id="bc9e0-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bc9e0-122">**Description**</span></span>|<span data-ttu-id="bc9e0-123">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="bc9e0-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bc9e0-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="bc9e0-124">AlignName</span></span>  <br/> |<span data-ttu-id="bc9e0-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bc9e0-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bc9e0-126">opcional</span><span class="sxs-lookup"><span data-stu-id="bc9e0-126">optional</span></span>  <br/> ||<span data-ttu-id="bc9e0-127">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bc9e0-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="bc9e0-128">IconSize</span></span>  <br/> |<span data-ttu-id="bc9e0-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bc9e0-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bc9e0-130">opcional</span><span class="sxs-lookup"><span data-stu-id="bc9e0-130">optional</span></span>  <br/> ||<span data-ttu-id="bc9e0-131">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bc9e0-132">ID</span><span class="sxs-lookup"><span data-stu-id="bc9e0-132">ID</span></span>  <br/> |<span data-ttu-id="bc9e0-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bc9e0-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bc9e0-134">necesario</span><span class="sxs-lookup"><span data-stu-id="bc9e0-134">required</span></span>  <br/> ||<span data-ttu-id="bc9e0-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bc9e0-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="bc9e0-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="bc9e0-137">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="bc9e0-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bc9e0-138">opcional</span><span class="sxs-lookup"><span data-stu-id="bc9e0-138">optional</span></span>  <br/> ||<span data-ttu-id="bc9e0-139">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="bc9e0-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="bc9e0-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="bc9e0-141">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="bc9e0-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bc9e0-142">opcional</span><span class="sxs-lookup"><span data-stu-id="bc9e0-142">optional</span></span>  <br/> ||<span data-ttu-id="bc9e0-143">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="bc9e0-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="bc9e0-144">MasterType</span></span>  <br/> |<span data-ttu-id="bc9e0-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bc9e0-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bc9e0-146">opcional</span><span class="sxs-lookup"><span data-stu-id="bc9e0-146">optional</span></span>  <br/> ||<span data-ttu-id="bc9e0-147">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bc9e0-148">Nombre</span><span class="sxs-lookup"><span data-stu-id="bc9e0-148">Name</span></span>  <br/> |<span data-ttu-id="bc9e0-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="bc9e0-149">xsd:string</span></span>  <br/> |<span data-ttu-id="bc9e0-150">opcional</span><span class="sxs-lookup"><span data-stu-id="bc9e0-150">optional</span></span>  <br/> ||<span data-ttu-id="bc9e0-151">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bc9e0-152">NameU</span><span class="sxs-lookup"><span data-stu-id="bc9e0-152">NameU</span></span>  <br/> |<span data-ttu-id="bc9e0-153">xsd: String</span><span class="sxs-lookup"><span data-stu-id="bc9e0-153">xsd:string</span></span>  <br/> |<span data-ttu-id="bc9e0-154">opcional</span><span class="sxs-lookup"><span data-stu-id="bc9e0-154">optional</span></span>  <br/> ||<span data-ttu-id="bc9e0-155">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bc9e0-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="bc9e0-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="bc9e0-157">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bc9e0-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bc9e0-158">opcional</span><span class="sxs-lookup"><span data-stu-id="bc9e0-158">optional</span></span>  <br/> ||<span data-ttu-id="bc9e0-159">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bc9e0-160">Prompt</span><span class="sxs-lookup"><span data-stu-id="bc9e0-160">Prompt</span></span>  <br/> |<span data-ttu-id="bc9e0-161">xsd: String</span><span class="sxs-lookup"><span data-stu-id="bc9e0-161">xsd:string</span></span>  <br/> |<span data-ttu-id="bc9e0-162">opcional</span><span class="sxs-lookup"><span data-stu-id="bc9e0-162">optional</span></span>  <br/> ||<span data-ttu-id="bc9e0-163">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bc9e0-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="bc9e0-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="bc9e0-165">xsd: String</span><span class="sxs-lookup"><span data-stu-id="bc9e0-165">xsd:string</span></span>  <br/> |<span data-ttu-id="bc9e0-166">opcional</span><span class="sxs-lookup"><span data-stu-id="bc9e0-166">optional</span></span>  <br/> ||<span data-ttu-id="bc9e0-167">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bc9e0-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="bc9e0-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="bc9e0-169">xsd: String</span><span class="sxs-lookup"><span data-stu-id="bc9e0-169">xsd:string</span></span>  <br/> |<span data-ttu-id="bc9e0-170">opcional</span><span class="sxs-lookup"><span data-stu-id="bc9e0-170">optional</span></span>  <br/> ||<span data-ttu-id="bc9e0-171">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-171">Values of the xsd:string type.</span></span>  <br/> |
   

