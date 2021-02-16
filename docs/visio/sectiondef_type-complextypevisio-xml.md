---
title: SectionDef_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 96812d1911d249ebce02aeab20b0a77ef518fbff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542082"
---
# <a name="sectiondef_type-complextype-visio-xml"></a><span data-ttu-id="dcb33-102">SectionDef_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="dcb33-102">SectionDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="dcb33-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="dcb33-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dcb33-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dcb33-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="dcb33-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="dcb33-105">**Schema file**</span></span> <br/> |<span data-ttu-id="dcb33-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="dcb33-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="dcb33-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="dcb33-107">**Extension base**</span></span> <br/> |<span data-ttu-id="dcb33-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="dcb33-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dcb33-109">Definición</span><span class="sxs-lookup"><span data-stu-id="dcb33-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="dcb33-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="dcb33-110">Elements and attributes</span></span>

<span data-ttu-id="dcb33-111">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="dcb33-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dcb33-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dcb33-112">Child elements</span></span>

|<span data-ttu-id="dcb33-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dcb33-113">**Element**</span></span>|<span data-ttu-id="dcb33-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dcb33-114">**Type**</span></span>|<span data-ttu-id="dcb33-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dcb33-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dcb33-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="dcb33-116">CellDef</span></span> <br/> |[<span data-ttu-id="dcb33-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="dcb33-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="dcb33-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="dcb33-118">RowDef</span></span> <br/> |[<span data-ttu-id="dcb33-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="dcb33-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="dcb33-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="dcb33-120">Attributes</span></span>

|<span data-ttu-id="dcb33-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="dcb33-121">**Attribute**</span></span>|<span data-ttu-id="dcb33-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dcb33-122">**Type**</span></span>|<span data-ttu-id="dcb33-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="dcb33-123">**Required**</span></span>|<span data-ttu-id="dcb33-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dcb33-124">**Description**</span></span>|<span data-ttu-id="dcb33-125">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="dcb33-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dcb33-126">N</span><span class="sxs-lookup"><span data-stu-id="dcb33-126">N</span></span>  <br/> |<span data-ttu-id="dcb33-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dcb33-127">xsd:string</span></span>  <br/> |<span data-ttu-id="dcb33-128">necesario</span><span class="sxs-lookup"><span data-stu-id="dcb33-128">required</span></span>  <br/> ||<span data-ttu-id="dcb33-129">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="dcb33-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dcb33-130">S</span><span class="sxs-lookup"><span data-stu-id="dcb33-130">S</span></span>  <br/> |<span data-ttu-id="dcb33-131">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dcb33-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dcb33-132">opcional</span><span class="sxs-lookup"><span data-stu-id="dcb33-132">optional</span></span>  <br/> ||<span data-ttu-id="dcb33-133">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="dcb33-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dcb33-134">T</span><span class="sxs-lookup"><span data-stu-id="dcb33-134">T</span></span>  <br/> |<span data-ttu-id="dcb33-135">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dcb33-135">xsd:string</span></span>  <br/> |<span data-ttu-id="dcb33-136">opcional</span><span class="sxs-lookup"><span data-stu-id="dcb33-136">optional</span></span>  <br/> ||<span data-ttu-id="dcb33-137">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="dcb33-137">Values of the xsd:string type.</span></span>  <br/> |
   

