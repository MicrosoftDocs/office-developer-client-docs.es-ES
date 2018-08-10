---
title: AuthorEntry_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 39cf47915230b18d22db78f5470fd9c26b9c77ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821527"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="efe7f-102">AuthorEntry_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="efe7f-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="efe7f-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="efe7f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="efe7f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="efe7f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="efe7f-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="efe7f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="efe7f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="efe7f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="efe7f-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="efe7f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="efe7f-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="efe7f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="efe7f-109">Definición</span><span class="sxs-lookup"><span data-stu-id="efe7f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="efe7f-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="efe7f-110">Elements and attributes</span></span>

<span data-ttu-id="efe7f-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="efe7f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="efe7f-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="efe7f-112">Child elements</span></span>

<span data-ttu-id="efe7f-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="efe7f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="efe7f-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="efe7f-114">Attributes</span></span>

|<span data-ttu-id="efe7f-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="efe7f-115">**Attribute**</span></span>|<span data-ttu-id="efe7f-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="efe7f-116">**Type**</span></span>|<span data-ttu-id="efe7f-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="efe7f-117">**Required**</span></span>|<span data-ttu-id="efe7f-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="efe7f-118">**Description**</span></span>|<span data-ttu-id="efe7f-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="efe7f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="efe7f-120">ID</span><span class="sxs-lookup"><span data-stu-id="efe7f-120">ID</span></span>  <br/> |<span data-ttu-id="efe7f-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="efe7f-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="efe7f-122">necesario</span><span class="sxs-lookup"><span data-stu-id="efe7f-122">required</span></span>  <br/> ||<span data-ttu-id="efe7f-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="efe7f-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="efe7f-124">Initials</span><span class="sxs-lookup"><span data-stu-id="efe7f-124">Initials</span></span>  <br/> |<span data-ttu-id="efe7f-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="efe7f-125">xsd:string</span></span>  <br/> |<span data-ttu-id="efe7f-126">opcional</span><span class="sxs-lookup"><span data-stu-id="efe7f-126">optional</span></span>  <br/> ||<span data-ttu-id="efe7f-127">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="efe7f-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="efe7f-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="efe7f-128">Name</span></span>  <br/> |<span data-ttu-id="efe7f-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="efe7f-129">xsd:string</span></span>  <br/> |<span data-ttu-id="efe7f-130">opcional</span><span class="sxs-lookup"><span data-stu-id="efe7f-130">optional</span></span>  <br/> ||<span data-ttu-id="efe7f-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="efe7f-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="efe7f-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="efe7f-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="efe7f-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="efe7f-133">xsd:string</span></span>  <br/> |<span data-ttu-id="efe7f-134">opcional</span><span class="sxs-lookup"><span data-stu-id="efe7f-134">optional</span></span>  <br/> ||<span data-ttu-id="efe7f-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="efe7f-135">Values of the xsd:string type.</span></span>  <br/> |
   

