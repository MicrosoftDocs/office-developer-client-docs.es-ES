---
title: Page_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: b3a4916f3de20d9350b6673a6000d56f3030b66e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822704"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="06026-102">Page_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="06026-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="06026-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="06026-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06026-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="06026-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="06026-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="06026-105">**Schema file**</span></span> <br/> |<span data-ttu-id="06026-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="06026-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="06026-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="06026-107">**Extension base**</span></span> <br/> |<span data-ttu-id="06026-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="06026-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="06026-109">Definición</span><span class="sxs-lookup"><span data-stu-id="06026-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="06026-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="06026-110">Elements and attributes</span></span>

<span data-ttu-id="06026-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="06026-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="06026-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="06026-112">Child elements</span></span>

|<span data-ttu-id="06026-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="06026-113">**Element**</span></span>|<span data-ttu-id="06026-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="06026-114">**Type**</span></span>|<span data-ttu-id="06026-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06026-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="06026-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="06026-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="06026-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="06026-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="06026-118">Rel</span><span class="sxs-lookup"><span data-stu-id="06026-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="06026-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="06026-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="06026-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="06026-120">Attributes</span></span>

|<span data-ttu-id="06026-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="06026-121">**Attribute**</span></span>|<span data-ttu-id="06026-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="06026-122">**Type**</span></span>|<span data-ttu-id="06026-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="06026-123">**Required**</span></span>|<span data-ttu-id="06026-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06026-124">**Description**</span></span>|<span data-ttu-id="06026-125">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="06026-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="06026-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="06026-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="06026-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="06026-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="06026-128">opcional</span><span class="sxs-lookup"><span data-stu-id="06026-128">optional</span></span>  <br/> ||<span data-ttu-id="06026-129">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="06026-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="06026-130">Fondo</span><span class="sxs-lookup"><span data-stu-id="06026-130">Background</span></span>  <br/> |<span data-ttu-id="06026-131">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="06026-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="06026-132">opcional</span><span class="sxs-lookup"><span data-stu-id="06026-132">optional</span></span>  <br/> ||<span data-ttu-id="06026-133">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="06026-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="06026-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="06026-134">BackPage</span></span>  <br/> |<span data-ttu-id="06026-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="06026-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="06026-136">opcional</span><span class="sxs-lookup"><span data-stu-id="06026-136">optional</span></span>  <br/> ||<span data-ttu-id="06026-137">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="06026-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="06026-138">ID</span><span class="sxs-lookup"><span data-stu-id="06026-138">ID</span></span>  <br/> |<span data-ttu-id="06026-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="06026-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="06026-140">necesario</span><span class="sxs-lookup"><span data-stu-id="06026-140">required</span></span>  <br/> ||<span data-ttu-id="06026-141">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="06026-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="06026-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="06026-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="06026-143">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="06026-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="06026-144">opcional</span><span class="sxs-lookup"><span data-stu-id="06026-144">optional</span></span>  <br/> ||<span data-ttu-id="06026-145">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="06026-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="06026-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="06026-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="06026-147">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="06026-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="06026-148">opcional</span><span class="sxs-lookup"><span data-stu-id="06026-148">optional</span></span>  <br/> ||<span data-ttu-id="06026-149">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="06026-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="06026-150">Nombre</span><span class="sxs-lookup"><span data-stu-id="06026-150">Name</span></span>  <br/> |<span data-ttu-id="06026-151">xsd: String</span><span class="sxs-lookup"><span data-stu-id="06026-151">xsd:string</span></span>  <br/> |<span data-ttu-id="06026-152">opcional</span><span class="sxs-lookup"><span data-stu-id="06026-152">optional</span></span>  <br/> ||<span data-ttu-id="06026-153">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="06026-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="06026-154">NameU</span><span class="sxs-lookup"><span data-stu-id="06026-154">NameU</span></span>  <br/> |<span data-ttu-id="06026-155">xsd: String</span><span class="sxs-lookup"><span data-stu-id="06026-155">xsd:string</span></span>  <br/> |<span data-ttu-id="06026-156">opcional</span><span class="sxs-lookup"><span data-stu-id="06026-156">optional</span></span>  <br/> ||<span data-ttu-id="06026-157">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="06026-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="06026-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="06026-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="06026-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="06026-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="06026-160">opcional</span><span class="sxs-lookup"><span data-stu-id="06026-160">optional</span></span>  <br/> ||<span data-ttu-id="06026-161">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="06026-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="06026-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="06026-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="06026-163">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="06026-163">xsd:double</span></span>  <br/> |<span data-ttu-id="06026-164">opcional</span><span class="sxs-lookup"><span data-stu-id="06026-164">optional</span></span>  <br/> ||<span data-ttu-id="06026-165">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="06026-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="06026-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="06026-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="06026-167">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="06026-167">xsd:double</span></span>  <br/> |<span data-ttu-id="06026-168">opcional</span><span class="sxs-lookup"><span data-stu-id="06026-168">optional</span></span>  <br/> ||<span data-ttu-id="06026-169">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="06026-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="06026-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="06026-170">ViewScale</span></span>  <br/> |<span data-ttu-id="06026-171">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="06026-171">xsd:double</span></span>  <br/> |<span data-ttu-id="06026-172">opcional</span><span class="sxs-lookup"><span data-stu-id="06026-172">optional</span></span>  <br/> ||<span data-ttu-id="06026-173">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="06026-173">Values of the xsd:double type.</span></span>  <br/> |
   

