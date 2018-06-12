---
title: Window_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: dc4dda48c037f7af03ee22a07bee288ce5d30872
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823547"
---
# <a name="windowtype-complextype-visio-xml"></a><span data-ttu-id="405cb-102">Window_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="405cb-102">Window_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="405cb-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="405cb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="405cb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="405cb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="405cb-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="405cb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="405cb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="405cb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="405cb-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="405cb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="405cb-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="405cb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="405cb-109">Definición</span><span class="sxs-lookup"><span data-stu-id="405cb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="405cb-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="405cb-110">Elements and attributes</span></span>

<span data-ttu-id="405cb-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="405cb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="405cb-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="405cb-112">Child elements</span></span>

|<span data-ttu-id="405cb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="405cb-113">**Element**</span></span>|<span data-ttu-id="405cb-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="405cb-114">**Type**</span></span>|<span data-ttu-id="405cb-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="405cb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="405cb-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="405cb-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="405cb-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="405cb-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="405cb-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="405cb-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="405cb-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="405cb-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="405cb-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="405cb-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="405cb-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="405cb-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="405cb-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="405cb-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="405cb-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="405cb-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="405cb-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="405cb-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="405cb-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="405cb-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="405cb-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="405cb-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="405cb-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="405cb-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="405cb-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="405cb-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="405cb-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="405cb-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="405cb-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="405cb-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="405cb-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="405cb-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="405cb-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="405cb-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="405cb-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="405cb-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="405cb-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="405cb-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="405cb-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="405cb-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="405cb-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="405cb-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="405cb-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="405cb-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="405cb-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="405cb-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="405cb-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="405cb-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="405cb-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="405cb-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="405cb-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="405cb-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="405cb-142">Atributos</span><span class="sxs-lookup"><span data-stu-id="405cb-142">Attributes</span></span>

