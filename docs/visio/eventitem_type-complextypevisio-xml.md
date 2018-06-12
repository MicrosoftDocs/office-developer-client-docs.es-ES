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
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="428e0-102">EventItem_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="428e0-102">EventItem_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="428e0-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="428e0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="428e0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="428e0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="428e0-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="428e0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="428e0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="428e0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="428e0-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="428e0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="428e0-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="428e0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="428e0-109">Definición</span><span class="sxs-lookup"><span data-stu-id="428e0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="428e0-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="428e0-110">Elements and attributes</span></span>

<span data-ttu-id="428e0-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="428e0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="428e0-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="428e0-112">Child elements</span></span>

<span data-ttu-id="428e0-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="428e0-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="428e0-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="428e0-114">Attributes</span></span>

|<span data-ttu-id="428e0-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="428e0-115">**Attribute**</span></span>|<span data-ttu-id="428e0-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="428e0-116">**Type**</span></span>|<span data-ttu-id="428e0-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="428e0-117">**Required**</span></span>|<span data-ttu-id="428e0-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="428e0-118">**Description**</span></span>|<span data-ttu-id="428e0-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="428e0-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="428e0-120">Acción</span><span class="sxs-lookup"><span data-stu-id="428e0-120">Action</span></span>  <br/> |<span data-ttu-id="428e0-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="428e0-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="428e0-122">necesario</span><span class="sxs-lookup"><span data-stu-id="428e0-122">required</span></span>  <br/> ||<span data-ttu-id="428e0-123">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="428e0-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="428e0-124">Habilitado</span><span class="sxs-lookup"><span data-stu-id="428e0-124">Enabled</span></span>  <br/> |<span data-ttu-id="428e0-125">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="428e0-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="428e0-126">opcional</span><span class="sxs-lookup"><span data-stu-id="428e0-126">optional</span></span>  <br/> ||<span data-ttu-id="428e0-127">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="428e0-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="428e0-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="428e0-128">EventCode</span></span>  <br/> |<span data-ttu-id="428e0-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="428e0-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="428e0-130">necesario</span><span class="sxs-lookup"><span data-stu-id="428e0-130">required</span></span>  <br/> ||<span data-ttu-id="428e0-131">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="428e0-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="428e0-132">id.</span><span class="sxs-lookup"><span data-stu-id="428e0-132">ID</span></span>  <br/> |<span data-ttu-id="428e0-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="428e0-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="428e0-134">necesario</span><span class="sxs-lookup"><span data-stu-id="428e0-134">required</span></span>  <br/> ||<span data-ttu-id="428e0-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="428e0-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="428e0-136">Destino</span><span class="sxs-lookup"><span data-stu-id="428e0-136">Target</span></span>  <br/> |<span data-ttu-id="428e0-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="428e0-137">xsd:string</span></span>  <br/> |<span data-ttu-id="428e0-138">necesario</span><span class="sxs-lookup"><span data-stu-id="428e0-138">required</span></span>  <br/> ||<span data-ttu-id="428e0-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="428e0-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="428e0-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="428e0-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="428e0-141">xsd: String</span><span class="sxs-lookup"><span data-stu-id="428e0-141">xsd:string</span></span>  <br/> |<span data-ttu-id="428e0-142">necesario</span><span class="sxs-lookup"><span data-stu-id="428e0-142">required</span></span>  <br/> ||<span data-ttu-id="428e0-143">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="428e0-143">Values of the xsd:string type.</span></span>  <br/> |
   

