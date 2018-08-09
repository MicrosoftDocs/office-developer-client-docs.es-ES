---
title: SectionDef_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 426e62ea7a9f990555776e3ac732dd43e614582d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823116"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="60417-102">SectionDef_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="60417-102">SectionDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="60417-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="60417-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60417-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="60417-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="60417-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="60417-105">**Schema file**</span></span> <br/> |<span data-ttu-id="60417-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="60417-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="60417-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="60417-107">**Extension base**</span></span> <br/> |<span data-ttu-id="60417-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="60417-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="60417-109">Definición</span><span class="sxs-lookup"><span data-stu-id="60417-109">Definition</span></span>

```XML
          <xs:complexType name="SectionDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowDef"  type="RowDef_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="60417-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="60417-110">Elements and attributes</span></span>

<span data-ttu-id="60417-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="60417-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="60417-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="60417-112">Child elements</span></span>

|<span data-ttu-id="60417-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="60417-113">**Element**</span></span>|<span data-ttu-id="60417-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="60417-114">**Type**</span></span>|<span data-ttu-id="60417-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="60417-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="60417-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="60417-116">CellDef</span></span>](http://msdn.microsoft.com/library/f0ec7afe-9e0a-b5e5-82dd-4adff1c1607f%28Office.15%29.aspx) <br/> |[<span data-ttu-id="60417-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="60417-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="60417-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="60417-118">RowDef</span></span>](http://msdn.microsoft.com/library/25615be9-1d19-1ba9-4192-7d4a0dfae717%28Office.15%29.aspx) <br/> |[<span data-ttu-id="60417-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="60417-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="60417-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="60417-120">Attributes</span></span>

|<span data-ttu-id="60417-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="60417-121">**Attribute**</span></span>|<span data-ttu-id="60417-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="60417-122">**Type**</span></span>|<span data-ttu-id="60417-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="60417-123">**Required**</span></span>|<span data-ttu-id="60417-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="60417-124">**Description**</span></span>|<span data-ttu-id="60417-125">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="60417-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="60417-126">N</span><span class="sxs-lookup"><span data-stu-id="60417-126">N</span></span>  <br/> |<span data-ttu-id="60417-127">xsd: String</span><span class="sxs-lookup"><span data-stu-id="60417-127">xsd:string</span></span>  <br/> |<span data-ttu-id="60417-128">necesario</span><span class="sxs-lookup"><span data-stu-id="60417-128">required</span></span>  <br/> ||<span data-ttu-id="60417-129">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="60417-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="60417-130">S</span><span class="sxs-lookup"><span data-stu-id="60417-130">S</span></span>  <br/> |<span data-ttu-id="60417-131">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="60417-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="60417-132">opcional</span><span class="sxs-lookup"><span data-stu-id="60417-132">optional</span></span>  <br/> ||<span data-ttu-id="60417-133">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="60417-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="60417-134">T</span><span class="sxs-lookup"><span data-stu-id="60417-134">T</span></span>  <br/> |<span data-ttu-id="60417-135">xsd: String</span><span class="sxs-lookup"><span data-stu-id="60417-135">xsd:string</span></span>  <br/> |<span data-ttu-id="60417-136">opcional</span><span class="sxs-lookup"><span data-stu-id="60417-136">optional</span></span>  <br/> ||<span data-ttu-id="60417-137">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="60417-137">Values of the xsd:string type.</span></span>  <br/> |
   

