---
title: StyleSheet_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 394712b65ee44a939a20fd3b65df504785f106ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823352"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="c401a-102">StyleSheet_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="c401a-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c401a-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="c401a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c401a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c401a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c401a-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c401a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c401a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c401a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c401a-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="c401a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c401a-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="c401a-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c401a-109">Definición</span><span class="sxs-lookup"><span data-stu-id="c401a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c401a-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c401a-110">Elements and attributes</span></span>

<span data-ttu-id="c401a-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="c401a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c401a-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c401a-112">Child elements</span></span>

<span data-ttu-id="c401a-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c401a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c401a-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="c401a-114">Attributes</span></span>

|<span data-ttu-id="c401a-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c401a-115">**Attribute**</span></span>|<span data-ttu-id="c401a-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c401a-116">**Type**</span></span>|<span data-ttu-id="c401a-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="c401a-117">**Required**</span></span>|<span data-ttu-id="c401a-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c401a-118">**Description**</span></span>|<span data-ttu-id="c401a-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="c401a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c401a-120">ID</span><span class="sxs-lookup"><span data-stu-id="c401a-120">ID</span></span>  <br/> |<span data-ttu-id="c401a-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c401a-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c401a-122">necesario</span><span class="sxs-lookup"><span data-stu-id="c401a-122">required</span></span>  <br/> ||<span data-ttu-id="c401a-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c401a-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c401a-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="c401a-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="c401a-125">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="c401a-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c401a-126">opcional</span><span class="sxs-lookup"><span data-stu-id="c401a-126">optional</span></span>  <br/> ||<span data-ttu-id="c401a-127">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="c401a-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c401a-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="c401a-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="c401a-129">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="c401a-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c401a-130">opcional</span><span class="sxs-lookup"><span data-stu-id="c401a-130">optional</span></span>  <br/> ||<span data-ttu-id="c401a-131">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="c401a-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c401a-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="c401a-132">Name</span></span>  <br/> |<span data-ttu-id="c401a-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c401a-133">xsd:string</span></span>  <br/> |<span data-ttu-id="c401a-134">opcional</span><span class="sxs-lookup"><span data-stu-id="c401a-134">optional</span></span>  <br/> ||<span data-ttu-id="c401a-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="c401a-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c401a-136">NameU</span><span class="sxs-lookup"><span data-stu-id="c401a-136">NameU</span></span>  <br/> |<span data-ttu-id="c401a-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c401a-137">xsd:string</span></span>  <br/> |<span data-ttu-id="c401a-138">opcional</span><span class="sxs-lookup"><span data-stu-id="c401a-138">optional</span></span>  <br/> ||<span data-ttu-id="c401a-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="c401a-139">Values of the xsd:string type.</span></span>  <br/> |
   

