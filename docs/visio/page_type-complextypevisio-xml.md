---
title: Page_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: d0c364164d2453c9dc64290db24890224a3c70e1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401555"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="28182-102">Page_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="28182-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="28182-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="28182-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28182-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="28182-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="28182-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="28182-105">**Schema file**</span></span> <br/> |<span data-ttu-id="28182-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="28182-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="28182-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="28182-107">**Extension base**</span></span> <br/> |<span data-ttu-id="28182-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="28182-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="28182-109">Definición</span><span class="sxs-lookup"><span data-stu-id="28182-109">Definition</span></span>

```XML
          <xs:complexType name="Page_Type">
          
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
    <xs:attribute name="Background"
  type="xsd:boolean"
    />
    <xs:attribute name="BackPage"
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
    <xs:attribute name="ReviewerID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AssociatedPage"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="28182-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="28182-110">Elements and attributes</span></span>

<span data-ttu-id="28182-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="28182-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="28182-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="28182-112">Child elements</span></span>

|<span data-ttu-id="28182-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="28182-113">**Element**</span></span>|<span data-ttu-id="28182-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="28182-114">**Type**</span></span>|<span data-ttu-id="28182-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28182-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="28182-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="28182-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="28182-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="28182-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="28182-118">Rel</span><span class="sxs-lookup"><span data-stu-id="28182-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="28182-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="28182-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="28182-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="28182-120">Attributes</span></span>

|<span data-ttu-id="28182-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="28182-121">**Attribute**</span></span>|<span data-ttu-id="28182-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="28182-122">**Type**</span></span>|<span data-ttu-id="28182-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="28182-123">**Required**</span></span>|<span data-ttu-id="28182-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28182-124">**Description**</span></span>|<span data-ttu-id="28182-125">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="28182-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="28182-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="28182-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="28182-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="28182-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28182-128">opcional</span><span class="sxs-lookup"><span data-stu-id="28182-128">optional</span></span>  <br/> ||<span data-ttu-id="28182-129">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="28182-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="28182-130">Fondo</span><span class="sxs-lookup"><span data-stu-id="28182-130">Background</span></span>  <br/> |<span data-ttu-id="28182-131">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="28182-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="28182-132">opcional</span><span class="sxs-lookup"><span data-stu-id="28182-132">optional</span></span>  <br/> ||<span data-ttu-id="28182-133">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="28182-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="28182-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="28182-134">BackPage</span></span>  <br/> |<span data-ttu-id="28182-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="28182-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28182-136">opcional</span><span class="sxs-lookup"><span data-stu-id="28182-136">optional</span></span>  <br/> ||<span data-ttu-id="28182-137">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="28182-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="28182-138">ID</span><span class="sxs-lookup"><span data-stu-id="28182-138">ID</span></span>  <br/> |<span data-ttu-id="28182-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="28182-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28182-140">necesario</span><span class="sxs-lookup"><span data-stu-id="28182-140">required</span></span>  <br/> ||<span data-ttu-id="28182-141">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="28182-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="28182-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="28182-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="28182-143">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="28182-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="28182-144">opcional</span><span class="sxs-lookup"><span data-stu-id="28182-144">optional</span></span>  <br/> ||<span data-ttu-id="28182-145">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="28182-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="28182-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="28182-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="28182-147">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="28182-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="28182-148">opcional</span><span class="sxs-lookup"><span data-stu-id="28182-148">optional</span></span>  <br/> ||<span data-ttu-id="28182-149">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="28182-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="28182-150">Nombre</span><span class="sxs-lookup"><span data-stu-id="28182-150">Name</span></span>  <br/> |<span data-ttu-id="28182-151">xsd: String</span><span class="sxs-lookup"><span data-stu-id="28182-151">xsd:string</span></span>  <br/> |<span data-ttu-id="28182-152">opcional</span><span class="sxs-lookup"><span data-stu-id="28182-152">optional</span></span>  <br/> ||<span data-ttu-id="28182-153">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="28182-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="28182-154">NameU</span><span class="sxs-lookup"><span data-stu-id="28182-154">NameU</span></span>  <br/> |<span data-ttu-id="28182-155">xsd: String</span><span class="sxs-lookup"><span data-stu-id="28182-155">xsd:string</span></span>  <br/> |<span data-ttu-id="28182-156">opcional</span><span class="sxs-lookup"><span data-stu-id="28182-156">optional</span></span>  <br/> ||<span data-ttu-id="28182-157">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="28182-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="28182-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="28182-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="28182-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="28182-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28182-160">opcional</span><span class="sxs-lookup"><span data-stu-id="28182-160">optional</span></span>  <br/> ||<span data-ttu-id="28182-161">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="28182-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="28182-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="28182-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="28182-163">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="28182-163">xsd:double</span></span>  <br/> |<span data-ttu-id="28182-164">opcional</span><span class="sxs-lookup"><span data-stu-id="28182-164">optional</span></span>  <br/> ||<span data-ttu-id="28182-165">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="28182-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="28182-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="28182-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="28182-167">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="28182-167">xsd:double</span></span>  <br/> |<span data-ttu-id="28182-168">opcional</span><span class="sxs-lookup"><span data-stu-id="28182-168">optional</span></span>  <br/> ||<span data-ttu-id="28182-169">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="28182-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="28182-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="28182-170">ViewScale</span></span>  <br/> |<span data-ttu-id="28182-171">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="28182-171">xsd:double</span></span>  <br/> |<span data-ttu-id="28182-172">opcional</span><span class="sxs-lookup"><span data-stu-id="28182-172">optional</span></span>  <br/> ||<span data-ttu-id="28182-173">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="28182-173">Values of the xsd:double type.</span></span>  <br/> |
   

