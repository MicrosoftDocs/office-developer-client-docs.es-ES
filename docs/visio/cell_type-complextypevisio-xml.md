---
title: Cell_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: b17a251844a00ce01ad572dc63d971329214a23f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821734"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="9dc23-102">Cell_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="9dc23-102">Cell_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9dc23-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="9dc23-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9dc23-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9dc23-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9dc23-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9dc23-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9dc23-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9dc23-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9dc23-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="9dc23-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9dc23-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9dc23-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9dc23-109">Definición</span><span class="sxs-lookup"><span data-stu-id="9dc23-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9dc23-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="9dc23-110">Elements and attributes</span></span>

<span data-ttu-id="9dc23-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="9dc23-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9dc23-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9dc23-112">Child elements</span></span>

|<span data-ttu-id="9dc23-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9dc23-113">**Element**</span></span>|<span data-ttu-id="9dc23-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9dc23-114">**Type**</span></span>|<span data-ttu-id="9dc23-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9dc23-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9dc23-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="9dc23-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9dc23-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="9dc23-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9dc23-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="9dc23-118">Attributes</span></span>

|<span data-ttu-id="9dc23-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="9dc23-119">**Attribute**</span></span>|<span data-ttu-id="9dc23-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9dc23-120">**Type**</span></span>|<span data-ttu-id="9dc23-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="9dc23-121">**Required**</span></span>|<span data-ttu-id="9dc23-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9dc23-122">**Description**</span></span>|<span data-ttu-id="9dc23-123">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="9dc23-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9dc23-124">E</span><span class="sxs-lookup"><span data-stu-id="9dc23-124">E</span></span>  <br/> |<span data-ttu-id="9dc23-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="9dc23-125">xsd:string</span></span>  <br/> |<span data-ttu-id="9dc23-126">opcional</span><span class="sxs-lookup"><span data-stu-id="9dc23-126">optional</span></span>  <br/> ||<span data-ttu-id="9dc23-127">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="9dc23-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9dc23-128">F</span><span class="sxs-lookup"><span data-stu-id="9dc23-128">F</span></span>  <br/> |<span data-ttu-id="9dc23-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="9dc23-129">xsd:string</span></span>  <br/> |<span data-ttu-id="9dc23-130">opcional</span><span class="sxs-lookup"><span data-stu-id="9dc23-130">optional</span></span>  <br/> ||<span data-ttu-id="9dc23-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="9dc23-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9dc23-132">N</span><span class="sxs-lookup"><span data-stu-id="9dc23-132">N</span></span>  <br/> |<span data-ttu-id="9dc23-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="9dc23-133">xsd:string</span></span>  <br/> |<span data-ttu-id="9dc23-134">necesario</span><span class="sxs-lookup"><span data-stu-id="9dc23-134">required</span></span>  <br/> ||<span data-ttu-id="9dc23-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="9dc23-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9dc23-136">U</span><span class="sxs-lookup"><span data-stu-id="9dc23-136">U</span></span>  <br/> |<span data-ttu-id="9dc23-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="9dc23-137">xsd:string</span></span>  <br/> |<span data-ttu-id="9dc23-138">opcional</span><span class="sxs-lookup"><span data-stu-id="9dc23-138">optional</span></span>  <br/> ||<span data-ttu-id="9dc23-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="9dc23-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9dc23-140">V</span><span class="sxs-lookup"><span data-stu-id="9dc23-140">V</span></span>  <br/> |<span data-ttu-id="9dc23-141">xsd: String</span><span class="sxs-lookup"><span data-stu-id="9dc23-141">xsd:string</span></span>  <br/> |<span data-ttu-id="9dc23-142">opcional</span><span class="sxs-lookup"><span data-stu-id="9dc23-142">optional</span></span>  <br/> ||<span data-ttu-id="9dc23-143">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="9dc23-143">Values of the xsd:string type.</span></span>  <br/> |
   

