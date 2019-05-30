---
title: ComplexType DataRecordSets_Type (XML de Visio)
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
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="67d4e-102">ComplexType DataRecordSets_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="67d4e-102">DataRecordSets_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="67d4e-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="67d4e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67d4e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="67d4e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="67d4e-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="67d4e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="67d4e-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="67d4e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="67d4e-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="67d4e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="67d4e-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="67d4e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="67d4e-109">Definición</span><span class="sxs-lookup"><span data-stu-id="67d4e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="67d4e-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="67d4e-110">Elements and attributes</span></span>

<span data-ttu-id="67d4e-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="67d4e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="67d4e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="67d4e-112">Child elements</span></span>

|<span data-ttu-id="67d4e-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="67d4e-113">**Element**</span></span>|<span data-ttu-id="67d4e-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="67d4e-114">**Type**</span></span>|<span data-ttu-id="67d4e-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="67d4e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67d4e-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="67d4e-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67d4e-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="67d4e-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="67d4e-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="67d4e-118">Attributes</span></span>

|<span data-ttu-id="67d4e-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="67d4e-119">**Attribute**</span></span>|<span data-ttu-id="67d4e-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="67d4e-120">**Type**</span></span>|<span data-ttu-id="67d4e-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="67d4e-121">**Required**</span></span>|<span data-ttu-id="67d4e-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="67d4e-122">**Description**</span></span>|<span data-ttu-id="67d4e-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="67d4e-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="67d4e-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="67d4e-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="67d4e-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="67d4e-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="67d4e-126">opcional</span><span class="sxs-lookup"><span data-stu-id="67d4e-126">optional</span></span>  <br/> ||<span data-ttu-id="67d4e-127">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="67d4e-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="67d4e-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="67d4e-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="67d4e-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="67d4e-129">xsd:string</span></span>  <br/> |<span data-ttu-id="67d4e-130">opcional</span><span class="sxs-lookup"><span data-stu-id="67d4e-130">optional</span></span>  <br/> ||<span data-ttu-id="67d4e-131">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="67d4e-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="67d4e-132">NextID</span><span class="sxs-lookup"><span data-stu-id="67d4e-132">NextID</span></span>  <br/> |<span data-ttu-id="67d4e-133">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="67d4e-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="67d4e-134">necesario</span><span class="sxs-lookup"><span data-stu-id="67d4e-134">required</span></span>  <br/> ||<span data-ttu-id="67d4e-135">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="67d4e-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