|<span data-ttu-id="405cb-143">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="405cb-143">**Attribute**</span></span>|<span data-ttu-id="405cb-144">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="405cb-144">**Type**</span></span>|<span data-ttu-id="405cb-145">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="405cb-145">**Required**</span></span>|<span data-ttu-id="405cb-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="405cb-146">**Description**</span></span>|<span data-ttu-id="405cb-147">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="405cb-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="405cb-148">Container</span><span class="sxs-lookup"><span data-stu-id="405cb-148">Container</span></span>  <br/> |<span data-ttu-id="405cb-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="405cb-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="405cb-150">opcional</span><span class="sxs-lookup"><span data-stu-id="405cb-150">optional</span></span>  <br/> ||<span data-ttu-id="405cb-151">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="405cb-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="405cb-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="405cb-152">ContainerType</span></span>  <br/> |<span data-ttu-id="405cb-153">xsd:token</span><span class="sxs-lookup"><span data-stu-id="405cb-153">xsd:token</span></span>  <br/> |<span data-ttu-id="405cb-154">opcional</span><span class="sxs-lookup"><span data-stu-id="405cb-154">optional</span></span>  <br/> ||<span data-ttu-id="405cb-155">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="405cb-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="405cb-156">Documento</span><span class="sxs-lookup"><span data-stu-id="405cb-156">Document</span></span>  <br/> |<span data-ttu-id="405cb-157">xsd: String</span><span class="sxs-lookup"><span data-stu-id="405cb-157">xsd:string</span></span>  <br/> |<span data-ttu-id="405cb-158">opcional</span><span class="sxs-lookup"><span data-stu-id="405cb-158">optional</span></span>  <br/> ||<span data-ttu-id="405cb-159">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="405cb-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="405cb-160">id.</span><span class="sxs-lookup"><span data-stu-id="405cb-160">ID</span></span>  <br/> |<span data-ttu-id="405cb-161">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="405cb-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="405cb-162">necesario</span><span class="sxs-lookup"><span data-stu-id="405cb-162">required</span></span>  <br/> ||<span data-ttu-id="405cb-163">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="405cb-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="405cb-164">Master</span><span class="sxs-lookup"><span data-stu-id="405cb-164">Master</span></span>  <br/> |<span data-ttu-id="405cb-165">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="405cb-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="405cb-166">opcional</span><span class="sxs-lookup"><span data-stu-id="405cb-166">optional</span></span>  <br/> ||<span data-ttu-id="405cb-167">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="405cb-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="405cb-168">Page</span><span class="sxs-lookup"><span data-stu-id="405cb-168">Page</span></span>  <br/> |<span data-ttu-id="405cb-169">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="405cb-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="405cb-170">opcional</span><span class="sxs-lookup"><span data-stu-id="405cb-170">optional</span></span>  <br/> ||<span data-ttu-id="405cb-171">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="405cb-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="405cb-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="405cb-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="405cb-173">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="405cb-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="405cb-174">opcional</span><span class="sxs-lookup"><span data-stu-id="405cb-174">optional</span></span>  <br/> ||<span data-ttu-id="405cb-175">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="405cb-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="405cb-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="405cb-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="405cb-177">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="405cb-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="405cb-178">opcional</span><span class="sxs-lookup"><span data-stu-id="405cb-178">optional</span></span>  <br/> ||<span data-ttu-id="405cb-179">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="405cb-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="405cb-180">Hoja</span><span class="sxs-lookup"><span data-stu-id="405cb-180">Sheet</span></span>  <br/> |<span data-ttu-id="405cb-181">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="405cb-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="405cb-182">opcional</span><span class="sxs-lookup"><span data-stu-id="405cb-182">optional</span></span>  <br/> ||<span data-ttu-id="405cb-183">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="405cb-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="405cb-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="405cb-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="405cb-185">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="405cb-185">xsd:double</span></span>  <br/> |<span data-ttu-id="405cb-186">opcional</span><span class="sxs-lookup"><span data-stu-id="405cb-186">optional</span></span>  <br/> ||<span data-ttu-id="405cb-187">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="405cb-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="405cb-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="405cb-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="405cb-189">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="405cb-189">xsd:double</span></span>  <br/> |<span data-ttu-id="405cb-190">opcional</span><span class="sxs-lookup"><span data-stu-id="405cb-190">optional</span></span>  <br/> ||<span data-ttu-id="405cb-191">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="405cb-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="405cb-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="405cb-192">ViewScale</span></span>  <br/> |<span data-ttu-id="405cb-193">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="405cb-193">xsd:double</span></span>  <br/> |<span data-ttu-id="405cb-194">opcional</span><span class="sxs-lookup"><span data-stu-id="405cb-194">optional</span></span>  <br/> ||<span data-ttu-id="405cb-195">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="405cb-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="405cb-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="405cb-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="405cb-197">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="405cb-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="405cb-198">opcional</span><span class="sxs-lookup"><span data-stu-id="405cb-198">optional</span></span>  <br/> ||<span data-ttu-id="405cb-199">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="405cb-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="405cb-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="405cb-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="405cb-201">xsd:short</span><span class="sxs-lookup"><span data-stu-id="405cb-201">xsd:short</span></span>  <br/> |<span data-ttu-id="405cb-202">opcional</span><span class="sxs-lookup"><span data-stu-id="405cb-202">optional</span></span>  <br/> ||<span data-ttu-id="405cb-203">Valores del tipo xsd:short.</span><span class="sxs-lookup"><span data-stu-id="405cb-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="405cb-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="405cb-204">WindowState</span></span>  <br/> |<span data-ttu-id="405cb-205">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="405cb-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="405cb-206">opcional</span><span class="sxs-lookup"><span data-stu-id="405cb-206">optional</span></span>  <br/> ||<span data-ttu-id="405cb-207">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="405cb-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="405cb-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="405cb-208">WindowTop</span></span>  <br/> |<span data-ttu-id="405cb-209">xsd:short</span><span class="sxs-lookup"><span data-stu-id="405cb-209">xsd:short</span></span>  <br/> |<span data-ttu-id="405cb-210">opcional</span><span class="sxs-lookup"><span data-stu-id="405cb-210">optional</span></span>  <br/> ||<span data-ttu-id="405cb-211">Valores del tipo xsd:short.</span><span class="sxs-lookup"><span data-stu-id="405cb-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="405cb-212">Tipo ventana</span><span class="sxs-lookup"><span data-stu-id="405cb-212">WindowType</span></span>  <br/> |<span data-ttu-id="405cb-213">xsd:token</span><span class="sxs-lookup"><span data-stu-id="405cb-213">xsd:token</span></span>  <br/> |<span data-ttu-id="405cb-214">necesario</span><span class="sxs-lookup"><span data-stu-id="405cb-214">required</span></span>  <br/> ||<span data-ttu-id="405cb-215">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="405cb-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="405cb-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="405cb-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="405cb-217">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="405cb-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="405cb-218">opcional</span><span class="sxs-lookup"><span data-stu-id="405cb-218">optional</span></span>  <br/> ||<span data-ttu-id="405cb-219">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="405cb-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

