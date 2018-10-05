---
title: StyleSheet_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 19440ab1365ff82bd37d705115fd123dcb630aba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396004"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="6d3cb-102">StyleSheet_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="6d3cb-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6d3cb-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="6d3cb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d3cb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6d3cb-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6d3cb-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6d3cb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6d3cb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6d3cb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6d3cb-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="6d3cb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6d3cb-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="6d3cb-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6d3cb-109">Definición</span><span class="sxs-lookup"><span data-stu-id="6d3cb-109">Definition</span></span>

```XML
      <xs:complexType name="StyleSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
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
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6d3cb-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="6d3cb-110">Elements and attributes</span></span>

<span data-ttu-id="6d3cb-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6d3cb-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6d3cb-112">Child elements</span></span>

<span data-ttu-id="6d3cb-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d3cb-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="6d3cb-114">Attributes</span></span>

|<span data-ttu-id="6d3cb-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="6d3cb-115">**Attribute**</span></span>|<span data-ttu-id="6d3cb-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6d3cb-116">**Type**</span></span>|<span data-ttu-id="6d3cb-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="6d3cb-117">**Required**</span></span>|<span data-ttu-id="6d3cb-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6d3cb-118">**Description**</span></span>|<span data-ttu-id="6d3cb-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="6d3cb-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6d3cb-120">ID</span><span class="sxs-lookup"><span data-stu-id="6d3cb-120">ID</span></span>  <br/> |<span data-ttu-id="6d3cb-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6d3cb-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6d3cb-122">necesario</span><span class="sxs-lookup"><span data-stu-id="6d3cb-122">required</span></span>  <br/> ||<span data-ttu-id="6d3cb-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6d3cb-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="6d3cb-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="6d3cb-125">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="6d3cb-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6d3cb-126">opcional</span><span class="sxs-lookup"><span data-stu-id="6d3cb-126">optional</span></span>  <br/> ||<span data-ttu-id="6d3cb-127">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6d3cb-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="6d3cb-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="6d3cb-129">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="6d3cb-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6d3cb-130">opcional</span><span class="sxs-lookup"><span data-stu-id="6d3cb-130">optional</span></span>  <br/> ||<span data-ttu-id="6d3cb-131">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6d3cb-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="6d3cb-132">Name</span></span>  <br/> |<span data-ttu-id="6d3cb-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="6d3cb-133">xsd:string</span></span>  <br/> |<span data-ttu-id="6d3cb-134">opcional</span><span class="sxs-lookup"><span data-stu-id="6d3cb-134">optional</span></span>  <br/> ||<span data-ttu-id="6d3cb-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6d3cb-136">NameU</span><span class="sxs-lookup"><span data-stu-id="6d3cb-136">NameU</span></span>  <br/> |<span data-ttu-id="6d3cb-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="6d3cb-137">xsd:string</span></span>  <br/> |<span data-ttu-id="6d3cb-138">opcional</span><span class="sxs-lookup"><span data-stu-id="6d3cb-138">optional</span></span>  <br/> ||<span data-ttu-id="6d3cb-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-139">Values of the xsd:string type.</span></span>  <br/> |
   

