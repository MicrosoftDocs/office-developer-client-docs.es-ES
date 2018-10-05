---
title: AuthorEntry_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 7d43d34559f212e3de1a91291cbf14b75a3b2e0c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386841"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="38924-102">AuthorEntry_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="38924-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="38924-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="38924-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38924-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="38924-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="38924-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="38924-105">**Schema file**</span></span> <br/> |<span data-ttu-id="38924-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="38924-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="38924-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="38924-107">**Extension base**</span></span> <br/> |<span data-ttu-id="38924-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="38924-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="38924-109">Definición</span><span class="sxs-lookup"><span data-stu-id="38924-109">Definition</span></span>

```XML
      <xs:complexType name="AuthorEntry_Type">
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="Initials"
  type="xsd:string"
    />
    <xs:attribute name="ResolutionID"
  type="xsd:string"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="38924-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="38924-110">Elements and attributes</span></span>

<span data-ttu-id="38924-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="38924-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="38924-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="38924-112">Child elements</span></span>

<span data-ttu-id="38924-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="38924-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38924-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="38924-114">Attributes</span></span>

|<span data-ttu-id="38924-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="38924-115">**Attribute**</span></span>|<span data-ttu-id="38924-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="38924-116">**Type**</span></span>|<span data-ttu-id="38924-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="38924-117">**Required**</span></span>|<span data-ttu-id="38924-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="38924-118">**Description**</span></span>|<span data-ttu-id="38924-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="38924-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="38924-120">ID</span><span class="sxs-lookup"><span data-stu-id="38924-120">ID</span></span>  <br/> |<span data-ttu-id="38924-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="38924-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="38924-122">necesario</span><span class="sxs-lookup"><span data-stu-id="38924-122">required</span></span>  <br/> ||<span data-ttu-id="38924-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="38924-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="38924-124">Initials</span><span class="sxs-lookup"><span data-stu-id="38924-124">Initials</span></span>  <br/> |<span data-ttu-id="38924-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="38924-125">xsd:string</span></span>  <br/> |<span data-ttu-id="38924-126">opcional</span><span class="sxs-lookup"><span data-stu-id="38924-126">optional</span></span>  <br/> ||<span data-ttu-id="38924-127">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="38924-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="38924-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="38924-128">Name</span></span>  <br/> |<span data-ttu-id="38924-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="38924-129">xsd:string</span></span>  <br/> |<span data-ttu-id="38924-130">opcional</span><span class="sxs-lookup"><span data-stu-id="38924-130">optional</span></span>  <br/> ||<span data-ttu-id="38924-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="38924-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="38924-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="38924-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="38924-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="38924-133">xsd:string</span></span>  <br/> |<span data-ttu-id="38924-134">opcional</span><span class="sxs-lookup"><span data-stu-id="38924-134">optional</span></span>  <br/> ||<span data-ttu-id="38924-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="38924-135">Values of the xsd:string type.</span></span>  <br/> |
   

