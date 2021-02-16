---
title: Page_Type complexType (Visio XML)
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
# <a name="page_type-complextype-visio-xml"></a><span data-ttu-id="ec954-102">Page_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ec954-102">Page_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ec954-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="ec954-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec954-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ec954-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ec954-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ec954-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ec954-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ec954-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ec954-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="ec954-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ec954-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ec954-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ec954-109">Definición</span><span class="sxs-lookup"><span data-stu-id="ec954-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ec954-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ec954-110">Elements and attributes</span></span>

<span data-ttu-id="ec954-111">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="ec954-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ec954-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ec954-112">Child elements</span></span>

|<span data-ttu-id="ec954-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ec954-113">**Element**</span></span>|<span data-ttu-id="ec954-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ec954-114">**Type**</span></span>|<span data-ttu-id="ec954-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ec954-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ec954-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="ec954-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec954-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="ec954-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec954-118">Rel</span><span class="sxs-lookup"><span data-stu-id="ec954-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec954-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="ec954-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ec954-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="ec954-120">Attributes</span></span>

|<span data-ttu-id="ec954-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ec954-121">**Attribute**</span></span>|<span data-ttu-id="ec954-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ec954-122">**Type**</span></span>|<span data-ttu-id="ec954-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="ec954-123">**Required**</span></span>|<span data-ttu-id="ec954-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ec954-124">**Description**</span></span>|<span data-ttu-id="ec954-125">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="ec954-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ec954-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="ec954-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="ec954-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ec954-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec954-128">opcional</span><span class="sxs-lookup"><span data-stu-id="ec954-128">optional</span></span>  <br/> ||<span data-ttu-id="ec954-129">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ec954-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec954-130">Información previa</span><span class="sxs-lookup"><span data-stu-id="ec954-130">Background</span></span>  <br/> |<span data-ttu-id="ec954-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="ec954-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ec954-132">opcional</span><span class="sxs-lookup"><span data-stu-id="ec954-132">optional</span></span>  <br/> ||<span data-ttu-id="ec954-133">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ec954-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ec954-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="ec954-134">BackPage</span></span>  <br/> |<span data-ttu-id="ec954-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ec954-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec954-136">opcional</span><span class="sxs-lookup"><span data-stu-id="ec954-136">optional</span></span>  <br/> ||<span data-ttu-id="ec954-137">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ec954-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec954-138">ID</span><span class="sxs-lookup"><span data-stu-id="ec954-138">ID</span></span>  <br/> |<span data-ttu-id="ec954-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ec954-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec954-140">necesario</span><span class="sxs-lookup"><span data-stu-id="ec954-140">required</span></span>  <br/> ||<span data-ttu-id="ec954-141">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ec954-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec954-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="ec954-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="ec954-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="ec954-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ec954-144">opcional</span><span class="sxs-lookup"><span data-stu-id="ec954-144">optional</span></span>  <br/> ||<span data-ttu-id="ec954-145">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ec954-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ec954-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="ec954-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="ec954-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="ec954-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ec954-148">opcional</span><span class="sxs-lookup"><span data-stu-id="ec954-148">optional</span></span>  <br/> ||<span data-ttu-id="ec954-149">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ec954-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ec954-150">Nombre</span><span class="sxs-lookup"><span data-stu-id="ec954-150">Name</span></span>  <br/> |<span data-ttu-id="ec954-151">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ec954-151">xsd:string</span></span>  <br/> |<span data-ttu-id="ec954-152">opcional</span><span class="sxs-lookup"><span data-stu-id="ec954-152">optional</span></span>  <br/> ||<span data-ttu-id="ec954-153">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ec954-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ec954-154">NameU</span><span class="sxs-lookup"><span data-stu-id="ec954-154">NameU</span></span>  <br/> |<span data-ttu-id="ec954-155">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ec954-155">xsd:string</span></span>  <br/> |<span data-ttu-id="ec954-156">opcional</span><span class="sxs-lookup"><span data-stu-id="ec954-156">optional</span></span>  <br/> ||<span data-ttu-id="ec954-157">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ec954-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ec954-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="ec954-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="ec954-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ec954-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec954-160">opcional</span><span class="sxs-lookup"><span data-stu-id="ec954-160">optional</span></span>  <br/> ||<span data-ttu-id="ec954-161">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ec954-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec954-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="ec954-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="ec954-163">xsd:double</span><span class="sxs-lookup"><span data-stu-id="ec954-163">xsd:double</span></span>  <br/> |<span data-ttu-id="ec954-164">opcional</span><span class="sxs-lookup"><span data-stu-id="ec954-164">optional</span></span>  <br/> ||<span data-ttu-id="ec954-165">Valores del tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="ec954-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="ec954-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="ec954-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="ec954-167">xsd:double</span><span class="sxs-lookup"><span data-stu-id="ec954-167">xsd:double</span></span>  <br/> |<span data-ttu-id="ec954-168">opcional</span><span class="sxs-lookup"><span data-stu-id="ec954-168">optional</span></span>  <br/> ||<span data-ttu-id="ec954-169">Valores del tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="ec954-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="ec954-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="ec954-170">ViewScale</span></span>  <br/> |<span data-ttu-id="ec954-171">xsd:double</span><span class="sxs-lookup"><span data-stu-id="ec954-171">xsd:double</span></span>  <br/> |<span data-ttu-id="ec954-172">opcional</span><span class="sxs-lookup"><span data-stu-id="ec954-172">optional</span></span>  <br/> ||<span data-ttu-id="ec954-173">Valores del tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="ec954-173">Values of the xsd:double type.</span></span>  <br/> |
   

