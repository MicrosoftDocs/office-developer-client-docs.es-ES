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
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="cb214-102">AuthorEntry_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="cb214-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cb214-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="cb214-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb214-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cb214-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cb214-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cb214-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cb214-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cb214-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cb214-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="cb214-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cb214-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="cb214-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cb214-109">Definición</span><span class="sxs-lookup"><span data-stu-id="cb214-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cb214-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="cb214-110">Elements and attributes</span></span>

<span data-ttu-id="cb214-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="cb214-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cb214-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cb214-112">Child elements</span></span>

<span data-ttu-id="cb214-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cb214-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb214-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="cb214-114">Attributes</span></span>

|<span data-ttu-id="cb214-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="cb214-115">**Attribute**</span></span>|<span data-ttu-id="cb214-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cb214-116">**Type**</span></span>|<span data-ttu-id="cb214-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="cb214-117">**Required**</span></span>|<span data-ttu-id="cb214-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cb214-118">**Description**</span></span>|<span data-ttu-id="cb214-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="cb214-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cb214-120">id.</span><span class="sxs-lookup"><span data-stu-id="cb214-120">ID</span></span>  <br/> |<span data-ttu-id="cb214-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cb214-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cb214-122">necesario</span><span class="sxs-lookup"><span data-stu-id="cb214-122">required</span></span>  <br/> ||<span data-ttu-id="cb214-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cb214-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cb214-124">Iniciales</span><span class="sxs-lookup"><span data-stu-id="cb214-124">Initials</span></span>  <br/> |<span data-ttu-id="cb214-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cb214-125">xsd:string</span></span>  <br/> |<span data-ttu-id="cb214-126">opcional</span><span class="sxs-lookup"><span data-stu-id="cb214-126">optional</span></span>  <br/> ||<span data-ttu-id="cb214-127">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="cb214-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cb214-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="cb214-128">Name</span></span>  <br/> |<span data-ttu-id="cb214-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cb214-129">xsd:string</span></span>  <br/> |<span data-ttu-id="cb214-130">opcional</span><span class="sxs-lookup"><span data-stu-id="cb214-130">optional</span></span>  <br/> ||<span data-ttu-id="cb214-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="cb214-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cb214-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="cb214-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="cb214-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cb214-133">xsd:string</span></span>  <br/> |<span data-ttu-id="cb214-134">opcional</span><span class="sxs-lookup"><span data-stu-id="cb214-134">optional</span></span>  <br/> ||<span data-ttu-id="cb214-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="cb214-135">Values of the xsd:string type.</span></span>  <br/> |
   

