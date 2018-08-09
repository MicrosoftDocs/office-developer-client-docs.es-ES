---
title: Rule_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: 380c59d659c820f0c5452ce37fa3616e1408a86c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823076"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="8c54d-102">Rule_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="8c54d-102">Rule_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="8c54d-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="8c54d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8c54d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8c54d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8c54d-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8c54d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8c54d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8c54d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8c54d-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="8c54d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8c54d-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8c54d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8c54d-109">Definición</span><span class="sxs-lookup"><span data-stu-id="8c54d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8c54d-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="8c54d-110">Elements and attributes</span></span>

<span data-ttu-id="8c54d-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="8c54d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8c54d-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8c54d-112">Child elements</span></span>

|<span data-ttu-id="8c54d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8c54d-113">**Element**</span></span>|<span data-ttu-id="8c54d-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8c54d-114">**Type**</span></span>|<span data-ttu-id="8c54d-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8c54d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8c54d-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="8c54d-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8c54d-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="8c54d-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="8c54d-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="8c54d-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8c54d-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="8c54d-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8c54d-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="8c54d-120">Attributes</span></span>

|<span data-ttu-id="8c54d-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="8c54d-121">**Attribute**</span></span>|<span data-ttu-id="8c54d-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8c54d-122">**Type**</span></span>|<span data-ttu-id="8c54d-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="8c54d-123">**Required**</span></span>|<span data-ttu-id="8c54d-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8c54d-124">**Description**</span></span>|<span data-ttu-id="8c54d-125">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="8c54d-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8c54d-126">Category</span><span class="sxs-lookup"><span data-stu-id="8c54d-126">Category</span></span>  <br/> |<span data-ttu-id="8c54d-127">xsd: String</span><span class="sxs-lookup"><span data-stu-id="8c54d-127">xsd:string</span></span>  <br/> |<span data-ttu-id="8c54d-128">opcional</span><span class="sxs-lookup"><span data-stu-id="8c54d-128">optional</span></span>  <br/> ||<span data-ttu-id="8c54d-129">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="8c54d-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8c54d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c54d-130">Description</span></span>  <br/> |<span data-ttu-id="8c54d-131">xsd: String</span><span class="sxs-lookup"><span data-stu-id="8c54d-131">xsd:string</span></span>  <br/> |<span data-ttu-id="8c54d-132">opcional</span><span class="sxs-lookup"><span data-stu-id="8c54d-132">optional</span></span>  <br/> ||<span data-ttu-id="8c54d-133">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="8c54d-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8c54d-134">ID</span><span class="sxs-lookup"><span data-stu-id="8c54d-134">ID</span></span>  <br/> |<span data-ttu-id="8c54d-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8c54d-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8c54d-136">necesario</span><span class="sxs-lookup"><span data-stu-id="8c54d-136">required</span></span>  <br/> ||<span data-ttu-id="8c54d-137">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8c54d-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8c54d-138">Pasa por alto</span><span class="sxs-lookup"><span data-stu-id="8c54d-138">Ignored</span></span>  <br/> |<span data-ttu-id="8c54d-139">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="8c54d-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8c54d-140">opcional</span><span class="sxs-lookup"><span data-stu-id="8c54d-140">optional</span></span>  <br/> ||<span data-ttu-id="8c54d-141">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="8c54d-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8c54d-142">NameU</span><span class="sxs-lookup"><span data-stu-id="8c54d-142">NameU</span></span>  <br/> |<span data-ttu-id="8c54d-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="8c54d-143">xsd:string</span></span>  <br/> |<span data-ttu-id="8c54d-144">necesario</span><span class="sxs-lookup"><span data-stu-id="8c54d-144">required</span></span>  <br/> ||<span data-ttu-id="8c54d-145">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="8c54d-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8c54d-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="8c54d-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="8c54d-147">xsd: int</span><span class="sxs-lookup"><span data-stu-id="8c54d-147">xsd:int</span></span>  <br/> |<span data-ttu-id="8c54d-148">opcional</span><span class="sxs-lookup"><span data-stu-id="8c54d-148">optional</span></span>  <br/> ||<span data-ttu-id="8c54d-149">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="8c54d-149">Values of the xsd:int type.</span></span>  <br/> |
   

