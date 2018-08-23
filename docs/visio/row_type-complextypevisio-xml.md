---
title: Row_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: 6ebd483ae9b0748a3afa15360bf2c88feae44aeb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586903"
---
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="79684-102">Row_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="79684-102">Row_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="79684-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="79684-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79684-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="79684-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="79684-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="79684-105">**Schema file**</span></span> <br/> |<span data-ttu-id="79684-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="79684-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="79684-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="79684-107">**Extension base**</span></span> <br/> |<span data-ttu-id="79684-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="79684-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="79684-109">Definición</span><span class="sxs-lookup"><span data-stu-id="79684-109">Definition</span></span>

```XML
          <xs:complexType name="Row_Type">
          
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Trigger"  type="Trigger_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
    />
    <xs:attribute name="LocalName"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="79684-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="79684-110">Elements and attributes</span></span>

<span data-ttu-id="79684-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="79684-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="79684-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="79684-112">Child elements</span></span>

|<span data-ttu-id="79684-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="79684-113">**Element**</span></span>|<span data-ttu-id="79684-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="79684-114">**Type**</span></span>|<span data-ttu-id="79684-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="79684-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="79684-116">Cell</span><span class="sxs-lookup"><span data-stu-id="79684-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="79684-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="79684-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="79684-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="79684-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="79684-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="79684-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="79684-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="79684-120">Attributes</span></span>

|<span data-ttu-id="79684-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="79684-121">**Attribute**</span></span>|<span data-ttu-id="79684-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="79684-122">**Type**</span></span>|<span data-ttu-id="79684-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="79684-123">**Required**</span></span>|<span data-ttu-id="79684-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="79684-124">**Description**</span></span>|<span data-ttu-id="79684-125">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="79684-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="79684-126">SUPR</span><span class="sxs-lookup"><span data-stu-id="79684-126">Del</span></span>  <br/> |<span data-ttu-id="79684-127">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="79684-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="79684-128">opcional</span><span class="sxs-lookup"><span data-stu-id="79684-128">optional</span></span>  <br/> ||<span data-ttu-id="79684-129">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="79684-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="79684-130">IX</span><span class="sxs-lookup"><span data-stu-id="79684-130">IX</span></span>  <br/> |<span data-ttu-id="79684-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="79684-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="79684-132">opcional</span><span class="sxs-lookup"><span data-stu-id="79684-132">optional</span></span>  <br/> ||<span data-ttu-id="79684-133">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="79684-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="79684-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="79684-134">LocalName</span></span>  <br/> |<span data-ttu-id="79684-135">xsd: String</span><span class="sxs-lookup"><span data-stu-id="79684-135">xsd:string</span></span>  <br/> |<span data-ttu-id="79684-136">opcional</span><span class="sxs-lookup"><span data-stu-id="79684-136">optional</span></span>  <br/> ||<span data-ttu-id="79684-137">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="79684-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="79684-138">N</span><span class="sxs-lookup"><span data-stu-id="79684-138">N</span></span>  <br/> |<span data-ttu-id="79684-139">xsd: String</span><span class="sxs-lookup"><span data-stu-id="79684-139">xsd:string</span></span>  <br/> |<span data-ttu-id="79684-140">opcional</span><span class="sxs-lookup"><span data-stu-id="79684-140">optional</span></span>  <br/> ||<span data-ttu-id="79684-141">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="79684-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="79684-142">T</span><span class="sxs-lookup"><span data-stu-id="79684-142">T</span></span>  <br/> |<span data-ttu-id="79684-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="79684-143">xsd:string</span></span>  <br/> |<span data-ttu-id="79684-144">opcional</span><span class="sxs-lookup"><span data-stu-id="79684-144">optional</span></span>  <br/> ||<span data-ttu-id="79684-145">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="79684-145">Values of the xsd:string type.</span></span>  <br/> |
   

