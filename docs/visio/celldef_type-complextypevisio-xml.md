---
title: CellDef_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: 6471158df8c89e8d7b0202f9bdbce196e24b93b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821731"
---
# <a name="celldeftype-complextype-visio-xml"></a><span data-ttu-id="0e307-102">CellDef_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="0e307-102">CellDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0e307-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="0e307-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e307-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0e307-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0e307-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0e307-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0e307-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0e307-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0e307-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="0e307-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0e307-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0e307-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0e307-109">Definición</span><span class="sxs-lookup"><span data-stu-id="0e307-109">Definition</span></span>

```XML
      <xs:complexType name="CellDef_Type">
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0e307-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0e307-110">Elements and attributes</span></span>

<span data-ttu-id="0e307-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="0e307-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0e307-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0e307-112">Child elements</span></span>

<span data-ttu-id="0e307-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0e307-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e307-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="0e307-114">Attributes</span></span>

|<span data-ttu-id="0e307-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0e307-115">**Attribute**</span></span>|<span data-ttu-id="0e307-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0e307-116">**Type**</span></span>|<span data-ttu-id="0e307-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="0e307-117">**Required**</span></span>|<span data-ttu-id="0e307-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e307-118">**Description**</span></span>|<span data-ttu-id="0e307-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="0e307-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0e307-120">F</span><span class="sxs-lookup"><span data-stu-id="0e307-120">F</span></span>  <br/> |<span data-ttu-id="0e307-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0e307-121">xsd:string</span></span>  <br/> |<span data-ttu-id="0e307-122">opcional</span><span class="sxs-lookup"><span data-stu-id="0e307-122">optional</span></span>  <br/> ||<span data-ttu-id="0e307-123">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0e307-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0e307-124">IX</span><span class="sxs-lookup"><span data-stu-id="0e307-124">IX</span></span>  <br/> |<span data-ttu-id="0e307-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="0e307-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="0e307-126">opcional</span><span class="sxs-lookup"><span data-stu-id="0e307-126">optional</span></span>  <br/> ||<span data-ttu-id="0e307-127">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="0e307-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="0e307-128">N</span><span class="sxs-lookup"><span data-stu-id="0e307-128">N</span></span>  <br/> |<span data-ttu-id="0e307-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0e307-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0e307-130">necesario</span><span class="sxs-lookup"><span data-stu-id="0e307-130">required</span></span>  <br/> ||<span data-ttu-id="0e307-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0e307-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0e307-132">S</span><span class="sxs-lookup"><span data-stu-id="0e307-132">S</span></span>  <br/> |<span data-ttu-id="0e307-133">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="0e307-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="0e307-134">opcional</span><span class="sxs-lookup"><span data-stu-id="0e307-134">optional</span></span>  <br/> ||<span data-ttu-id="0e307-135">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="0e307-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="0e307-136">T</span><span class="sxs-lookup"><span data-stu-id="0e307-136">T</span></span>  <br/> |<span data-ttu-id="0e307-137">xsd:token</span><span class="sxs-lookup"><span data-stu-id="0e307-137">xsd:token</span></span>  <br/> |<span data-ttu-id="0e307-138">necesario</span><span class="sxs-lookup"><span data-stu-id="0e307-138">required</span></span>  <br/> ||<span data-ttu-id="0e307-139">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="0e307-139">Values of the xsd:token type.</span></span>  <br/> |
   

