---
title: ComplexType Page_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: 3a0153b724539136fe142c2489badcf9895af765
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537986"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="8d3f0-102">ComplexType Page_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="8d3f0-102">Page_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="8d3f0-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="8d3f0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d3f0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8d3f0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8d3f0-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8d3f0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8d3f0-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="8d3f0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8d3f0-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="8d3f0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8d3f0-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8d3f0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8d3f0-109">Definición</span><span class="sxs-lookup"><span data-stu-id="8d3f0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8d3f0-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="8d3f0-110">Elements and attributes</span></span>

<span data-ttu-id="8d3f0-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="8d3f0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8d3f0-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8d3f0-112">Child elements</span></span>

|<span data-ttu-id="8d3f0-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8d3f0-113">**Element**</span></span>|<span data-ttu-id="8d3f0-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8d3f0-114">**Type**</span></span>|<span data-ttu-id="8d3f0-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8d3f0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8d3f0-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="8d3f0-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8d3f0-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="8d3f0-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="8d3f0-118">REL</span><span class="sxs-lookup"><span data-stu-id="8d3f0-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8d3f0-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="8d3f0-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8d3f0-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="8d3f0-120">Attributes</span></span>

|<span data-ttu-id="8d3f0-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="8d3f0-121">**Attribute**</span></span>|<span data-ttu-id="8d3f0-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8d3f0-122">**Type**</span></span>|<span data-ttu-id="8d3f0-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="8d3f0-123">**Required**</span></span>|<span data-ttu-id="8d3f0-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8d3f0-124">**Description**</span></span>|<span data-ttu-id="8d3f0-125">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="8d3f0-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8d3f0-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="8d3f0-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="8d3f0-127">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8d3f0-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8d3f0-128">opcional</span><span class="sxs-lookup"><span data-stu-id="8d3f0-128">optional</span></span>  <br/> ||<span data-ttu-id="8d3f0-129">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8d3f0-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8d3f0-130">Fondo</span><span class="sxs-lookup"><span data-stu-id="8d3f0-130">Background</span></span>  <br/> |<span data-ttu-id="8d3f0-131">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="8d3f0-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8d3f0-132">opcional</span><span class="sxs-lookup"><span data-stu-id="8d3f0-132">optional</span></span>  <br/> ||<span data-ttu-id="8d3f0-133">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="8d3f0-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8d3f0-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="8d3f0-134">BackPage</span></span>  <br/> |<span data-ttu-id="8d3f0-135">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8d3f0-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8d3f0-136">opcional</span><span class="sxs-lookup"><span data-stu-id="8d3f0-136">optional</span></span>  <br/> ||<span data-ttu-id="8d3f0-137">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8d3f0-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8d3f0-138">ID</span><span class="sxs-lookup"><span data-stu-id="8d3f0-138">ID</span></span>  <br/> |<span data-ttu-id="8d3f0-139">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8d3f0-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8d3f0-140">necesario</span><span class="sxs-lookup"><span data-stu-id="8d3f0-140">required</span></span>  <br/> ||<span data-ttu-id="8d3f0-141">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8d3f0-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8d3f0-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="8d3f0-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="8d3f0-143">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="8d3f0-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8d3f0-144">opcional</span><span class="sxs-lookup"><span data-stu-id="8d3f0-144">optional</span></span>  <br/> ||<span data-ttu-id="8d3f0-145">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="8d3f0-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8d3f0-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="8d3f0-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="8d3f0-147">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="8d3f0-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8d3f0-148">opcional</span><span class="sxs-lookup"><span data-stu-id="8d3f0-148">optional</span></span>  <br/> ||<span data-ttu-id="8d3f0-149">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="8d3f0-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8d3f0-150">Nombre</span><span class="sxs-lookup"><span data-stu-id="8d3f0-150">Name</span></span>  <br/> |<span data-ttu-id="8d3f0-151">xsd: String</span><span class="sxs-lookup"><span data-stu-id="8d3f0-151">xsd:string</span></span>  <br/> |<span data-ttu-id="8d3f0-152">opcional</span><span class="sxs-lookup"><span data-stu-id="8d3f0-152">optional</span></span>  <br/> ||<span data-ttu-id="8d3f0-153">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8d3f0-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8d3f0-154">NameU</span><span class="sxs-lookup"><span data-stu-id="8d3f0-154">NameU</span></span>  <br/> |<span data-ttu-id="8d3f0-155">xsd: String</span><span class="sxs-lookup"><span data-stu-id="8d3f0-155">xsd:string</span></span>  <br/> |<span data-ttu-id="8d3f0-156">opcional</span><span class="sxs-lookup"><span data-stu-id="8d3f0-156">optional</span></span>  <br/> ||<span data-ttu-id="8d3f0-157">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8d3f0-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8d3f0-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="8d3f0-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="8d3f0-159">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8d3f0-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8d3f0-160">opcional</span><span class="sxs-lookup"><span data-stu-id="8d3f0-160">optional</span></span>  <br/> ||<span data-ttu-id="8d3f0-161">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8d3f0-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8d3f0-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="8d3f0-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="8d3f0-163">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="8d3f0-163">xsd:double</span></span>  <br/> |<span data-ttu-id="8d3f0-164">opcional</span><span class="sxs-lookup"><span data-stu-id="8d3f0-164">optional</span></span>  <br/> ||<span data-ttu-id="8d3f0-165">Valores del tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="8d3f0-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="8d3f0-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="8d3f0-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="8d3f0-167">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="8d3f0-167">xsd:double</span></span>  <br/> |<span data-ttu-id="8d3f0-168">opcional</span><span class="sxs-lookup"><span data-stu-id="8d3f0-168">optional</span></span>  <br/> ||<span data-ttu-id="8d3f0-169">Valores del tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="8d3f0-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="8d3f0-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="8d3f0-170">ViewScale</span></span>  <br/> |<span data-ttu-id="8d3f0-171">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="8d3f0-171">xsd:double</span></span>  <br/> |<span data-ttu-id="8d3f0-172">opcional</span><span class="sxs-lookup"><span data-stu-id="8d3f0-172">optional</span></span>  <br/> ||<span data-ttu-id="8d3f0-173">Valores del tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="8d3f0-173">Values of the xsd:double type.</span></span>  <br/> |
   

