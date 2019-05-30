---
title: ComplexType DataColumns_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: ffe0fbfeaf0b0b67386a6cadd1beb78058819d39
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541151"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="0ab65-102">ComplexType DataColumns_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="0ab65-102">DataColumns_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="0ab65-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="0ab65-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ab65-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0ab65-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0ab65-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0ab65-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0ab65-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="0ab65-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0ab65-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="0ab65-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0ab65-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0ab65-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0ab65-109">Definición</span><span class="sxs-lookup"><span data-stu-id="0ab65-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0ab65-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0ab65-110">Elements and attributes</span></span>

<span data-ttu-id="0ab65-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="0ab65-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0ab65-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0ab65-112">Child elements</span></span>

|<span data-ttu-id="0ab65-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0ab65-113">**Element**</span></span>|<span data-ttu-id="0ab65-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0ab65-114">**Type**</span></span>|<span data-ttu-id="0ab65-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ab65-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0ab65-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="0ab65-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0ab65-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="0ab65-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0ab65-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="0ab65-118">Attributes</span></span>

|<span data-ttu-id="0ab65-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="0ab65-119">**Attribute**</span></span>|<span data-ttu-id="0ab65-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0ab65-120">**Type**</span></span>|<span data-ttu-id="0ab65-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="0ab65-121">**Required**</span></span>|<span data-ttu-id="0ab65-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ab65-122">**Description**</span></span>|<span data-ttu-id="0ab65-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="0ab65-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0ab65-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="0ab65-124">SortAsc</span></span>  <br/> |<span data-ttu-id="0ab65-125">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="0ab65-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0ab65-126">opcional</span><span class="sxs-lookup"><span data-stu-id="0ab65-126">optional</span></span>  <br/> ||<span data-ttu-id="0ab65-127">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="0ab65-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0ab65-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="0ab65-128">SortColumn</span></span>  <br/> |<span data-ttu-id="0ab65-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0ab65-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0ab65-130">opcional</span><span class="sxs-lookup"><span data-stu-id="0ab65-130">optional</span></span>  <br/> ||<span data-ttu-id="0ab65-131">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0ab65-131">Values of the xsd:string type.</span></span>  <br/> |
   

