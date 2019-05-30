---
title: ComplexType PrimaryKey_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 2e8b1a8238133bf579dadf80363a70be949f48d2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538798"
---
# <a name="primarykeytype-complextype-visio-xml"></a><span data-ttu-id="72839-102">ComplexType PrimaryKey_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="72839-102">PrimaryKey_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="72839-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="72839-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72839-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="72839-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="72839-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="72839-105">**Schema file**</span></span> <br/> |<span data-ttu-id="72839-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="72839-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="72839-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="72839-107">**Extension base**</span></span> <br/> |<span data-ttu-id="72839-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="72839-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="72839-109">Definición</span><span class="sxs-lookup"><span data-stu-id="72839-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="72839-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="72839-110">Elements and attributes</span></span>

<span data-ttu-id="72839-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="72839-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="72839-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="72839-112">Child elements</span></span>

|<span data-ttu-id="72839-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="72839-113">**Element**</span></span>|<span data-ttu-id="72839-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="72839-114">**Type**</span></span>|<span data-ttu-id="72839-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="72839-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="72839-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="72839-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="72839-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="72839-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="72839-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="72839-118">Attributes</span></span>

|<span data-ttu-id="72839-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="72839-119">**Attribute**</span></span>|<span data-ttu-id="72839-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="72839-120">**Type**</span></span>|<span data-ttu-id="72839-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="72839-121">**Required**</span></span>|<span data-ttu-id="72839-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="72839-122">**Description**</span></span>|<span data-ttu-id="72839-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="72839-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="72839-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="72839-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="72839-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="72839-125">xsd:string</span></span>  <br/> |<span data-ttu-id="72839-126">necesario</span><span class="sxs-lookup"><span data-stu-id="72839-126">required</span></span>  <br/> ||<span data-ttu-id="72839-127">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="72839-127">Values of the xsd:string type.</span></span>  <br/> |
   

