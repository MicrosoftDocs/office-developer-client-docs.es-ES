---
title: EventItem_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: 7fc23d9e2a9e4567693a4979b796804b16f148e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822090"
---
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="7e0f6-102">EventItem_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="7e0f6-102">EventItem_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7e0f6-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="7e0f6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e0f6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7e0f6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7e0f6-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7e0f6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7e0f6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7e0f6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7e0f6-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="7e0f6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7e0f6-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7e0f6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7e0f6-109">Definición</span><span class="sxs-lookup"><span data-stu-id="7e0f6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7e0f6-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="7e0f6-110">Elements and attributes</span></span>

<span data-ttu-id="7e0f6-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7e0f6-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7e0f6-112">Child elements</span></span>

<span data-ttu-id="7e0f6-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7e0f6-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="7e0f6-114">Attributes</span></span>

|<span data-ttu-id="7e0f6-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7e0f6-115">**Attribute**</span></span>|<span data-ttu-id="7e0f6-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7e0f6-116">**Type**</span></span>|<span data-ttu-id="7e0f6-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="7e0f6-117">**Required**</span></span>|<span data-ttu-id="7e0f6-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7e0f6-118">**Description**</span></span>|<span data-ttu-id="7e0f6-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="7e0f6-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7e0f6-120">Acción</span><span class="sxs-lookup"><span data-stu-id="7e0f6-120">Action</span></span>  <br/> |<span data-ttu-id="7e0f6-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="7e0f6-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="7e0f6-122">necesario</span><span class="sxs-lookup"><span data-stu-id="7e0f6-122">required</span></span>  <br/> ||<span data-ttu-id="7e0f6-123">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="7e0f6-124">Habilitado</span><span class="sxs-lookup"><span data-stu-id="7e0f6-124">Enabled</span></span>  <br/> |<span data-ttu-id="7e0f6-125">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="7e0f6-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7e0f6-126">opcional</span><span class="sxs-lookup"><span data-stu-id="7e0f6-126">optional</span></span>  <br/> ||<span data-ttu-id="7e0f6-127">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7e0f6-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="7e0f6-128">EventCode</span></span>  <br/> |<span data-ttu-id="7e0f6-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="7e0f6-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="7e0f6-130">necesario</span><span class="sxs-lookup"><span data-stu-id="7e0f6-130">required</span></span>  <br/> ||<span data-ttu-id="7e0f6-131">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="7e0f6-132">ID</span><span class="sxs-lookup"><span data-stu-id="7e0f6-132">ID</span></span>  <br/> |<span data-ttu-id="7e0f6-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7e0f6-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7e0f6-134">necesario</span><span class="sxs-lookup"><span data-stu-id="7e0f6-134">required</span></span>  <br/> ||<span data-ttu-id="7e0f6-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7e0f6-136">Destino</span><span class="sxs-lookup"><span data-stu-id="7e0f6-136">Target</span></span>  <br/> |<span data-ttu-id="7e0f6-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="7e0f6-137">xsd:string</span></span>  <br/> |<span data-ttu-id="7e0f6-138">necesario</span><span class="sxs-lookup"><span data-stu-id="7e0f6-138">required</span></span>  <br/> ||<span data-ttu-id="7e0f6-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7e0f6-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="7e0f6-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="7e0f6-141">xsd: String</span><span class="sxs-lookup"><span data-stu-id="7e0f6-141">xsd:string</span></span>  <br/> |<span data-ttu-id="7e0f6-142">necesario</span><span class="sxs-lookup"><span data-stu-id="7e0f6-142">required</span></span>  <br/> ||<span data-ttu-id="7e0f6-143">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-143">Values of the xsd:string type.</span></span>  <br/> |
   

