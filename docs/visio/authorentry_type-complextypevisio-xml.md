---
title: AuthorEntry_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 7d43d34559f212e3de1a91291cbf14b75a3b2e0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341387"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="0d8f3-102">AuthorEntry_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="0d8f3-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0d8f3-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="0d8f3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d8f3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0d8f3-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0d8f3-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0d8f3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0d8f3-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="0d8f3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0d8f3-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="0d8f3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0d8f3-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0d8f3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0d8f3-109">Definición</span><span class="sxs-lookup"><span data-stu-id="0d8f3-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0d8f3-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0d8f3-110">Elements and attributes</span></span>

<span data-ttu-id="0d8f3-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="0d8f3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0d8f3-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0d8f3-112">Child elements</span></span>

<span data-ttu-id="0d8f3-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0d8f3-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d8f3-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="0d8f3-114">Attributes</span></span>

|<span data-ttu-id="0d8f3-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="0d8f3-115">**Attribute**</span></span>|<span data-ttu-id="0d8f3-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0d8f3-116">**Type**</span></span>|<span data-ttu-id="0d8f3-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="0d8f3-117">**Required**</span></span>|<span data-ttu-id="0d8f3-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0d8f3-118">**Description**</span></span>|<span data-ttu-id="0d8f3-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="0d8f3-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0d8f3-120">ID</span><span class="sxs-lookup"><span data-stu-id="0d8f3-120">ID</span></span>  <br/> |<span data-ttu-id="0d8f3-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0d8f3-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0d8f3-122">necesario</span><span class="sxs-lookup"><span data-stu-id="0d8f3-122">required</span></span>  <br/> ||<span data-ttu-id="0d8f3-123">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0d8f3-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0d8f3-124">Iniciales</span><span class="sxs-lookup"><span data-stu-id="0d8f3-124">Initials</span></span>  <br/> |<span data-ttu-id="0d8f3-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0d8f3-125">xsd:string</span></span>  <br/> |<span data-ttu-id="0d8f3-126">opcional</span><span class="sxs-lookup"><span data-stu-id="0d8f3-126">optional</span></span>  <br/> ||<span data-ttu-id="0d8f3-127">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0d8f3-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0d8f3-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="0d8f3-128">Name</span></span>  <br/> |<span data-ttu-id="0d8f3-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0d8f3-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0d8f3-130">opcional</span><span class="sxs-lookup"><span data-stu-id="0d8f3-130">optional</span></span>  <br/> ||<span data-ttu-id="0d8f3-131">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0d8f3-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0d8f3-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="0d8f3-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="0d8f3-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0d8f3-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0d8f3-134">opcional</span><span class="sxs-lookup"><span data-stu-id="0d8f3-134">optional</span></span>  <br/> ||<span data-ttu-id="0d8f3-135">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0d8f3-135">Values of the xsd:string type.</span></span>  <br/> |
   

