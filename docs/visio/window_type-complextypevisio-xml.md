---
title: Window_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: 08b65a5f0e108c5503e29c7e195d681d0a343521
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538455"
---
# <a name="window_type-complextype-visio-xml"></a><span data-ttu-id="1f395-102">Window_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1f395-102">Window_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1f395-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="1f395-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f395-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1f395-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1f395-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1f395-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1f395-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1f395-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1f395-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="1f395-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1f395-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1f395-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1f395-109">Definición</span><span class="sxs-lookup"><span data-stu-id="1f395-109">Definition</span></span>

```XML
          <xs:complexType name="Window_Type">
          
          <xs:sequence>
    <xs:element name="StencilGroup"  type="StencilGroup_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="StencilGroupPos"  type="StencilGroupPos_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowRulers"  type="ShowRulers_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowGrid"  type="ShowGrid_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowPageBreaks"  type="ShowPageBreaks_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowGuides"  type="ShowGuides_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowConnectionPoints"  type="ShowConnectionPoints_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
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
    
    <xs:element name="TabSplitterPos"  type="TabSplitterPos_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="WindowType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="WindowState"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Document"
  type="xsd:string"
    />
    <xs:attribute name="WindowLeft"
  type="xsd:short"
    />
    <xs:attribute name="WindowTop"
  type="xsd:short"
    />
    <xs:attribute name="WindowWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="WindowHeight"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Master"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ContainerType"
  type="xsd:token"
    />
    <xs:attribute name="Container"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Sheet"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ReadOnly"
  type="xsd:boolean"
    />
    <xs:attribute name="ParentWindow"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Page"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ViewScale"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterX"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterY"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1f395-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1f395-110">Elements and attributes</span></span>

<span data-ttu-id="1f395-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="1f395-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1f395-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1f395-112">Child elements</span></span>

|<span data-ttu-id="1f395-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1f395-113">**Element**</span></span>|<span data-ttu-id="1f395-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1f395-114">**Type**</span></span>|<span data-ttu-id="1f395-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1f395-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1f395-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="1f395-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f395-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="1f395-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1f395-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="1f395-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f395-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="1f395-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1f395-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="1f395-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f395-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="1f395-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1f395-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="1f395-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f395-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="1f395-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1f395-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="1f395-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f395-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="1f395-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1f395-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="1f395-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f395-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="1f395-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1f395-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="1f395-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f395-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="1f395-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1f395-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="1f395-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f395-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="1f395-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1f395-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="1f395-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f395-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="1f395-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1f395-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="1f395-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f395-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="1f395-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1f395-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="1f395-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f395-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="1f395-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1f395-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="1f395-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f395-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="1f395-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1f395-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="1f395-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f395-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="1f395-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1f395-142">Atributos</span><span class="sxs-lookup"><span data-stu-id="1f395-142">Attributes</span></span>

|<span data-ttu-id="1f395-143">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1f395-143">**Attribute**</span></span>|<span data-ttu-id="1f395-144">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1f395-144">**Type**</span></span>|<span data-ttu-id="1f395-145">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="1f395-145">**Required**</span></span>|<span data-ttu-id="1f395-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1f395-146">**Description**</span></span>|<span data-ttu-id="1f395-147">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="1f395-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1f395-148">Container</span><span class="sxs-lookup"><span data-stu-id="1f395-148">Container</span></span>  <br/> |<span data-ttu-id="1f395-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1f395-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1f395-150">opcional</span><span class="sxs-lookup"><span data-stu-id="1f395-150">optional</span></span>  <br/> ||<span data-ttu-id="1f395-151">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1f395-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1f395-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="1f395-152">ContainerType</span></span>  <br/> |<span data-ttu-id="1f395-153">xsd:token</span><span class="sxs-lookup"><span data-stu-id="1f395-153">xsd:token</span></span>  <br/> |<span data-ttu-id="1f395-154">opcional</span><span class="sxs-lookup"><span data-stu-id="1f395-154">optional</span></span>  <br/> ||<span data-ttu-id="1f395-155">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="1f395-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="1f395-156">Documento</span><span class="sxs-lookup"><span data-stu-id="1f395-156">Document</span></span>  <br/> |<span data-ttu-id="1f395-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1f395-157">xsd:string</span></span>  <br/> |<span data-ttu-id="1f395-158">opcional</span><span class="sxs-lookup"><span data-stu-id="1f395-158">optional</span></span>  <br/> ||<span data-ttu-id="1f395-159">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1f395-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1f395-160">ID</span><span class="sxs-lookup"><span data-stu-id="1f395-160">ID</span></span>  <br/> |<span data-ttu-id="1f395-161">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1f395-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1f395-162">necesario</span><span class="sxs-lookup"><span data-stu-id="1f395-162">required</span></span>  <br/> ||<span data-ttu-id="1f395-163">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1f395-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1f395-164">Master</span><span class="sxs-lookup"><span data-stu-id="1f395-164">Master</span></span>  <br/> |<span data-ttu-id="1f395-165">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1f395-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1f395-166">opcional</span><span class="sxs-lookup"><span data-stu-id="1f395-166">optional</span></span>  <br/> ||<span data-ttu-id="1f395-167">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1f395-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1f395-168">Page</span><span class="sxs-lookup"><span data-stu-id="1f395-168">Page</span></span>  <br/> |<span data-ttu-id="1f395-169">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1f395-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1f395-170">opcional</span><span class="sxs-lookup"><span data-stu-id="1f395-170">optional</span></span>  <br/> ||<span data-ttu-id="1f395-171">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1f395-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1f395-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="1f395-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="1f395-173">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1f395-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1f395-174">opcional</span><span class="sxs-lookup"><span data-stu-id="1f395-174">optional</span></span>  <br/> ||<span data-ttu-id="1f395-175">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1f395-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1f395-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1f395-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="1f395-177">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="1f395-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1f395-178">opcional</span><span class="sxs-lookup"><span data-stu-id="1f395-178">optional</span></span>  <br/> ||<span data-ttu-id="1f395-179">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="1f395-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1f395-180">Sheet</span><span class="sxs-lookup"><span data-stu-id="1f395-180">Sheet</span></span>  <br/> |<span data-ttu-id="1f395-181">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1f395-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1f395-182">opcional</span><span class="sxs-lookup"><span data-stu-id="1f395-182">optional</span></span>  <br/> ||<span data-ttu-id="1f395-183">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1f395-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1f395-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="1f395-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="1f395-185">xsd:double</span><span class="sxs-lookup"><span data-stu-id="1f395-185">xsd:double</span></span>  <br/> |<span data-ttu-id="1f395-186">opcional</span><span class="sxs-lookup"><span data-stu-id="1f395-186">optional</span></span>  <br/> ||<span data-ttu-id="1f395-187">Valores del tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="1f395-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="1f395-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="1f395-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="1f395-189">xsd:double</span><span class="sxs-lookup"><span data-stu-id="1f395-189">xsd:double</span></span>  <br/> |<span data-ttu-id="1f395-190">opcional</span><span class="sxs-lookup"><span data-stu-id="1f395-190">optional</span></span>  <br/> ||<span data-ttu-id="1f395-191">Valores del tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="1f395-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="1f395-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="1f395-192">ViewScale</span></span>  <br/> |<span data-ttu-id="1f395-193">xsd:double</span><span class="sxs-lookup"><span data-stu-id="1f395-193">xsd:double</span></span>  <br/> |<span data-ttu-id="1f395-194">opcional</span><span class="sxs-lookup"><span data-stu-id="1f395-194">optional</span></span>  <br/> ||<span data-ttu-id="1f395-195">Valores del tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="1f395-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="1f395-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="1f395-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="1f395-197">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1f395-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1f395-198">opcional</span><span class="sxs-lookup"><span data-stu-id="1f395-198">optional</span></span>  <br/> ||<span data-ttu-id="1f395-199">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1f395-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1f395-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="1f395-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="1f395-201">xsd:short</span><span class="sxs-lookup"><span data-stu-id="1f395-201">xsd:short</span></span>  <br/> |<span data-ttu-id="1f395-202">opcional</span><span class="sxs-lookup"><span data-stu-id="1f395-202">optional</span></span>  <br/> ||<span data-ttu-id="1f395-203">Valores del tipo xsd:short.</span><span class="sxs-lookup"><span data-stu-id="1f395-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="1f395-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="1f395-204">WindowState</span></span>  <br/> |<span data-ttu-id="1f395-205">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1f395-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1f395-206">opcional</span><span class="sxs-lookup"><span data-stu-id="1f395-206">optional</span></span>  <br/> ||<span data-ttu-id="1f395-207">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1f395-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1f395-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="1f395-208">WindowTop</span></span>  <br/> |<span data-ttu-id="1f395-209">xsd:short</span><span class="sxs-lookup"><span data-stu-id="1f395-209">xsd:short</span></span>  <br/> |<span data-ttu-id="1f395-210">opcional</span><span class="sxs-lookup"><span data-stu-id="1f395-210">optional</span></span>  <br/> ||<span data-ttu-id="1f395-211">Valores del tipo xsd:short.</span><span class="sxs-lookup"><span data-stu-id="1f395-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="1f395-212">WindowType</span><span class="sxs-lookup"><span data-stu-id="1f395-212">WindowType</span></span>  <br/> |<span data-ttu-id="1f395-213">xsd:token</span><span class="sxs-lookup"><span data-stu-id="1f395-213">xsd:token</span></span>  <br/> |<span data-ttu-id="1f395-214">necesario</span><span class="sxs-lookup"><span data-stu-id="1f395-214">required</span></span>  <br/> ||<span data-ttu-id="1f395-215">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="1f395-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="1f395-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="1f395-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="1f395-217">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1f395-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1f395-218">opcional</span><span class="sxs-lookup"><span data-stu-id="1f395-218">optional</span></span>  <br/> ||<span data-ttu-id="1f395-219">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1f395-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

