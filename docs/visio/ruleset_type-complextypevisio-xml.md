---
title: RuleSet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: 3d8279b2995bcdf75f67fc7f65709dc3dab49642
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307745"
---
# <a name="rulesettype-complextype-visio-xml"></a><span data-ttu-id="1ace7-102">RuleSet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1ace7-102">RuleSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1ace7-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="1ace7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ace7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1ace7-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1ace7-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1ace7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1ace7-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="1ace7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1ace7-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="1ace7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1ace7-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1ace7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1ace7-109">Definición</span><span class="sxs-lookup"><span data-stu-id="1ace7-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1ace7-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1ace7-110">Elements and attributes</span></span>

<span data-ttu-id="1ace7-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="1ace7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1ace7-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1ace7-112">Child elements</span></span>

|<span data-ttu-id="1ace7-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1ace7-113">**Element**</span></span>|<span data-ttu-id="1ace7-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1ace7-114">**Type**</span></span>|<span data-ttu-id="1ace7-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ace7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1ace7-116">Rule</span><span class="sxs-lookup"><span data-stu-id="1ace7-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1ace7-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="1ace7-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1ace7-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="1ace7-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1ace7-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="1ace7-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1ace7-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="1ace7-120">Attributes</span></span>

|<span data-ttu-id="1ace7-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1ace7-121">**Attribute**</span></span>|<span data-ttu-id="1ace7-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1ace7-122">**Type**</span></span>|<span data-ttu-id="1ace7-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="1ace7-123">**Required**</span></span>|<span data-ttu-id="1ace7-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ace7-124">**Description**</span></span>|<span data-ttu-id="1ace7-125">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="1ace7-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1ace7-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ace7-126">Description</span></span>  <br/> |<span data-ttu-id="1ace7-127">xsd: String</span><span class="sxs-lookup"><span data-stu-id="1ace7-127">xsd:string</span></span>  <br/> |<span data-ttu-id="1ace7-128">opcional</span><span class="sxs-lookup"><span data-stu-id="1ace7-128">optional</span></span>  <br/> ||<span data-ttu-id="1ace7-129">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1ace7-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1ace7-130">Habilitado</span><span class="sxs-lookup"><span data-stu-id="1ace7-130">Enabled</span></span>  <br/> |<span data-ttu-id="1ace7-131">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="1ace7-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1ace7-132">opcional</span><span class="sxs-lookup"><span data-stu-id="1ace7-132">optional</span></span>  <br/> ||<span data-ttu-id="1ace7-133">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="1ace7-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1ace7-134">ID</span><span class="sxs-lookup"><span data-stu-id="1ace7-134">ID</span></span>  <br/> |<span data-ttu-id="1ace7-135">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1ace7-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1ace7-136">necesario</span><span class="sxs-lookup"><span data-stu-id="1ace7-136">required</span></span>  <br/> ||<span data-ttu-id="1ace7-137">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1ace7-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1ace7-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="1ace7-138">Name</span></span>  <br/> |<span data-ttu-id="1ace7-139">xsd: String</span><span class="sxs-lookup"><span data-stu-id="1ace7-139">xsd:string</span></span>  <br/> |<span data-ttu-id="1ace7-140">opcional</span><span class="sxs-lookup"><span data-stu-id="1ace7-140">optional</span></span>  <br/> ||<span data-ttu-id="1ace7-141">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1ace7-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1ace7-142">NameU</span><span class="sxs-lookup"><span data-stu-id="1ace7-142">NameU</span></span>  <br/> |<span data-ttu-id="1ace7-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="1ace7-143">xsd:string</span></span>  <br/> |<span data-ttu-id="1ace7-144">necesario</span><span class="sxs-lookup"><span data-stu-id="1ace7-144">required</span></span>  <br/> ||<span data-ttu-id="1ace7-145">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1ace7-145">Values of the xsd:string type.</span></span>  <br/> |
   

