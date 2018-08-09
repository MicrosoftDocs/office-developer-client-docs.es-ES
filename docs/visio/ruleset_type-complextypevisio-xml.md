---
title: RuleSet_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: dfb0d50cd1c39be9b98a880028b5c4b4dc597bc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823089"
---
# <a name="rulesettype-complextype-visio-xml"></a><span data-ttu-id="597e8-102">RuleSet_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="597e8-102">RuleSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="597e8-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="597e8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="597e8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="597e8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="597e8-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="597e8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="597e8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="597e8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="597e8-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="597e8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="597e8-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="597e8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="597e8-109">Definición</span><span class="sxs-lookup"><span data-stu-id="597e8-109">Definition</span></span>

```XML
          <xs:complexType name="RuleSet_Type">
          
          <xs:sequence>
    <xs:element name="RuleSetFlags"  type="RuleSetFlags_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rule"  type="Rule_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Description"
  type="xsd:string"
    />
    <xs:attribute name="Enabled"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="597e8-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="597e8-110">Elements and attributes</span></span>

<span data-ttu-id="597e8-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="597e8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="597e8-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="597e8-112">Child elements</span></span>

|<span data-ttu-id="597e8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="597e8-113">**Element**</span></span>|<span data-ttu-id="597e8-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="597e8-114">**Type**</span></span>|<span data-ttu-id="597e8-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="597e8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="597e8-116">Rule</span><span class="sxs-lookup"><span data-stu-id="597e8-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="597e8-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="597e8-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="597e8-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="597e8-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="597e8-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="597e8-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="597e8-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="597e8-120">Attributes</span></span>

|<span data-ttu-id="597e8-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="597e8-121">**Attribute**</span></span>|<span data-ttu-id="597e8-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="597e8-122">**Type**</span></span>|<span data-ttu-id="597e8-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="597e8-123">**Required**</span></span>|<span data-ttu-id="597e8-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="597e8-124">**Description**</span></span>|<span data-ttu-id="597e8-125">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="597e8-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="597e8-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="597e8-126">Description</span></span>  <br/> |<span data-ttu-id="597e8-127">xsd: String</span><span class="sxs-lookup"><span data-stu-id="597e8-127">xsd:string</span></span>  <br/> |<span data-ttu-id="597e8-128">opcional</span><span class="sxs-lookup"><span data-stu-id="597e8-128">optional</span></span>  <br/> ||<span data-ttu-id="597e8-129">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="597e8-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="597e8-130">Habilitado</span><span class="sxs-lookup"><span data-stu-id="597e8-130">Enabled</span></span>  <br/> |<span data-ttu-id="597e8-131">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="597e8-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="597e8-132">opcional</span><span class="sxs-lookup"><span data-stu-id="597e8-132">optional</span></span>  <br/> ||<span data-ttu-id="597e8-133">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="597e8-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="597e8-134">ID</span><span class="sxs-lookup"><span data-stu-id="597e8-134">ID</span></span>  <br/> |<span data-ttu-id="597e8-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="597e8-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="597e8-136">necesario</span><span class="sxs-lookup"><span data-stu-id="597e8-136">required</span></span>  <br/> ||<span data-ttu-id="597e8-137">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="597e8-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="597e8-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="597e8-138">Name</span></span>  <br/> |<span data-ttu-id="597e8-139">xsd: String</span><span class="sxs-lookup"><span data-stu-id="597e8-139">xsd:string</span></span>  <br/> |<span data-ttu-id="597e8-140">opcional</span><span class="sxs-lookup"><span data-stu-id="597e8-140">optional</span></span>  <br/> ||<span data-ttu-id="597e8-141">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="597e8-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="597e8-142">NameU</span><span class="sxs-lookup"><span data-stu-id="597e8-142">NameU</span></span>  <br/> |<span data-ttu-id="597e8-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="597e8-143">xsd:string</span></span>  <br/> |<span data-ttu-id="597e8-144">necesario</span><span class="sxs-lookup"><span data-stu-id="597e8-144">required</span></span>  <br/> ||<span data-ttu-id="597e8-145">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="597e8-145">Values of the xsd:string type.</span></span>  <br/> |
   

