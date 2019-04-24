---
title: Rule_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: 9af47c47137e51f7189dd3f845d7bd8f35297f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283425"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="6c304-102">Rule_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="6c304-102">Rule_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6c304-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="6c304-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c304-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6c304-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6c304-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6c304-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6c304-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="6c304-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6c304-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="6c304-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6c304-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6c304-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6c304-109">Definición</span><span class="sxs-lookup"><span data-stu-id="6c304-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6c304-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="6c304-110">Elements and attributes</span></span>

<span data-ttu-id="6c304-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="6c304-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6c304-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6c304-112">Child elements</span></span>

|<span data-ttu-id="6c304-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6c304-113">**Element**</span></span>|<span data-ttu-id="6c304-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6c304-114">**Type**</span></span>|<span data-ttu-id="6c304-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6c304-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6c304-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="6c304-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6c304-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="6c304-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6c304-118">Msdnprobar</span><span class="sxs-lookup"><span data-stu-id="6c304-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6c304-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="6c304-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6c304-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="6c304-120">Attributes</span></span>

|<span data-ttu-id="6c304-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6c304-121">**Attribute**</span></span>|<span data-ttu-id="6c304-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6c304-122">**Type**</span></span>|<span data-ttu-id="6c304-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="6c304-123">**Required**</span></span>|<span data-ttu-id="6c304-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6c304-124">**Description**</span></span>|<span data-ttu-id="6c304-125">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="6c304-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6c304-126">Categoría</span><span class="sxs-lookup"><span data-stu-id="6c304-126">Category</span></span>  <br/> |<span data-ttu-id="6c304-127">xsd: String</span><span class="sxs-lookup"><span data-stu-id="6c304-127">xsd:string</span></span>  <br/> |<span data-ttu-id="6c304-128">opcional</span><span class="sxs-lookup"><span data-stu-id="6c304-128">optional</span></span>  <br/> ||<span data-ttu-id="6c304-129">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6c304-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6c304-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c304-130">Description</span></span>  <br/> |<span data-ttu-id="6c304-131">xsd: String</span><span class="sxs-lookup"><span data-stu-id="6c304-131">xsd:string</span></span>  <br/> |<span data-ttu-id="6c304-132">opcional</span><span class="sxs-lookup"><span data-stu-id="6c304-132">optional</span></span>  <br/> ||<span data-ttu-id="6c304-133">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6c304-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6c304-134">ID</span><span class="sxs-lookup"><span data-stu-id="6c304-134">ID</span></span>  <br/> |<span data-ttu-id="6c304-135">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6c304-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6c304-136">necesario</span><span class="sxs-lookup"><span data-stu-id="6c304-136">required</span></span>  <br/> ||<span data-ttu-id="6c304-137">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6c304-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6c304-138">Ignored</span><span class="sxs-lookup"><span data-stu-id="6c304-138">Ignored</span></span>  <br/> |<span data-ttu-id="6c304-139">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="6c304-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6c304-140">opcional</span><span class="sxs-lookup"><span data-stu-id="6c304-140">optional</span></span>  <br/> ||<span data-ttu-id="6c304-141">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="6c304-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6c304-142">NameU</span><span class="sxs-lookup"><span data-stu-id="6c304-142">NameU</span></span>  <br/> |<span data-ttu-id="6c304-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="6c304-143">xsd:string</span></span>  <br/> |<span data-ttu-id="6c304-144">necesario</span><span class="sxs-lookup"><span data-stu-id="6c304-144">required</span></span>  <br/> ||<span data-ttu-id="6c304-145">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6c304-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6c304-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="6c304-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="6c304-147">xsd: int</span><span class="sxs-lookup"><span data-stu-id="6c304-147">xsd:int</span></span>  <br/> |<span data-ttu-id="6c304-148">opcional</span><span class="sxs-lookup"><span data-stu-id="6c304-148">optional</span></span>  <br/> ||<span data-ttu-id="6c304-149">Valores del tipo xsd: int.</span><span class="sxs-lookup"><span data-stu-id="6c304-149">Values of the xsd:int type.</span></span>  <br/> |
   

