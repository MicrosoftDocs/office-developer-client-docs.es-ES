---
title: DocumentSheet_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: a1f51ef6f0340b4430860eabde3ad778e923fed0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396347"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="11dca-102">DocumentSheet_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="11dca-102">DocumentSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="11dca-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="11dca-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11dca-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="11dca-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="11dca-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="11dca-105">**Schema file**</span></span> <br/> |<span data-ttu-id="11dca-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="11dca-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="11dca-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="11dca-107">**Extension base**</span></span> <br/> |<span data-ttu-id="11dca-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="11dca-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="11dca-109">Definición</span><span class="sxs-lookup"><span data-stu-id="11dca-109">Definition</span></span>

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="11dca-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="11dca-110">Elements and attributes</span></span>

<span data-ttu-id="11dca-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="11dca-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="11dca-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="11dca-112">Child elements</span></span>

<span data-ttu-id="11dca-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="11dca-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11dca-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="11dca-114">Attributes</span></span>

|<span data-ttu-id="11dca-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="11dca-115">**Attribute**</span></span>|<span data-ttu-id="11dca-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="11dca-116">**Type**</span></span>|<span data-ttu-id="11dca-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="11dca-117">**Required**</span></span>|<span data-ttu-id="11dca-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="11dca-118">**Description**</span></span>|<span data-ttu-id="11dca-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="11dca-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="11dca-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="11dca-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="11dca-121">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="11dca-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="11dca-122">opcional</span><span class="sxs-lookup"><span data-stu-id="11dca-122">optional</span></span>  <br/> ||<span data-ttu-id="11dca-123">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="11dca-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="11dca-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="11dca-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="11dca-125">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="11dca-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="11dca-126">opcional</span><span class="sxs-lookup"><span data-stu-id="11dca-126">optional</span></span>  <br/> ||<span data-ttu-id="11dca-127">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="11dca-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="11dca-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="11dca-128">Name</span></span>  <br/> |<span data-ttu-id="11dca-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="11dca-129">xsd:string</span></span>  <br/> |<span data-ttu-id="11dca-130">opcional</span><span class="sxs-lookup"><span data-stu-id="11dca-130">optional</span></span>  <br/> ||<span data-ttu-id="11dca-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="11dca-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="11dca-132">NameU</span><span class="sxs-lookup"><span data-stu-id="11dca-132">NameU</span></span>  <br/> |<span data-ttu-id="11dca-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="11dca-133">xsd:string</span></span>  <br/> |<span data-ttu-id="11dca-134">opcional</span><span class="sxs-lookup"><span data-stu-id="11dca-134">optional</span></span>  <br/> ||<span data-ttu-id="11dca-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="11dca-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="11dca-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="11dca-136">UniqueID</span></span>  <br/> |<span data-ttu-id="11dca-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="11dca-137">xsd:string</span></span>  <br/> |<span data-ttu-id="11dca-138">opcional</span><span class="sxs-lookup"><span data-stu-id="11dca-138">optional</span></span>  <br/> ||<span data-ttu-id="11dca-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="11dca-139">Values of the xsd:string type.</span></span>  <br/> |
   

