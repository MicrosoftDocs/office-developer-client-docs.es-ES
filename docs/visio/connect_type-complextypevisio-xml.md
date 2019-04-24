---
title: Connect_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 158fad1f3ec18bbc9565229338f4710c145c17e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327086"
---
# <a name="connecttype-complextype-visio-xml"></a><span data-ttu-id="ff4f8-102">Connect_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="ff4f8-102">Connect_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ff4f8-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="ff4f8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff4f8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ff4f8-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ff4f8-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ff4f8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ff4f8-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ff4f8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ff4f8-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="ff4f8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ff4f8-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ff4f8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ff4f8-109">Definición</span><span class="sxs-lookup"><span data-stu-id="ff4f8-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ff4f8-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ff4f8-110">Elements and attributes</span></span>

<span data-ttu-id="ff4f8-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="ff4f8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ff4f8-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ff4f8-112">Child elements</span></span>

<span data-ttu-id="ff4f8-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ff4f8-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff4f8-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="ff4f8-114">Attributes</span></span>

|<span data-ttu-id="ff4f8-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ff4f8-115">**Attribute**</span></span>|<span data-ttu-id="ff4f8-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ff4f8-116">**Type**</span></span>|<span data-ttu-id="ff4f8-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="ff4f8-117">**Required**</span></span>|<span data-ttu-id="ff4f8-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ff4f8-118">**Description**</span></span>|<span data-ttu-id="ff4f8-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="ff4f8-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ff4f8-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="ff4f8-120">FromCell</span></span>  <br/> |<span data-ttu-id="ff4f8-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ff4f8-121">xsd:string</span></span>  <br/> |<span data-ttu-id="ff4f8-122">opcional</span><span class="sxs-lookup"><span data-stu-id="ff4f8-122">optional</span></span>  <br/> ||<span data-ttu-id="ff4f8-123">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ff4f8-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ff4f8-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="ff4f8-124">FromPart</span></span>  <br/> |<span data-ttu-id="ff4f8-125">xsd: int</span><span class="sxs-lookup"><span data-stu-id="ff4f8-125">xsd:int</span></span>  <br/> |<span data-ttu-id="ff4f8-126">opcional</span><span class="sxs-lookup"><span data-stu-id="ff4f8-126">optional</span></span>  <br/> ||<span data-ttu-id="ff4f8-127">Valores del tipo xsd: int.</span><span class="sxs-lookup"><span data-stu-id="ff4f8-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="ff4f8-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="ff4f8-128">FromSheet</span></span>  <br/> |<span data-ttu-id="ff4f8-129">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff4f8-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff4f8-130">necesario</span><span class="sxs-lookup"><span data-stu-id="ff4f8-130">required</span></span>  <br/> ||<span data-ttu-id="ff4f8-131">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ff4f8-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ff4f8-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="ff4f8-132">ToCell</span></span>  <br/> |<span data-ttu-id="ff4f8-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ff4f8-133">xsd:string</span></span>  <br/> |<span data-ttu-id="ff4f8-134">opcional</span><span class="sxs-lookup"><span data-stu-id="ff4f8-134">optional</span></span>  <br/> ||<span data-ttu-id="ff4f8-135">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ff4f8-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ff4f8-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="ff4f8-136">ToPart</span></span>  <br/> |<span data-ttu-id="ff4f8-137">xsd: int</span><span class="sxs-lookup"><span data-stu-id="ff4f8-137">xsd:int</span></span>  <br/> |<span data-ttu-id="ff4f8-138">opcional</span><span class="sxs-lookup"><span data-stu-id="ff4f8-138">optional</span></span>  <br/> ||<span data-ttu-id="ff4f8-139">Valores del tipo xsd: int.</span><span class="sxs-lookup"><span data-stu-id="ff4f8-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="ff4f8-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="ff4f8-140">ToSheet</span></span>  <br/> |<span data-ttu-id="ff4f8-141">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff4f8-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff4f8-142">necesario</span><span class="sxs-lookup"><span data-stu-id="ff4f8-142">required</span></span>  <br/> ||<span data-ttu-id="ff4f8-143">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ff4f8-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

