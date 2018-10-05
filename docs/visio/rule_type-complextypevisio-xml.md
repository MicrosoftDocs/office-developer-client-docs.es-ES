---
title: Rule_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: 9af47c47137e51f7189dd3f845d7bd8f35297f0d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393512"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="36c41-102">Rule_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="36c41-102">Rule_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="36c41-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="36c41-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36c41-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="36c41-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="36c41-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="36c41-105">**Schema file**</span></span> <br/> |<span data-ttu-id="36c41-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="36c41-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="36c41-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="36c41-107">**Extension base**</span></span> <br/> |<span data-ttu-id="36c41-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="36c41-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="36c41-109">Definición</span><span class="sxs-lookup"><span data-stu-id="36c41-109">Definition</span></span>

```XML
          <xs:complexType name="Rule_Type">
          
          <xs:sequence>
    <xs:element name="RuleFilter"  type="RuleFilter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleTest"  type="RuleTest_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Category"
  type="xsd:string"
    />
    <xs:attribute name="Description"
  type="xsd:string"
    />
    <xs:attribute name="RuleTarget"
  type="xsd:int"
    />
    <xs:attribute name="Ignored"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="36c41-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="36c41-110">Elements and attributes</span></span>

<span data-ttu-id="36c41-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="36c41-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="36c41-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="36c41-112">Child elements</span></span>

|<span data-ttu-id="36c41-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="36c41-113">**Element**</span></span>|<span data-ttu-id="36c41-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="36c41-114">**Type**</span></span>|<span data-ttu-id="36c41-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="36c41-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="36c41-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="36c41-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="36c41-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="36c41-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="36c41-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="36c41-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="36c41-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="36c41-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="36c41-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="36c41-120">Attributes</span></span>

|<span data-ttu-id="36c41-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="36c41-121">**Attribute**</span></span>|<span data-ttu-id="36c41-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="36c41-122">**Type**</span></span>|<span data-ttu-id="36c41-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="36c41-123">**Required**</span></span>|<span data-ttu-id="36c41-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="36c41-124">**Description**</span></span>|<span data-ttu-id="36c41-125">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="36c41-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="36c41-126">Category</span><span class="sxs-lookup"><span data-stu-id="36c41-126">Category</span></span>  <br/> |<span data-ttu-id="36c41-127">xsd: String</span><span class="sxs-lookup"><span data-stu-id="36c41-127">xsd:string</span></span>  <br/> |<span data-ttu-id="36c41-128">opcional</span><span class="sxs-lookup"><span data-stu-id="36c41-128">optional</span></span>  <br/> ||<span data-ttu-id="36c41-129">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="36c41-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="36c41-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="36c41-130">Description</span></span>  <br/> |<span data-ttu-id="36c41-131">xsd: String</span><span class="sxs-lookup"><span data-stu-id="36c41-131">xsd:string</span></span>  <br/> |<span data-ttu-id="36c41-132">opcional</span><span class="sxs-lookup"><span data-stu-id="36c41-132">optional</span></span>  <br/> ||<span data-ttu-id="36c41-133">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="36c41-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="36c41-134">ID</span><span class="sxs-lookup"><span data-stu-id="36c41-134">ID</span></span>  <br/> |<span data-ttu-id="36c41-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="36c41-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="36c41-136">necesario</span><span class="sxs-lookup"><span data-stu-id="36c41-136">required</span></span>  <br/> ||<span data-ttu-id="36c41-137">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="36c41-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="36c41-138">Pasa por alto</span><span class="sxs-lookup"><span data-stu-id="36c41-138">Ignored</span></span>  <br/> |<span data-ttu-id="36c41-139">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="36c41-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="36c41-140">opcional</span><span class="sxs-lookup"><span data-stu-id="36c41-140">optional</span></span>  <br/> ||<span data-ttu-id="36c41-141">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="36c41-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="36c41-142">NameU</span><span class="sxs-lookup"><span data-stu-id="36c41-142">NameU</span></span>  <br/> |<span data-ttu-id="36c41-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="36c41-143">xsd:string</span></span>  <br/> |<span data-ttu-id="36c41-144">necesario</span><span class="sxs-lookup"><span data-stu-id="36c41-144">required</span></span>  <br/> ||<span data-ttu-id="36c41-145">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="36c41-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="36c41-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="36c41-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="36c41-147">xsd: int</span><span class="sxs-lookup"><span data-stu-id="36c41-147">xsd:int</span></span>  <br/> |<span data-ttu-id="36c41-148">opcional</span><span class="sxs-lookup"><span data-stu-id="36c41-148">optional</span></span>  <br/> ||<span data-ttu-id="36c41-149">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="36c41-149">Values of the xsd:int type.</span></span>  <br/> |
   

