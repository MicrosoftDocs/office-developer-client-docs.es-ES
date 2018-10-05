---
title: DataRecordSets_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: 1705d0ea92e278008c33321f135409373b7317fd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388563"
---
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="11518-102">DataRecordSets_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="11518-102">DataRecordSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="11518-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="11518-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11518-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="11518-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="11518-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="11518-105">**Schema file**</span></span> <br/> |<span data-ttu-id="11518-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="11518-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="11518-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="11518-107">**Extension base**</span></span> <br/> |<span data-ttu-id="11518-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="11518-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="11518-109">Definición</span><span class="sxs-lookup"><span data-stu-id="11518-109">Definition</span></span>

```XML
          <xs:complexType name="DataRecordSets_Type">
          
          <xs:sequence>
    <xs:element name="DataRecordSet"  type="DataRecordSet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="NextID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ActiveRecordsetID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DataWindowOrder"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="11518-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="11518-110">Elements and attributes</span></span>

<span data-ttu-id="11518-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="11518-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="11518-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="11518-112">Child elements</span></span>

|<span data-ttu-id="11518-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="11518-113">**Element**</span></span>|<span data-ttu-id="11518-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="11518-114">**Type**</span></span>|<span data-ttu-id="11518-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="11518-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="11518-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="11518-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="11518-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="11518-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="11518-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="11518-118">Attributes</span></span>

|<span data-ttu-id="11518-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="11518-119">**Attribute**</span></span>|<span data-ttu-id="11518-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="11518-120">**Type**</span></span>|<span data-ttu-id="11518-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="11518-121">**Required**</span></span>|<span data-ttu-id="11518-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="11518-122">**Description**</span></span>|<span data-ttu-id="11518-123">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="11518-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="11518-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="11518-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="11518-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="11518-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="11518-126">opcional</span><span class="sxs-lookup"><span data-stu-id="11518-126">optional</span></span>  <br/> ||<span data-ttu-id="11518-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="11518-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="11518-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="11518-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="11518-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="11518-129">xsd:string</span></span>  <br/> |<span data-ttu-id="11518-130">opcional</span><span class="sxs-lookup"><span data-stu-id="11518-130">optional</span></span>  <br/> ||<span data-ttu-id="11518-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="11518-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="11518-132">NextID</span><span class="sxs-lookup"><span data-stu-id="11518-132">NextID</span></span>  <br/> |<span data-ttu-id="11518-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="11518-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="11518-134">necesario</span><span class="sxs-lookup"><span data-stu-id="11518-134">required</span></span>  <br/> ||<span data-ttu-id="11518-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="11518-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

