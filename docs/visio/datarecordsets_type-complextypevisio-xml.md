---
title: DataRecordSets_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: 77a6588a1b5fba05d14e91a39ba570d21142f953
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539161"
---
# <a name="datarecordsets_type-complextype-visio-xml"></a><span data-ttu-id="327ef-102">DataRecordSets_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="327ef-102">DataRecordSets_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="327ef-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="327ef-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="327ef-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="327ef-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="327ef-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="327ef-105">**Schema file**</span></span> <br/> |<span data-ttu-id="327ef-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="327ef-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="327ef-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="327ef-107">**Extension base**</span></span> <br/> |<span data-ttu-id="327ef-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="327ef-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="327ef-109">Definición</span><span class="sxs-lookup"><span data-stu-id="327ef-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="327ef-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="327ef-110">Elements and attributes</span></span>

<span data-ttu-id="327ef-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="327ef-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="327ef-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="327ef-112">Child elements</span></span>

|<span data-ttu-id="327ef-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="327ef-113">**Element**</span></span>|<span data-ttu-id="327ef-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="327ef-114">**Type**</span></span>|<span data-ttu-id="327ef-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="327ef-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="327ef-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="327ef-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="327ef-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="327ef-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="327ef-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="327ef-118">Attributes</span></span>

|<span data-ttu-id="327ef-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="327ef-119">**Attribute**</span></span>|<span data-ttu-id="327ef-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="327ef-120">**Type**</span></span>|<span data-ttu-id="327ef-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="327ef-121">**Required**</span></span>|<span data-ttu-id="327ef-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="327ef-122">**Description**</span></span>|<span data-ttu-id="327ef-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="327ef-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="327ef-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="327ef-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="327ef-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="327ef-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="327ef-126">opcional</span><span class="sxs-lookup"><span data-stu-id="327ef-126">optional</span></span>  <br/> ||<span data-ttu-id="327ef-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="327ef-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="327ef-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="327ef-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="327ef-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="327ef-129">xsd:string</span></span>  <br/> |<span data-ttu-id="327ef-130">opcional</span><span class="sxs-lookup"><span data-stu-id="327ef-130">optional</span></span>  <br/> ||<span data-ttu-id="327ef-131">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="327ef-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="327ef-132">NextID</span><span class="sxs-lookup"><span data-stu-id="327ef-132">NextID</span></span>  <br/> |<span data-ttu-id="327ef-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="327ef-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="327ef-134">necesario</span><span class="sxs-lookup"><span data-stu-id="327ef-134">required</span></span>  <br/> ||<span data-ttu-id="327ef-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="327ef-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

