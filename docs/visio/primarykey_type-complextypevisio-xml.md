---
title: PrimaryKey_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 679c6335d89855febd82bdeb6e9ac88f4089e1c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355989"
---
# <a name="primarykeytype-complextype-visio-xml"></a><span data-ttu-id="67b99-102">PrimaryKey_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="67b99-102">PrimaryKey_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="67b99-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="67b99-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67b99-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="67b99-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="67b99-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="67b99-105">**Schema file**</span></span> <br/> |<span data-ttu-id="67b99-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="67b99-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="67b99-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="67b99-107">**Extension base**</span></span> <br/> |<span data-ttu-id="67b99-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="67b99-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="67b99-109">Definición</span><span class="sxs-lookup"><span data-stu-id="67b99-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="67b99-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="67b99-110">Elements and attributes</span></span>

<span data-ttu-id="67b99-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="67b99-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="67b99-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="67b99-112">Child elements</span></span>

|<span data-ttu-id="67b99-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="67b99-113">**Element**</span></span>|<span data-ttu-id="67b99-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="67b99-114">**Type**</span></span>|<span data-ttu-id="67b99-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="67b99-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67b99-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="67b99-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67b99-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="67b99-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="67b99-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="67b99-118">Attributes</span></span>

|<span data-ttu-id="67b99-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="67b99-119">**Attribute**</span></span>|<span data-ttu-id="67b99-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="67b99-120">**Type**</span></span>|<span data-ttu-id="67b99-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="67b99-121">**Required**</span></span>|<span data-ttu-id="67b99-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="67b99-122">**Description**</span></span>|<span data-ttu-id="67b99-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="67b99-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="67b99-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="67b99-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="67b99-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="67b99-125">xsd:string</span></span>  <br/> |<span data-ttu-id="67b99-126">necesario</span><span class="sxs-lookup"><span data-stu-id="67b99-126">required</span></span>  <br/> ||<span data-ttu-id="67b99-127">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="67b99-127">Values of the xsd:string type.</span></span>  <br/> |
   

