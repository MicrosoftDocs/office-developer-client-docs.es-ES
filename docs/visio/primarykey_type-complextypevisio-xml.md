---
title: PrimaryKey_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 2d13ac2b6d55fdda752f16af28a0843d5a388f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822862"
---
# <a name="primarykeytype-complextype-visio-xml"></a><span data-ttu-id="3e58a-102">PrimaryKey_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="3e58a-102">PrimaryKey_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3e58a-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="3e58a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e58a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3e58a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3e58a-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3e58a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3e58a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3e58a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3e58a-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="3e58a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3e58a-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3e58a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3e58a-109">Definición</span><span class="sxs-lookup"><span data-stu-id="3e58a-109">Definition</span></span>

```XML
          <xs:complexType name="PrimaryKey_Type">
          
          <xs:sequence>
    <xs:element name="RowKeyValue"  type="RowKeyValue_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3e58a-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="3e58a-110">Elements and attributes</span></span>

<span data-ttu-id="3e58a-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="3e58a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3e58a-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3e58a-112">Child elements</span></span>

|<span data-ttu-id="3e58a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3e58a-113">**Element**</span></span>|<span data-ttu-id="3e58a-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3e58a-114">**Type**</span></span>|<span data-ttu-id="3e58a-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3e58a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3e58a-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="3e58a-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3e58a-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="3e58a-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3e58a-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="3e58a-118">Attributes</span></span>

|<span data-ttu-id="3e58a-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="3e58a-119">**Attribute**</span></span>|<span data-ttu-id="3e58a-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3e58a-120">**Type**</span></span>|<span data-ttu-id="3e58a-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="3e58a-121">**Required**</span></span>|<span data-ttu-id="3e58a-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3e58a-122">**Description**</span></span>|<span data-ttu-id="3e58a-123">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="3e58a-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3e58a-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="3e58a-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="3e58a-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="3e58a-125">xsd:string</span></span>  <br/> |<span data-ttu-id="3e58a-126">necesario</span><span class="sxs-lookup"><span data-stu-id="3e58a-126">required</span></span>  <br/> ||<span data-ttu-id="3e58a-127">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="3e58a-127">Values of the xsd:string type.</span></span>  <br/> |
   

