---
title: Page_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: d0c364164d2453c9dc64290db24890224a3c70e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334401"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="cdb28-102">Page_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="cdb28-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cdb28-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="cdb28-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cdb28-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cdb28-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cdb28-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cdb28-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cdb28-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="cdb28-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cdb28-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="cdb28-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cdb28-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cdb28-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cdb28-109">Definición</span><span class="sxs-lookup"><span data-stu-id="cdb28-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cdb28-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="cdb28-110">Elements and attributes</span></span>

<span data-ttu-id="cdb28-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="cdb28-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cdb28-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cdb28-112">Child elements</span></span>

|<span data-ttu-id="cdb28-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cdb28-113">**Element**</span></span>|<span data-ttu-id="cdb28-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cdb28-114">**Type**</span></span>|<span data-ttu-id="cdb28-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cdb28-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cdb28-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="cdb28-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cdb28-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="cdb28-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="cdb28-118">REL</span><span class="sxs-lookup"><span data-stu-id="cdb28-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cdb28-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="cdb28-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cdb28-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="cdb28-120">Attributes</span></span>

|<span data-ttu-id="cdb28-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cdb28-121">**Attribute**</span></span>|<span data-ttu-id="cdb28-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cdb28-122">**Type**</span></span>|<span data-ttu-id="cdb28-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="cdb28-123">**Required**</span></span>|<span data-ttu-id="cdb28-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cdb28-124">**Description**</span></span>|<span data-ttu-id="cdb28-125">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="cdb28-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cdb28-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="cdb28-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="cdb28-127">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cdb28-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cdb28-128">opcional</span><span class="sxs-lookup"><span data-stu-id="cdb28-128">optional</span></span>  <br/> ||<span data-ttu-id="cdb28-129">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cdb28-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cdb28-130">Fondo</span><span class="sxs-lookup"><span data-stu-id="cdb28-130">Background</span></span>  <br/> |<span data-ttu-id="cdb28-131">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="cdb28-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cdb28-132">opcional</span><span class="sxs-lookup"><span data-stu-id="cdb28-132">optional</span></span>  <br/> ||<span data-ttu-id="cdb28-133">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="cdb28-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cdb28-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="cdb28-134">BackPage</span></span>  <br/> |<span data-ttu-id="cdb28-135">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cdb28-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cdb28-136">opcional</span><span class="sxs-lookup"><span data-stu-id="cdb28-136">optional</span></span>  <br/> ||<span data-ttu-id="cdb28-137">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cdb28-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cdb28-138">ID</span><span class="sxs-lookup"><span data-stu-id="cdb28-138">ID</span></span>  <br/> |<span data-ttu-id="cdb28-139">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cdb28-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cdb28-140">necesario</span><span class="sxs-lookup"><span data-stu-id="cdb28-140">required</span></span>  <br/> ||<span data-ttu-id="cdb28-141">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cdb28-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cdb28-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="cdb28-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="cdb28-143">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="cdb28-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cdb28-144">opcional</span><span class="sxs-lookup"><span data-stu-id="cdb28-144">optional</span></span>  <br/> ||<span data-ttu-id="cdb28-145">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="cdb28-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cdb28-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="cdb28-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="cdb28-147">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="cdb28-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cdb28-148">opcional</span><span class="sxs-lookup"><span data-stu-id="cdb28-148">optional</span></span>  <br/> ||<span data-ttu-id="cdb28-149">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="cdb28-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cdb28-150">Nombre</span><span class="sxs-lookup"><span data-stu-id="cdb28-150">Name</span></span>  <br/> |<span data-ttu-id="cdb28-151">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cdb28-151">xsd:string</span></span>  <br/> |<span data-ttu-id="cdb28-152">opcional</span><span class="sxs-lookup"><span data-stu-id="cdb28-152">optional</span></span>  <br/> ||<span data-ttu-id="cdb28-153">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="cdb28-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cdb28-154">NameU</span><span class="sxs-lookup"><span data-stu-id="cdb28-154">NameU</span></span>  <br/> |<span data-ttu-id="cdb28-155">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cdb28-155">xsd:string</span></span>  <br/> |<span data-ttu-id="cdb28-156">opcional</span><span class="sxs-lookup"><span data-stu-id="cdb28-156">optional</span></span>  <br/> ||<span data-ttu-id="cdb28-157">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="cdb28-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cdb28-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="cdb28-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="cdb28-159">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cdb28-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cdb28-160">opcional</span><span class="sxs-lookup"><span data-stu-id="cdb28-160">optional</span></span>  <br/> ||<span data-ttu-id="cdb28-161">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cdb28-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cdb28-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="cdb28-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="cdb28-163">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="cdb28-163">xsd:double</span></span>  <br/> |<span data-ttu-id="cdb28-164">opcional</span><span class="sxs-lookup"><span data-stu-id="cdb28-164">optional</span></span>  <br/> ||<span data-ttu-id="cdb28-165">Valores del tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="cdb28-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="cdb28-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="cdb28-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="cdb28-167">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="cdb28-167">xsd:double</span></span>  <br/> |<span data-ttu-id="cdb28-168">opcional</span><span class="sxs-lookup"><span data-stu-id="cdb28-168">optional</span></span>  <br/> ||<span data-ttu-id="cdb28-169">Valores del tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="cdb28-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="cdb28-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="cdb28-170">ViewScale</span></span>  <br/> |<span data-ttu-id="cdb28-171">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="cdb28-171">xsd:double</span></span>  <br/> |<span data-ttu-id="cdb28-172">opcional</span><span class="sxs-lookup"><span data-stu-id="cdb28-172">optional</span></span>  <br/> ||<span data-ttu-id="cdb28-173">Valores del tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="cdb28-173">Values of the xsd:double type.</span></span>  <br/> |
   

