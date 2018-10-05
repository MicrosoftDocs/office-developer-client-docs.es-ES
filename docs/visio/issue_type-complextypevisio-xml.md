---
title: Issue_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6768062-37aa-5658-f068-dae8d3a24717
ms.openlocfilehash: 1cdc38db93da57969230c280a2df24ac3b20ad0d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399702"
---
# <a name="issuetype-complextype-visio-xml"></a><span data-ttu-id="220e1-102">Issue_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="220e1-102">Issue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="220e1-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="220e1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="220e1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="220e1-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="220e1-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="220e1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="220e1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="220e1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="220e1-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="220e1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="220e1-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="220e1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="220e1-109">Definición</span><span class="sxs-lookup"><span data-stu-id="220e1-109">Definition</span></span>

```XML
          <xs:complexType name="Issue_Type">
          
          <xs:sequence>
    <xs:element name="IssueTarget"  type="IssueTarget_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleInfo"  type="RuleInfo_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Ignored"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="220e1-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="220e1-110">Elements and attributes</span></span>

<span data-ttu-id="220e1-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="220e1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="220e1-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="220e1-112">Child elements</span></span>

|<span data-ttu-id="220e1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="220e1-113">**Element**</span></span>|<span data-ttu-id="220e1-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="220e1-114">**Type**</span></span>|<span data-ttu-id="220e1-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="220e1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="220e1-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="220e1-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="220e1-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="220e1-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="220e1-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="220e1-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="220e1-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="220e1-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="220e1-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="220e1-120">Attributes</span></span>

|<span data-ttu-id="220e1-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="220e1-121">**Attribute**</span></span>|<span data-ttu-id="220e1-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="220e1-122">**Type**</span></span>|<span data-ttu-id="220e1-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="220e1-123">**Required**</span></span>|<span data-ttu-id="220e1-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="220e1-124">**Description**</span></span>|<span data-ttu-id="220e1-125">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="220e1-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="220e1-126">ID</span><span class="sxs-lookup"><span data-stu-id="220e1-126">ID</span></span>  <br/> |<span data-ttu-id="220e1-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="220e1-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="220e1-128">necesario</span><span class="sxs-lookup"><span data-stu-id="220e1-128">required</span></span>  <br/> ||<span data-ttu-id="220e1-129">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="220e1-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="220e1-130">Pasa por alto</span><span class="sxs-lookup"><span data-stu-id="220e1-130">Ignored</span></span>  <br/> |<span data-ttu-id="220e1-131">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="220e1-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="220e1-132">opcional</span><span class="sxs-lookup"><span data-stu-id="220e1-132">optional</span></span>  <br/> ||<span data-ttu-id="220e1-133">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="220e1-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

