---
title: RuleSet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: 5d3d29ee7ae48c344afcdce3faf5e26d5f564501
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541627"
---
# <a name="ruleset_type-complextype-visio-xml"></a><span data-ttu-id="65345-102">RuleSet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="65345-102">RuleSet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="65345-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="65345-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65345-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="65345-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="65345-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="65345-105">**Schema file**</span></span> <br/> |<span data-ttu-id="65345-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="65345-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="65345-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="65345-107">**Extension base**</span></span> <br/> |<span data-ttu-id="65345-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="65345-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="65345-109">Definición</span><span class="sxs-lookup"><span data-stu-id="65345-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="65345-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="65345-110">Elements and attributes</span></span>

<span data-ttu-id="65345-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="65345-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="65345-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="65345-112">Child elements</span></span>

|<span data-ttu-id="65345-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="65345-113">**Element**</span></span>|<span data-ttu-id="65345-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="65345-114">**Type**</span></span>|<span data-ttu-id="65345-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65345-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="65345-116">Rule</span><span class="sxs-lookup"><span data-stu-id="65345-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65345-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="65345-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="65345-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="65345-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65345-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="65345-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="65345-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="65345-120">Attributes</span></span>

|<span data-ttu-id="65345-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="65345-121">**Attribute**</span></span>|<span data-ttu-id="65345-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="65345-122">**Type**</span></span>|<span data-ttu-id="65345-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="65345-123">**Required**</span></span>|<span data-ttu-id="65345-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65345-124">**Description**</span></span>|<span data-ttu-id="65345-125">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="65345-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="65345-126">Description</span><span class="sxs-lookup"><span data-stu-id="65345-126">Description</span></span>  <br/> |<span data-ttu-id="65345-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="65345-127">xsd:string</span></span>  <br/> |<span data-ttu-id="65345-128">opcional</span><span class="sxs-lookup"><span data-stu-id="65345-128">optional</span></span>  <br/> ||<span data-ttu-id="65345-129">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="65345-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="65345-130">Habilitado</span><span class="sxs-lookup"><span data-stu-id="65345-130">Enabled</span></span>  <br/> |<span data-ttu-id="65345-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="65345-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="65345-132">opcional</span><span class="sxs-lookup"><span data-stu-id="65345-132">optional</span></span>  <br/> ||<span data-ttu-id="65345-133">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="65345-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="65345-134">ID</span><span class="sxs-lookup"><span data-stu-id="65345-134">ID</span></span>  <br/> |<span data-ttu-id="65345-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="65345-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="65345-136">necesario</span><span class="sxs-lookup"><span data-stu-id="65345-136">required</span></span>  <br/> ||<span data-ttu-id="65345-137">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="65345-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="65345-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="65345-138">Name</span></span>  <br/> |<span data-ttu-id="65345-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="65345-139">xsd:string</span></span>  <br/> |<span data-ttu-id="65345-140">opcional</span><span class="sxs-lookup"><span data-stu-id="65345-140">optional</span></span>  <br/> ||<span data-ttu-id="65345-141">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="65345-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="65345-142">NameU</span><span class="sxs-lookup"><span data-stu-id="65345-142">NameU</span></span>  <br/> |<span data-ttu-id="65345-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="65345-143">xsd:string</span></span>  <br/> |<span data-ttu-id="65345-144">necesario</span><span class="sxs-lookup"><span data-stu-id="65345-144">required</span></span>  <br/> ||<span data-ttu-id="65345-145">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="65345-145">Values of the xsd:string type.</span></span>  <br/> |
   

