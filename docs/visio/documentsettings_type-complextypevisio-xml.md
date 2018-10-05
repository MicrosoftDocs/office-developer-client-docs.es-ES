---
title: DocumentSettings_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8fb61b5f-1bab-78b6-c56c-384e52609397
ms.openlocfilehash: 704591a2bf03f3eaf4d93b167475a8bae286da3e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384678"
---
# <a name="documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="a9a36-102">DocumentSettings_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="a9a36-102">DocumentSettings_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a9a36-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="a9a36-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9a36-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a9a36-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a9a36-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a9a36-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a9a36-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a9a36-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a9a36-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="a9a36-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a9a36-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a9a36-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a9a36-109">Definición</span><span class="sxs-lookup"><span data-stu-id="a9a36-109">Definition</span></span>

```XML
          <xs:complexType name="DocumentSettings_Type">
          
          <xs:all>
    <xs:element name="GlueSettings"  type="GlueSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapSettings"  type="SnapSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapExtensions"  type="SnapExtensions_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapAngles"  type="SnapAngles_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DynamicGridEnabled"  type="DynamicGridEnabled_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectStyles"  type="ProtectStyles_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectShapes"  type="ProtectShapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectMasters"  type="ProtectMasters_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectBkgnds"  type="ProtectBkgnds_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CustomMenusFile"  type="CustomMenusFile_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CustomToolbarsFile"  type="CustomToolbarsFile_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="AttachedToolbars"  type="AttachedToolbars_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="TopPage"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultTextStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultLineStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultFillStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultGuideStyle"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a9a36-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a9a36-110">Elements and attributes</span></span>

<span data-ttu-id="a9a36-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="a9a36-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a9a36-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a9a36-112">Child elements</span></span>

|<span data-ttu-id="a9a36-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9a36-113">**Element**</span></span>|<span data-ttu-id="a9a36-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a9a36-114">**Type**</span></span>|<span data-ttu-id="a9a36-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9a36-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a9a36-116">AttachedToolbars</span><span class="sxs-lookup"><span data-stu-id="a9a36-116">AttachedToolbars</span></span>](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a9a36-117">AttachedToolbars_Type</span><span class="sxs-lookup"><span data-stu-id="a9a36-117">AttachedToolbars_Type</span></span>](attachedtoolbars_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a9a36-118">CustomMenusFile</span><span class="sxs-lookup"><span data-stu-id="a9a36-118">CustomMenusFile</span></span>](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a9a36-119">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="a9a36-119">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a9a36-120">CustomToolbarsFile</span><span class="sxs-lookup"><span data-stu-id="a9a36-120">CustomToolbarsFile</span></span>](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a9a36-121">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="a9a36-121">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a9a36-122">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="a9a36-122">DynamicGridEnabled</span></span>](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a9a36-123">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="a9a36-123">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a9a36-124">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="a9a36-124">GlueSettings</span></span>](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a9a36-125">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="a9a36-125">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a9a36-126">ProtectBkgnds</span><span class="sxs-lookup"><span data-stu-id="a9a36-126">ProtectBkgnds</span></span>](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a9a36-127">ProtectBkgnds_Type</span><span class="sxs-lookup"><span data-stu-id="a9a36-127">ProtectBkgnds_Type</span></span>](protectbkgnds_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a9a36-128">ProtectMasters</span><span class="sxs-lookup"><span data-stu-id="a9a36-128">ProtectMasters</span></span>](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a9a36-129">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="a9a36-129">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a9a36-130">ProtectShapes</span><span class="sxs-lookup"><span data-stu-id="a9a36-130">ProtectShapes</span></span>](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a9a36-131">ProtectShapes_Type</span><span class="sxs-lookup"><span data-stu-id="a9a36-131">ProtectShapes_Type</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a9a36-132">ProtectStyles</span><span class="sxs-lookup"><span data-stu-id="a9a36-132">ProtectStyles</span></span>](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a9a36-133">ProtectStyles_Type</span><span class="sxs-lookup"><span data-stu-id="a9a36-133">ProtectStyles_Type</span></span>](protectstyles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a9a36-134">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="a9a36-134">SnapAngles</span></span>](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a9a36-135">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="a9a36-135">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a9a36-136">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="a9a36-136">SnapExtensions</span></span>](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a9a36-137">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="a9a36-137">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a9a36-138">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="a9a36-138">SnapSettings</span></span>](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a9a36-139">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="a9a36-139">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a9a36-140">Atributos</span><span class="sxs-lookup"><span data-stu-id="a9a36-140">Attributes</span></span>

|<span data-ttu-id="a9a36-141">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a9a36-141">**Attribute**</span></span>|<span data-ttu-id="a9a36-142">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a9a36-142">**Type**</span></span>|<span data-ttu-id="a9a36-143">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="a9a36-143">**Required**</span></span>|<span data-ttu-id="a9a36-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9a36-144">**Description**</span></span>|<span data-ttu-id="a9a36-145">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="a9a36-145">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a9a36-146">DefaultFillStyle</span><span class="sxs-lookup"><span data-stu-id="a9a36-146">DefaultFillStyle</span></span>  <br/> |<span data-ttu-id="a9a36-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a9a36-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a9a36-148">opcional</span><span class="sxs-lookup"><span data-stu-id="a9a36-148">optional</span></span>  <br/> ||<span data-ttu-id="a9a36-149">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a9a36-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a9a36-150">DefaultGuideStyle</span><span class="sxs-lookup"><span data-stu-id="a9a36-150">DefaultGuideStyle</span></span>  <br/> |<span data-ttu-id="a9a36-151">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a9a36-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a9a36-152">opcional</span><span class="sxs-lookup"><span data-stu-id="a9a36-152">optional</span></span>  <br/> ||<span data-ttu-id="a9a36-153">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a9a36-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a9a36-154">DefaultLineStyle</span><span class="sxs-lookup"><span data-stu-id="a9a36-154">DefaultLineStyle</span></span>  <br/> |<span data-ttu-id="a9a36-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a9a36-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a9a36-156">opcional</span><span class="sxs-lookup"><span data-stu-id="a9a36-156">optional</span></span>  <br/> ||<span data-ttu-id="a9a36-157">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a9a36-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a9a36-158">DefaultTextStyle</span><span class="sxs-lookup"><span data-stu-id="a9a36-158">DefaultTextStyle</span></span>  <br/> |<span data-ttu-id="a9a36-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a9a36-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a9a36-160">opcional</span><span class="sxs-lookup"><span data-stu-id="a9a36-160">optional</span></span>  <br/> ||<span data-ttu-id="a9a36-161">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a9a36-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a9a36-162">TopPage</span><span class="sxs-lookup"><span data-stu-id="a9a36-162">TopPage</span></span>  <br/> |<span data-ttu-id="a9a36-163">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a9a36-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a9a36-164">opcional</span><span class="sxs-lookup"><span data-stu-id="a9a36-164">optional</span></span>  <br/> ||<span data-ttu-id="a9a36-165">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a9a36-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

