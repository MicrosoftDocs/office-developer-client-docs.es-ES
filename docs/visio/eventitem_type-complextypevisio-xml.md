---
title: EventItem_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: 77c51ab76a1d7c5c4450c429b1d3ccb8e3442f34
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395731"
---
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="c479c-102">EventItem_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="c479c-102">EventItem_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c479c-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="c479c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c479c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c479c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c479c-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c479c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c479c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c479c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c479c-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="c479c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c479c-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c479c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c479c-109">Definición</span><span class="sxs-lookup"><span data-stu-id="c479c-109">Definition</span></span>

```XML
      <xs:complexType name="EventItem_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Action"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="EventCode"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="Enabled"
  type="xsd:boolean"
    />
    <xs:attribute name="Target"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="TargetArgs"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c479c-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c479c-110">Elements and attributes</span></span>

<span data-ttu-id="c479c-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="c479c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c479c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c479c-112">Child elements</span></span>

<span data-ttu-id="c479c-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c479c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c479c-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="c479c-114">Attributes</span></span>

|<span data-ttu-id="c479c-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c479c-115">**Attribute**</span></span>|<span data-ttu-id="c479c-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c479c-116">**Type**</span></span>|<span data-ttu-id="c479c-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="c479c-117">**Required**</span></span>|<span data-ttu-id="c479c-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c479c-118">**Description**</span></span>|<span data-ttu-id="c479c-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="c479c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c479c-120">Acción</span><span class="sxs-lookup"><span data-stu-id="c479c-120">Action</span></span>  <br/> |<span data-ttu-id="c479c-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c479c-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c479c-122">necesario</span><span class="sxs-lookup"><span data-stu-id="c479c-122">required</span></span>  <br/> ||<span data-ttu-id="c479c-123">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c479c-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c479c-124">Habilitado</span><span class="sxs-lookup"><span data-stu-id="c479c-124">Enabled</span></span>  <br/> |<span data-ttu-id="c479c-125">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="c479c-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c479c-126">opcional</span><span class="sxs-lookup"><span data-stu-id="c479c-126">optional</span></span>  <br/> ||<span data-ttu-id="c479c-127">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="c479c-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c479c-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="c479c-128">EventCode</span></span>  <br/> |<span data-ttu-id="c479c-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c479c-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c479c-130">necesario</span><span class="sxs-lookup"><span data-stu-id="c479c-130">required</span></span>  <br/> ||<span data-ttu-id="c479c-131">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c479c-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c479c-132">ID</span><span class="sxs-lookup"><span data-stu-id="c479c-132">ID</span></span>  <br/> |<span data-ttu-id="c479c-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c479c-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c479c-134">necesario</span><span class="sxs-lookup"><span data-stu-id="c479c-134">required</span></span>  <br/> ||<span data-ttu-id="c479c-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c479c-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c479c-136">Destino</span><span class="sxs-lookup"><span data-stu-id="c479c-136">Target</span></span>  <br/> |<span data-ttu-id="c479c-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c479c-137">xsd:string</span></span>  <br/> |<span data-ttu-id="c479c-138">necesario</span><span class="sxs-lookup"><span data-stu-id="c479c-138">required</span></span>  <br/> ||<span data-ttu-id="c479c-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="c479c-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c479c-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="c479c-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="c479c-141">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c479c-141">xsd:string</span></span>  <br/> |<span data-ttu-id="c479c-142">necesario</span><span class="sxs-lookup"><span data-stu-id="c479c-142">required</span></span>  <br/> ||<span data-ttu-id="c479c-143">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="c479c-143">Values of the xsd:string type.</span></span>  <br/> |
   

