---
title: DataColumns_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: f125bce02fab43b808608ef6b14d59dfc08a1179
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821912"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="fa36c-102">DataColumns_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="fa36c-102">DataColumns_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fa36c-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="fa36c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa36c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fa36c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fa36c-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fa36c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fa36c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fa36c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fa36c-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="fa36c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fa36c-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fa36c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fa36c-109">Definición</span><span class="sxs-lookup"><span data-stu-id="fa36c-109">Definition</span></span>

```XML
          <xs:complexType name="DataColumns_Type">
          
          <xs:sequence>
    <xs:element name="DataColumn"  type="DataColumn_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="SortColumn"
  type="xsd:string"
    />
    <xs:attribute name="SortAsc"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fa36c-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="fa36c-110">Elements and attributes</span></span>

<span data-ttu-id="fa36c-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="fa36c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fa36c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fa36c-112">Child elements</span></span>

|<span data-ttu-id="fa36c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa36c-113">**Element**</span></span>|<span data-ttu-id="fa36c-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fa36c-114">**Type**</span></span>|<span data-ttu-id="fa36c-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa36c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fa36c-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="fa36c-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fa36c-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="fa36c-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="fa36c-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="fa36c-118">Attributes</span></span>

|<span data-ttu-id="fa36c-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="fa36c-119">**Attribute**</span></span>|<span data-ttu-id="fa36c-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fa36c-120">**Type**</span></span>|<span data-ttu-id="fa36c-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="fa36c-121">**Required**</span></span>|<span data-ttu-id="fa36c-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa36c-122">**Description**</span></span>|<span data-ttu-id="fa36c-123">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="fa36c-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fa36c-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="fa36c-124">SortAsc</span></span>  <br/> |<span data-ttu-id="fa36c-125">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="fa36c-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fa36c-126">opcional</span><span class="sxs-lookup"><span data-stu-id="fa36c-126">optional</span></span>  <br/> ||<span data-ttu-id="fa36c-127">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="fa36c-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="fa36c-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="fa36c-128">SortColumn</span></span>  <br/> |<span data-ttu-id="fa36c-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="fa36c-129">xsd:string</span></span>  <br/> |<span data-ttu-id="fa36c-130">opcional</span><span class="sxs-lookup"><span data-stu-id="fa36c-130">optional</span></span>  <br/> ||<span data-ttu-id="fa36c-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="fa36c-131">Values of the xsd:string type.</span></span>  <br/> |
   

