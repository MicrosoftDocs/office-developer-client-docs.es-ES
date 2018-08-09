---
title: Issue_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6768062-37aa-5658-f068-dae8d3a24717
ms.openlocfilehash: f0346c20e4a290819e3f23a0384a59b308a5e907
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822408"
---
# <a name="issuetype-complextype-visio-xml"></a><span data-ttu-id="4e46f-102">Issue_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="4e46f-102">Issue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4e46f-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="4e46f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e46f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4e46f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4e46f-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4e46f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4e46f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4e46f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4e46f-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="4e46f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4e46f-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4e46f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4e46f-109">Definición</span><span class="sxs-lookup"><span data-stu-id="4e46f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4e46f-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="4e46f-110">Elements and attributes</span></span>

<span data-ttu-id="4e46f-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="4e46f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4e46f-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4e46f-112">Child elements</span></span>

|<span data-ttu-id="4e46f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4e46f-113">**Element**</span></span>|<span data-ttu-id="4e46f-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4e46f-114">**Type**</span></span>|<span data-ttu-id="4e46f-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4e46f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4e46f-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="4e46f-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4e46f-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="4e46f-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4e46f-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="4e46f-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4e46f-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="4e46f-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4e46f-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="4e46f-120">Attributes</span></span>

|<span data-ttu-id="4e46f-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="4e46f-121">**Attribute**</span></span>|<span data-ttu-id="4e46f-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4e46f-122">**Type**</span></span>|<span data-ttu-id="4e46f-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="4e46f-123">**Required**</span></span>|<span data-ttu-id="4e46f-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4e46f-124">**Description**</span></span>|<span data-ttu-id="4e46f-125">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="4e46f-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4e46f-126">ID</span><span class="sxs-lookup"><span data-stu-id="4e46f-126">ID</span></span>  <br/> |<span data-ttu-id="4e46f-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4e46f-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4e46f-128">necesario</span><span class="sxs-lookup"><span data-stu-id="4e46f-128">required</span></span>  <br/> ||<span data-ttu-id="4e46f-129">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4e46f-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4e46f-130">Pasa por alto</span><span class="sxs-lookup"><span data-stu-id="4e46f-130">Ignored</span></span>  <br/> |<span data-ttu-id="4e46f-131">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="4e46f-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4e46f-132">opcional</span><span class="sxs-lookup"><span data-stu-id="4e46f-132">optional</span></span>  <br/> ||<span data-ttu-id="4e46f-133">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="4e46f-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

