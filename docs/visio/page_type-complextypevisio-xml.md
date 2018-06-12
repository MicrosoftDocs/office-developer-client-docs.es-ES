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
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="470ea-102">Page_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="470ea-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="470ea-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="470ea-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="470ea-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="470ea-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="470ea-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="470ea-105">**Schema file**</span></span> <br/> |<span data-ttu-id="470ea-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="470ea-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="470ea-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="470ea-107">**Extension base**</span></span> <br/> |<span data-ttu-id="470ea-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="470ea-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="470ea-109">Definición</span><span class="sxs-lookup"><span data-stu-id="470ea-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="470ea-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="470ea-110">Elements and attributes</span></span>

<span data-ttu-id="470ea-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="470ea-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="470ea-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="470ea-112">Child elements</span></span>

|<span data-ttu-id="470ea-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="470ea-113">**Element**</span></span>|<span data-ttu-id="470ea-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="470ea-114">**Type**</span></span>|<span data-ttu-id="470ea-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="470ea-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="470ea-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="470ea-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="470ea-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="470ea-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="470ea-118">Rel</span><span class="sxs-lookup"><span data-stu-id="470ea-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="470ea-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="470ea-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="470ea-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="470ea-120">Attributes</span></span>

|<span data-ttu-id="470ea-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="470ea-121">**Attribute**</span></span>|<span data-ttu-id="470ea-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="470ea-122">**Type**</span></span>|<span data-ttu-id="470ea-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="470ea-123">**Required**</span></span>|<span data-ttu-id="470ea-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="470ea-124">**Description**</span></span>|<span data-ttu-id="470ea-125">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="470ea-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="470ea-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="470ea-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="470ea-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="470ea-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="470ea-128">opcional</span><span class="sxs-lookup"><span data-stu-id="470ea-128">optional</span></span>  <br/> ||<span data-ttu-id="470ea-129">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="470ea-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="470ea-130">Fondo</span><span class="sxs-lookup"><span data-stu-id="470ea-130">Background</span></span>  <br/> |<span data-ttu-id="470ea-131">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="470ea-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="470ea-132">opcional</span><span class="sxs-lookup"><span data-stu-id="470ea-132">optional</span></span>  <br/> ||<span data-ttu-id="470ea-133">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="470ea-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="470ea-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="470ea-134">BackPage</span></span>  <br/> |<span data-ttu-id="470ea-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="470ea-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="470ea-136">opcional</span><span class="sxs-lookup"><span data-stu-id="470ea-136">optional</span></span>  <br/> ||<span data-ttu-id="470ea-137">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="470ea-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="470ea-138">id.</span><span class="sxs-lookup"><span data-stu-id="470ea-138">ID</span></span>  <br/> |<span data-ttu-id="470ea-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="470ea-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="470ea-140">necesario</span><span class="sxs-lookup"><span data-stu-id="470ea-140">required</span></span>  <br/> ||<span data-ttu-id="470ea-141">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="470ea-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="470ea-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="470ea-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="470ea-143">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="470ea-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="470ea-144">opcional</span><span class="sxs-lookup"><span data-stu-id="470ea-144">optional</span></span>  <br/> ||<span data-ttu-id="470ea-145">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="470ea-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="470ea-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="470ea-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="470ea-147">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="470ea-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="470ea-148">opcional</span><span class="sxs-lookup"><span data-stu-id="470ea-148">optional</span></span>  <br/> ||<span data-ttu-id="470ea-149">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="470ea-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="470ea-150">Nombre</span><span class="sxs-lookup"><span data-stu-id="470ea-150">Name</span></span>  <br/> |<span data-ttu-id="470ea-151">xsd: String</span><span class="sxs-lookup"><span data-stu-id="470ea-151">xsd:string</span></span>  <br/> |<span data-ttu-id="470ea-152">opcional</span><span class="sxs-lookup"><span data-stu-id="470ea-152">optional</span></span>  <br/> ||<span data-ttu-id="470ea-153">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="470ea-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="470ea-154">NameU</span><span class="sxs-lookup"><span data-stu-id="470ea-154">NameU</span></span>  <br/> |<span data-ttu-id="470ea-155">xsd: String</span><span class="sxs-lookup"><span data-stu-id="470ea-155">xsd:string</span></span>  <br/> |<span data-ttu-id="470ea-156">opcional</span><span class="sxs-lookup"><span data-stu-id="470ea-156">optional</span></span>  <br/> ||<span data-ttu-id="470ea-157">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="470ea-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="470ea-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="470ea-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="470ea-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="470ea-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="470ea-160">opcional</span><span class="sxs-lookup"><span data-stu-id="470ea-160">optional</span></span>  <br/> ||<span data-ttu-id="470ea-161">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="470ea-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="470ea-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="470ea-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="470ea-163">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="470ea-163">xsd:double</span></span>  <br/> |<span data-ttu-id="470ea-164">opcional</span><span class="sxs-lookup"><span data-stu-id="470ea-164">optional</span></span>  <br/> ||<span data-ttu-id="470ea-165">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="470ea-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="470ea-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="470ea-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="470ea-167">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="470ea-167">xsd:double</span></span>  <br/> |<span data-ttu-id="470ea-168">opcional</span><span class="sxs-lookup"><span data-stu-id="470ea-168">optional</span></span>  <br/> ||<span data-ttu-id="470ea-169">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="470ea-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="470ea-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="470ea-170">ViewScale</span></span>  <br/> |<span data-ttu-id="470ea-171">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="470ea-171">xsd:double</span></span>  <br/> |<span data-ttu-id="470ea-172">opcional</span><span class="sxs-lookup"><span data-stu-id="470ea-172">optional</span></span>  <br/> ||<span data-ttu-id="470ea-173">Valores del tipo XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="470ea-173">Values of the xsd:double type.</span></span>  <br/> |
   

