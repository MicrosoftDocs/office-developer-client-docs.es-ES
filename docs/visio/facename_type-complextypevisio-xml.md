---
title: FaceName_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 8035f541e619360403336bd2fbd931cf05dbfe59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322557"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="dc46f-102">FaceName_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="dc46f-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="dc46f-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="dc46f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc46f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dc46f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="dc46f-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="dc46f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="dc46f-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="dc46f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="dc46f-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="dc46f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="dc46f-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="dc46f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dc46f-109">Definición</span><span class="sxs-lookup"><span data-stu-id="dc46f-109">Definition</span></span>

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dc46f-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="dc46f-110">Elements and attributes</span></span>

<span data-ttu-id="dc46f-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="dc46f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dc46f-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dc46f-112">Child elements</span></span>

<span data-ttu-id="dc46f-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dc46f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc46f-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="dc46f-114">Attributes</span></span>

|<span data-ttu-id="dc46f-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="dc46f-115">**Attribute**</span></span>|<span data-ttu-id="dc46f-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dc46f-116">**Type**</span></span>|<span data-ttu-id="dc46f-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="dc46f-117">**Required**</span></span>|<span data-ttu-id="dc46f-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dc46f-118">**Description**</span></span>|<span data-ttu-id="dc46f-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="dc46f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dc46f-120">Juegos de caracteres</span><span class="sxs-lookup"><span data-stu-id="dc46f-120">CharSets</span></span>  <br/> |<span data-ttu-id="dc46f-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="dc46f-121">xsd:string</span></span>  <br/> |<span data-ttu-id="dc46f-122">opcional</span><span class="sxs-lookup"><span data-stu-id="dc46f-122">optional</span></span>  <br/> ||<span data-ttu-id="dc46f-123">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="dc46f-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dc46f-124">Flags</span><span class="sxs-lookup"><span data-stu-id="dc46f-124">Flags</span></span>  <br/> |<span data-ttu-id="dc46f-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dc46f-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dc46f-126">opcional</span><span class="sxs-lookup"><span data-stu-id="dc46f-126">optional</span></span>  <br/> ||<span data-ttu-id="dc46f-127">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="dc46f-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dc46f-128">NameU</span><span class="sxs-lookup"><span data-stu-id="dc46f-128">NameU</span></span>  <br/> |<span data-ttu-id="dc46f-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="dc46f-129">xsd:string</span></span>  <br/> |<span data-ttu-id="dc46f-130">necesario</span><span class="sxs-lookup"><span data-stu-id="dc46f-130">required</span></span>  <br/> ||<span data-ttu-id="dc46f-131">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="dc46f-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dc46f-132">Panos</span><span class="sxs-lookup"><span data-stu-id="dc46f-132">Panos</span></span>  <br/> |<span data-ttu-id="dc46f-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="dc46f-133">xsd:string</span></span>  <br/> |<span data-ttu-id="dc46f-134">opcional</span><span class="sxs-lookup"><span data-stu-id="dc46f-134">optional</span></span>  <br/> ||<span data-ttu-id="dc46f-135">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="dc46f-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dc46f-136">Panose</span><span class="sxs-lookup"><span data-stu-id="dc46f-136">Panose</span></span>  <br/> |<span data-ttu-id="dc46f-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="dc46f-137">xsd:string</span></span>  <br/> |<span data-ttu-id="dc46f-138">opcional</span><span class="sxs-lookup"><span data-stu-id="dc46f-138">optional</span></span>  <br/> ||<span data-ttu-id="dc46f-139">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="dc46f-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dc46f-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="dc46f-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="dc46f-141">xsd: String</span><span class="sxs-lookup"><span data-stu-id="dc46f-141">xsd:string</span></span>  <br/> |<span data-ttu-id="dc46f-142">opcional</span><span class="sxs-lookup"><span data-stu-id="dc46f-142">optional</span></span>  <br/> ||<span data-ttu-id="dc46f-143">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="dc46f-143">Values of the xsd:string type.</span></span>  <br/> |
   

