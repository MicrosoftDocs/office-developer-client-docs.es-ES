---
title: Connect_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 9dee421915cb3e69ef5223280a425e785d29e4ec
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538742"
---
# <a name="connect_type-complextype-visio-xml"></a><span data-ttu-id="a03ec-102">Connect_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a03ec-102">Connect_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a03ec-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="a03ec-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a03ec-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a03ec-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a03ec-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a03ec-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a03ec-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a03ec-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a03ec-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="a03ec-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a03ec-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a03ec-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a03ec-109">Definición</span><span class="sxs-lookup"><span data-stu-id="a03ec-109">Definition</span></span>

```XML
      <xs:complexType name="Connect_Type">
    <xs:attribute name="FromSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FromCell"
  type="xsd:string"
    />
    <xs:attribute name="FromPart"
  type="xsd:int"
    />
    <xs:attribute name="ToSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ToCell"
  type="xsd:string"
    />
    <xs:attribute name="ToPart"
  type="xsd:int"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a03ec-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a03ec-110">Elements and attributes</span></span>

<span data-ttu-id="a03ec-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="a03ec-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a03ec-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a03ec-112">Child elements</span></span>

<span data-ttu-id="a03ec-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a03ec-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a03ec-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="a03ec-114">Attributes</span></span>

|<span data-ttu-id="a03ec-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a03ec-115">**Attribute**</span></span>|<span data-ttu-id="a03ec-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a03ec-116">**Type**</span></span>|<span data-ttu-id="a03ec-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="a03ec-117">**Required**</span></span>|<span data-ttu-id="a03ec-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a03ec-118">**Description**</span></span>|<span data-ttu-id="a03ec-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="a03ec-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a03ec-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="a03ec-120">FromCell</span></span>  <br/> |<span data-ttu-id="a03ec-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a03ec-121">xsd:string</span></span>  <br/> |<span data-ttu-id="a03ec-122">opcional</span><span class="sxs-lookup"><span data-stu-id="a03ec-122">optional</span></span>  <br/> ||<span data-ttu-id="a03ec-123">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a03ec-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a03ec-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="a03ec-124">FromPart</span></span>  <br/> |<span data-ttu-id="a03ec-125">xsd:int</span><span class="sxs-lookup"><span data-stu-id="a03ec-125">xsd:int</span></span>  <br/> |<span data-ttu-id="a03ec-126">opcional</span><span class="sxs-lookup"><span data-stu-id="a03ec-126">optional</span></span>  <br/> ||<span data-ttu-id="a03ec-127">Valores del tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="a03ec-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="a03ec-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="a03ec-128">FromSheet</span></span>  <br/> |<span data-ttu-id="a03ec-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a03ec-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a03ec-130">necesario</span><span class="sxs-lookup"><span data-stu-id="a03ec-130">required</span></span>  <br/> ||<span data-ttu-id="a03ec-131">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a03ec-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a03ec-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="a03ec-132">ToCell</span></span>  <br/> |<span data-ttu-id="a03ec-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a03ec-133">xsd:string</span></span>  <br/> |<span data-ttu-id="a03ec-134">opcional</span><span class="sxs-lookup"><span data-stu-id="a03ec-134">optional</span></span>  <br/> ||<span data-ttu-id="a03ec-135">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a03ec-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a03ec-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="a03ec-136">ToPart</span></span>  <br/> |<span data-ttu-id="a03ec-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="a03ec-137">xsd:int</span></span>  <br/> |<span data-ttu-id="a03ec-138">opcional</span><span class="sxs-lookup"><span data-stu-id="a03ec-138">optional</span></span>  <br/> ||<span data-ttu-id="a03ec-139">Valores del tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="a03ec-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="a03ec-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="a03ec-140">ToSheet</span></span>  <br/> |<span data-ttu-id="a03ec-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a03ec-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a03ec-142">necesario</span><span class="sxs-lookup"><span data-stu-id="a03ec-142">required</span></span>  <br/> ||<span data-ttu-id="a03ec-143">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a03ec-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

