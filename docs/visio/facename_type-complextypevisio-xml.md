---
title: FaceName_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 8035f541e619360403336bd2fbd931cf05dbfe59
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382445"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="0a8b7-102">FaceName_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="0a8b7-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0a8b7-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="0a8b7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a8b7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0a8b7-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0a8b7-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0a8b7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0a8b7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0a8b7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0a8b7-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="0a8b7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0a8b7-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0a8b7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0a8b7-109">Definición</span><span class="sxs-lookup"><span data-stu-id="0a8b7-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0a8b7-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0a8b7-110">Elements and attributes</span></span>

<span data-ttu-id="0a8b7-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="0a8b7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0a8b7-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0a8b7-112">Child elements</span></span>

<span data-ttu-id="0a8b7-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0a8b7-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a8b7-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="0a8b7-114">Attributes</span></span>

|<span data-ttu-id="0a8b7-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0a8b7-115">**Attribute**</span></span>|<span data-ttu-id="0a8b7-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0a8b7-116">**Type**</span></span>|<span data-ttu-id="0a8b7-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="0a8b7-117">**Required**</span></span>|<span data-ttu-id="0a8b7-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0a8b7-118">**Description**</span></span>|<span data-ttu-id="0a8b7-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="0a8b7-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0a8b7-120">Juegos de caracteres</span><span class="sxs-lookup"><span data-stu-id="0a8b7-120">CharSets</span></span>  <br/> |<span data-ttu-id="0a8b7-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0a8b7-121">xsd:string</span></span>  <br/> |<span data-ttu-id="0a8b7-122">opcional</span><span class="sxs-lookup"><span data-stu-id="0a8b7-122">optional</span></span>  <br/> ||<span data-ttu-id="0a8b7-123">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0a8b7-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0a8b7-124">Marcas</span><span class="sxs-lookup"><span data-stu-id="0a8b7-124">Flags</span></span>  <br/> |<span data-ttu-id="0a8b7-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0a8b7-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0a8b7-126">opcional</span><span class="sxs-lookup"><span data-stu-id="0a8b7-126">optional</span></span>  <br/> ||<span data-ttu-id="0a8b7-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0a8b7-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0a8b7-128">NameU</span><span class="sxs-lookup"><span data-stu-id="0a8b7-128">NameU</span></span>  <br/> |<span data-ttu-id="0a8b7-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0a8b7-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0a8b7-130">necesario</span><span class="sxs-lookup"><span data-stu-id="0a8b7-130">required</span></span>  <br/> ||<span data-ttu-id="0a8b7-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0a8b7-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0a8b7-132">Panos</span><span class="sxs-lookup"><span data-stu-id="0a8b7-132">Panos</span></span>  <br/> |<span data-ttu-id="0a8b7-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0a8b7-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0a8b7-134">opcional</span><span class="sxs-lookup"><span data-stu-id="0a8b7-134">optional</span></span>  <br/> ||<span data-ttu-id="0a8b7-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0a8b7-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0a8b7-136">Panose</span><span class="sxs-lookup"><span data-stu-id="0a8b7-136">Panose</span></span>  <br/> |<span data-ttu-id="0a8b7-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0a8b7-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0a8b7-138">opcional</span><span class="sxs-lookup"><span data-stu-id="0a8b7-138">optional</span></span>  <br/> ||<span data-ttu-id="0a8b7-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0a8b7-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0a8b7-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="0a8b7-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="0a8b7-141">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0a8b7-141">xsd:string</span></span>  <br/> |<span data-ttu-id="0a8b7-142">opcional</span><span class="sxs-lookup"><span data-stu-id="0a8b7-142">optional</span></span>  <br/> ||<span data-ttu-id="0a8b7-143">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0a8b7-143">Values of the xsd:string type.</span></span>  <br/> |
   

