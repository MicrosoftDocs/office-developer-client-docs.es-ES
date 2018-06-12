---
title: DocumentSheet_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: 47378b039d11294dcb566f61cf20b0ed1ed7fed8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822017"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="5befe-102">DocumentSheet_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="5befe-102">DocumentSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5befe-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="5befe-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5befe-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5befe-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5befe-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5befe-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5befe-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5befe-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5befe-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="5befe-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5befe-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="5befe-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5befe-109">Definición</span><span class="sxs-lookup"><span data-stu-id="5befe-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5befe-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="5befe-110">Elements and attributes</span></span>

<span data-ttu-id="5befe-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="5befe-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5befe-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5befe-112">Child elements</span></span>

<span data-ttu-id="5befe-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5befe-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5befe-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="5befe-114">Attributes</span></span>

|<span data-ttu-id="5befe-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="5befe-115">**Attribute**</span></span>|<span data-ttu-id="5befe-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5befe-116">**Type**</span></span>|<span data-ttu-id="5befe-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="5befe-117">**Required**</span></span>|<span data-ttu-id="5befe-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5befe-118">**Description**</span></span>|<span data-ttu-id="5befe-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="5befe-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5befe-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="5befe-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="5befe-121">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="5befe-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5befe-122">opcional</span><span class="sxs-lookup"><span data-stu-id="5befe-122">optional</span></span>  <br/> ||<span data-ttu-id="5befe-123">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="5befe-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5befe-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="5befe-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="5befe-125">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="5befe-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5befe-126">opcional</span><span class="sxs-lookup"><span data-stu-id="5befe-126">optional</span></span>  <br/> ||<span data-ttu-id="5befe-127">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="5befe-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5befe-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="5befe-128">Name</span></span>  <br/> |<span data-ttu-id="5befe-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="5befe-129">xsd:string</span></span>  <br/> |<span data-ttu-id="5befe-130">opcional</span><span class="sxs-lookup"><span data-stu-id="5befe-130">optional</span></span>  <br/> ||<span data-ttu-id="5befe-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="5befe-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5befe-132">NameU</span><span class="sxs-lookup"><span data-stu-id="5befe-132">NameU</span></span>  <br/> |<span data-ttu-id="5befe-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="5befe-133">xsd:string</span></span>  <br/> |<span data-ttu-id="5befe-134">opcional</span><span class="sxs-lookup"><span data-stu-id="5befe-134">optional</span></span>  <br/> ||<span data-ttu-id="5befe-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="5befe-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5befe-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="5befe-136">UniqueID</span></span>  <br/> |<span data-ttu-id="5befe-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="5befe-137">xsd:string</span></span>  <br/> |<span data-ttu-id="5befe-138">opcional</span><span class="sxs-lookup"><span data-stu-id="5befe-138">optional</span></span>  <br/> ||<span data-ttu-id="5befe-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="5befe-139">Values of the xsd:string type.</span></span>  <br/> |
   

