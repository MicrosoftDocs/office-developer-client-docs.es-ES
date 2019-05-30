---
title: ComplexType Issue_Type (XML de Visio)
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
# <a name="issuetype-complextype-visio-xml"></a><span data-ttu-id="e166e-102">ComplexType Issue_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="e166e-102">Issue_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="e166e-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="e166e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e166e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e166e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e166e-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e166e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e166e-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="e166e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e166e-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="e166e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e166e-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e166e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e166e-109">Definición</span><span class="sxs-lookup"><span data-stu-id="e166e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e166e-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e166e-110">Elements and attributes</span></span>

<span data-ttu-id="e166e-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="e166e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e166e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e166e-112">Child elements</span></span>

|<span data-ttu-id="e166e-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e166e-113">**Element**</span></span>|<span data-ttu-id="e166e-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e166e-114">**Type**</span></span>|<span data-ttu-id="e166e-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e166e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e166e-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="e166e-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e166e-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="e166e-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e166e-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="e166e-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e166e-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="e166e-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e166e-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="e166e-120">Attributes</span></span>

|<span data-ttu-id="e166e-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="e166e-121">**Attribute**</span></span>|<span data-ttu-id="e166e-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e166e-122">**Type**</span></span>|<span data-ttu-id="e166e-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="e166e-123">**Required**</span></span>|<span data-ttu-id="e166e-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e166e-124">**Description**</span></span>|<span data-ttu-id="e166e-125">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="e166e-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e166e-126">ID</span><span class="sxs-lookup"><span data-stu-id="e166e-126">ID</span></span>  <br/> |<span data-ttu-id="e166e-127">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e166e-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e166e-128">necesario</span><span class="sxs-lookup"><span data-stu-id="e166e-128">required</span></span>  <br/> ||<span data-ttu-id="e166e-129">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e166e-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e166e-130">Ignored</span><span class="sxs-lookup"><span data-stu-id="e166e-130">Ignored</span></span>  <br/> |<span data-ttu-id="e166e-131">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="e166e-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e166e-132">opcional</span><span class="sxs-lookup"><span data-stu-id="e166e-132">optional</span></span>  <br/> ||<span data-ttu-id="e166e-133">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="e166e-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

