---
title: ComplexType DocumentSettings_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8fb61b5f-1bab-78b6-c56c-384e52609397
ms.openlocfilehash: 0ec1f0dc21d7795e659fcdb512a912a00d1aacd6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540017"
---
# <a name="documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="b1dce-102">ComplexType DocumentSettings_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="b1dce-102">DocumentSettings_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b1dce-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="b1dce-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1dce-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b1dce-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b1dce-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b1dce-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b1dce-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="b1dce-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b1dce-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="b1dce-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b1dce-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b1dce-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b1dce-109">Definición</span><span class="sxs-lookup"><span data-stu-id="b1dce-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b1dce-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b1dce-110">Elements and attributes</span></span>

<span data-ttu-id="b1dce-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="b1dce-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b1dce-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b1dce-112">Child elements</span></span>

|<span data-ttu-id="b1dce-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b1dce-113">**Element**</span></span>|<span data-ttu-id="b1dce-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b1dce-114">**Type**</span></span>|<span data-ttu-id="b1dce-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b1dce-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b1dce-116">AttachedToolbars</span><span class="sxs-lookup"><span data-stu-id="b1dce-116">AttachedToolbars</span></span>](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b1dce-117">AttachedToolbars_Type</span><span class="sxs-lookup"><span data-stu-id="b1dce-117">AttachedToolbars_Type</span></span>](attachedtoolbars_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b1dce-118">CustomMenusFile</span><span class="sxs-lookup"><span data-stu-id="b1dce-118">CustomMenusFile</span></span>](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b1dce-119">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="b1dce-119">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b1dce-120">CustomToolbarsFile</span><span class="sxs-lookup"><span data-stu-id="b1dce-120">CustomToolbarsFile</span></span>](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b1dce-121">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="b1dce-121">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b1dce-122">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="b1dce-122">DynamicGridEnabled</span></span>](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b1dce-123">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="b1dce-123">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b1dce-124">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="b1dce-124">GlueSettings</span></span>](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b1dce-125">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="b1dce-125">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b1dce-126">ProtectBkgnds</span><span class="sxs-lookup"><span data-stu-id="b1dce-126">ProtectBkgnds</span></span>](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b1dce-127">ProtectBkgnds_Type</span><span class="sxs-lookup"><span data-stu-id="b1dce-127">ProtectBkgnds_Type</span></span>](protectbkgnds_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b1dce-128">ProtectMasters</span><span class="sxs-lookup"><span data-stu-id="b1dce-128">ProtectMasters</span></span>](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b1dce-129">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="b1dce-129">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b1dce-130">ProtectShapes</span><span class="sxs-lookup"><span data-stu-id="b1dce-130">ProtectShapes</span></span>](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b1dce-131">ProtectShapes_Type</span><span class="sxs-lookup"><span data-stu-id="b1dce-131">ProtectShapes_Type</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b1dce-132">ProtectStyles</span><span class="sxs-lookup"><span data-stu-id="b1dce-132">ProtectStyles</span></span>](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b1dce-133">ProtectStyles_Type</span><span class="sxs-lookup"><span data-stu-id="b1dce-133">ProtectStyles_Type</span></span>](protectstyles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b1dce-134">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="b1dce-134">SnapAngles</span></span>](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b1dce-135">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="b1dce-135">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b1dce-136">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="b1dce-136">SnapExtensions</span></span>](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b1dce-137">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="b1dce-137">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b1dce-138">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="b1dce-138">SnapSettings</span></span>](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b1dce-139">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="b1dce-139">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b1dce-140">Atributos</span><span class="sxs-lookup"><span data-stu-id="b1dce-140">Attributes</span></span>

|<span data-ttu-id="b1dce-141">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b1dce-141">**Attribute**</span></span>|<span data-ttu-id="b1dce-142">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b1dce-142">**Type**</span></span>|<span data-ttu-id="b1dce-143">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="b1dce-143">**Required**</span></span>|<span data-ttu-id="b1dce-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b1dce-144">**Description**</span></span>|<span data-ttu-id="b1dce-145">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="b1dce-145">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b1dce-146">DefaultFillStyle</span><span class="sxs-lookup"><span data-stu-id="b1dce-146">DefaultFillStyle</span></span>  <br/> |<span data-ttu-id="b1dce-147">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b1dce-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b1dce-148">opcional</span><span class="sxs-lookup"><span data-stu-id="b1dce-148">optional</span></span>  <br/> ||<span data-ttu-id="b1dce-149">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b1dce-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b1dce-150">DefaultGuideStyle</span><span class="sxs-lookup"><span data-stu-id="b1dce-150">DefaultGuideStyle</span></span>  <br/> |<span data-ttu-id="b1dce-151">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b1dce-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b1dce-152">opcional</span><span class="sxs-lookup"><span data-stu-id="b1dce-152">optional</span></span>  <br/> ||<span data-ttu-id="b1dce-153">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b1dce-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b1dce-154">DefaultLineStyle</span><span class="sxs-lookup"><span data-stu-id="b1dce-154">DefaultLineStyle</span></span>  <br/> |<span data-ttu-id="b1dce-155">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b1dce-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b1dce-156">opcional</span><span class="sxs-lookup"><span data-stu-id="b1dce-156">optional</span></span>  <br/> ||<span data-ttu-id="b1dce-157">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b1dce-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b1dce-158">DefaultTextStyle</span><span class="sxs-lookup"><span data-stu-id="b1dce-158">DefaultTextStyle</span></span>  <br/> |<span data-ttu-id="b1dce-159">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b1dce-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b1dce-160">opcional</span><span class="sxs-lookup"><span data-stu-id="b1dce-160">optional</span></span>  <br/> ||<span data-ttu-id="b1dce-161">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b1dce-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b1dce-162">Página Web</span><span class="sxs-lookup"><span data-stu-id="b1dce-162">TopPage</span></span>  <br/> |<span data-ttu-id="b1dce-163">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b1dce-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b1dce-164">opcional</span><span class="sxs-lookup"><span data-stu-id="b1dce-164">optional</span></span>  <br/> ||<span data-ttu-id="b1dce-165">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b1dce-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

