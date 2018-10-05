---
title: DataColumns_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: 6d802bf646ee87f4c96b9ce041352af3cab48a16
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382382"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="e1337-102">DataColumns_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="e1337-102">DataColumns_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e1337-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="e1337-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1337-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e1337-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e1337-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e1337-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e1337-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e1337-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e1337-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="e1337-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e1337-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e1337-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e1337-109">Definición</span><span class="sxs-lookup"><span data-stu-id="e1337-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e1337-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e1337-110">Elements and attributes</span></span>

<span data-ttu-id="e1337-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="e1337-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e1337-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e1337-112">Child elements</span></span>

|<span data-ttu-id="e1337-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e1337-113">**Element**</span></span>|<span data-ttu-id="e1337-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e1337-114">**Type**</span></span>|<span data-ttu-id="e1337-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e1337-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e1337-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="e1337-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e1337-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="e1337-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e1337-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="e1337-118">Attributes</span></span>

|<span data-ttu-id="e1337-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="e1337-119">**Attribute**</span></span>|<span data-ttu-id="e1337-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e1337-120">**Type**</span></span>|<span data-ttu-id="e1337-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="e1337-121">**Required**</span></span>|<span data-ttu-id="e1337-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e1337-122">**Description**</span></span>|<span data-ttu-id="e1337-123">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="e1337-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e1337-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="e1337-124">SortAsc</span></span>  <br/> |<span data-ttu-id="e1337-125">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="e1337-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e1337-126">opcional</span><span class="sxs-lookup"><span data-stu-id="e1337-126">optional</span></span>  <br/> ||<span data-ttu-id="e1337-127">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="e1337-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e1337-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="e1337-128">SortColumn</span></span>  <br/> |<span data-ttu-id="e1337-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e1337-129">xsd:string</span></span>  <br/> |<span data-ttu-id="e1337-130">opcional</span><span class="sxs-lookup"><span data-stu-id="e1337-130">optional</span></span>  <br/> ||<span data-ttu-id="e1337-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="e1337-131">Values of the xsd:string type.</span></span>  <br/> |
   

