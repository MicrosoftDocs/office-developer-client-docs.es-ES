---
title: Issue_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6768062-37aa-5658-f068-dae8d3a24717
ms.openlocfilehash: b351554fe7919cada99172f721f5dbe2fd8f243a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542964"
---
# <a name="issue_type-complextype-visio-xml"></a><span data-ttu-id="b68d6-102">Issue_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b68d6-102">Issue_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b68d6-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="b68d6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b68d6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b68d6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b68d6-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b68d6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b68d6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b68d6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b68d6-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="b68d6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b68d6-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b68d6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b68d6-109">Definición</span><span class="sxs-lookup"><span data-stu-id="b68d6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b68d6-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b68d6-110">Elements and attributes</span></span>

<span data-ttu-id="b68d6-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="b68d6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b68d6-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b68d6-112">Child elements</span></span>

|<span data-ttu-id="b68d6-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b68d6-113">**Element**</span></span>|<span data-ttu-id="b68d6-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b68d6-114">**Type**</span></span>|<span data-ttu-id="b68d6-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b68d6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b68d6-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="b68d6-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b68d6-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="b68d6-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b68d6-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="b68d6-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b68d6-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="b68d6-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b68d6-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="b68d6-120">Attributes</span></span>

|<span data-ttu-id="b68d6-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b68d6-121">**Attribute**</span></span>|<span data-ttu-id="b68d6-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b68d6-122">**Type**</span></span>|<span data-ttu-id="b68d6-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="b68d6-123">**Required**</span></span>|<span data-ttu-id="b68d6-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b68d6-124">**Description**</span></span>|<span data-ttu-id="b68d6-125">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="b68d6-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b68d6-126">ID</span><span class="sxs-lookup"><span data-stu-id="b68d6-126">ID</span></span>  <br/> |<span data-ttu-id="b68d6-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b68d6-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b68d6-128">necesario</span><span class="sxs-lookup"><span data-stu-id="b68d6-128">required</span></span>  <br/> ||<span data-ttu-id="b68d6-129">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b68d6-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b68d6-130">Omitido</span><span class="sxs-lookup"><span data-stu-id="b68d6-130">Ignored</span></span>  <br/> |<span data-ttu-id="b68d6-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="b68d6-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b68d6-132">opcional</span><span class="sxs-lookup"><span data-stu-id="b68d6-132">optional</span></span>  <br/> ||<span data-ttu-id="b68d6-133">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="b68d6-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

