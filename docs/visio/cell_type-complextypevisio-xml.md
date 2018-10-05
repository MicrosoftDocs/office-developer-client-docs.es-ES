---
title: Cell_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: ae5f481d787ae5d07968df8cd0ef0eba6af26f9c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389466"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="3e96e-102">Cell_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="3e96e-102">Cell_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3e96e-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="3e96e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e96e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3e96e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3e96e-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3e96e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3e96e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3e96e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3e96e-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="3e96e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3e96e-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3e96e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3e96e-109">Definición</span><span class="sxs-lookup"><span data-stu-id="3e96e-109">Definition</span></span>

```XML
          <xs:complexType name="Cell_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="U"
  type="xsd:string"
    />
    <xs:attribute name="E"
  type="xsd:string"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="V"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3e96e-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="3e96e-110">Elements and attributes</span></span>

<span data-ttu-id="3e96e-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="3e96e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3e96e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3e96e-112">Child elements</span></span>

|<span data-ttu-id="3e96e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3e96e-113">**Element**</span></span>|<span data-ttu-id="3e96e-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3e96e-114">**Type**</span></span>|<span data-ttu-id="3e96e-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3e96e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3e96e-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="3e96e-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3e96e-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="3e96e-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3e96e-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="3e96e-118">Attributes</span></span>

|<span data-ttu-id="3e96e-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="3e96e-119">**Attribute**</span></span>|<span data-ttu-id="3e96e-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3e96e-120">**Type**</span></span>|<span data-ttu-id="3e96e-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="3e96e-121">**Required**</span></span>|<span data-ttu-id="3e96e-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3e96e-122">**Description**</span></span>|<span data-ttu-id="3e96e-123">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="3e96e-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3e96e-124">E</span><span class="sxs-lookup"><span data-stu-id="3e96e-124">E</span></span>  <br/> |<span data-ttu-id="3e96e-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="3e96e-125">xsd:string</span></span>  <br/> |<span data-ttu-id="3e96e-126">opcional</span><span class="sxs-lookup"><span data-stu-id="3e96e-126">optional</span></span>  <br/> ||<span data-ttu-id="3e96e-127">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="3e96e-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3e96e-128">F</span><span class="sxs-lookup"><span data-stu-id="3e96e-128">F</span></span>  <br/> |<span data-ttu-id="3e96e-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="3e96e-129">xsd:string</span></span>  <br/> |<span data-ttu-id="3e96e-130">opcional</span><span class="sxs-lookup"><span data-stu-id="3e96e-130">optional</span></span>  <br/> ||<span data-ttu-id="3e96e-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="3e96e-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3e96e-132">N</span><span class="sxs-lookup"><span data-stu-id="3e96e-132">N</span></span>  <br/> |<span data-ttu-id="3e96e-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="3e96e-133">xsd:string</span></span>  <br/> |<span data-ttu-id="3e96e-134">necesario</span><span class="sxs-lookup"><span data-stu-id="3e96e-134">required</span></span>  <br/> ||<span data-ttu-id="3e96e-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="3e96e-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3e96e-136">U</span><span class="sxs-lookup"><span data-stu-id="3e96e-136">U</span></span>  <br/> |<span data-ttu-id="3e96e-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="3e96e-137">xsd:string</span></span>  <br/> |<span data-ttu-id="3e96e-138">opcional</span><span class="sxs-lookup"><span data-stu-id="3e96e-138">optional</span></span>  <br/> ||<span data-ttu-id="3e96e-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="3e96e-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3e96e-140">V</span><span class="sxs-lookup"><span data-stu-id="3e96e-140">V</span></span>  <br/> |<span data-ttu-id="3e96e-141">xsd: String</span><span class="sxs-lookup"><span data-stu-id="3e96e-141">xsd:string</span></span>  <br/> |<span data-ttu-id="3e96e-142">opcional</span><span class="sxs-lookup"><span data-stu-id="3e96e-142">optional</span></span>  <br/> ||<span data-ttu-id="3e96e-143">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="3e96e-143">Values of the xsd:string type.</span></span>  <br/> |
   

