---
title: ComplexType AuthorEntry_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 41279e9f4ffa0bba17d4f74eb2f40d724589c17d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537881"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="2f1ed-102">ComplexType AuthorEntry_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="2f1ed-102">AuthorEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="2f1ed-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="2f1ed-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f1ed-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2f1ed-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2f1ed-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2f1ed-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2f1ed-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="2f1ed-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2f1ed-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="2f1ed-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2f1ed-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="2f1ed-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2f1ed-109">Definición</span><span class="sxs-lookup"><span data-stu-id="2f1ed-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2f1ed-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="2f1ed-110">Elements and attributes</span></span>

<span data-ttu-id="2f1ed-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="2f1ed-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2f1ed-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2f1ed-112">Child elements</span></span>

<span data-ttu-id="2f1ed-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2f1ed-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f1ed-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="2f1ed-114">Attributes</span></span>

|<span data-ttu-id="2f1ed-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2f1ed-115">**Attribute**</span></span>|<span data-ttu-id="2f1ed-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2f1ed-116">**Type**</span></span>|<span data-ttu-id="2f1ed-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="2f1ed-117">**Required**</span></span>|<span data-ttu-id="2f1ed-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2f1ed-118">**Description**</span></span>|<span data-ttu-id="2f1ed-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="2f1ed-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2f1ed-120">ID</span><span class="sxs-lookup"><span data-stu-id="2f1ed-120">ID</span></span>  <br/> |<span data-ttu-id="2f1ed-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2f1ed-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2f1ed-122">necesario</span><span class="sxs-lookup"><span data-stu-id="2f1ed-122">required</span></span>  <br/> ||<span data-ttu-id="2f1ed-123">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2f1ed-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2f1ed-124">Iniciales</span><span class="sxs-lookup"><span data-stu-id="2f1ed-124">Initials</span></span>  <br/> |<span data-ttu-id="2f1ed-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="2f1ed-125">xsd:string</span></span>  <br/> |<span data-ttu-id="2f1ed-126">opcional</span><span class="sxs-lookup"><span data-stu-id="2f1ed-126">optional</span></span>  <br/> ||<span data-ttu-id="2f1ed-127">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="2f1ed-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2f1ed-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="2f1ed-128">Name</span></span>  <br/> |<span data-ttu-id="2f1ed-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="2f1ed-129">xsd:string</span></span>  <br/> |<span data-ttu-id="2f1ed-130">opcional</span><span class="sxs-lookup"><span data-stu-id="2f1ed-130">optional</span></span>  <br/> ||<span data-ttu-id="2f1ed-131">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="2f1ed-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2f1ed-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="2f1ed-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="2f1ed-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="2f1ed-133">xsd:string</span></span>  <br/> |<span data-ttu-id="2f1ed-134">opcional</span><span class="sxs-lookup"><span data-stu-id="2f1ed-134">optional</span></span>  <br/> ||<span data-ttu-id="2f1ed-135">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="2f1ed-135">Values of the xsd:string type.</span></span>  <br/> |
   

