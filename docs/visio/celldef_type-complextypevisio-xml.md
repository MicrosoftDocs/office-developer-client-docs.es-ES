---
title: CellDef_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: 7b437e35aadfef0390908cb1337cc738668382e5
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542299"
---
# <a name="celldef_type-complextype-visio-xml"></a><span data-ttu-id="93f6c-102">CellDef_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="93f6c-102">CellDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="93f6c-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="93f6c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93f6c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="93f6c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="93f6c-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="93f6c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="93f6c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="93f6c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="93f6c-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="93f6c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="93f6c-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="93f6c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="93f6c-109">Definición</span><span class="sxs-lookup"><span data-stu-id="93f6c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="93f6c-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="93f6c-110">Elements and attributes</span></span>

<span data-ttu-id="93f6c-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="93f6c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="93f6c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="93f6c-112">Child elements</span></span>

<span data-ttu-id="93f6c-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="93f6c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="93f6c-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="93f6c-114">Attributes</span></span>

|<span data-ttu-id="93f6c-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="93f6c-115">**Attribute**</span></span>|<span data-ttu-id="93f6c-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="93f6c-116">**Type**</span></span>|<span data-ttu-id="93f6c-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="93f6c-117">**Required**</span></span>|<span data-ttu-id="93f6c-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="93f6c-118">**Description**</span></span>|<span data-ttu-id="93f6c-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="93f6c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="93f6c-120">F</span><span class="sxs-lookup"><span data-stu-id="93f6c-120">F</span></span>  <br/> |<span data-ttu-id="93f6c-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="93f6c-121">xsd:string</span></span>  <br/> |<span data-ttu-id="93f6c-122">opcional</span><span class="sxs-lookup"><span data-stu-id="93f6c-122">optional</span></span>  <br/> ||<span data-ttu-id="93f6c-123">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="93f6c-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="93f6c-124">IX</span><span class="sxs-lookup"><span data-stu-id="93f6c-124">IX</span></span>  <br/> |<span data-ttu-id="93f6c-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="93f6c-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="93f6c-126">opcional</span><span class="sxs-lookup"><span data-stu-id="93f6c-126">optional</span></span>  <br/> ||<span data-ttu-id="93f6c-127">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="93f6c-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="93f6c-128">N</span><span class="sxs-lookup"><span data-stu-id="93f6c-128">N</span></span>  <br/> |<span data-ttu-id="93f6c-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="93f6c-129">xsd:string</span></span>  <br/> |<span data-ttu-id="93f6c-130">necesario</span><span class="sxs-lookup"><span data-stu-id="93f6c-130">required</span></span>  <br/> ||<span data-ttu-id="93f6c-131">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="93f6c-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="93f6c-132">S</span><span class="sxs-lookup"><span data-stu-id="93f6c-132">S</span></span>  <br/> |<span data-ttu-id="93f6c-133">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="93f6c-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="93f6c-134">opcional</span><span class="sxs-lookup"><span data-stu-id="93f6c-134">optional</span></span>  <br/> ||<span data-ttu-id="93f6c-135">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="93f6c-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="93f6c-136">T</span><span class="sxs-lookup"><span data-stu-id="93f6c-136">T</span></span>  <br/> |<span data-ttu-id="93f6c-137">xsd:token</span><span class="sxs-lookup"><span data-stu-id="93f6c-137">xsd:token</span></span>  <br/> |<span data-ttu-id="93f6c-138">necesario</span><span class="sxs-lookup"><span data-stu-id="93f6c-138">required</span></span>  <br/> ||<span data-ttu-id="93f6c-139">Valores del tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="93f6c-139">Values of the xsd:token type.</span></span>  <br/> |
   

