---
title: FaceName_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: f0a136cec6d620ba7001ed0e6fae01af82c2180d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542901"
---
# <a name="facename_type-complextype-visio-xml"></a><span data-ttu-id="94992-102">FaceName_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="94992-102">FaceName_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="94992-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="94992-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94992-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="94992-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="94992-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="94992-105">**Schema file**</span></span> <br/> |<span data-ttu-id="94992-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="94992-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="94992-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="94992-107">**Extension base**</span></span> <br/> |<span data-ttu-id="94992-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="94992-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="94992-109">Definición</span><span class="sxs-lookup"><span data-stu-id="94992-109">Definition</span></span>

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="94992-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="94992-110">Elements and attributes</span></span>

<span data-ttu-id="94992-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="94992-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="94992-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="94992-112">Child elements</span></span>

<span data-ttu-id="94992-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="94992-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94992-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="94992-114">Attributes</span></span>

|<span data-ttu-id="94992-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="94992-115">**Attribute**</span></span>|<span data-ttu-id="94992-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="94992-116">**Type**</span></span>|<span data-ttu-id="94992-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="94992-117">**Required**</span></span>|<span data-ttu-id="94992-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="94992-118">**Description**</span></span>|<span data-ttu-id="94992-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="94992-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="94992-120">CharSets</span><span class="sxs-lookup"><span data-stu-id="94992-120">CharSets</span></span>  <br/> |<span data-ttu-id="94992-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="94992-121">xsd:string</span></span>  <br/> |<span data-ttu-id="94992-122">opcional</span><span class="sxs-lookup"><span data-stu-id="94992-122">optional</span></span>  <br/> ||<span data-ttu-id="94992-123">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="94992-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="94992-124">Flags</span><span class="sxs-lookup"><span data-stu-id="94992-124">Flags</span></span>  <br/> |<span data-ttu-id="94992-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="94992-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="94992-126">opcional</span><span class="sxs-lookup"><span data-stu-id="94992-126">optional</span></span>  <br/> ||<span data-ttu-id="94992-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="94992-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="94992-128">NameU</span><span class="sxs-lookup"><span data-stu-id="94992-128">NameU</span></span>  <br/> |<span data-ttu-id="94992-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="94992-129">xsd:string</span></span>  <br/> |<span data-ttu-id="94992-130">necesario</span><span class="sxs-lookup"><span data-stu-id="94992-130">required</span></span>  <br/> ||<span data-ttu-id="94992-131">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="94992-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="94992-132">Panos</span><span class="sxs-lookup"><span data-stu-id="94992-132">Panos</span></span>  <br/> |<span data-ttu-id="94992-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="94992-133">xsd:string</span></span>  <br/> |<span data-ttu-id="94992-134">opcional</span><span class="sxs-lookup"><span data-stu-id="94992-134">optional</span></span>  <br/> ||<span data-ttu-id="94992-135">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="94992-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="94992-136">Panose</span><span class="sxs-lookup"><span data-stu-id="94992-136">Panose</span></span>  <br/> |<span data-ttu-id="94992-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="94992-137">xsd:string</span></span>  <br/> |<span data-ttu-id="94992-138">opcional</span><span class="sxs-lookup"><span data-stu-id="94992-138">optional</span></span>  <br/> ||<span data-ttu-id="94992-139">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="94992-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="94992-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="94992-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="94992-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="94992-141">xsd:string</span></span>  <br/> |<span data-ttu-id="94992-142">opcional</span><span class="sxs-lookup"><span data-stu-id="94992-142">optional</span></span>  <br/> ||<span data-ttu-id="94992-143">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="94992-143">Values of the xsd:string type.</span></span>  <br/> |
   

