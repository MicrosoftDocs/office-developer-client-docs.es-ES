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
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="0cee9-102">DocumentSheet_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="0cee9-102">DocumentSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0cee9-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="0cee9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0cee9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0cee9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0cee9-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0cee9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0cee9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0cee9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0cee9-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="0cee9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0cee9-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="0cee9-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0cee9-109">Definición</span><span class="sxs-lookup"><span data-stu-id="0cee9-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0cee9-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0cee9-110">Elements and attributes</span></span>

<span data-ttu-id="0cee9-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="0cee9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0cee9-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0cee9-112">Child elements</span></span>

<span data-ttu-id="0cee9-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0cee9-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0cee9-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="0cee9-114">Attributes</span></span>

|<span data-ttu-id="0cee9-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0cee9-115">**Attribute**</span></span>|<span data-ttu-id="0cee9-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0cee9-116">**Type**</span></span>|<span data-ttu-id="0cee9-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="0cee9-117">**Required**</span></span>|<span data-ttu-id="0cee9-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0cee9-118">**Description**</span></span>|<span data-ttu-id="0cee9-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="0cee9-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0cee9-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="0cee9-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="0cee9-121">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="0cee9-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0cee9-122">opcional</span><span class="sxs-lookup"><span data-stu-id="0cee9-122">optional</span></span>  <br/> ||<span data-ttu-id="0cee9-123">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="0cee9-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0cee9-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="0cee9-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="0cee9-125">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="0cee9-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0cee9-126">opcional</span><span class="sxs-lookup"><span data-stu-id="0cee9-126">optional</span></span>  <br/> ||<span data-ttu-id="0cee9-127">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="0cee9-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0cee9-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="0cee9-128">Name</span></span>  <br/> |<span data-ttu-id="0cee9-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0cee9-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0cee9-130">opcional</span><span class="sxs-lookup"><span data-stu-id="0cee9-130">optional</span></span>  <br/> ||<span data-ttu-id="0cee9-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0cee9-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0cee9-132">NameU</span><span class="sxs-lookup"><span data-stu-id="0cee9-132">NameU</span></span>  <br/> |<span data-ttu-id="0cee9-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0cee9-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0cee9-134">opcional</span><span class="sxs-lookup"><span data-stu-id="0cee9-134">optional</span></span>  <br/> ||<span data-ttu-id="0cee9-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0cee9-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0cee9-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="0cee9-136">UniqueID</span></span>  <br/> |<span data-ttu-id="0cee9-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0cee9-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0cee9-138">opcional</span><span class="sxs-lookup"><span data-stu-id="0cee9-138">optional</span></span>  <br/> ||<span data-ttu-id="0cee9-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0cee9-139">Values of the xsd:string type.</span></span>  <br/> |
   

