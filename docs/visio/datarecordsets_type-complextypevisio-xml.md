---
title: DataRecordSets_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: b646e7a0d4e1f49aa71b162aecdd901813b01f49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821930"
---
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="4edb6-102">DataRecordSets_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="4edb6-102">DataRecordSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4edb6-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="4edb6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4edb6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4edb6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4edb6-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4edb6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4edb6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4edb6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4edb6-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="4edb6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4edb6-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4edb6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4edb6-109">Definición</span><span class="sxs-lookup"><span data-stu-id="4edb6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4edb6-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="4edb6-110">Elements and attributes</span></span>

<span data-ttu-id="4edb6-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="4edb6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4edb6-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4edb6-112">Child elements</span></span>

|<span data-ttu-id="4edb6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4edb6-113">**Element**</span></span>|<span data-ttu-id="4edb6-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4edb6-114">**Type**</span></span>|<span data-ttu-id="4edb6-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4edb6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4edb6-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="4edb6-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4edb6-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="4edb6-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4edb6-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="4edb6-118">Attributes</span></span>

|<span data-ttu-id="4edb6-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="4edb6-119">**Attribute**</span></span>|<span data-ttu-id="4edb6-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4edb6-120">**Type**</span></span>|<span data-ttu-id="4edb6-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="4edb6-121">**Required**</span></span>|<span data-ttu-id="4edb6-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4edb6-122">**Description**</span></span>|<span data-ttu-id="4edb6-123">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="4edb6-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4edb6-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="4edb6-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="4edb6-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4edb6-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4edb6-126">opcional</span><span class="sxs-lookup"><span data-stu-id="4edb6-126">optional</span></span>  <br/> ||<span data-ttu-id="4edb6-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4edb6-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4edb6-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="4edb6-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="4edb6-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="4edb6-129">xsd:string</span></span>  <br/> |<span data-ttu-id="4edb6-130">opcional</span><span class="sxs-lookup"><span data-stu-id="4edb6-130">optional</span></span>  <br/> ||<span data-ttu-id="4edb6-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="4edb6-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4edb6-132">NextID</span><span class="sxs-lookup"><span data-stu-id="4edb6-132">NextID</span></span>  <br/> |<span data-ttu-id="4edb6-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4edb6-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4edb6-134">necesario</span><span class="sxs-lookup"><span data-stu-id="4edb6-134">required</span></span>  <br/> ||<span data-ttu-id="4edb6-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4edb6-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

