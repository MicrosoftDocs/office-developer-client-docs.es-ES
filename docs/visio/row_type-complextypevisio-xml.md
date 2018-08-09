---
title: Row_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: dfa3a90aaec51ba89845934c1d4fad484914afa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823057"
---
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="5a49d-102">Row_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="5a49d-102">Row_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5a49d-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="5a49d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a49d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5a49d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5a49d-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5a49d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5a49d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5a49d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5a49d-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="5a49d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5a49d-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5a49d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5a49d-109">Definición</span><span class="sxs-lookup"><span data-stu-id="5a49d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5a49d-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="5a49d-110">Elements and attributes</span></span>

<span data-ttu-id="5a49d-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="5a49d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5a49d-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5a49d-112">Child elements</span></span>

|<span data-ttu-id="5a49d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a49d-113">**Element**</span></span>|<span data-ttu-id="5a49d-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5a49d-114">**Type**</span></span>|<span data-ttu-id="5a49d-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5a49d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5a49d-116">Cell</span><span class="sxs-lookup"><span data-stu-id="5a49d-116">Cell</span></span>](http://msdn.microsoft.com/library/5e060a3f-e804-834f-531b-78a544fee61f%28Office.15%29.aspx) <br/> |[<span data-ttu-id="5a49d-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="5a49d-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5a49d-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="5a49d-118">Trigger</span></span>](http://msdn.microsoft.com/library/6dbd2c66-3b29-03f6-648f-723d359ded0d%28Office.15%29.aspx) <br/> |[<span data-ttu-id="5a49d-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="5a49d-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5a49d-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="5a49d-120">Attributes</span></span>

|<span data-ttu-id="5a49d-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="5a49d-121">**Attribute**</span></span>|<span data-ttu-id="5a49d-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5a49d-122">**Type**</span></span>|<span data-ttu-id="5a49d-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="5a49d-123">**Required**</span></span>|<span data-ttu-id="5a49d-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5a49d-124">**Description**</span></span>|<span data-ttu-id="5a49d-125">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="5a49d-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5a49d-126">SUPR</span><span class="sxs-lookup"><span data-stu-id="5a49d-126">Del</span></span>  <br/> |<span data-ttu-id="5a49d-127">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="5a49d-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5a49d-128">opcional</span><span class="sxs-lookup"><span data-stu-id="5a49d-128">optional</span></span>  <br/> ||<span data-ttu-id="5a49d-129">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="5a49d-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5a49d-130">IX</span><span class="sxs-lookup"><span data-stu-id="5a49d-130">IX</span></span>  <br/> |<span data-ttu-id="5a49d-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5a49d-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5a49d-132">opcional</span><span class="sxs-lookup"><span data-stu-id="5a49d-132">optional</span></span>  <br/> ||<span data-ttu-id="5a49d-133">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5a49d-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5a49d-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="5a49d-134">LocalName</span></span>  <br/> |<span data-ttu-id="5a49d-135">xsd: String</span><span class="sxs-lookup"><span data-stu-id="5a49d-135">xsd:string</span></span>  <br/> |<span data-ttu-id="5a49d-136">opcional</span><span class="sxs-lookup"><span data-stu-id="5a49d-136">optional</span></span>  <br/> ||<span data-ttu-id="5a49d-137">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="5a49d-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5a49d-138">N</span><span class="sxs-lookup"><span data-stu-id="5a49d-138">N</span></span>  <br/> |<span data-ttu-id="5a49d-139">xsd: String</span><span class="sxs-lookup"><span data-stu-id="5a49d-139">xsd:string</span></span>  <br/> |<span data-ttu-id="5a49d-140">opcional</span><span class="sxs-lookup"><span data-stu-id="5a49d-140">optional</span></span>  <br/> ||<span data-ttu-id="5a49d-141">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="5a49d-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5a49d-142">T</span><span class="sxs-lookup"><span data-stu-id="5a49d-142">T</span></span>  <br/> |<span data-ttu-id="5a49d-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="5a49d-143">xsd:string</span></span>  <br/> |<span data-ttu-id="5a49d-144">opcional</span><span class="sxs-lookup"><span data-stu-id="5a49d-144">optional</span></span>  <br/> ||<span data-ttu-id="5a49d-145">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="5a49d-145">Values of the xsd:string type.</span></span>  <br/> |
   

